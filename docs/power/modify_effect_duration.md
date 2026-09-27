#   Modify Effect Duration

Modifies the duration of a status effect inflicted on the entity holding the power.


Type ID: `neo-apoli:modify/effect/duration`


!!! note "Context info"

    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:actor_entity` | The entity that inflicted the status effect.
    `neo-apoli:target_entity` | The entity holding the power.
    `neo-apoli:applied_effect` | The inflicted status effect.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`modifiers` | [Array][array] of [Modifiers][modifier] | | The modifiers to apply to the duration of an inflicted status effect.


### Example

```json
{
    "type": "neo-apoli:modify/effect/duration",
    "modifiers": [
        {
            "type": "neo-apoli:multiply_additive",
            "phase": "total",
            "amount": 1.0
        }
    ],
    "active_condition": {
        "type": "neo-apoli:is_effect_of_type",
        "effect_type": "minecraft:poison",
        "effect": "applied_effect"
    }
}
```

This example doubles the duration of the Poison status effect.


### History

<table>
    <tr>
        <td style="text-align: center; vertical-align: middle"><b>Minecraft</b></td>
        <td style="text-align: center; vertical-align: middle"><b>Mod</b></td>
        <td style="vertical-align: middle"><b>Changelog</b></td>
    </tr>
    <tr style="text-align: center; vertical-align: middle">
        <td style="text-align: center; vertical-align: middle">1.21.5</td>
        <td style="text-align: center; vertical-align: middle">0.1.0</td>
        <td style="vertical-align: middle">Added the power type.</td>
    </tr>
</table>
