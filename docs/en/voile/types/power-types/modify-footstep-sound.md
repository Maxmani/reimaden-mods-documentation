---
title: Modify Footstep Sound (Power Type)
description: Voile Documentation
---

# Modify Footstep Sound

`Since v1.0.0`

Modifies the sound played when the entity that has the power walks on a block.

Type ID: `voile:modify_footstep_sound`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`silent` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether footstep sounds are played or not.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, this sound event is played.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, a random sound event from this array is played.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The volume of the sound event(s).
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The pitch of the sound event(s).

### Examples

```json
{
    "type": "voile:modify_footstep_sound",
    "silent": true
}
```

This example will mute the footsteps of the entity that has the power.

```json
{
    "type": "voile:modify_footstep_sound",
    "sounds": [
        "minecraft:block.sand.step",
        "minecraft:block.gravel.step"
    ],
    "volume": 0.5,
    "pitch": 1.5
}
```

This example will replace the footstep sound of the entity that has the power with the `minecraft:block.sand.step` and `minecraft:block.gravel.step` sound events with a volume of `0.5` and a pitch of `1.5`.