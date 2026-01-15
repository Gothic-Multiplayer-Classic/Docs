---
title: 'setPlayerWorld'
---
# `function` setPlayerWorld <font size="4">(server-side)</font>

Move a player to a different world, optionally specifying a start point.

## Declaration
```cpp
boolean setPlayerWorld(int player_id, string world, string start_point)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **world**: World name.
* `string` **start_point**: Optional start point name.
  
## Returns `boolean`
True on success.
