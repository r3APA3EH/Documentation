# Creating Emotes With Blender

To make emotes in Blender, you need to use one of the available rigs on the Emotecraft's [GitHub](https://github.com/KosmX/emotes/tree/dev/blender). Please read the readme.    
In this guide we will be using the `emote_creator_bend_item_scale` one as it has more features. The process will be roughly the same with other rigs.   
It is expected that you are already familliar with Blender in some way. If you are not, please read the [Blender Documentation](https://docs.blender.org/manual/en/latest/) first. I recommend reading `User Interface`, `Editors`, `Scenes & Objects` and `Animation` sections.    

# How do I make emotes??
You place all the keyframes you want on the body parts, go to the `Export` tab, change the contents of the variables for your liking and run the script. Your emote will be placed in the same directory as the rig.    

:::warning
Items are animated with the `rightItem` and `leftItem` objects, not the sword models!
:::

Press F12 to make an icon for your emote. You can set up the camera however you want.

# Limitations
- `Bezier` interpolation is replaced with `QUAD`
- `Automatic` easing is replaced with `INOUT`
- The script reads keyframes only, so you can't use `Graph Editor`, `Drivers` and `Nonlinear Animation` unless you bake the animation
- You can't change relations between body parts
- You can't scale bend objects, scale their parents instead
- Scaled item's position gets exported incorecctly (Location needs to be divided by scale on corresponding axes, but it can't be done well without baking)

# Tricks
Baking the animation is your best friend. It allows to do nearly any animation feature in Blender.  
Baking the animation enables you to using `Bezier` interpolation and `Automatic` easing as it gets baked into keyframes that the script can read. The same with `Graph Editor`, `Drivers` and `Nonlinear Animation` editors.    
