#   Callback Power Removed

Invokes an action upon "removing" the power (1) from the entity.
{ .annotate }

1. "Removing"/"removed" in this context means that the power is revoked for the Nth or last time.


Type ID: `neo-apoli:callback/power/removed`


### Format

Field   | Type  | Default   | Description 
--------|-------|:---------:|-------------
`action` | Action    |       | The action to invoke after the power is "removed" from the entity.


### Example

```json
{
	"type": "neo-apoli:callback/power/removed",
	"action": {
		"type": "neo-apoli:execute_command",
		"source": {
			"type": "neo-apoli:entity",
			"entity": "this"
		},
		"command": "scoreboard players remove @s somethingCoolAndFun 1"
	}
}
```

This example decrements the entity's score by 1 on the `somethingCoolAndFun` scoreboard objective upon "removing" the power from the entity.


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
