#   Power Types
A power type defines how an instance of a power should function. It also contains the additional required/optional fields used for parsing.

!!! note
    Each power type, **unless stated otherwise**, supports an optional `active_condition` field which determines whether the power is considered active. If the field is absent, the power will be considered as always active.

!!! note
    Every power type provides and requires the `neo-apoli:this_entity` context parameter, which refers to the entity holding the power.

    Some power types may provide certain context parameters that can be used in actions/conditions/value providers, so make sure to check their corresponding pages for more information.


### List of power types
- [`callback/block/break`](callback_block_break.md)
- [`callback/block/place`](callback_block_place.md)
- `callback/damage/dealt`
- `callback/player/respawned`
- `callback/player/wake_up`
- `callback/power/added`
- `callback/power/granted`
- `callback/power/removed`
- `callback/power/revoked`
- `callback/power/tick`
- `callback/projectile/land`
- `cooldown`
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