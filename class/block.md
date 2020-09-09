# Introduction
A `block` is a three-dimensional object that holds a variety of **properties** and can be manipulated with **methods**, as listed below. Blocks can be interacted with in the three-dimensional space in a handful of ways, usually through *events*.

## Block Properties
A block has several properties than can be altered via a simple script. As an example, we could alter a block's colour:
```
block.colour = colour.white()
```

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
