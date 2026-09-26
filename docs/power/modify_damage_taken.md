#   Modify Damage Taken

Modifies the damage taken by the entity holding the power from another entity.


Type ID: `neo-apoli:modify/damage/taken`


!!! note "Context info"

    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:actor_entity` | The attacker entity.
    `neo-apoli:target_entity` | The entity that was attacked (the entity holding the power.)
    `neo-apoli:taken_damage/source` | The damage source dealt to the attacked entity.
    `neo-apoli:taken_damage/amount` | The amount of damage dealt to the attacked entity.
    `neo-apoli:damaging_entity` | The projectile used for the attack (or the attacker if no projectiles are used.)
    `neo-apoli:direct_damaging_entity` | The owner of the projectile used for the attack (or the attacker if no projectiles are used.)


### Format

Field | Type | Default | Description
------|------|---------|------------
`modifiers` | [Array][array] of [Modifiers][modifier] | | The modifiers to apply to the damage taken by the entity holding the power.
`on_modify_action` | [Action][action] | *optional* | If specified, this action will be executed when the taken damage is modified.


### Example

```json
{
    "type": "neo-apoli:modify/damage/dealt",
    "modifiers": [
        {
            "type": "neo-apoli:multiply_multiplicative",
            "phase": "total",
            "amount": 1.0
        }
    ],
    "active_condition": {
        "type": "neo-apoli:is_entity_in_tag",
        "tag": "#minecraft:skeletons",
        "entity": "actor"
    }
}
```

This example essentially doubles the damage taken by the entity holding the power if the attacker is in the `#minecraft:skeletons` entity type tag.


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
