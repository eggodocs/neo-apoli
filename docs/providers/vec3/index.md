# Vec3 Provider

Vec3 providers are data objects that operate on the given context, and return a `Vec3`(1) based on the provided information.
{ .annotate }


1. A vector that contains 3 doubles.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired vec3 provider type. |

???+ question "Implicit `constant`"
    
    When defining a vec3 provider, if you specify an array, it will implicitly use the `constant` vec3 provider type.


### List of vec3 provider types

-   `conditional/composite`
-   `conditional`
-   `constant`
-   `direction`
-   `dynamic`
-   `entity/position`
-   `entity/velocity`
-   `entity/view`
-   `offset`
