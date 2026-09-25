#   Modify Block Use

Modifies the interaction of a block.


!!! note "Context info"

    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:used_block` | The block which the player interacted with.
    `neo-apoli:used_side` | The side of the block the player interacted with.
    `neo-apoli:used_item_slot` | The item slot used for interacting with the player.
    `neo-apoli:used_item` | The item stack used for interacting with the player.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`action` | [Action][action] | *optional* | If specified, this action will be executed when the player interacts with a block.
`result` | [Interaction Result][interaction_result] | `"success"` | Determines the result of the player's interaction with a block.
`directions` | Array of [Directions][direction] | `["down", "up", "north", "south", "west", "east"]` | Determines whether to trigger instances of this type when the player interacts with the specified sides of a block.
`hands` | Array of [Hands][hand] | `["main_hand", "off_hand"]` | Determines whether to trigger instances of this type when the player interacts with a block with the specified hands.
`use_phases` | Array of [Block Use Phases][block_use_phase] | `["block", "block_with_item"]` | Determines whether to trigger instances of this type when the player's interaction with a block enters the specified phases.
`priority` | Integer | `0` | Determines the order of which instances of this type is checked and executed.


??? question "About priorities"

    The instances of this type will be sorted in its **reversed** *natural order* meaning that instances that have a higher priority value will be checked and executed first before those that have lower priority values. 
    
    This instance also has specific rules with specific values of priorities:
    
    - If the priority value is equal or greater than 1, the instance will be executed and override the result of the interaction.
    - If the priority value is equal or less than -1, the instance will only be executed if the previous interaction result is a pass.
    - If the priority value is equal to 0, the instance will be executed and will **not** override the end result.


### Example

```json
{
    "type": "neo-apoli:modify/block/use",
    "action": {
        "type": "neo-apoli:execute_command",
        "source": {
            "type": "neo-apoli:entity",
            "entity": "this"
        },
        "command": "tellraw @s {\"text\": \"You cannot open chests made of copper!\", \"color\": \"red\"}"
    },
    "result": "fail",
    "priority": 1,
    "active_condition": {
        "type": "neo-apoli:is_block_in_tag",
        "tag": "#minecraft:copper_chests",
        "block": "used_block"
    }
}
```

This example prevents the player from opening a copper chest (or any blocks included in the `#minecraft:copper_chests` tag).


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
