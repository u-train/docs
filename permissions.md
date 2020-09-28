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

# Avaliable permissions
| permission | default | type | description |
| --- | --- | --- | --- | 
| disconnect | false | function | Provides the power of disconnecting event listeners |
| scene | false | singleton | The 3D scene |
| input | false | singleton | Manages the inputs such as mouse and also gives access to screen. |
| json | false | singleton | Json |
| base64 | false | singleton | Base64 encryption and decryption. |
| dev\* | false | singleton | Gives access to internal functionalities, such as coreInterface. |
| networking | false | singleton | Communication between the server and client. |
| http | false | singleton | Communication to the webs with HTTP. |
| interface | false | singleton | This is where the UI are located. |
| construct | false | function | Provides the ability to create new instances |
| debug | false | singleton | Debug such as print events and traceback. |
| tween | false | singleton | Tweens |
| graphics | false | singleton | 3D rendering. |
| reflection | false | singleton | Reflection of ``core`` class. |
| datastore | false | singleton | Storage of data that is persisent. |
| process | false | singleton | Work in progress. |
| workshop\* | false | singleton | Soon to be depericated. Was used for special functionalities made for workshop. |

\*If these classes are allowed, your app will most likely be rejected. This is because they are not to meant to be used outside of internal code.
