---
title: Zombie Arms (Power Type)
description: Voile Documentation
---

# Zombie Arms

`Since v1.0.0`

Makes the entity's arms point forward like a zombie.

Type ID: `voile:zombie_arms`

!!! note
    
    This power only works on biped entities.  
    It it also not active while using items, swimming, or gliding with elytra.

### Fields

*None.*

### Examples

```json
{
    "type": "voile:zombie_arms",
    "condition": {
        "type": "apoli:sneaking",
        "inverted": true
    }
}
```

This example makes the entity's arms point forward like a zombie when not sneaking.