---
title: Modify Scale (Power Type)
description: Voile Documentation
---

# Modify Scale

`Since v1.0.0`

Allows changing the size and scale of an entity.

Type ID: `voile:modify_scale`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`scale_types` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | `["pehkui:width", "pehkui:height", "pehkui:drops", "pehkui:visibility"]` | The scale types to modify. You can find a list of all scale types on [Pehkui](https://modrinth.com/mod/pehkui)'s mod page.
`scale` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The scale to set.

### Examples

```json
{
    "type": "voile:modify_scale",
    "scale": 0.5
}
```

This example halves the size of the entity, including its drops and visibility.

```json
{
    "type": "voile:modify_scale",
    "scale_types": [
        "pehkui:width",
        "pehkui:height"
    ],
    "scale": 1.25
}
```

This example increases only the width and height of the entity by 25%.

```json
{
    "type": "voile:modify_scale",
    "scale_types": [
        "pehkui:entity_reach"
    ],
    "scale": 2
}
```

This example doubles the entity reach of the entity.