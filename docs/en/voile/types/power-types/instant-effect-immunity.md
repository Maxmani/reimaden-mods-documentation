---
title: Instant Effect Immunity (Power Type)
description: Voile Documentation
---

# Instant Effect Immunity

Prevents instant status effects from being applied to the entity with this power.

Type ID: `voile:instant_effect_immunity`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`effect` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, only the instant status effect with this namespace and ID cannot be applied to the entity.
`effects` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, only the instant status effects with these namespaces and IDs cannot be applied to the entity.
`inverted` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether the effects specified are used as a blacklist or a whitelist.

### Examples

```json
{
    "type": "voile:instant_effect_immunity",
    "effect": "minecraft:instant_health",
}
```

This example makes the power holder immune to [Instant Health](https://minecraft.wiki/w/Instant_Health).

```json
{
    "type": "voile:instant_effect_immunity",
    "effect": "minecraft:instant_damage",
    "inverted": true
}
```

This example makes the power holder immune to all instant status effects that are not [Instant Damage](https://minecraft.wiki/w/Instant_Damage).