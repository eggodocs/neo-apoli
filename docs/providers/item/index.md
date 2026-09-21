#   Item Provider

Item providers are data objects that operate on the given context, and return an item stack based on the provided information.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired item provider type.


???+ question "Implicit `context`"

    When defining an item provider, if you specify a string, it will implicitly use the `context` item provider type.


### List of item provider types

- `conditional/composite`
- `conditional`
- `context`
