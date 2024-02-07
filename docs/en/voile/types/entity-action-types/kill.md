---
title: Kill (Entity Action Type)
description: Voile Documentation
---

# Kill

Kills the entity, similarly to the `/kill` command.

Type ID: `voile:kill`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`damage_type` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | `minecraft:generic_kill` | The damage type to be used. Controls e.g. the death message, invulnerabilities (e.g. towards fire), or whether armor is taken into account.

### Examples

```json
"entity_action": {
    "type": "voile:kill"
}
```

This example will kill the entity using the generic damage type.

```json
"entity_action": {
    "type": "voile:kill",
    "damage_type": "minecraft:on_fire"
}
```

This example will kill the entity using the `on_fire` damage type. Note that Fire Resistance will prevent the entity from dying in this case.