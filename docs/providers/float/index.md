#   Float Provider

Float providers are data objects that operate on the given context, and return a float based on the provided information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired float provider type.


???+ question "Implicit types"

    When defining an float provider, specifying certain data types will implicitly use a specific type:

    Data Type | Float Provider Type
    ----------|------------------
    String | `context`
    Float | `constant`


### List of float provider types

<div class="annotate" markdown>

- `absolute`(1)
- `clamped`
- `conditional/composite`
- `conditional`
- `constant`
- `context`
- `difference`(2)
- `from_int`
- `linear_interpolated`(3)
- `max`
- `min`
- `nbt`
- `negate`
- `power`
- `product`(4)
- `quotient`(5)
- `random/uniform`(6)
- `round`
- `sum`(7)
- `weighted`
- `box/component`
- `box/size`
- `brightness`
- `distance_between_positions`
- `entity/attribute`
- `entity/fluid_height`
- `item/attribute`
- `player/saturation`
- `power/cooldown/progress`
- `vector/component`
- `vector/length`

</div>

1. Aliases: `abs`
2. Aliases: `sub`, `diff`, `subtract`
3. Aliases: `lerp`
4. Aliases: `mul`, `multiply`
5. Aliases: `div`, `divide`
6. Aliases: `random`, `rand`
7. Aliases: `add`, `addition`
