#   Callback Player Respawned

Invokes an action upon the player respawning.

Type ID: `neo-apoli:callback/player/respawned`


### Format

Field | Type | Default | Description 
------|------|:-------:|-------------
`action` | [Action][action] | | The action to invoke when the player respawns.


### Example

```json
{
	"type": "neo-apoli:callback/player/respawned",
	"action": {
		"type": "neo-apoli:apply_effects",
		"effects": [
			{
				"id": "minecraft:resistance",
				"duration": -1,
				"amplifier": 199
			}
		],
		"entity": "this"
	}
}
```

This example applies the Resistance CC (Infinite) effect when the player respawns.


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
