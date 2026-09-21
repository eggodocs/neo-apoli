#   Command Source Provider

Command source providers are data objects that operate on the given context, and return a `CommandSourceStack`(1) based on the provided information.
{ .annotate }


1. `CommandSourceStack` is vanilla's object used for executing commands.


???+ warning

    Command source providers are strictly **server-sided** only.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired command source provider.


### List of command source provider types

<div class="annotate" markdown>

- `conditional/composite`
- `conditional`
- `block`
- `entity`
- `server`(1)

</div>


1. This type can be inlined. (e.g: `"source": "server"`)
