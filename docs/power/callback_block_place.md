#   Callback Block Place

Invokes an action upon the player placing a block.


Type ID: `neo-apoli:callback/block/place`


!!! note "Context info"
    
    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:placed_on_block` | The block the player placed a block on.
    `neo-apoli:placed_to_block` | The block the player placed.
    `neo-apoli:placed_side` | The side of the block the player placed on.


### Format

Field | Type | Default | Description 
------|------|:-------:|-------------
`on_place_action` | [Action][action] | | The action to invoke when a block is placed.
`directions` | [Array][array] of [Directions][direction] | `["down", "up", "north", "south", "west", "east"]` | Determines if the action is invoked when the block is placed at the specified sides.
`hands` | [Array][array] of [Hands][hand] | `["main_hand", "off_hand"]` | Determines if the action should be invoked when the block is held and placed with the specified hands.
`priority` | [Integer][integer] | `0` | Determines the order of which powers of this type will be iterated.


??? question "About priorities"
    
    The instances of this type will be sorted in its **reversed** *natural order* meaning that instances that have a higher priority value will be executed first before those that have lower priority values.


### Example

```json
{
	"type": "neo-apoli:callback/block/place",
	"on_place_action": [
		{
			"type": "neo-apoli:bone_meal",
			"position": {
				"type": "neo-apoli:block/position",
				"block": "neo-apoli:placed_to_block"
			}
		},
		{
			"type": "neo-apoli:apply_effects",
			"effects": [
				{
					"id": "minecraft:regeneration",
					"amplifier": 1,
					"duration": 80
				}
			]
		}
	],
	"active_condition": {
		"type": "neo-apoli:is_block_in_tag",
		"block_tag": "#minecraft:flowers",
		"block": "placed_to_block"
	}
}
```

This example applies a bone meal effect to where the block was placed and gives the player the Regeneration II (00:04) effect upon placing any kind of flowers (or any block included in the `#minecraft:flowers` block tag.)


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
