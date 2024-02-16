---
title: Disguised (Bi-entity Condition Type)
description: Voile Documentation
---

# Disguised

`Since v1.0.0`

Checks if the actor entity is currently [disguised](../bientity-action-types/disguise.md) as the target entity.

Type ID: `voile:disguised`

!!! note

    This bi-entity condition type will only work on players.

### Fields

*None.*

### Examples

```json
"bientity_condition": {
    "type": "voile:disguised"
}
```

This example will check if the actor entity is currently disguised as the target entity.