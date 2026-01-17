---
title: 'onPlayerHit'
---
# `event` onPlayerHit <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player is hit.

## Parameters
```c++
void onPlayerHit(int attacker_id, int victim_id, int damage)
```

* `int` **attacker_id**: Optional attacker id (nil if none).
* `int` **victim_id**: Victim player id.
* `int` **damage**: Damage dealt.
