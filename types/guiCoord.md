---
title: guiCoord
description: 
published: true
tags: 
---

# guiCoord

guiCoords consist of two `vector2` components: `scale` and `offset`

## Constructors

`guiCoord(float scaleX, int offsetX, float scaleY, int offsetY)`  

## Methods

`vector2` `a:get2D(vector2 parentAbsoluteSize)`  
Returns a calculated absolute size based on the provided `parentAbsoluteSize`

## Usage

```lua
  local size = guiCoord(1, 0, 1, 0)
  
  print(size.scale) --> vector2(1, 1)
  print(size.offset) --> vector2(0, 0)
```
