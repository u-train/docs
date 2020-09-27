---
title: Permissions
description: 
published: true
tags: 
---

# Permissions in Deviap's manifest.json

Applications within Deviap are ran in a sandboxed environment. You need to specify explicitly what singletons your app will access in the manifest file. 

Apps should not request permission to access singletons that it does not need or use, doing so is bad practice and may have your app removed from the library.

Example:
```json
{
    "schema": 1,
    "id": "example",
    "networked": true,
    "version": "0.0.5",
    "permissions": {
        "client": {
            "networking": true,
            "interface": true,
            "construct": true,
            "tween": true
        },
        "server": {
            "networking": true
        }
    }
}
```

| permission | default | type | description |
| --- | --- | --- | --- | 
| disconnect | false | function | Provides the power of disconnecting event listeners |
| scene | false | singleton | The 3D scene |
| input | false | singleton | placeholder |
| json | false | singleton | placeholder |
| base64 | false | singleton | placeholder |
| dev | false | singleton | **Restricted, requesting this permission may have your app rejected** |
| networking | false | singleton | placeholder |
| http | false | singleton | placeholder |
| interface | false | singleton | placeholder |
| construct | false | function | Provides the ability to create new instances |
| debug | false | singleton | placeholder |
| tween | false | singleton | placeholder |
| graphics | false | singleton | placeholder |
| reflection | false | singleton | placeholder |
| datastore | false | singleton | placeholder |
| process | false | singleton | placeholder |
| workshop | false | singleton | **Restricted, requesting this permission may have your app rejected**  |
