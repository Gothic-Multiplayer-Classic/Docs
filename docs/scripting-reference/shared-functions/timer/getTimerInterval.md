---
title: 'getTimerInterval'
---
# `function` getTimerInterval <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Returns the interval (in milliseconds) of a timer, or nil if the timer does not exist.

## Declaration
```cpp
int|nil getTimerInterval(int timer_id)
```

## Parameters
* `int` **timer_id**: Timer ID returned by setTimer.
  
## Returns `int|nil`
Interval in milliseconds, or nil if not found.
