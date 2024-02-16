---
title: Moon Phase (Entity Condition Type)
description: Voile Documentation
---

# Moon Phase

`Since v1.0.0`

Check the moon phase of the entity's current dimension. Will always be false if the player is in a dimension without a moon.  

Type ID: `voile:moon_phase`

!!! note

    This entity condition type can still return true during day time.

### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | | How the current moon phase should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The moon phase to compare against. Has to be between 0 and 7, inclusive. See [here](https://minecraft.wiki/w/Moon#Phases) for a list of moon phases.

### Examples

```json
"condition": {
    "type": "voile:moon_phase",
    "comparison": "!=",
    "compare_to": 0
}
```

This example will check if the entity's current dimension has a moon and it is not a full moon.