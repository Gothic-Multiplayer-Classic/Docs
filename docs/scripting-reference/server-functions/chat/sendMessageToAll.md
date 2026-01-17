---
title: 'sendMessageToAll'
---
# `function` sendMessageToAll <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Send a colored chat message to all connected players.

## Declaration
```cpp
boolean sendMessageToAll(int r, int g, int b, string text)
```

## Parameters
* `int` **r**: Red component (0-255).
* `int` **g**: Green component (0-255).
* `int` **b**: Blue component (0-255).
* `string` **text**: Message text to send.
  
## Returns `boolean`
True on success.
