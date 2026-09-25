#   Modifier

Modifiers are objects used to specify how a floating point value is modified.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired modifier type.
`phase` | Phase | | Determines when the modifier will be applied.
`modifiers` | Array of [Modifiers](index.md) | *optional* | If specified, these modifiers will be applied first before the this modifier is applied.
`amount` | [Float Provider](../providers/float/index.md) | | The amount of the modifier.


??? note "About fields"

    The table contains the common fields used by modifiers. Some modifiers may not have the same fields, so make sure to check!


!!! question "Modifier phases"

    Modifiers are applied in the following two phases, listed in order:

    Phase | Description
    ------|------------
    `base` | Determines that the base value will be modified.
    `total` | Determines that the total value will be modified.


### List of modifier types

- `add`
- `multiply`
- `multiply_additive`
- `multiply_multiplicative`
- `divide`
- `min`
- `max`
- `set`

!!! question "Order of modifiers"

    The modifiers are applied in the order they're listed in, where `add` is applied first and `set` is applied last.
