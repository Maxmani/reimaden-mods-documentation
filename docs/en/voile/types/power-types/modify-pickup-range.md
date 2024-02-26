---
title: Modify Pickup Range (Power Type)
description: Voile Documentation
---

# Modify Pickup Range

`Since v1.1.0`

Expands or shrinks the pickup range of the player that has the power.

Type ID: `voile:modify_pickup_range`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`range` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The value to expand or shrink the pickup range by. `1` is roughly double the default pickup range.

### Examples

```json
{
    "type": "voile:modify_pickup_range",
    "range": 1,
    "condition": {
        "type": "apoli:sneaking"
    }
}
```

This example will double the pickup range of the player while they are sneaking.