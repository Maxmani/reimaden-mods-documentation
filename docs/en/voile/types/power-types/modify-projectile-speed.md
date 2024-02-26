---
title: Modify Projectile Speed (Power Type)
description: Voile Documentation
---

# Modify Projectile Speed

`Since v1.1.0`

Modifies the speed of the projectiles fired by the entity that has the power.

Type ID: `voile:modify_projectile_speed`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`self_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | The action to execute on the entity.
`projectile_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | The action to execute on the projectile.
`projectile_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If specified, the specified actions/modifiers will only be executed/applied if this condition is fulfilled by the projectile.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If specified, this modifier will be applied to the projectile's speed.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If specified, these modifiers will be applied to the projectile's speed.

### Examples

```json
{
    "type": "voile:modify_projectile_speed",
    "modifier": {
        "operation": "multiply_total_multiplicative",
        "value": 0.3
    },
    "projectile_condition": {
        "type": "apoli:in_tag",
        "tag": "minecraft:arrows"
    }
}
```

This example will increase the total speed of all arrows fired by the entity that has the power by 30%.