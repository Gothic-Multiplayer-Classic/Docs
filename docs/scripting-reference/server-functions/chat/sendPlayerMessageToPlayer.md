---
title: 'sendPlayerMessageToPlayer'
---
# `function` sendPlayerMessageToPlayer <font size="4">(server-side)</font>

Send a player-sourced colored message to a specific player.

## Declaration
```cpp
boolean sendPlayerMessageToPlayer(int sender_id, int receiver_id, int r, int g, int b, string text)
```

## Parameters
* `int` **sender_id**: Sender player id.
* `int` **receiver_id**: Receiver player id.
* `int` **r**: Red component (0-255).
* `int` **g**: Green component (0-255).
* `int` **b**: Blue component (0-255).
* `string` **text**: Message text.
  
## Returns `boolean`
True on success.

