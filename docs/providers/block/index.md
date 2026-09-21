#   Block Provider

Block providers are data objects that operate on the given context, and return a `CachedBlock` based on the provided information.

`CachedBlock` is a record that contains the provided block's position, state, and entity.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired boolean provider.


### List of boolean provider types

- `conditional/composite`
- `conditional`
- `context`
- `world`