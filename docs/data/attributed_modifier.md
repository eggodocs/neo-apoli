#   Attributed Modifier

An object that contains an attribute and its modifier.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`attribute` | [Identifier]({{ mc.identifier }}) | | The identifier of the attribute to modify.
`id` | [Identifier]({{ mc.identifier }}) | | The identifier of the modifier. This can be arbitrary.
`amount` | Float | | The amount of the modifier.
`operation` | String | | Determines how the modifier modifies the value.


!!! question "Operations"

    Here are the possible operations an attributed modifier can perform:

    Operation | Description
    ----------|------------
    `add_value` | Adds all of the modifiers' amounts to the base value of the attribute.<br>$(Total = Base + Amount_1 + Amount_2 + ... + Amount_n)$
    `add_multiplied_base` | Multiplies the base value of the attribute by (1 + sum of modifiers' amounts.)<br>$(Total = Base * (1 + Amount_1 + Amount_2 + ... + Amount_n))$
    `add_multiplied_total` | Multiplies the base value of the attribute by (1 + modifiers' amounts) for every modifier.<br>$(Total = Base * (1 + Amount_1) * (1 + Amount_2) * ... * (1 + Amount_n))$


### Example

=== "Single"

    ```json
    {
        "attribute": "minecraft:burning_time",
        "id": "example:longer_burning_time",
        "amount": 1.0,
        "operation": "add_multiplied_total"
    }
    ```

    This example doubles the base value of the `minecraft:burning_time` attribute of the entity, which is used as a multiplier for how long the entity will burn. $(Total = Base * (1 + 1.0))$

=== "Multiple"

    ```json
    [
        {
            "attribute": "minecraft:armor",
            "id": "example:tuff",
            "amount": 1.0,
            "operation": "add_multiplied_base"
        },
        {
            "attribute": "minecraft:armor",
            "id": "example:so_tuff",
            "amount": 3.0,
            "operation": "add_multiplied_base"
        }
    ]
    ```

    This example multiplies the base value of the `minecraft:armor` attribute by the sum of the modifiers' amounts. $(Total = Base + 1.0 + 3.0)$
