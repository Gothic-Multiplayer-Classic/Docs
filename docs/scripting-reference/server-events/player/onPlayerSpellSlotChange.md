---
title: 'onPlayerSpellSlotChange'
---
# `event` onPlayerSpellSlotChange <font size="4">(server-side)</font>

Triggered when a player's active spell slot changes.

## Parameters
```c++
void onPlayerSpellSlotChange(int player_id, int slot_id, int|nil instance)
```

* `int` **player_id**: Player id.
* `int` **slot_id**: Active spell slot id.
* `int|nil` **instance**: Spell instance id (nil if none).
