---
title: 'Mat4'
---
# `class` Mat4 <font size="4">(shared-side)</font>

4x4 matrix with common transformation utilities (rotation, scaling, translation).

### Constructor
```cpp
Mat4.new()
```

**Parameters:**

No parameters.
### Constructor
```cpp
Mat4.new(number value)
```

**Parameters:**

* `number` **value**: Scalar initialization value.
### Constructor
```cpp
Mat4.new(Vec4 v0, Vec4 v1, Vec4 v2, Vec4 v3)
```

**Parameters:**

* `Vec4` **v0**: First row vector.
* `Vec4` **v1**: Second row vector.
* `Vec4` **v2**: Third row vector.
* `Vec4` **v3**: Fourth row vector.

## Properties
No properties.

----

## Methods
### makeIdentity

Resets the matrix to identity.

```cpp
void makeIdentity()
```

  

----
### makeZero

Sets all matrix elements to zero.

```cpp
void makeZero()
```

  

----
### makeOrthonormal

Orthonormalizes the upper-left 3x3 basis vectors while preserving translation.

```cpp
void makeOrthonormal()
```

  

----
### isUpper3x3Orthonormal

Returns true if the upper 3x3 basis vectors are orthonormal.

```cpp
bool isUpper3x3Orthonormal()
```

  
**Returns `bool`:**

True if orthonormal within epsilon tolerance.

----
### transpose

Returns the transposed matrix.

```cpp
Mat4 transpose()
```

  
**Returns `Mat4`:**

Transposed matrix.

----
### inverse

Returns the inverse matrix.

```cpp
Mat4 inverse()
```

  
**Returns `Mat4`:**

Inverse matrix.

----
### inverseLinTrafo

Returns the inverse of a linear transform with translation.

This is intended for typical transform matrices (rotation/scale + translation).

```cpp
Mat4 inverseLinTrafo()
```

  
**Returns `Mat4`:**

Inverse linear transform matrix.

----
### rotate

Rotates a vector by the matrix (ignores translation).

```cpp
Vec3 rotate(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: Vector to rotate.
  
**Returns `Vec3`:**

Rotated vector.

----
### setRightVector

Sets the right basis vector.

```cpp
void setRightVector(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: New right vector.
  

----
### getRightVector

Returns the right basis vector.

```cpp
Vec3 getRightVector()
```

  
**Returns `Vec3`:**

Right vector.

----
### setAtVector

Sets the forward (at) basis vector.

```cpp
void setAtVector(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: New at vector.
  

----
### getAtVector

Returns the forward (at) basis vector.

```cpp
Vec3 getAtVector()
```

  
**Returns `Vec3`:**

At vector.

----
### setUpVector

Sets the up basis vector.

```cpp
void setUpVector(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: New up vector.
  

----
### getUpVector

Returns the up basis vector.

```cpp
Vec3 getUpVector()
```

  
**Returns `Vec3`:**

Up vector.

----
### setTranslation

Sets the translation component.

```cpp
void setTranslation(Vec3 vec)
```

**Parameters:**

* `Vec3` **vec**: New translation vector.
  

----
### getTranslation

Returns the translation component.

```cpp
Vec3 getTranslation()
```

  
**Returns `Vec3`:**

Translation vector.

----
### resetRotation

Resets rotation to identity while preserving translation.

```cpp
void resetRotation()
```

  

----
### extractRotation

Extracts the rotation part of the matrix (scaling removed).

```cpp
Mat3 extractRotation()
```

  
**Returns `Mat3`:**

Rotation matrix.

----
### extractScaling

Extracts scaling factors from the matrix basis vectors.

```cpp
Vec3 extractScaling()
```

  
**Returns `Vec3`:**

Scaling factors for x, y and z axes.

----
### postRotateX

Post-multiplies a rotation around the X axis (degrees).

```cpp
void postRotateX(number angle_degrees)
```

**Parameters:**

* `number` **angle_degrees**: Rotation angle in degrees.
  

----
### postRotateY

Post-multiplies a rotation around the Y axis (degrees).

```cpp
void postRotateY(number angle_degrees)
```

**Parameters:**

* `number` **angle_degrees**: Rotation angle in degrees.
  

----
### postRotateZ

Post-multiplies a rotation around the Z axis (degrees).

```cpp
void postRotateZ(number angle_degrees)
```

**Parameters:**

* `number` **angle_degrees**: Rotation angle in degrees.
  

----
### preScale

Pre-multiplies a scaling transformation.

```cpp
void preScale(Vec3 scale)
```

**Parameters:**

* `Vec3` **scale**: Scaling factors for x, y and z axes.
  

----
### postScale

Post-multiplies a scaling transformation.

```cpp
void postScale(Vec3 scale)
```

**Parameters:**

* `Vec3` **scale**: Scaling factors for x, y and z axes.
  

----
### `static` swap

Swaps two matrices.

```cpp
void swap(Mat4 mat1, Mat4 mat2)
```

**Parameters:**

* `Mat4` **mat1**: First matrix.
* `Mat4` **mat2**: Second matrix.
  

----
### `static` lookAt

Builds a look-at transform from a position, target and up vector.

```cpp
Mat4 lookAt(Vec3 from, Vec3 to, Vec3 up)
```

**Parameters:**

* `Vec3` **from**: Camera/world position.
* `Vec3` **to**: Target position to look at.
* `Vec3` **up**: Up direction vector.
  
**Returns `Mat4`:**

Look-at matrix.

----
### data

Returns a pointer to the raw matrix data (column-major float array).

```cpp
userdata data()
```

  
**Returns `userdata`:**

Pointer to matrix float data.

----

## Callbacks
No callbacks.

----
