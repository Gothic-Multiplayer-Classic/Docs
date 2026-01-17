---
title: 'onUseItem'
---
# `event` onUseItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when the hero uses, interacts with, opens, or consumes an item.

## Parameters
```c++
void onUseItem(string item, string scheme, int from, int to)
```

* `string` **item**: Item instance.
* `string` **scheme**: Item scheme name, if available.
* `int` **from**: Previous interact state.
* `int` **to**: Current interact state.
