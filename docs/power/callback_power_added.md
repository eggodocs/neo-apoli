#   Callback Power Added

Invokes an action upon "adding" the power (1) to the entity.
{ .annotate }

1. "Adding"/"added" in this context means that the power is granted for the first time, or granted with a different source.


Type ID: `neo-apoli:callback/power/added`


### Format

Field | Type | Default | Description 
------|------|:-------:|-------------
`action` | [Action][action] | | The action to invoke after the power is "added" to the entity.


### Example

```json
{
	"type": "neo-apoli:callback/power/added",
	"action": {
		"type": "neo-apoli:execute_command",
		"source": {
			"type": "neo-apoli:entity",
			"entity": "this"
		},
		"command": "scoreboard players add @s somethingCoolAndFun 1"
	}
}
```

This example increments the entity's score by 1 on the `somethingCoolAndFun` scoreboard objective upon adding the power to the entity.


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
