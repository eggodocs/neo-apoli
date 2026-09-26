#   Modify Block Selectable

Modifies whether the player holding the power or not should be able to break or interact with the block being looked at.


!!! note "Context info"

    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:selected_block` | The block the player is looking at.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`allow` | [Boolean Provider][boolean_provider] | | Determines whether to allow the player to break or interact with the block.
`priority` | [Integer][integer] | `0` | Determines the order of which powers of this type is checked.


??? question "About priorities"

    The instances of this type will be sorted in its **reversed** *natural order* meaning that instances that have a higher priority value will be checked first before those that have lower priority values.


### Example

```json
{
    "type": "neo-apoli:modify/block/selectable",
    "allow": {
        "type": "neo-apoli:is_entity_sneaking",
        "entity": "this"
    },
    "active_condition": {
        "type": "neo-apoli:is_block_of_type",
        "block_type": "minecraft:cobweb",
        "block": "selected_block"
    }
}
```

This example will make Cobweb blocks only selectable if the player is sneaking.


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
