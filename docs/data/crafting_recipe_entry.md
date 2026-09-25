#   Crafting Recipe Entry

An object that contains a recipe and its identifier.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`id` | [Identifier]({{ mc.identifier }}) | | The identifier of the recipe.
`type` | [Identifier]({{ mc.identifier }}) | | The identifier for the type of the desired crafting recipe.


!!! note 

    See [Recipe (JSON format)](https://minecraft.wiki/w/Recipe_(Java_Edition)#JSON_format) for more information regarding recipe types provided by vanilla. Please note that this specific data type will only accept **crafting** variants.


### Example

```json
"recipe": {
    "id": "example:epic_sword",
    "type": "minecraft:crafting_shaped",
    "pattern": [
        "I",
        "I",
        "S"
    ],
    "key": {
        "I": "minecraft:iron_block",
        "S": "minecraft:stick"
    },
    "result": {
        "id": "minecraft:iron_sword",
        "components": {
            "minecraft:attack_range": {
                "max_reach": 8.0,
                "max_creative_reach": 8.0
            },
            "minecraft:custom_name": "{\"text\": \"Epic Sword\", \"italic\": false}",
            "minecraft:rarity": "epic"
        }
    }
}
```

This example provides a shaped crafting recipe for crafting an Iron Sword that has the *"Epic Sword"* name, a rarity of epic, and an attack range with a max reach of 8.0.
