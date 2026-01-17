---
title: 'getPlayerVisual'
---
# `function` getPlayerVisual <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Get a player's visual information as a table or nil if unavailable.

## Declaration
```cpp
{bodyModel, bodyTexture, headModel, headTexture}|nil getPlayerVisual(int player_id)
```

## Parameters
* `int` **player_id**: Target player id.
  
## Returns `{bodyModel, bodyTexture, headModel, headTexture}|nil`
Table with bodyModel, bodyTexture, headModel, headTexture or nil.
