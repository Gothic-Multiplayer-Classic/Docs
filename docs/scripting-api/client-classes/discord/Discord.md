---
title: 'Discord'
---
# `class` Discord <font size="4">(client-side)</font>

This class exposes static methods for updating the user's Discord activity from the game client.


## Properties
No properties.

----

## Methods
### `static` SetActivity

Updates the Discord Rich Presence activity. 

All parameters are optional and should be passed via a table. Missing fields default to empty values.

```cpp
void SetActivity(table params, string params, string params, string params, string params, string params, string params)
```

**Parameters:**

* `table` **params**: Activity configuration table.
* `string` **params**: .state Text shown as the activity state.
* `string` **params**: .details Text shown as activity details.
* `string` **params**: .largeImageKey Key of the large image asset.
* `string` **params**: .largeImageText Tooltip text for the large image.
* `string` **params**: .smallImageKey Key of the small image asset.
* `string` **params**: .smallImageText Tooltip text for the small image.
  

----

## Callbacks
No callbacks.

----
