---
title: Water Breathing (Power Type)
description: Voile Documentation
---

# Water Breathing

`Since v1.0.0`

Allows the entity that has the power to breathe underwater.

Type ID: `voile:water_breathing`

### Fields

*None.*

### Examples

```json
{
    "type": "voile:water_breathing",
    "condition": {
        "type": "apoli:daytime",
        "inverted": true
    }
}
```

This example allows the entity that has the power to breathe underwater, but only at night.