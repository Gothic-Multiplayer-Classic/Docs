# Lua Resource System

This document describes **how Lua resources actually behave**, from the creator's point of view.
It focuses on **structure, lifecycle, guarantees, and correct mental models**, without relying on engine internals.

---

## What a Resource is

A **resource** is a **versioned, self-contained Lua package** authored on the server and distributed automatically to clients.

Client-side flow:

1. Download on server handshake
2. Integrity verification
3. Load into an isolated Lua environment
4. Explicit start by the engine

You never load or install resources manually on the client.
You write code that runs **when the resource starts**.

---

## Mandatory Structure

Every resource **must** be a directory containing `resource.toml`.

!!! note
	If missing, the resource is not recognized and no script is executed.

Minimal valid layout:

```yaml
my_resource/
  resource.toml
  client/
    main.lua
my_resource_two/
  resource.toml
  server/
    main.lua
```

---

### `resource.toml`

`resource.toml` defines resource metadata. It's used only for identification and validation

Minimal example:

```toml
version = "1.0.0"
author = "YourName"
description = "Example resource"
```

---

### Folder Roles

Recommended full layout:

```yaml
my_resource/
  resource.toml
  client/
    main.lua
    ui.lua
    events.lua
  shared/
    init.lua
  server/
    main.lua
```

Meaning:

* `client/` - client-only Lua
* `shared/` - Lua shared between client and server
* `server/` - server-only Lua

Client can only load from `client/` and `shared/`.

---

## Client Guarantees Before Lua Runs

Before **any** client Lua executes, the engine guarantees:

* All resources are fully downloaded
* All declared files exist
* Integrity checks passed
* Lua environment is initialized
* Engine Lua bindings are registered

Implications:

* No partial scripts
* No early execution
* If Lua runs, all files are present

---

## Single Client Entrypoint

Each client resource has **exactly one automatic entrypoint**: `client/main.lua`

!!! note
	If code is not reachable from `client/main.lua`, it never executes.

Rules:

* Executed automatically on resource start
* No other file runs unless required explicitly
* File order is irrelevant

---

## Role of `client/main.lua`

`client/main.lua` is a **bootstrap**, not the application.

Its job:

* Load modules
* Register lifecycle hooks
* Prepare initial state

Typical pattern:

```lua
require("shared.init")
require("client.events")
require("client.ui")

function onResourceStart()
end

function onResourceStop()
end
```

Avoid:

* Heavy logic
* World assumptions
* Gameplay execution

---

## Lifecycle Hooks

Supported lifecycle functions:

```lua
function onResourceStart() end
function onResourceStop() end
```

!!! note
	Side effects belong in lifecycle hooks, not at file top level.

### `onResourceStart`

Called after:

* All files are loaded
* `client/main.lua` has executed
* The resource is live

Use for:

* Registering events
* Initializing UI
* Starting timers
* Creating runtime state

### `onResourceStop`

Called when:

* Disconnecting
* Resource unload or replacement

Use for cleanup:

* Remove handlers
* Destroy UI
* Stop timers

---

## `require()` Behavior

`require()` loads Lua modules from **inside the resource**, not the filesystem.

Example:

```lua
require("client.ui")
```

Resolution order:

* `client/ui.lua`
* `shared/ui.lua`
* fallback paths

Rules:

* Modules load once per resource
* Results are cached
* Missing modules abort resource startup

---

## Lua Environment Isolation

Each resource runs in its **own Lua environment**.

!!! note
	Engine-provided globals remain accessible, but do not use globals for cross-resource communication.

Consequences:

* Globals are resource-local
* Globals persist for the resource lifetime
* No global leakage between resources

---

## Exports

Resources may explicitly expose functionality:

```lua
exports = {
  showUI = function() end
}
```

Exports:

* Are discovered after resource start
* Are explicit and opt-in
* Are not injected into globals
* Form the intentional external interface

---

## Event-Driven Design

Client Lua is **event-driven**, not sequence-driven.

Assume:

* World may not exist at start
* Player may not be ready
* Visual systems may initialize later

Correct:

* Register handlers
* React to engine events

Incorrect:

* Acting at file load
* Assuming immediate world availability

---

## Assets and Files

A resource starts only if all declared assets exist.

!!! note
	Assets are referenced by name; the engine manages loading.
	Missing assets are packaging errors, not runtime concerns.

Lua scripts:

* Do not open files
* Do not load assets manually
* Do not access arbitrary paths

---
