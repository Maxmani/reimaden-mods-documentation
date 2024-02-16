---
title: Disguise (Bi-entity Action Type)
description: Voile Documentation
---

# Disguise

`Since v1.0.0`

Disguises the actor entity as the target entity (including in chat messages and the player list).

Type ID: `voile:disguise`

!!! note

    This bi-entity action type will only work on players.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`overwrite` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | When false, the actor entity is not disguised as the target entity if the actor entity is already disguised as another entity.

### Examples

```json
"bientity_action": {
    "type": "voile:disguise",
    "overwrite": false
}
```

This example will disguise the actor entity as the target entity, but only if the actor entity is not already disguised as another entity.