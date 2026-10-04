#   Modify Effect Immunity

Modifies whether the entity holding the power should be immune to the afflicted status effect or not.


Type ID: `neo-apoli:modify/effect/immunity`


!!! note "Context info"

    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:actor_entity` | The entity that inflicted the status effect.
    `neo-apoli:target_entity` | The entity holding the power.
    `neo-apoli:applied_effect` | The inflicted status effect.


### Format

*No additional fields.*


### Example

```json
{
    "type": "neo-apoli:modify/effect/immunity",
    "active_condition": {
        "type": "neo-apoli:is_effect_in_tag",
        "tag": "#example:effects_immune_to",
        "effect": "applied_effect"
    }
}
```

This example will make the entity holding the power immune to any status effect included in the `#example:effects_immune_to` (`data/example/tags/mob_effect/effects_immune_to.json`) effect tag.


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
