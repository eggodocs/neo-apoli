#   NBT Provider

NBT providers are data objects that operate on the given context, and return an NBT based on the provided information.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired NBT provider type.


???+ question "Implicit `constant`"

    When defining an NBT provider, if you specify a string or NBT, it will implicitly use the `constant` NBT provider type.


### List of NBT provider types

- `conditional/composite`
- `conditional`
- `constant`
- `block`
- `entity`
- `item`
- `power`
- `storage`
