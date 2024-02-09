---
title: Check Set (Entity Condition Type)
description: Voile Documentation
---

# Check Set

Checks if the entities stored in a power that uses the [Entity Set (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/entity_set/) fulfill the specified [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/).

Type ID: `voile:check_set`

!!! note

    In the context of this entity condition type, the '**actor**' is the entity that invoked the condition and the '**target**' will be the entities stored in the power.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`set` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The ID of the power.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | | The bi-entity condition that the entities stored within the power must fulfill.
`limit` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `0` | Determines the max amount of times the entity condition type should iterate and check the entities stored within the power. If the value is less than or equal to `0`, then there will be no limit.
`reverse` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether to reverse the order of the entities within the power when processing.

### Examples

```json
"condition": {
    "type": "voile:check_set",
    "set": "example:allies",
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
              "type": "apoli:exists"
        }
    }
}
```

This example will check if the entities stored in the `example:allies` `(data/example/powers/allies.json)` power exist. Useful for checking if players stored in a set are online.