---
title: 'Discord'
---
# `class` Discord <font size="4">(client-side)</font>

This class exposes static methods for updating the user's Discord activity from the game client.


## Properties
### `string` state 

Gets or sets the draw position in pixel coordinates.

----
### `string` details 

Gets or sets the draw position in pixel coordinates.

----
### `string` largeImageKey 

Gets or sets the draw position in pixel coordinates.

----
### `string` largeImageText 

Gets or sets the draw position in pixel coordinates.

----
### `string` smallImageKey 

Gets or sets the draw position in pixel coordinates.

----
### `string` smallImageText 

Gets or sets the draw position in pixel coordinates.

----

## Methods
### `static` SetActivity

Updates the Discord Rich Presence activity.

All parameters are optional and should be passed via a table. Missing fields default to empty values.

```cpp
void SetActivity(table Activity)
```

**Parameters:**

* `table` **Activity**: configuration table.
  

----

## Callbacks
No callbacks.

----
