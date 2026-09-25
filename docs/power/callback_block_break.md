#   Callback Block Break

Invokes an action upon the player breaking a block.

Type ID: `neo-apoli:callback/block/break`


!!! note "Context info"
    
    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:broken_block` | The block broken by the player.
    `neo-apoli:broken_side` | The side at which the player broke the block.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`on_break_action` | [Action][action] | | The action to invoke when a block is broken.
`only_when_harvested` | [Boolean Provider][boolean_provider] | `false` | Determines whether the action should only be invoked when the block is broken with its correct tool.
`priority` | Integer | `0` | Determines the order of which powers of this type will be iterated.


??? question "About priorities"

    The instances of this type will be sorted in its **reversed** *natural order* meaning that instances that have a higher priority value will be executed first before those that have lower priority values.


### Example

```json
{
    "type": "neo-apoli:callback/block/break",
    "on_break_action": {
        "type": "neo-apoli:set_entity_on_fire",
        "ticks": 20,
        "entity": "this"
    },
    "active_condition": {
        "type": "neo-apoli:is_block_of_type",
        "block_type": "minecraft:magma_block",
        "block": "broken_block"
	}
 }
```

This example sets the entity on fire if the block they broke was a Magma block.


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
