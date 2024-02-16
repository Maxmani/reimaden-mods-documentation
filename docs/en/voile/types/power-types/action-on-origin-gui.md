---
title: Action On Origin GUI (Power Type)
description: Voile Documentation
---

# Action On Origin GUI

`Since v2.0.0 of Touhou Origins`

Executes an [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) when the player opens the origin selection screen (either by using an `Orb of Origin` or the `/origin gui` command).

Type ID: `touhouorigins:action_on_origin_gui`

!!! note
    
    This power type is provided by [Touhou Origins](https://modrinth.com/mod/touhou-origins) and uses the `touhouorigins` namespace. It is listed here for completeness' sake.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | | The action to execute on the player.

### Examples

```json
{
    "type": "touhouorigins:action_on_origin_gui",
    "entity_action": {
        "type": "apoli:apply_effect",
        "effect": {
            "effect": "minecraft:regeneration",
            "amplifier": 1
        }
    }
}
```

This example will apply Regeneration II that lasts for 5 seconds when the player opens the origin selection screen.