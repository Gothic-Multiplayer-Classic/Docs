---
title: 'onPlayerUnspawnFor'
---
# `event` onPlayerUnspawnFor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player is unspawned for another player (streaming out).

## Parameters
```c++
void onPlayerUnspawnFor(int player_id, int spawn_id)
```

* `int` **player_id**: Player id losing the spawn.
* `int` **spawn_id**: Player id removed for the receiver.
