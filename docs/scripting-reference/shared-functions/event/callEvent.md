---
title: 'callEvent'
---
# `function` callEvent <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will notify (call) every handler bound to specified custom event.

## Declaration
```cpp
boolean callEvent(string eventName, ... arguments)
```

## Parameters
* `string` **eventName**: The name of the event.
* `...` **arguments**: Variable number of arguments.
  
## Returns `boolean`
True when event was dispatched and not cancelled, otherwise false.
