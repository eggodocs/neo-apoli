#   Key Reference

An object that references a key binding, mainly used by powers to define which key it reacts to.


### Format

Field | Type | Default | Description
------|------|---------|------------
`id` | [String Provider](../providers/string/index.md) | | The ID of the referenced key binding.
`continuous` | [Boolean Provider](../providers/boolean/index.md) | `false` | Determines whether the the referenced key binding is held.


!!! question "Implicit formatting"

    When defining a key reference, if a string is specified, it will implicitly create a key reference which has its `continuous` field set to `false`.


### Example

=== "Full"

    ```json
    "key": {
        "id": "key.use",
        "continous": false
    }
    ```

=== "Implicit"

    ```json
    "key": "key.use"
    ```


### History

<table>
    <tr>
        <td style="text-align: center; vertical-align: middle"><b>Minecraft</b></td>
        <td style="text-align: center; vertical-align: middle"><b>Mod</b></td>
        <td style="vertical-align: middle"><b>Changelog</b></td>
    </tr>
    <tr style="text-align: center; vertical-align: middle">
        <td style="text-align: center; vertical-align: middle">1.21.5</td>
        <td style="text-align: center; vertical-align: middle">0.1.0</td>
        <td style="vertical-align: middle">Added the power type.</td>
    </tr>
</table>
