#   Modify Climbing

Modifies whether an entity is considered climbing.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`holding_condition` | [Condition][condition] | `{"type": "neo-apoli:is_entity_sneaking", "entity": "this"}` | Determines when an entity is considered holding onto a block.
`allow_holding` | [Boolean Provider][boolean_provider] | `true` | Determines whether "holding" onto a block is allowed.


### Example

```json
{
    "type": "neo-apoli:modify/climbing",
    "active_condition": {
        "type": "neo-apoli:compare",
        "comparison": {
            "type": "neo-apoli:int",
            "comparator": ">=",
            "first": {
                "type": "neo-apoli:blocks_intersecting_box",
                "condition": {
                    "type": "neo-apoli:is_block_of_type",
                    "block_type": "minecraft:sugar_cane",
                    "block": "block_intersecting_box"
                },
                "box": {
                    "type": "neo-apoli:entity/bounds",
                    "entity": "this"
                }
            },
            "second": 1
        }
    }
}
```

This example allows entities to climb in sugar canes.


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
