---
title: Action On Block (Power Type)
description: Voile Documentation
---

# Action On Block

Executes an action when the entity that has the power blocks an attack with a shield.

Type ID: `voile:action_on_block`

!!! note
    
    In the context of this power type, the '**actor**' entity is the entity that has the power whilst the '**target**' entity is the entity that hit the shield.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | The action to be executed on either or both the '**actor**' or '**target**' entities.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, the specified action will only be executed if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`damage_condition` | [Damage Condition Type](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, the specified action will only be executed if this condition is fulfilled by the attempted damage dealt by the '**target**' entity.
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render/) | `{"should_render": false}` | Determines how the cooldown of this power is visualized on the HUD.

### Examples

```json
{
    "type": "voile:action_on_block",
    "bientity_action": {
        "type": "apoli:target_action",
        "action": {
            "type": "apoli:set_on_fire",
            "duration": 5
        }
    }
}
```

This example will set the entity that hit the shield of the entity that has the power on fire for 5 seconds.

```json
{
    "type": "voile:action_on_block",
    "bientity_action": {
        "type": "apoli:damage",
        "amount": 10,
        "damage_type": "minecraft:on_fire"
    },
    "cooldown": 20
}
```

This example will deal 10 fire damage to the entity that hit the shield of the entity that has the power. The power will then have a cooldown of 20 ticks before it can be triggered again.