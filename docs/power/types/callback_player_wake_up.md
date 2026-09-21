#   Callback Player Wake Up

Invokes an action upon the player waking up.

Type ID: `neo-apoli:callback/player/wake_up`


### Format

Field   | Type  | Default   | Description 
--------|-------|:---------:|-------------
`action` | Action    |       | The action to invoke after the player wakes up.


### Example

```json
{
	"type": "neo-apoli:callback/player/wake_up",
	"action": [
		{
			"type": "neo-apoli:give_items",
			"stacks": [
				{
					"id": "minecraft:egg"
				}
			],
			"entity": "this"
		},
		{
			"type": "neo-apoli:execute_command",
			"source": {
				"type": "neo-apoli:entity",
				"entity": "this"
			},
			"command": "/playsound minecraft:entity.chicken.egg"
		}
	]
}
```

This example gives the player an Egg and plays the `minecraft:entity.chicken.egg` sound event after the player wakes up.


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
