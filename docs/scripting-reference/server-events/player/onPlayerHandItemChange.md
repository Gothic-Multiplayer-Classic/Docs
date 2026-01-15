---
title: 'onPlayerHandItemChange'
---
# `event` onPlayerHandItemChange <font size="4">(server-side)</font>

Triggered when a player's hand item changes.

## Parameters
```c++
void onPlayerHandItemChange(int player_id, int hand, int|nil instance)
```

* `int` **player_id**: Player id.
* `int` **hand**: Hand id (0 = left, 1 = right).
* `int|nil` **instance**: New hand item instance id (nil if none).
