#   Dummy

Does nothing. Mainly serves as a placeholder for implementations that are implemented via Java code or by other data-driven powers.


### Format

*No additional fields.*


### Example

```json
{
    "type": "neo-apoli:dummy",
    "active_condition": {
        "type": "neo-apoli:is_entity_sneaking",
        "entity": "this"
    }
}
```

This example does nothing, but will be considered as active if the entity holding the power is sneaking.
