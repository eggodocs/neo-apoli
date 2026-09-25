#   Hud Render

Renders the specified HUD elements.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`hud_elements` | Array of [HUD Elements][hud_element] | | The HUD elements to render.


!!! warning

    This power type does **not** support the `active_condition` field.


### Example

```json
{
    "type": "neo-apoli:hud_render",
    "hud_elements": [
        {
            "type": "neo-apoli:overlay/texture",
            "sprite": {
                "atlas": "minecraft:textures/atlas/blocks.png",
                "id": "minecraft:block/dirt"
            },
            "color": "#ffffff40",
            "render_phase": "below_hud",
            "hide_with_hud": false,
            "visible_in_third_person": false
        }
    ]
}
```

This example renders a dirt overlay below the HUD that won't be hidden when the HUD is hidden, but won't be visible in third person.


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
