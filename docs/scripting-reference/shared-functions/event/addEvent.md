---
title: 'addEvent'
---
# `function` addEvent <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will register a new custom event with specified name.

## Declaration
```cpp
boolean addEvent(string eventName, bool allowRemoteTrigger)
```

## Parameters
* `string` **eventName**: The name of the event.
* `bool` **allowRemoteTrigger**: Whether the event can be triggered remotely. (Optional)
  
## Returns `boolean`
True on success, false if the event already exists.
