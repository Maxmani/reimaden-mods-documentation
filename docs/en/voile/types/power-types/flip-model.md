---
title: Flip Model (Power Type)
description: Voile Documentation
---

# Flip Model

Flips the entity's model upside down as if it has the name `Dinnerbone` or `Grumm`. Entities that have already been named this way are flipped back.

Type ID: `voile:flip_model`

### Fields

*None.*

### Examples

```json
{
    "type": "voile:flip_model"
}
```

This example flips the entity's model upside down.

```json
{
    "type": "voile:flip_model",
    "condition": {
        "type": "apoli:on_block",
        "inverted": true
    }
}
```

This example flips the entity's model upside down when not standing on a block.