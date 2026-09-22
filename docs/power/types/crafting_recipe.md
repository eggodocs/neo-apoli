#   Crafting Recipe

Provides a crafting recipe that can only be crafted by the player holding the power.


### Format

Field | Type | Default | Description
------|------|---------|------------
`recipe` | Crafting Recipe Entry | | The crafting recipe to provide.
`priority` | Integer | `0` | Determines the order of which recipes of this type will be prioritized.


??? question "About priorities"

    The recipes of this type will prioritize powers that have a higher priority value over powers that have a lower priority value. This means that the power that has the highest priority value will have its recipe provided.


### Example

```json
{
	"type": "neo-apoli:crafting_recipe",
	"recipe": {
		"id": "example:epic_cookie",
		"type": "minecraft:crafting_shapeless",
		"ingredients": [
			"minecraft:cookie",
			"minecraft:diamond"
		],
		"result": {
			"id": "minecraft:golden_apple"
		}
	}
}
```

This example provides a shapeless crafting recipe where a Golden Apple can be crafted by placing a cookie and a diamond in the crafting grid.


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
