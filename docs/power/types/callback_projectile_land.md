#   Callback Projectile Land

Invokes an action when a projectile hits a block or an entity.

Type ID: `neo-apoli:callback/projectile/land`


!!! note "Context info"
    
    This power type provides the following context parameters:

    Parameter | Description
    ----------|------------
    `neo-apoli:landed_on_block` | The block the projectile hit. **This parameter is optional.**
    `neo-apoli:landed_on_side` | The side of the entity or block the projectile hit.
    `neo-apoli:projectile_entity` | The projectile.
    `neo-apoli:actor_entity` | The owner of the projectile. **This parameter is optional.**
    `neo-apoli:target_entity` | The entity that was hit by the projectile. **This parameter is optional.**


### Format

Field | Type | Default | Description 
------|------|:-------:|-------------
`action` | [Action](../../action/index.md) | | The action to invoke when the entity's projectile hits a block or an entity.


### Example

```json
{
	"type": "neo-apoli:callback/projectile/land",
	"action": {
		"type": "neo-apoli:place_block",
		"block": "minecraft:slime_block",
		"position": {
			"type": "neo-apoli:entity/position",
			"entity": "projectile"
		},
		"offset_direction": {
			"type": "neo-apoli:context",
			"parameter": "landed_on_side"
		}
	}
}
```

This example will place a Slime block at the position of the projectile or at the side of the block/entity when a projectile hits a block/entity.


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
