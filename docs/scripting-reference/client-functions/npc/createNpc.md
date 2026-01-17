---
title: 'createNpc'
---
# `function` createNpc <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Create a client-side NPC entry and return an internal npc id (<0).

## Declaration
```cpp
int createNpc(string name)
```

## Parameters
* `string` **name**: Name for the created NPC.
  
## Returns `int`
Internal npc id (negative) or 0 on failure.
