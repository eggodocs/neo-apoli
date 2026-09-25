#   Interaction Result

A string that indicates the result of an interaction. Mainly used for when players interact with a block or entity.


### List of values

Result | Description
-------|------------
`success` | Indicates that the interafction and the player's hand is swung on the client.
`success_server` | Indicates that the interaction is performed and the player's hand is swung on the server.
`consume` | Indicates that the interaction is performed but the player's hand is not swung. 
`fail` | Indicates that the interaction is not performed.
`pass` | Indicates that the interaction is not performed but allows other interactions to perform.
