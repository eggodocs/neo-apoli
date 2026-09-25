#   Entity Provider

Entity providers are data objects that operate on the given context, and return an entity based on the provided information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired entity provider type.


???+ question "Implicit `context`"

    When defining a entity provider, if you specify a string, it will implicitly use the `context` entity provider type.


### List of entity provider types

- `conditional/composite`
- `conditional`
- `context`
- `selector`
