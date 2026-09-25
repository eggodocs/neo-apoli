#   Callback Projectile Land

Invokes an action when a projectile hits a block or an entity.

Type ID: `neo-apoli:callback/projectile/land`


!!! note "Context info"

    This power type provides the following context parameters depending on the scenario:

    === "An entity was hit"

        Parameter | Description
        ----------|------------
        `neo-apoli:projectile_entity` | The projectile entity itself.
        `neo-apoli:actor_entity` | The owner of the projectile or nothing if the projectile doesn't have an owner.
        `neo-apoli:target_entity` | The entity that was hit by the projectile.

    === "A block was hit"

        Parameter | Description
        ----------|------------
        `neo-apoli:landed_on_block` | The block that was hit by the projectile.
        `neo-apoli:landed_on_side` | The side of the block the projectile hit.
        `neo-apoli:projectile_entity` | The projectile entity itself.
        `neo-apoli:actor_entity` | The owner of the projectile or nothing if the projectile doesn't have an owner.


### Format

Field | Type | Default | Description 
------|------|:-------:|-------------
`action` | [Action][action] | | The action to invoke when the entity's projectile hits a block or an entity.


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
