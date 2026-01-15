---
title: 'onPlayerCastSpell'
---
# `event` onPlayerCastSpell <font size="4">(server-side)</font>

Triggered when a player casts a spell.

## Parameters
```c++
void onPlayerCastSpell(int caster_id, int spell_id, int target_id)
```

* `int` **caster_id**: Caster player id.
* `int` **spell_id**: Spell identifier.
* `int` **target_id**: Optional target player id (nil if none).
