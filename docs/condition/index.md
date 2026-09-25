#   Condition

Conditions are used to test against a given context, checking the provided information and return either a pass or fail. 

Custom conditions can be defined as JSON/JSON5/JSONC files in the `data/<namespace>/neo-apoli/condition` directory of a data pack. Data packs that load later with a condition file with the same name and directory will replace the existing condition.


!!! note

    Some conditions require certain context parameters to function properly. Make sure to check the page for the desired condition type for more information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier]({{ mc.identifier }}) | | The identifier of the desired condition type.


### List of condition types

- `all_of`
- `any_of`
- `block_state_property`
- `compare`
- `constant`
- `difficulty`
- `dynamic`
- `entity_has_active_power`
- `entity_has_correct_tool_for_block`
- `entity_has_item_equipped`
- `entity_has_power`
- `entity_has_pressed_keys_simultaneously`
- `exists`
- `inverted`
- `is_block_entity`
- `is_block_in_tag`
- `is_block_of_type`
- `is_block_replaceable`
- `is_damage_source_in_tag`
- `is_damage_source_of_type`
- `is_effect_in_tag`
- `is_effect_of_type`
- `is_entity_climbing`
- `is_entity_fall_flying`
- `is_entity_horizontally_colliding`
- `is_entity_in_tag`
- `is_entity_of_type`
- `is_entity_on_fire`
- `is_entity_owned_by_other`
- `is_entity_sneaking`
- `is_entity_sprinting`
- `is_entity_stepping_on_block`
- `is_exposed_to_precipitation`
- `is_exposed_to_sky`
- `item_matches_ingredient`
- `item_matches_predicate`
- `matches_block_pattern`
- `reference`