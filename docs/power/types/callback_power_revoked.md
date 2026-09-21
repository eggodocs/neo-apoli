#   Callback Power Revoked

Invokes an action upon revoking the power for the last time from the entity.


Type ID: `neo-apoli:callback/power/revoked`


### Format

Field   | Type  | Default   | Description 
--------|-------|:---------:|-------------
`action` | Action    |       | The action to invoke after the power is revoked from the entity.


### Example

```json
{
    "type": "neo-apoli:callback/power/granted",
    "action": {
        "type": "neo-apoli:execute_command",
        "source": {
            "type": "neo-apoli:entity",
            "entity": "this"
        },
        "command": "tag @s remove init"
    }
}
```

This example removes the `init` tag from the entity upon the power being revoked.


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
