#   Modify Attribute Vanilla

Modifies the specified attributes with vanilla modifiers.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`modifiers` | [Array][array] of [Attributed Modifiers][attributed_modifier] | | The vanilla modifiers with attributes to modify.


### Example

```json
{
    "type": "neo-apoli:modify/attribute/vanilla",
    "modifiers": [
        {
            "id": "example:extra_armor",
            "attribute": "minecraft:armor",
            "operation": "add_value",
            "amount": 4
        }
    ]
}
```

This example adds 4 armor points to the entity.


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
