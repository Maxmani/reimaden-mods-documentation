---
title: Flip Model (Power Type)
description: Voile Documentation
---

# Flip Model

Flips the entity's model upside down as if it had the name `Dinnerbone` or `Grumm`. Entities that have already been named this way are flipped back instead.

Type ID: `voile:flip_model`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`flip_view` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether to flip the entity's view as well (only works on players).

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

```json
{
    "type": "voile:flip_model",
    "flip_view": true
}
```

This example flips the entity's model and view upside down.