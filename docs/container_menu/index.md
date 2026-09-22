#   Container Menu

Container menus are types that indicate how a GUI (graphical user interface) should be constructed for an inventory.


!!! note

    This type is mainly used by the `inventory` power type.


### Format

Field   | Type  | Default   | Description
--------|-------|-----------|------------
`type`  | Identifier    |   | The identifier of the desired container menu type.


## List of container menu types

<div class="annotate" markdown>

- `generic_9x1`(1)
- `generic_9x2`(2)
- `generic_9x3`(3)
- `generic_9x4`(4)
- `generic_9x5`(5)
- `generic_9x6`(6)
- `generic_3x3`(7)
- `hopper`(8)
- `dynamic`(9)

</div>

1. This type can be inlined. (e.g: `"menu": "generic_9x1"`)
2. This type can be inlined (e.g: `"menu": "generic_9x2"`). Aliases: `chest`
3. This type can be inlined (e.g: `"menu": "generic_9x3"`). Aliases: `double_chest`
4. This type can be inlined (e.g: `"menu": "generic_9x4"`)
5. This type can be inlined (e.g: `"menu": "generic_9x5"`)
6. This type can be inlined (e.g: `"menu": "generic_9x6"`)
7. This type can be inlined (e.g: `"menu": "generic_3x3"`) Aliases: `dropper`, `dispenser`
8. This type can be inlined (e.g: `"menu": "hopper"`)
9. This type is currently <span style="color:darkred;"><b>not supported</b></span>