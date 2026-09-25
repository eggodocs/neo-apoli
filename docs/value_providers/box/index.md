#   Box Provider

Box providers are data objects that operate on the given context, and return an `AABB` (axis-aligned bounding box) based on the provided information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired box provider.


### List of box provider types

- `conditional/composite`
- `conditional`
- `constant`
- `dynamic`
- `offset`
- `translate`
- `block/bounds`
- `entity/bounds`
