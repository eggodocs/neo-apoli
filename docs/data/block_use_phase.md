#   Block Use Phase

A string that indicates the phase of which the player is using a block.


!!! note

    With the way Minecraft's block interaction system works, it will first check if the block has an interaction result when interacted with an item (`block_with_item`). If the interaction result indicates a pass (allowing for other interactions to perform), it will then check if the block has an interaction result without an item (`block`)


### Values

Phase | Description
------|------------
`block_with_item` | Indicates that the interaction of a block is with an item.
`block` | Indicates that the interaction of a block.
