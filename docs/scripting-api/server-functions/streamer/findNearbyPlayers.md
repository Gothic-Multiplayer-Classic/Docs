---
title: 'findNearbyPlayers'
---
# `function` findNearbyPlayers <font size="4">(server-side)</font>

Find player ids within a radius of a given position in a world.

## Declaration
```cpp
{...} findNearbyPlayers({x, y, z} position_table, int radius, string world, int virtual_world)
```

## Parameters
* `{x, y, z}` **position_table**: Table with x,y,z coordinates.
* `int` **radius**: Search radius.
* `string` **world**: World name to search in.
* `int` **virtual_world**: Optional virtual world id.
  
## Returns `{...}`
Array of player ids.

