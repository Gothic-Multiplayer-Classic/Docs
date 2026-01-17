---
title: 'onPlayerDeath'
---
# `event` onPlayerDeath <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player dies.

## Parameters
```c++
void onPlayerDeath(int player_id, int killer_id)
```

* `int` **player_id**: The id of the player who died.
* `int` **killer_id**: Optional id of the killer (nil if none).
