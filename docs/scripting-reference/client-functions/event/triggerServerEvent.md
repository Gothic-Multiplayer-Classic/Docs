---
title: 'triggerServerEvent'
---
# `function` triggerServerEvent <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    You may optionally provide a numeric source element id as the next argument, followed by any number of additional arguments to send with the event.
!!! note
    `sourceElement` is an optional numeric identifier that represents the object or entity that caused the event. Its meaning is user-defined and depends on the game logic.

Triggers a custom server-side event and optionally passes arguments.
The first argument is always the event name.

## Declaration
```cpp
bool triggerServerEvent(string eventName, int|nil sourceElement, ... ...)
```

## Parameters
* `string` **eventName**: Name of the server-side event to trigger.
* `int|nil` **sourceElement**: Optional source element id. Use nil or omit it if not needed.
* `...` **...**: Optional arguments passed to the server event handler.
  
## Returns `bool`
True if the event was sent successfully, otherwise false.
