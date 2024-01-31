---
title: Nearby Entities (Entity Condition Type)
description: Voile Documentation
---

# Nearby Entities

Checks if there are any entities nearby.

Type ID: `voile:nearby_entities`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If specified, only entities that fulfill this condition will be counted.
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The maximum distance between the entity that has the power and the nearby entities.
`count` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The minimum amount of entities that must be nearby to fulfill the condition.

### Examples

```json
"condition": {
    "type": "voile:nearby_entities",
    "entity_condition": {
        "type": "apoli:entity_type",
        "entity_type": "minecraft:boat"
    },
    "distance": 16
}
```

This example will check if there is at least one boat within 16 blocks of the entity.

```json
"condition": {
    "type": "voile:nearby_entities",
    "distance": 32,
    "count": 2
}
```

This example will check if there are at least two entities within 32 blocks of the entity, including items, mobs, players, etc.