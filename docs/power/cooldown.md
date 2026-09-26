#   Cooldown

Provides a timer to be used for powers that normally do not have a built-in cooldown, or just as a simple timer.


Type ID: `neo-apoli:cooldown`


!!! note "Context info"

    This power type provides the following context parameter:

    Parameter | Description
    ----------|------------
    `hud/value` | An integer that refers to the cooldown's remaining ticks.
    `hud/max_value` | An integer specified in the `cooldown` field.
    `hud/min_value` | `0`


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`hud_element` | [HUD Element][hud_element] | | The HUD element to display while the cooldown is in progress.
`cooldown` | [Int Provider][int_provider] | | Determines the amount of ticks the cooldown will be in progress before it can be triggered again.


### Example

```json
{
	"type": "neo-apoli:cooldown",
	"hud_element": {
		"type": "neo-apoli:overlay/texture",
		"sprite": {
			"atlas": "minecraft:textures/atlas/blocks.png",
			"id": "minecraft:block/water_still"
		},
		"color": {
			"type": "neo-apoli:biome/water",
			"position": {
				"type": "neo-apoli:entity/position",
				"entity": "this"
			},
			"alpha": {
				"type": "neo-apoli:clamped",
				"value": {
					"type": "neo-apoli:quotient",
					"dividend": {
						"type": "neo-apoli:from_int",
						"value": "hud/value"
					},
					"divisor": {
						"type": "neo-apoli:from_int",
						"value": "hud/max_value"
					}
				},
				"min": 0.0,
				"max": 0.75
			}
		}
	},
	"cooldown": 400
}
```

This example provides a cooldown that displays a biome color-dependent water overlay that gradually disappears based from the cooldown's remaining ticks.


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
