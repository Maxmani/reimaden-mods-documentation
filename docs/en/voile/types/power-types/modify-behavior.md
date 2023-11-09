---
title: Modify Behavior (Power Type)
description: Voile Documentation
---

# Modify Behavior

Allows changing the behavior (passive, neutral, hostile) of mobs towards the power holder.  
Note that most passive mobs cannot be made hostile, as they lack the ability to attack.

Type ID: `voile:modify_behavior`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`behavior` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The desired behavior of the entity. Has to be either `passive`, `neutral`, or `hostile`.
`entity_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If specified, the behavior will only be applied to entities that fulfill this condition.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, the behavior will only be applied if this condition is fulfilled by either or both 'actor' and 'target' entities.

### Examples

```json
{
    "type": "voile:modify_behavior",
    "behavior": "passive",
    "entity_condition": {
        "type": "apoli:entity_group",
        "group": "undead"
    }
}
```

This example makes all undead mobs passive towards the player.

```json
{
    "type": "voile:modify_behavior",
    "behavior": "hostile",
    "entity_condition": {
        "type": "apoli:entity_type",
        "entity_type": "minecraft:cat"
    }
}
```

This example makes (untamed) cats hostile towards the player.