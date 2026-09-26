#   Effect Provider

Effect providers are data objects that operate on the given context, and return an effect instance based on the provided information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired effect provider type.


???+ question "Implicit `context`"

    When defining a direction provider, if you specify a [string][string], it will implicitly use the `context` direction provider type.


### List of effect provider types

- `conditional/composite`
- `conditional`
- `context`
