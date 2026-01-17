---
title: 'getPlayerSkillWeapon'
---
# `function` getPlayerSkillWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Get a player's weapon skill hit chance.

## Declaration
```cpp
int|nil getPlayerSkillWeapon(int player_id, int skill_id)
```

## Parameters
* `int` **player_id**: Target player id.
* `int` **skill_id**: Skill identifier.
  
## Returns `int|nil`
Hit chance (0-100) or nil.
