#   Power

Powers give a certain "ability" to the entity it's granted to. The functionality of the "ability" will depend on the specified type.

Custom powers can be defined as JSON/JSON5/JSONC files in the `data/<namespace>/neo-apoli/power` directory of a data pack.

Data packs that load later with a power file with the same name and directory will replace the existing power.

???+ note annotate "Powers providing context"

    Power types provide the context used by other context-based data objects, such as actions and conditions, for flexibility.(1)

    Some power types may provide more context parameters, so make sure to check the corresponding pages for your desired power type.


1. The `neo-apoli:this_entity` context parameter is also automatically provided, which refers to the entity holding the power.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired power type.
`name` | [Text Component](https://minecraft.wiki/w/Text_component_format) | *optional* | The display name of the power, prioritizing translations from resource packs. <br><br>If unspecified, a translatable name with the key `power.<namespace>.<path>.name` is provided.
`description` | [Text Component](https://minecraft.wiki/w/Text_component_format) | *optional* | The display description of the power, prioritizing translations from resource packs. <br><br>If unspecified, a translatable name with the key `power.<namespace>.<path>.description` is provided.
`hidden` | Boolean | `false` | Determines whether the power should be hidden.
    

???+ question "Powers and its `active_condition`"
    A power, **unless stated otherwise** by its type, supports an optional `active_condition` field which determines whether the power is considered active. If the field is absent, the power will be considered as always active.


### List of power types

- [`callback/block/break`](types/callback_block_break.md)
- [`callback/block/place`](types/callback_block_place.md)
- [`callback/damage/dealt`](types/callback_damage_dealt.md)
- [`callback/player/respawned`](types/callback_player_respawned.md)
- [`callback/player/wake_up`](types/callback_player_wake_up.md)
- [`callback/power/added`](types/callback_power_added.md)
- [`callback/power/granted`](types/callback_power_granted.md)
- [`callback/power/removed`](types/callback_power_removed.md)
- [`callback/power/revoked`](types/callback_power_revoked.md)
- [`callback/power/tick`](types/callback_power_tick.md)
- [`callback/projectile/land`](types/callback_projectile_land.md)
- [`cooldown`](types/cooldown.md)
- `crafting_recipe`
- `dummy`
- `hud_render`
- `inventory`
- `modify/air/speed`
- `modify/attribute/vanilla`
- `modify/attribute`
- `modify/block/harvestable`
- `modify/block/selectable`
- `modify/block/use`
- `modify/climbing`
- `modify/damage/dealt`
- `modify/damage/invulnerability`
- `modify/damage/taken`
- `modify/effect/duration`
- `modify/effect/immunity`
- `modify/elytra/flight`
- `modify/elytra/render`
- `modify/entity/type_tag`
- `modify/exhaustion`
- `modify/falling`
- `modify/glowing/other`
- `modify/glowing/self`
- `modify/invisibility`
- `modify/item/use`
- `modify/item/wearable`
- `modify/model/color/other`
- `modify/model/color/self`
- `modify/model/shaking`
- `modify/player/spawn`
- `modify/recipe/crafting`
- `multiple`
- `nbt`
- `replace_loot_table`
- `toggle`