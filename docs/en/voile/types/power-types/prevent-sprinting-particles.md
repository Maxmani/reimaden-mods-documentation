---
title: Prevent Sprinting Particles (Power Type)
description: Voile Documentation
---

# Prevent Sprinting Particles

Prevents the entity that has the power from creating sprinting particles (the block particles spawned at the entity's feet when sprinting).

Type ID: `voile:prevent_sprinting_particles`

### Fields

*None.*

### Examples

```json
{
    "type": "voile:prevent_sprinting_particles"
}
```

This example will prevent the entity that has the power from creating sprinting particles.

```json
{
    "type": "voile:prevent_sprinting_particles",
    "condition": {
        "type": "apoli:in_rain"
    }
}
```

This example will prevent the entity that has the power from creating sprinting particles while in rain.