---
title: Action On Entity Death (Power Type)
description: Voile Documentation
---

# Action On Entity Death

Executes an action when an entity on the server dies.

Type ID: `voile:action_on_entity_death`

!!! note
    
    In the context of this power type, the '**actor**' entity is the entity that has the power whilst the '**target**' entity is the entity that died.

!!! warning

    The damage amount in the damage condition always evaluates to `0`.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | The action to be executed on either or both the '**actor**' and '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, the specified action will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`damage_condition` | [Damage Condition Type](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, the specified action will only be executed if this condition is fulfilled by the damage that killed the '**target**' entity.

### Examples

```json
{
    "type": "voile:action_on_entity_death",
    "bientity_action": {
        "type": "apoli:actor_action",
        "action": {
            "type": "apoli:execute_command",
            "command": "title @s actionbar \"A pig has died!\""
        }
    },
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:pig"
        }
    },
    "damage_condition": {
        "type": "apoli:in_tag",
        "tag": "minecraft:is_fall"
    }
}
```

This example will execute a command that displays a message in the action bar of the entity that has the power when a pig dies from fall damage.