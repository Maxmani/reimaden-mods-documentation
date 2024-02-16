---
title: Apply Random Effect (Entity Action Type)
description: Voile Documentation
---

# Apply Random Effect

`Since v1.0.0`

Adds a random status effect to the living entity. Does not have an effect on non-living entities.

Type ID: `voile:apply_random_effect`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`category` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | If specified, only status effects of this category can be applied. Can be `beneficial`, `harmful`, or `neutral`.
`duration` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `100` | Determines the duration of the status effect (in ticks).
`amplifier` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `0` | Determines the strength of the status effect (0 being level 1).
`is_ambient` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether the particle effects of the status effect are less noticeable.
`show_particles` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Determines whether the status effect should display particle effects on the entity.
`show_icon` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Determines whether the status effect should display an icon on the HUD.
`filtered_effects` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, these status effects will be excluded from the random selection.

### Examples

```json
"entity_action": {
    "type": "voile:apply_random_effect",
    "category": "harmful",
    "filtered_effects": [
        "minecraft:instant_damage"
    ]
}
```

This example will apply a random level 1 negative status effect to the entity that would last for 5 seconds, excluding Instant Damage.

```json
"entity_action": {
    "type": "voile:apply_random_effect",
    "duration": 200,
    "amplifier": 1,
    "filtered_effects": [
        "minecraft:instant_health",
        "minecraft:regeneration",
        "minecraft:strength",
        "minecraft:absorption"
    ]
}
```

This example will apply a random level 2 status effect to the entity that would last for 10 seconds, excluding Instant Health, Regeneration, Strength, and Absorption.