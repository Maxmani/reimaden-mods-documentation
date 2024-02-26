---
title: Prevent Totem (Power Type)
description: Voile Documentation
---

# Prevent Totem

`Since v1.1.0`

Prevents the entity that has the power from activating totems of undying.

Type ID: `voile:prevent_totem`

### Fields

*None.*

### Examples

```json
{
    "type": "voile:prevent_totem",
    "condition": {
        "type": "apoli:on_block",
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:grass_block"
        }
    }
}
```

This example will prevent the entity that has the power from activating totems of undying while standing on grass blocks.