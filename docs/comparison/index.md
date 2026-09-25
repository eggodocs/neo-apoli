#   Comparison

Comparisons are data objects used to compare two comparable objects and return whether it passes or fails.

Some comparisons use a comparator, while others rely on the compared objects' equality.


!!! note

    This is mainly used by the `compare` condition type.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired comparison type.


### List of comparison types

- `entity`
- `float`
- `int`
- `nbt`
- `string`
