#   Inventory

Provides a customizable inventory where items can be stored and may or may not persist on the player's death.


!!! note "Context info"

    When the player dies, this type checks its `drop_on_death_condition` on each item it contains and provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:item_in_container` | The item stack in the inventory being checked if it should be dropped on death or not.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`title` | [Text Component]({{ mc.text_component }}) | `{"translatable": "container.inventory"}` | The displayed title for the inventory's GUI.
`menu` | [Container Menu][container_menu] | `"neo-apoli:generic_3x3"` | The basis that will be rendered as the inventory's GUI.
`drop_on_death_condition` | [Condition][condition] | *optional* | If specified, this checks each item stack if they should be dropped when the player holding the power dies.
`recoverable` | [Boolean Provider][boolean_provider] | `true` | Determines whether the item stacks can be recovered when the power is revoked.
`key` | [Key Reference][key_reference] | | The referenced key binding to use for opening the inventory.
`priority` | Integer | `0` | Determines the priority at which power should have its inventory opened.


??? question "About priorities"

    The instances of this type will be sorted in its **reversed** *natural order* meaning that instances that have a higher priority value will be selected first before those that have lower priority values.


### Example

```json
{
    "type": "neo-apoli:inventory",
    "title": {
        "translatable": "example.pockets.title"
    },
    "menu": "hopper",
    "key": "key.hotbar.9",
    "active_condition": {
        "type": "neo-apoli:is_entity_sneaking",
        "entity": "this"
    }
}
```

This example provides an inventory with the GUI of the hopper block (consisting of 1 row and 5 columns of slots) that is opened when the player is sneaking and presses the 9th hotbar slot.


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
