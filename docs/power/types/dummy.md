#   Dummy

Does nothing. Mainly serves as a placeholder for implementations that are implemented via Java code or by other data-driven powers.


### Format

*No additional fields.*


### Example

```json
{
    "type": "neo-apoli:dummy",
    "active_condition": {
        "type": "neo-apoli:is_entity_sneaking",
        "entity": "this"
    }
}
```

This example does nothing, but will be considered as active if the entity holding the power is sneaking.


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
