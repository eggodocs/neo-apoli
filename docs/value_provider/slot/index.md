# Slot Provider

Slot providers are data objects that operate on the given context, and return a `SlotAccess`(1) based on the provided information.
{ .annotate }


1. `SlotAccess` is a functional interface that essentially references an item from an entity or an inventory.


### Format

Field | Type | Default | Description                                       
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired slot provider type.

???+ question "Implicit `context`"
    
    When defining a slot provider, if you specify a string, it will implicitly use the `context` slot provider type.


### List of slot provider types

-   `conditional/composite`
-   `conditional`
-   `context`
-   `block`
-   `entity`
