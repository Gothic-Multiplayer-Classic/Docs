---
title: 'equipItem'
---
# `function` equipItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Equip an item for a player or NPC on the client.

## Declaration
```cpp
boolean equipItem(int player_id, string instance, int slot_id)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **instance**: Item instance name.
* `int` **slot_id**: Optional slot id, ignored on client.
  
## Returns `boolean`
True on success.
