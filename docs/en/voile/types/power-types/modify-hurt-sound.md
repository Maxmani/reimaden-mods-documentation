---
title: Modify Hurt Sound (Power Type)
description: Voile Documentation
---

# Modify Hurt Sound

Modifies the sound played when the entity that has the power takes damage.

Type ID: `voile:modify_hurt_sound`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`silent` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether the hurt sound is played or not.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, this sound event is played.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, a random sound event from this array is played.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The volume of the sound event(s).
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The pitch of the sound event(s).

### Examples

```json
{
    "type": "voile:modify_hurt_sound",
    "sound": "minecraft:entity.ghast.hurt"
}
```

This example will replace the hurt sound of the entity that has the power with the `minecraft:entity.ghast.hurt` sound event.