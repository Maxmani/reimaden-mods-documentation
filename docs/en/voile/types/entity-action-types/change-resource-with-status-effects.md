---
title: Change Resource With Status Effects (Entity Action Type)
description: Voile Documentation
---

# Change Resource With Status Effects

Changes the value of a power that either uses the [Resource](https://origins.readthedocs.io/en/latest/types/power_types/resource/) power type, or has a built-in cooldown, based on the status effects applied on the entity.

Type ID: `voile:change_resource_with_status_effects`

!!! warning
    
    This action type is very niche and may be changed in the future.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`resource` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the power that uses the [Resource (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/resource/) or has a built-in cooldown.
`category` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The category of status effects to check for. Can be `beneficial`, `harmful`, or `neutral`.
`change` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | Each status effect of the given category adds this value to the resource (won't go below `min` or above `max` of the [Resource (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/resource/)).
`operation` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"add"` | Determines if the action should add or set the value of the resource. Accepts `"add"` or `"set"`.

### Examples

```json
"entity_action": {
    "type": "voile:change_resource_with_status_effects",
    "resource": "namespace:example",
    "category": "harmful"
}
```

This example will add 1 for each harmful status effect applied on the entity to the `namespace:example` (`data/namespace/powers/example.json`) power that uses the [Resource (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/resource/).

```json
"entity_action": {
    "type": "voile:change_resource_with_status_effects",
    "resource": "namespace:example",
    "category": "beneficial",
    "change": 2,
    "operation": "set"
}
```

This example will set the value of the `namespace:example` (`data/namespace/powers/example.json`) power to 2 times the amount of beneficial status effects applied on the entity.