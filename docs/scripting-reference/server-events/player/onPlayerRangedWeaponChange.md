---
title: 'onPlayerRangedWeaponChange'
---
# `event` onPlayerRangedWeaponChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player's ranged weapon changes.

## Parameters
```c++
void onPlayerRangedWeaponChange(int player_id, int|nil instance)
```

* `int` **player_id**: Player id.
* `int|nil` **instance**: New ranged weapon instance id (nil if none).
