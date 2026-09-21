#   Action Types
Action types define how an action should operate on a context. Depending on the action, it can also pass the inherited context to its types that also use a context.

!!! note
    Some if not most action types require certain context parameters to function. Make sure to check the page for the corresponding action type that you want to use.

### List of action types
- `add_velocity`
- `apply_effects`
- `area_of_effect`
- `bone_meal`
- `clear_powers`
- `conditional/composite`
- `conditional`
- `consume_item`
- `damage_entity`
- `damage_item`
- `dismount`
- `emit_game_event`
- `execute_command`
- `exhaust`
- `explode`
- `extinguish_entity_fire`
- `gain_air`
- `give_items`
- `grant_power`
- `loop`
- `modify_block_state_property`
- `modify_item`
- `mount`
- `nothing`
- `place_block`
- `play_sound`
- `random_chance`
- `reference`
- `remove_power`
- `revoke_all_powers`
- `revoke_power`
- `sequence`
- `set_entity_on_fire`
- `shoot_entity`
- `side`
- `spawn_particles`
- `swing_hand`
- `tame`
- `toggle_power`
- `trigger_power_cooldown`
- `weighted`