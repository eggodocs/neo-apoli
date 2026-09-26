# String Provider

String providers are data objects that operate on the given context, and return a [string][string] based on the provided information.


### Format
Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired string provider type. |

???+ question "Implicit `constant`"
    
    When defining a string provider, if you specify a [string][string], it will implicitly use the `constant` string provider type.


### List of string provider types

-   `conditional/composite`
-   `conditional`
-   `constant`
-   `join`
-   `entity/uuid`
-   `nbt`
-   `from_int`
-   `from_float`
