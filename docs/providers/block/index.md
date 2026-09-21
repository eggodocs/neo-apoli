#   Block Provider

Block providers are data objects that operate on the given context, and return a `CachedBlock`(1) based on the provided information.
{ .annotate }


1. `CachedBlock` is a record that contains the provided block's position, state, and entity.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired block provider.


### List of block provider types

- `conditional/composite`
- `conditional`
- `context`
- `world`