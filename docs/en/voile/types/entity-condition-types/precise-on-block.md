---
title: Precise On Block (Entity Condition Type)
description: Voile Documentation
---

# Precise On Block

`Since v1.0.0`

Checks if a block underneath the entity's feet fulfills the specified [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types/).  
Unlike [On Block](https://origins.readthedocs.io/en/latest/types/entity_condition_types/on_block/), this only checks what's immediately under the entity, meaning you can, for example, still stand on a slab above the block you're checking for.

Type ID: `voile:precise_on_block`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_condition` | [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | If specified, the condition will evaluate to true if the block underneath the entity's feet fulfills the specified block condition type. Otherwise, only check if the entity is on the ground.

### Examples

```json
"condition": {
    "type": "voile:precise_on_block"
}
```

This example will check if the entity is currently on the ground.

```json
"condition": {
    "type": "voile:precise_on_block",
    "block_condition": {
        "type": "apoli:in_tag",
        "tag": "minecraft:soul_speed_blocks"
    }
}
```

This example will check if the entity is currently on a Soul Sand or Soul Soil block.