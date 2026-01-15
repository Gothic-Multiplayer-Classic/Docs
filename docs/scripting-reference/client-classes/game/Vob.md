---
title: 'Vob'
---
# `class` Vob <font size="4">(client-side)</font>

Represents a 3D object in the world.

### Constructor
```cpp
Vob.new(string model)
```

**Parameters:**

* `string` **model**: Visual model name (e.g. "SPHERE.3DS").

## Properties
### `string` objectName 

Represents the internal engine object name.

----
### `Mat4` matrix 

Represents the reference to the vob matrix.

----
### `Vob|nil` parent 

Represents the reference to the parent vob.
Note: the vob hierarchy will be lost after changing the world.

----
### `boolean` cdDynamic 

Represents the state of dynamic collision of vob. Enabling this option will prevent other dynamic objects from passing through it.

----
### `boolean` cdStatic 

Represents the state of static collision of vob. Enabling this option will prevent static objects (i.e. world mesh) from passing through it.

----
### `float` farClipZScale 

Represents the max distance at which the vob will still be rendered.

----
### `string` visual 

Represents the model file name used as vob visual, e.g. SPHERE.3DS.

----
### `float` visualAlpha 

Represents the transparency of the vob visual.

----

## Methods
### setPosition

Set the position of the vob in the world.

```cpp
void setPosition(float x, float y, float z)
```

**Parameters:**

* `float` **x**: Position on X axis.
* `float` **y**: Position on Y axis.
* `float` **z**: Position on Z axis.
  

----
### getPosition

Get the position of the vob in the world.

```cpp
{x, y, z} getPosition()
```

  
**Returns `{x, y, z}`:**



----
### setRotation

Set the euler rotation of the vob in the world.

```cpp
void setRotation(float x, float y, float z)
```

**Parameters:**

* `float` **x**: Rotation on X axis.
* `float` **y**: Rotation on Y axis.
* `float` **z**: Rotation on Z axis.
  

----
### getRotation

Get the euler rotation of the vob in the world.

```cpp
{x, y, z} getRotation()
```

  
**Returns `{x, y, z}`:**



----
### addToWorld

Add the vob to the currently loaded world. If the vob is not added, it won't show up.

```cpp
void addToWorld(Vob|nil parent)
```

**Parameters:**

* `Vob|nil` **parent**: Optional parent vob to attach to.
  

----
### removeFromWorld

Remove the vob from the currently loaded world.

```cpp
void removeFromWorld()
```

  

----
### floor

Try to put the vob on the floor. If the difference between vob position and the floor y position is <= 1000, the method succeeds.

```cpp
void floor()
```

  

----

## Callbacks
No callbacks.

----
