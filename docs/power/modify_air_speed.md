#   Modify Air Speed

Modifies the entity's air horizontal speed.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`modifiers` | Array of [Modifiers][modifier] | | The modifiers to apply to the entity's air horizontal speed.


### Example

```json
{
    "type": "neo-apoli:modify/air/speed",
    "modifiers": [
        {
            "type": "neo-apoli:multiply_multiplicative",
            "phase": "base",
            "amount": 0.5
        }
    ]
}
```

This example modifies the entity's air speed by 150%.


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
