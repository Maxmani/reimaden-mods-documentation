---
title: Scoreboard (Bi-entity Condition Type)
description: Voile Documentation
---

# Scoreboard

Compares the score of the actor entity from a specified scoreboard objective to the score of the target entity from another specified scoreboard objective.

Type ID: `voile:scoreboard`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`actor_objective` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The name of the actor's scoreboard objective to retrieve the value from and compare.
`target_objective` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The name of the target's scoreboard objective to retrieve the value from and compare.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | `==` | How to compare the actor's objective value to the target's objective value.

### Examples

```json
"bientity_condition": {
    "type": "voile:scoreboard",
    "actor_objective": "deaths",
    "target_objective": "deaths"
}
```

This example will check if the score of the actor in the `deaths` scoreboard objective is equal to the score of the target in the `deaths` scoreboard objective.

```json
"bientity_condition": {
    "type": "voile:scoreboard",
    "actor_objective": "foo",
    "target_objective": "bar",
    "comparison": "<"
}
```

This example will check if the score of the actor in the `foo` scoreboard objective is less than the score of the target in the `bar` scoreboard objective.