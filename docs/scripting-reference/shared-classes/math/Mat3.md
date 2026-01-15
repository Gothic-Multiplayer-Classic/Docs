---
title: 'Mat3'
---
# `class` Mat3 <font size="4">(shared-side)</font>

3x3 matrix with common transformation utilities.

### Constructor
```cpp
Mat3.new()
```

**Parameters:**

No parameters.
### Constructor
```cpp
Mat3.new(number value)
```

**Parameters:**

* `number` **value**: Scalar initialization value.
### Constructor
```cpp
Mat3.new(Vec3 v0, Vec3 v1, Vec3 v2)
```

**Parameters:**

* `Vec3` **v0**: First row vector.
* `Vec3` **v1**: Second row vector.
* `Vec3` **v2**: Third row vector.

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

Orthonormalizes the matrix basis vectors.

This makes the basis vectors unit-length and mutually orthogonal.

```cpp
void makeOrthonormal()
```

  

----
### isUpper3x3Orthonormal

Returns true if the matrix basis vectors are orthonormal.

```cpp
bool isUpper3x3Orthonormal()
```

  
**Returns `bool`:**

True if orthonormal within epsilon tolerance.

----
### transpose

Returns the transposed matrix.

```cpp
Mat3 transpose()
```

  
**Returns `Mat3`:**

Transposed matrix.

----
### inverse

Returns the inverse matrix.

```cpp
Mat3 inverse()
```

  
**Returns `Mat3`:**

Inverse matrix.

----
### rotate

Rotates a vector by this matrix.

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
### resetRotation

Resets rotation to identity.

```cpp
void resetRotation()
```

  

----
### extractRotation

Returns a copy of this matrix with scaling removed.

```cpp
Mat3 extractRotation()
```

  
**Returns `Mat3`:**

Rotation-only matrix.

----
### extractScaling

Extracts scaling factors from the basis vectors.

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
void swap(Mat3 mat1, Mat3 mat2)
```

**Parameters:**

* `Mat3` **mat1**: First matrix.
* `Mat3` **mat2**: Second matrix.
  

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
