---
title: 'triggerClientEvent'
---
# `function` triggerClientEvent <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    If sendTo is omitted or `nil`, the event is sent to all connected players. If sendTo is a number, it is treated as a single player id. If sendTo is a table, it must contain player ids.
!!! note
    You may optionally provide a numeric source element id after the event name, followed by any number of additional arguments to send with the event.

Triggers a custom client-side event for one or more players and optionally passes arguments.

## Declaration
```cpp
bool triggerClientEvent(int|{...}|nil sendTo, string eventName, int|nil sourceElement, ... ...)
```

## Parameters
* `int|{...}|nil` **sendTo**: Target player id, table of player ids, or nil to send to all players.
* `string` **eventName**: Name of the client-side event to trigger.
* `int|nil` **sourceElement**: Optional source element id. If omitted or nil, defaults to 0.
* `...` **...**: Optional arguments passed to the client event handler.
  
## Returns `bool`
True if the event was sent successfully, otherwise false.
