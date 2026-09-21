#   Int Provider

Int providers are data objects that operate on the given context, and return an integer based on the provided information.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired int provider type.


???+ question "Implicit `constant`"

    When defining an int provider, if you specify an integer value, it will implicitly use the `constant` int provider type.


### List of int provider types

<div class="annotate" markdown>

- `absolute`(1)
- `clamped`
- `conditional/composite`
- `conditional`
- `constant`
- `context`
- `difference` (2)
- `from_float`
- `max`
- `min`
- `nbt`
- `negate`
- `product` (3)
- `quotient`(4)
- `random/binomial`
- `random/uniform`(5)
- `sum`(6)
- `weighted`
- `adjacent_blocks`
- `blocks_colliding_box`
- `blocks_in_radius`
- `blocks_intersecting_box`
- `effect/amplifier`
- `entities_in_radius`
- `entity/active_effects`
- `equipped_enchantment_level`
- `item/count`
- `item/count/max`
- `item/fuel`
- `key/pressed_ticks`
- `key/pressed_time`
- `light_level`
- `player/food`
- `power/cooldown/remaining_ticks`
- `slot_id`
- `time`

</div>

1. Aliases: `abs`
2. Aliases: `sub`, `diff`, `subtract`
3. Aliases: `mul`, `multiply`
4. Aliases: `div`, `divide`
5. Aliases: `rand`, `random`
6. Aliases: `add`, `addition`
