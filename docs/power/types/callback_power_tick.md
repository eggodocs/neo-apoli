#   Callback Power Tick

Invokes an action every time the power ticks.

Type ID: `neo-apoli:callback/power/tick`


### Format

Field   | Type  | Default   | Description 
--------|-------|:---------:|-------------
`action`            | Action        | *optional*    | If specified, this action will be invoked every interval ticks.
`rising_action`     | Action        | *optional*    | If specified, this action will be invoked in the first interval tick the power was active.
`falling_action`    | Action        | *optional*    | If specified, this action will be invoked in the first interval tick the power was inactive.
`interval`          | Int Provider  | `20`          | Determines the period for which this power will tick. The provided integer is automatically clamped within the range of 0 and 2,147,483,647.


### Example

```json
{
	"type": "neo-apoli:callback/power/tick",
	"action": {
		"type": "neo-apoli:set_entity_on_fire",
		"ticks": 40,
		"entity": "this"
	},
	"interval": 100
}
```

This example sets the entity on fire for 2 seconds every 5 seconds.


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
