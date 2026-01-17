---
title: 'sendPlayerMessageToAll'
---
# `function` sendPlayerMessageToAll <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Send a player-sourced colored message to all players (includes sender id).

## Declaration
```cpp
boolean sendPlayerMessageToAll(int sender_id, int r, int g, int b, string text)
```

## Parameters
* `int` **sender_id**: Sender player id.
* `int` **r**: Red component (0-255).
* `int` **g**: Green component (0-255).
* `int` **b**: Blue component (0-255).
* `string` **text**: Message text.
  
## Returns `boolean`
True on success.
