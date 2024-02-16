---
title: Prevent Taming (Power Type)
description: Voile Documentation
---

# Prevent Taming

`Since v1.0.0`

Prevents the player that has the power from taming animals and executes a [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) upon being prevented.

Type ID: `voile:prevent_taming`

!!! note
    
    In the context of this power type, the '**actor**' entity is the entity that has the power whilst the '**target**' entity is the entity that the '**actor**' attempted to tame.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, the specified actions will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.

### Examples

```json
{
    "type": "voile:prevent_taming",
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:cat"
        }
    },
    "bientity_action": {
        "type": "apoli:actor_action",
        "action": {
            "type": "apoli:execute_command",
            "command": "title @s actionbar \"Taming failed!\""
        }
    }
}
```

This example will prevent the player that has the power from taming cats and executes an [Execute Command (Entity Action Type)](https://origins.readthedocs.io/en/latest/types/entity_action_types/execute_command/) to the entity that has attempted to tame a cat.