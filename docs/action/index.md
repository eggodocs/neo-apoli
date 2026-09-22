# Action

Actions are used to operate on a given context. Actions can change or affect the world and/or its entities depending on the specified type.

Custom actions can be defined as JSON/JSON5/JSONC files in the `data/<namespace>/neo-apoli/action` directory of a data pack.

Data packs that load later with an action file with the same name and directory will replace the existing action.


!!! note

    Some actions require certain context parameters to function properly. Make sure to check the page for the desired action type for more information.


### Format

Field | Type | Default | Description
------|------|:-------:|------------
`type` | [Identifier](https://minecraft.wiki/w/Identifier) | | The identifier of the desired action type.


???+ question "Implicit `sequence`"

    When defining an action, if you specify an array instead of an object, it will implicitly use the `sequence` action type.


### List of action types

-   `add_velocity`
-   `apply_effects`
-   `area_of_effect`
-   `bone_meal`
-   `clear_powers`
-   `conditional/composite`
-   `conditional`
-   `consume_item`
-   `damage_entity`
-   `damage_item`
-   `dismount`
-   `emit_game_event`
-   `execute_command`
-   `exhaust`
-   `explode`
-   `extinguish_entity_fire`
-   `gain_air`
-   `give_items`
-   `grant_power`
-   `loop`
-   `modify_block_state_property`
-   `modify_item`
-   `mount`
-   `nothing`
-   `place_block`
-   `play_sound`
-   `random_chance`
-   `reference`
-   `remove_power`
-   `revoke_all_powers`
-   `revoke_power`
-   `sequence`
-   `set_entity_on_fire`
-   `shoot_entity`
-   `side`
-   `spawn_particles`
-   `swing_hand`
-   `tame`
-   `toggle_power`
-   `trigger_power_cooldown`
-   `weighted`
