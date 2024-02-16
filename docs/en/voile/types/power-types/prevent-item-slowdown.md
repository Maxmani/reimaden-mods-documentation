---
title: Prevent Item Slowdown (Power Type)
description: Voile Documentation
---

# Prevent Item Slowdown

`Since v1.0.0`

Prevents the player from being slowed down when using items.

Type ID: `voile:prevent_item_slowdown`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`item_condition` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types/) | *optional* | If specified, only items that fulfill this condition will be prevented from slowing down the player.
`can_start_sprinting` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Whether the player can start sprinting whilst using the specified items.

### Examples

```json
{
    "type": "voile:prevent_item_slowdown",
    "item_condition": {
        "type": "apoli:food"
    }
}
```

This example will prevent the player from being slowed down when eating food.

```json
{
    "type": "voile:prevent_item_slowdown",
    "can_start_sprinting": false
}
```

This example will prevent the player from being slowed down when using any item. The player will not be able to start sprinting while using items, as usual.