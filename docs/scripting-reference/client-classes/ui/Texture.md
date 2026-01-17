---
title: 'Texture'
---
# `class` Texture <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"



### Constructor
```cpp
Texture.new(int x, int y, int width, int height, string file)
```

**Parameters:**

* `int` **x**: X position (virtual units).
* `int` **y**: Y position (virtual units).
* `int` **width**: Width (virtual units).
* `int` **height**: Height (virtual units).
* `string` **file**: Texture file path.

## Properties
### `{x, y}` position 

Gets or sets the texture position in virtual screen units.

----
### `{x, y}` positionPx 

Gets or sets the texture position in pixel coordinates.

----
### `{width, height}` size 

Gets or sets the texture size in virtual screen units.

----
### `{width, height}` sizePx 

Gets or sets the texture size in pixel coordinates.

----
### `{x, y, width, height}` rect 

Gets or sets the texture rectangle in virtual screen units.

----
### `{x, y, width, height}` rectPx 

Gets or sets the texture rectangle in pixel coordinates.

----
### `{r, g, b}` color 

Gets or sets the texture color.

----
### `int` alpha 

Gets or sets the texture alpha (opacity).

----
### `bool` visible 

Gets or sets whether the texture is rendered.

----
### `string` file 

Gets or sets the texture file path.

----

## Methods
### setPosition

Sets the texture position in virtual screen units.

```cpp
void setPosition(int x, int y)
```

**Parameters:**

* `int` **x**: X position (virtual units).
* `int` **y**: Y position (virtual units).
  

----
### getPosition

Returns the texture position in virtual screen units.

```cpp
{x, y} getPosition()
```

  
**Returns `{x, y}`:**

Table containing x and y (virtual units).

----
### setPositionPx

Sets the texture position in pixel coordinates.

```cpp
void setPositionPx(int x, int y)
```

**Parameters:**

* `int` **x**: X position (pixels).
* `int` **y**: Y position (pixels).
  

----
### getPositionPx

Returns the texture position in pixel coordinates.

```cpp
{x, y} getPositionPx()
```

  
**Returns `{x, y}`:**

Table containing x and y (pixels).

----
### setSize

Sets the texture size in virtual screen units.

```cpp
void setSize(int width, int height)
```

**Parameters:**

* `int` **width**: Width (virtual units).
* `int` **height**: Height (virtual units).
  

----
### getSize

Returns the texture size in virtual screen units.

```cpp
{width, height} getSize()
```

  
**Returns `{width, height}`:**

Table containing width and height (virtual units).

----
### setSizePx

Sets the texture size in pixel coordinates.

```cpp
void setSizePx(int width, int height)
```

**Parameters:**

* `int` **width**: Width (pixels).
* `int` **height**: Height (pixels).
  

----
### getSizePx

Returns the texture size in pixel coordinates.

```cpp
{width, height} getSizePx()
```

  
**Returns `{width, height}`:**

Table containing width and height (pixels).

----
### setRect

Sets the texture rectangle in virtual screen units.

```cpp
void setRect(int x, int y, int width, int height)
```

**Parameters:**

* `int` **x**: X position (virtual units).
* `int` **y**: Y position (virtual units).
* `int` **width**: Width (virtual units).
* `int` **height**: Height (virtual units).
  

----
### getRect

Returns the texture rectangle in virtual screen units.

```cpp
{x, y, width, height} getRect()
```

  
**Returns `{x, y, width, height}`:**

Table containing x,y,width,height (virtual units).

----
### setRectPx

Sets the texture rectangle in pixel coordinates.

```cpp
void setRectPx(int x, int y, int width, int height)
```

**Parameters:**

* `int` **x**: X position (pixels).
* `int` **y**: Y position (pixels).
* `int` **width**: Width (pixels).
* `int` **height**: Height (pixels).
  

----
### getRectPx

Returns the texture rectangle in pixel coordinates.

```cpp
{x, y, width, height} getRectPx()
```

  
**Returns `{x, y, width, height}`:**

Table containing x,y,width,height (pixels).

----
### setColor

Sets the texture color.

```cpp
void setColor(int r, int g, int b)
```

**Parameters:**

* `int` **r**: Red component (0-255).
* `int` **g**: Green component (0-255).
* `int` **b**: Blue component (0-255).
  

----
### getColor

Returns the texture color.

```cpp
{r, g, b} getColor()
```

  
**Returns `{r, g, b}`:**

Table containing r,g,b (0-255).

----
### setAlpha

Sets the texture alpha (opacity).

```cpp
void setAlpha(int alpha)
```

**Parameters:**

* `int` **alpha**: Opacity value (0-255).
  

----
### getAlpha

Returns the texture alpha (opacity).

```cpp
int getAlpha()
```

  
**Returns `int`:**

Opacity value (0-255).

----
### setFile

Sets the texture file name.

```cpp
void setFile(string file)
```

**Parameters:**

* `string` **file**: Texture file name.
  

----
### getFile

Returns the texture file name.

```cpp
string getFile()
```

  
**Returns `string`:**

Texture file name.

----
### setVisible

Sets whether the texture should be rendered.

```cpp
void setVisible(bool visible)
```

**Parameters:**

* `bool` **visible**: True to render, false to hide.
  

----
### getVisible

Returns whether the texture is visible.

```cpp
bool getVisible()
```

  
**Returns `bool`:**

True if visible.

----
### top

Moves the texture to the top of the render order.

```cpp
void top()
```

  

----

## Callbacks
No callbacks.

----
