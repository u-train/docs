The block is one of the most basic components in any 3D app. They can be coloured, textured and can have transparency and a variety of other effects applied to them.
Blocks are primarily kept within `core.scene`, and this is the space where users will be able to see and interact with your blocks.


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