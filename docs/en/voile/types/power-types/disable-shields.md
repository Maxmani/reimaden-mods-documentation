---
title: Disable Shields (Power Type)
description: Voile Documentation
---

# Disable Shields

`Since v1.0.0`

Allows the entity that has the power to disable shields as if they were using an axe.

Type ID: `voile:disable_shields`

!!! tip
    
    Also check out the [Disable Shield](../entity-action-types/disable-shield.md) entity action type if you want to disable shields in other ways than just using melee attacks.

### Fields

*None.*

### Examples

```json
{
    "type": "voile:disable_shields"
}
```

This example allows the entity that has the power to disable shields at all times.

```json
{
    "type": "voile:disable_shields",
    "condition": {
        "type": "apoli:status_effect",
        "effect": "minecraft:strength"
    }
}
```

This example allows the entity that has the power to disable shields while they have the Strength effect.