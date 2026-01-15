---
title: 'sendMessageToPlayer'
---
# `function` sendMessageToPlayer <font size="4">(server-side)</font>

Send a colored chat message to a specific player.

## Declaration
```cpp
boolean sendMessageToPlayer(int player_id, int r, int g, int b, string text)
```

## Parameters
* `int` **player_id**: Target player id.
* `int` **r**: Red component (0-255).
* `int` **g**: Green component (0-255).
* `int` **b**: Blue component (0-255).
* `string` **text**: Message text to send.
  
## Returns `boolean`
True on success.
