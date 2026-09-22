#   Callback Power Granted

Invokes an action upon granting the power to the entity.


Type ID: `neo-apoli:callback/power/granted`


### Format

Field | Type | Default | Description 
------|------|:-------:|-------------
`action` | [Action](../../action/index.md) | | The action to invoke after the power is granted to the entity.


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
        "command": "tag @s add init"
    }
}
```

This example adds an `init` tag to the entity after the power is granted. The tag will only be added once, unless the power is revoked and granted again.


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
