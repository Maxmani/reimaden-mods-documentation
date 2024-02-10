---
title: Nearby Entities (Entity Condition Type)
description: Voile Documentation
---

# Nearby Entities

Checks if there are any entities nearby.

Type ID: `voile:nearby_entities`

!!! note

    In the context of this entity condition type, the '**actor**' is the entity that invoked the condition and the '**target**' will be the nearby entities.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, only counts entities if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The maximum distance between the '**actor**' and the nearby entities.
`count` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The minimum amount of entities that must be nearby to fulfill the condition.

### Examples

```json
"condition": {
    "type": "voile:nearby_entities",
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:boat"
        }
    },
    "distance": 16
}
```

This example will check if there is at least one boat within 16 blocks of the actor entity.

```json
"condition": {
    "type": "voile:nearby_entities",
    "distance": 32,
    "count": 2
}
```

This example will check if there are at least two entities within 32 blocks of the actor entity, including items, mobs, players, etc.