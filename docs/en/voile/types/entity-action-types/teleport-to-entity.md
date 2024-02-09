---
title: Teleport To Entity (Entity Action Type)
description: Voile Documentation
---

# Teleport To Entity

Teleports the entity to a random entity on the server and executes a [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) upon teleporting.

Type ID: `voile:teleport_to_entity`

!!! note
    
    In the context of this entity action type, the '**actor**' is the entity that invoked the action and the '**target**' is the entity that the actor is teleporting to.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, this bi-entity action type will be executed on either or both the '**actor**' or '**target**'.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, only teleports to an entity if this bi-entity condition is fulfilled by both or either the '**actor**' or '**target**'.
`fail_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | If specified, this entity action type will be executed if there are no valid entities to teleport to.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, this sound event is played by the '**actor**' upon teleporting.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The volume of the sound event.
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The pitch of the sound event.

### Examples

```json
"entity_action": {
    "type": "voile:teleport_to_entity",
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:player"
        }
    },
    "fail_action": {
        "type": "apoli:play_sound",
        "sound": "minecraft:block.note_block.bass",
        "pitch": 0.5
    },
    "sound": "minecraft:entity.enderman.teleport"
}
```

This example will attempt to teleport the entity to a random player on the server. If there are no players to teleport to, the entity will play a bass note block sound at a pitch of 0.5. Upon teleporting, the entity will play the enderman teleport sound.