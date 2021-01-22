---
title: quaternion
description: 
published: true
tags: 
---

Quaternions consist of four components: `x`, `y`, `z` and `w`.

## Constructors

`quaternion(float x, float y, float z, float w)`  
Creates a rotation with the specific x, y, z, w components provided

`quaternion.euler(float x, float y, float z)`  
`quaternion.euler(vector3 euler)`  
Creates a rotation from the provided Euler angle.

`quaternion.fromTo(vector3 fromDir, vector3 toDir)`  
Creates a rotation that rotates from `fromDir` to `toDir`.

`quaternion.lookRotation(vector3 forward, vector3 up = vector3(0, 1, 0))`  
Creates a rotation with the provided forward and up directions. Note that the up parameter is optional and most commonly can be left nil.

`quaternion.angleAxis(float angle, vector3 axis)`  
Creates a rotation which rotates `angle` around `axis`.

## Methods

`bool` `a:isNan()`  
Returns true if the `a` quaternion is a NaN value

`quaternion` `a:inverse()`  
Returns the inverse of the `a` quaternion

`quaternion` `a:lerp(quaternion target, float alpha)`  
Returns a quaternion lerped towards `target` from `a`

`quaternion` `a:slerp(quaternion target, float alpha)`  
Returns a quaternion slerped towards `target` from `a`

`quaternion` `a:dot(quaternion b)`  
Returns a the dot product between the two `a` and `b` rotations

`float` `a:angle(quaternion b)`  
Returns the angle between the two `a` and `b` rotations

`quaternion` `a:normal()`  
Returns a normalised version of the `a` rotation

`quaternion` `from:rotateTowards(quaternion to, float maxDegreesDelta)`  
Returns a rotation rotated towards `to` from `from`

`float angle`, `vector3 axis` `a:getAngleAxis()`  
Returns two values, the `angle` and `axis` of the `a` rotation.

`vector3 euler` `a:getEuler()`  
Returns the rotation expressed as an Euler angle

## Usage

```lua
  local rotation = quaternion(0, 0, 0, 1) -- identity
  
  rotation = rotation * quaternion.euler(0, math.rad(45), 0)
```
