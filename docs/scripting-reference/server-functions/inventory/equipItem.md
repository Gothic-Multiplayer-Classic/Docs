---
title: 'equipItem'
---
# `function` equipItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Equip an item for all players.

## Declaration
```cpp
boolean equipItem(int player_id, string instance, int slot_id)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **instance**: Item instance name from scripts.
* `int` **slot_id**: Optional slot id. Defaults to -1 for first free slot.
  
## Returns `boolean`
True on success.
