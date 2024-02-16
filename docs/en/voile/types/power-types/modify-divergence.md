---
title: Modify Divergence (Power Type)
description: Voile Documentation
---

# Modify Divergence

`Since v1.0.0`

Modifies the divergence (accuracy) of the entity's projectiles.

Type ID: `voile:modify_divergence`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`divergence` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The divergence to set. Most projectiles have a default divergence of 1.

### Examples

```json
{
    "type": "voile:modify_divergence",
    "divergence": 10
}
```

This example sets the divergence of all the entity's projectiles to 10.

```json
{
    "type": "voile:modify_divergence",
    "divergence": 5,
    "condition": {
        "type": "apoli:equipped_item",
        "equipment_slot": "mainhand",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:bow"
            }
        }
    }
}
```

This example sets the divergence of the entity's projectiles to 5 if the entity is holding a bow in their main hand.