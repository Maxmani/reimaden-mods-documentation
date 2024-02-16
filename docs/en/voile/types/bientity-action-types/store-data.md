---
title: Store Data (Bi-entity Action Type)
description: Voile Documentation
---

# Store Data

`Since v1.0.0`

Stores entity data from the target entity in the actor entity's scoreboard.

Type ID: `voile:store_data`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`path` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The path to the NBT tag to store the data from. Use `.` to separate compound tags and `[n]` to index into lists.
`objective` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The name of the scoreboard objective to store the data in.

### Examples

```json
"bientity_action": {
    "type": "voile:store_data",
    "path": "UUID[0]",
    "objective": "UUID_1"
}
```

This example will store the first of the four integers of the target entity's UUID in the actor entity's `UUID_1` scoreboard objective.

```json
"bientity_action": {
    "type": "voile:store_data",
    "path": "warden_spawn_tracker.ticks_since_last_warning",
    "objective": "wardenTicks"
}
```

This example will store the `ticks_since_last_warning` NBT tag of the target entity's `warden_spawn_tracker` compound tag in the actor entity's `wardenTicks` scoreboard objective.

```json
"bientity_action": {
    "type": "voile:store_data",
    "path": "Health",
    "objective": "health"
}
```

This example will store the target entity's health in the actor entity's `health` scoreboard objective.