#   Modify Effect Duration

Modifies whether to allow the entity holding the power to glide.


Type ID: `neo-apoli:modify/elytra/flight`


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`allow` | [Boolean Provider][boolean_provider] | | Determines whether it should allow the entity to glide.
`priority` | [Integer][integer] | `0` | Determines how instances of this type will be prioritized.


??? question "About priorities"

    The instances of this type will be sorted in its **reversed** *natural order* meaning that instance that has the highest priority value will be chosen.


### Example

```json
{
    "type": "neo-apoli:modify/elytra/flight",
    "allow": {
        "type": "neo-apoli:entity_has_item_equipped",
        "equipped_condition": {
            "type": "neo-apoli:item_matches_ingredient",
            "ingredient": "#example:leather_caps",
            "item": "equipped_item"
        },
        "slot": "head",
        "entity": "this"
    }
}
```

This example allows the entity holding the power to glide only when they have an item included in the `#example:leather_caps` (`data/example/tags/item/leather_caps.json`) equipped to their head slot.


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
