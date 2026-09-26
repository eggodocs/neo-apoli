#   Modify Damage Dealt

Modifies the damage dealt by the entity holding the power to another entity.


Type ID: `neo-apoli:modify/damage/dealt`


### Format

Field | Type | Default | Description
------|------|---------|------------
`modifiers` | [Array][array] of [Modifiers][modifier] | | The modifiers to apply to the damage dealt by the entity holding the power.
`on_modify_action` | [Action][action] | *optional* | If specified, this action will be executed when the dealt damage is modified.


### Example

```json
{
    "type": "neo-apoli:modify/damage/dealt",
    "modifiers": [
        {
            "type": "neo-apoli:multiply_multiplicative",
            "phase": "total",
            "amount": -0.5
        }
    ]
}
```

This example essentially halves the damage dealt by the entity holding the power.


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
