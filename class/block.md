# Introduction

A `block` is a three-dimensional object that holds a variety of **properties** and can be manipulated with **methods**, as listed below. Blocks can be interacted with in the three-dimensional space in a handful of ways, usually through *events*.

## Block Properties

A block has several properties than can be altered via a simple script. As an example, we could alter a block's colour:

```lua
block.colour = colour.white()
```

**Note**:
`block.metalness` and `block.roughness` can ***only*** have a value from 0 to 1.

## Block Events

Sometimes, on certain *events*, we may want to manipulate properties of a block. The `block` class accepts three events:

- Changed,
- Collision Ended, and
- Collision Started

### On Changed Events

These events are fired when a property is changed.

### On Collision Ended Events

These events are fired when there is no collision detected.

### On Collision Started Events

These events are fired when there is a collision detected.

## Examples

### Creating a block

You can use `core.construct` to create any object, and a block is no exception.

```lua
local myBlock = core.construct("block", {
    -- The initial properties of the block
    parent = core.scene,
    name = "My block",
    size = vector3(1,2,3)    
})
```

This would create a block within your scene with the name `My block` and which is 1 by 2 by 3 units in size.
