#   Modify Attribute

Modifies the specified attribute with modifiers.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`attribute` | [Identifier]({{ mc.identifier }}) | | The identifier of the attribute to modify.
`modifiers` | Array of [Modifiers][modifier] | | The modifiers to apply to the specified attribute.


### Example

```json
{
    "type": "neo-apoli:modify/attribute",
    "attribute": "minecraft:burning_time",
    "modifiers": [
        {
            "type": "neo-apoli:add",
            "phase": "base",
            "amount": {
                "type": "neo-apoli:product",
                "values": [
                    {
                        "type": "neo-apoli:quotient",
                        "dividend": {
                           "type": "neo-apoli:entity/attribute",
                           "attribute": "minecraft:max_health",
                            "entity": "this"
                        },
                        "divisor": 2
                    },
                    0.1
                ]
            }
        }
    ]
}
```

This example adds the total value of the entity's `minecraft:max_health` attribute (divided by `2.0` and multiplied by `0.1`) to the entity's `minecraft:burning_time` attribute, making them burn longer the more health they have.

For instance, let's say the entity has a max health of `20`, and a burning time of `1.0`. The formula would be $1.0 + ((20 / 2) * 0.1) = 2.0$.


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
