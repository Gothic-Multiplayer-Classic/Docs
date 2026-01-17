---
title: 'getPlayerPosition'
---
# `function` getPlayerPosition <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Get a player's world position as tuple (x,y,z).

## Declaration
```cpp
{x,y,z}|nil getPlayerPosition(int player_id)
```

## Parameters
* `int` **player_id**: Target player id.
  
## Returns `{x,y,z}|nil`
Table with keys `x`,`y`,`z` or nil.
