# Creating Emotes With Blockbench

You must understand how the json structure is organized before you start!

# Extra data
To specify author, description, and more, you must use the `player_animation_library` object in your animation object:

```json5
{
  "format_version": "1.8.0",
  "animations": {
    "key": {
      "player_animation_library": { // Here!
        "name": "My animation", // If no name is specified, the key will be used
        "description": "My first animation",
        "author": "dima_dencep"
        // etc...
      },
      "bones": {}
    }
  },
  "geckolib_format_version": 2
}
```

:::warning
Don't copy the code above, json doesn't support comments and the code above may break your animation when copied!
:::
