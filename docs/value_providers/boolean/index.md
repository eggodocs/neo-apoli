#   Boolean Provider

Boolean providers are data objects that operate on the given context, and return a boolean value based on the provided information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired boolean provider.


### List of boolean provider types

- `conditional/composite`
- `conditional`
- `constant`
- `condition_result`