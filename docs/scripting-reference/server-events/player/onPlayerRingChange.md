---
title: 'onPlayerRingChange'
---
# `event` onPlayerRingChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player's ring changes.

## Parameters
```c++
void onPlayerRingChange(int player_id, int hand_id, int|nil instance)
```

* `int` **player_id**: Player id.
* `int` **hand_id**: Hand id (0 = left, 1 = right).
* `int|nil` **instance**: New ring instance id (nil if none).
