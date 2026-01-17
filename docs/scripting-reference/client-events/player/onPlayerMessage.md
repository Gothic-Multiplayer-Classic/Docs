---
title: 'onPlayerMessage'
---
# `event` onPlayerMessage <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a chat message is received locally.

## Parameters
```c++
void onPlayerMessage(int sender_id, int r, int g, int b, string message)
```

* `int` **sender_id**: Optional sender id (nil for system).
* `int` **r**: Red color component.
* `int` **g**: Green color component.
* `int` **b**: Blue color component.
* `string` **message**: Message text.
