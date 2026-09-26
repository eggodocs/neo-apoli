#   Callback Damage Dealt

Invokes an action upon the player placing a block.


Type ID: `neo-apoli:callback/block/place`


!!! note "Context info"
    
    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:dealt_damage_source` | The damage source dealt by the entity holding the power.
    `neo-apoli:dealt_damage_amount` | The damage amount dealt by the entity holding the power.
    `neo-apoli:actor_entity` | The attacker entity (the entity holding the power.)
    `neo-apoli:target_entity` | The entity that was attacked.
    `neo-apoli:damaging_entity` | The projectile used for the attack (or the attacker if no projectiles are used.)
    `neo-apoli:direct_damaging_entity` | The owner of the projectile used for the attack (or the attacker if no projectiles are used.)


### Format

Field | Type | Default | Description 
------|------|:-------:|------------
`on_hit_action` | [Action][action] | | The action to invoke when damage is dealt to an entity.
`priority` | [Integer][integer] | `0` | Determines the order of which powers of this type will be iterated.


??? question "About priorities"
    
    The instances of this type will be sorted in its **reversed** *natural order* meaning that instances that have a higher priority value will be executed first before those that have lower priority values.


### Example

```json
{
	"type": "neo-apoli:callback/damage/dealt",
	"on_hit_action": {
		"type": "neo-apoli:execute_command",
		"source": {
			"type": "neo-apoli:entity",
			"entity": "this"
		},
		"command": {
			"type": "neo-apoli:join",
			"strings": [
				"tp @s",
				{
					"type": "neo-apoli:entity/uuid",
					"entity": "target"
				}
			],
			"separator": " "
		}
	}
}
```

This example teleports the entity that was attacked to the entity holding the power.


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
