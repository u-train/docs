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
| input | false | singleton | Provides an entry point to user input (mouse, keyboard, etc) |
| json | false | singleton | JSON utility functionality |
| base64 | false | singleton | placeholder |
| dev | false | singleton | **Restricted, requesting this permission may have your app rejected** |
| networking | false | singleton | Provides the functionality to interact with the server (client - server model) |
| http | false | singleton | Provides the functionality to make web requests (GET, POST, etc) |
| interface | false | singleton | Top-level interface that controls what is displayed on the screen |
| construct | false | function | Provides the ability to create new instances |
| debug | false | singleton | Provides a way to debug the current enviroment |
| tween | false | singleton | Provides functionality to interpolate smoothly via a value or set of values under an object |
| graphics | false | singleton | Provides functionality to change or debug graphics |
| reflection | false | singleton | Provides a way to see what objects, values or enums are reflected from the engine to lua visibility |
| datastore | false | singleton | Provides a way to save, store and manipulate client data |
| process | false | singleton | Provides functionality to redirect |
| workshop | false | singleton | **Restricted, requesting this permission may have your app rejected**  |
