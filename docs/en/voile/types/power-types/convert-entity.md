---
title: Convert Entity (Power Type)
description: Voile Documentation
---

# Convert Entity

Allows the power holder to convert entities into other entities, similarly to how zombies can convert villagers into zombie villagers.

Type ID: `voile:convert_entity`

!!! note
    
    The entities to convert can only be mob entities.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If specified, only entities that fulfill this condition can be converted.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, entities can only be converted if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`convert_to` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the entity to convert to.
`ignore_difficulty` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Determines whether the power should follow the same rules as the zombie villager conversion mechanic, where the difficulty of the game affects the chance of the conversion succeeding.

### Examples

```json
{
    "type": "voile:convert_entity",
    "entity_condition": {
        "type": "apoli:entity_type",
        "entity_type": "minecraft:villager"
    },
    "convert_to": "minecraft:zombie_villager",
    "ignore_difficulty": false
}
```

This example allows the power holder to convert villagers into zombie villagers, with a 50% chance on normal difficulty or 100% on hard.

```json
{
    "type": "voile:convert_entity",
    "entity_condition": {
        "type": "apoli:entity_type",
        "entity_type": "minecraft:chicken"
    },
    "convert_to": "minecraft:cow"
}
```

This example allows the power holder to convert chickens into cows, with a 100% chance regardless of difficulty.