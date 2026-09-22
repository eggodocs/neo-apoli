#   Color

Colors are objects used to provide an integer from a context object. The provided integer is a packed ARGB color.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired color type.


!!! question "Implicit `rgba`"

    When defining a color, if a string is specified, it will implicitly use the `rgba` color type.


### List of color types

- `argb`
- `hsv`
- `rgba`
- `dynamic/argb`
- `dynamic/hsv`
- `dynamic/rgba`
- `biome/foliage`
- `biome/grass`
- `biome/water`
