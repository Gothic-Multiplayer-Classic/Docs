---
title: 'getPlayerPosition'
---
# `function` getPlayerPosition <font size="4">(server-side)</font>

Get a player's position as a table {x,y,z} or nil if unavailable.

## Declaration
```cpp
{x, y, z}|nil getPlayerPosition(int player_id)
```

## Parameters
* `int` **player_id**: Target player id.
  
## Returns `{x, y, z}|nil`
Table containing x,y,z or nil.
