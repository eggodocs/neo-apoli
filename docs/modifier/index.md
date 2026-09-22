#   Modifier

Modifiers are objects used to specify how a floating point value is modified.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`      | Identifier            |               | The identifier of the desired modifier type.
`phase`     | Phase                 |               | Determines when the modifier will be applied.
`modifiers` | Array of Modifiers    | *optional*    | If specified, these modifiers will be applied first before the this modifier is applied.
`amount`    | Float Provider        |               | The amount of the modifier.


??? note "About fields"

    The table contains the common fields used by modifiers. Some modifiers may not have the same fields, so make sure to check!


### List of modifier types.

!!! question inline end "Order of modifiers"

    The modifiers are applied at the order they're displayed in this list, with `add` being first and `set` being last.

- `add`
- `multiply`
- `multiply_additive`
- `multiply_multiplicative`
- `divide`
- `min`
- `max`
- `set`
