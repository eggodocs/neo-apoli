#   HUD element

HUD elements are objects that are displayed on the player's screen. This may vary from icon sprites to screen overlays.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired HUD element type.
`order` | Integer       |   | Determines the order at which the element is rendered.


??? question "About orders"

    HUD elements will be sorted in *natural order* meaning that the elements that have a lower order values will be rendered first before those that have higher order values.


### List of HUD element types

- `overlay/nausea`
- `overlay/texture`
- `resource_bar`
