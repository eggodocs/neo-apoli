#   Power { #power }

Powers give a certain "ability" to the entity it's granted to. The functionality of the "ability" will depend on the specified type.

Custom powers can be defined as JSON/JSON5/JSONC files in the `data/<namespace>/neo-apoli/power` directory of a data pack. Data packs that load later with a power file with the same name and directory will replace the existing power.

???+ note annotate "Powers providing context"

    Power types provide the context used by other context-based data objects, such as actions and conditions, for flexibility.(1) Some power types may provide more context parameters, so make sure to check the corresponding pages for your desired power type.


1. The `neo-apoli:this_entity` context parameter is also automatically provided, which refers to the entity holding the power.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired power type.
`name` | [Text Component]({{ mc.text_component }}) | *optional* | The display name of the power, prioritizing translations from resource packs. <br><br>If unspecified, a translatable name with the key `power.<namespace>.<path>.name` is provided.
`description` | [Text Component]({{ mc.text_component }}) | *optional* | The display description of the power, prioritizing translations from resource packs. <br><br>If unspecified, a translatable name with the key `power.<namespace>.<path>.description` is provided.
`hidden` | Boolean | `false` | Determines whether the power should be hidden.
    

???+ question "Powers and its `active_condition`"
    A power, **unless stated otherwise** by its type, supports an optional `active_condition` field which determines whether the power is considered active. If the field is absent, the power will be considered as always active.


### List of power types

- [`callback/block/break`](callback_block_break.md)
- [`callback/block/place`](callback_block_place.md)
- [`callback/damage/dealt`](callback_damage_dealt.md)
- [`callback/player/respawned`](callback_player_respawned.md)
- [`callback/player/wake_up`](callback_player_wake_up.md)
- [`callback/power/added`](callback_power_added.md)
- [`callback/power/granted`](callback_power_granted.md)
- [`callback/power/removed`](callback_power_removed.md)
- [`callback/power/revoked`](callback_power_revoked.md)
- [`callback/power/tick`](callback_power_tick.md)
- [`callback/projectile/land`](callback_projectile_land.md)
- [`cooldown`](cooldown.md)
- [`crafting_recipe`](crafting_recipe.md)
- [`dummy`](dummy.md)
- [`hud_render`](hud_render.md)
- [`inventory`](inventory.md)
- [`modify/air/speed`](modify_air_speed.md)
- [`modify/attribute/vanilla`](modify_attribute_vanilla.md)
- [`modify/attribute`](modify_attribute.md)
- [`modify/block/harvestable`](modify_block_harvestable.md)
- [`modify/block/selectable`](modify_block_selectable.md)
- [`modify/block/use`](modify_block_use.md)
- [`modify/climbing`](modify_climbing.md)
- [`modify/damage/dealt`](modify_damage_dealt.md)
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