# Server Configuration
This document explains all available options in the **server configuration file**.
The configuration uses **TOML** format. All settings are optional unless stated otherwise.
Changes require a **server restart** to take effect.

## Basic Server Information
### `name`
- **Type:** string
- **Description:** Human-readable name of the server. This is shown to players in server lists.
---
### `port`
- **Type:** integer
- **Description:** Network port the server listens on.
---
### `public`
- **Type:** boolean
- **Description:**
- `true` - the server is publicly visible (for example in server lists).
- `false` - the server is private and not publicly listed.
---
### `slots`
- **Type:** integer
- **Description:** Maximum number of players that can connect to the server at the same time.
---
### `admin_passwd`
- **Type:** string
- **Description:** Password required for administrative access.
---
### `auth_key`
- **Type:** string
- **Description:** Authentication key used for secure communication or external services.
---
### `seconds_per_game_minute`
- **Type:** integer
- **Description:** Controls how fast in-game time passes.
Lower values make game time pass faster; higher values slow it down.
A value of `0` disables custom time scaling and uses the default behavior.

---
## Server Identity
### `server_identity_seed`
- **Type:** string
- **Description:**
Unique secret value that defines the server's identity.
This seed is used to generate cryptographic keys that identify the server.
- **Important notes:**
- **Do not share this value.**
- Keep a backup to preserve the server's identity when moving or reinstalling.
- Changing this value makes the server appear as a completely new server.

---
## Gameplay
### `map`
- **Type:** string
- **Description:** Path to the world (`.ZEN`) file that the server loads.
---
### `map_md5`
- **Type:** string
- **Description:** Optional checksum of the map file.
Can be used to ensure players are using the correct version of the map.
---
### `allow_modification`
- **Type:** boolean
- **Description:** Allows or disallows client-side modifications when connecting to the server.
---
### `hide_map`
- **Type:** boolean
- **Description:** Hides map information from clients when enabled.
---
### `respawn_time_seconds`
- **Type:** integer
- **Description:** Time (in seconds) before a player respawns after death.

---
## Logging
### `log_file`
- **Type:** string
- **Description:** File path where the server writes its log output.
---
### `log_to_stdout`
- **Type:** boolean
- **Description:**
- `true` - logs are also printed to the console.
- `false` - logs are written only to the log file.
---
### `log_level`
- **Type:** string
- **Allowed values:** `"trace"`, `"debug"`, `"info"`, `"warn"`, `"error"`, `"critical"`
- **Description:** Controls how detailed the server logs are.

---
## Performance
### `tick_rate_ms`
- **Type:** integer
- **Description:** Server update interval in milliseconds.
Lower values increase update frequency but require more CPU resources.

---
## Process Management
### `daemon`
- **Type:** boolean
- **Description:**
- `true` - runs the server as a background (detached) process on Linux.
- `false` - runs the server in the foreground.
