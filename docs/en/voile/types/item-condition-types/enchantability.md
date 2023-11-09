---
title: Enchantability (Item Condition Type)
description: Voile Documentation
---

# Enchantability

Checks an item's enchantability. Vanilla enchantability values can be found [here](https://minecraft.wiki/w/Enchanting_mechanics#Enchantability).  
Items without an enchantability value are considered to have 0 enchantability.

Type ID: `voile:enchantability`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | `">="` | How the item's enchantability should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The value to compare the item's enchantability against.

### Examples

```json
"item_condition": {
    "type": "voile:enchantability",
    "comparison": ">=",
    "compare_to": 15
}
```

This example checks if the item has an enchantability of 15 or higher, which, in the context of tools, would allow wood, Netherite, and gold to return true.