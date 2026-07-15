---
sidebar_position: 1
description: "How to create emotes using Blender rigs."
---

# Creating Emotes With Blender

To make emotes in Blender, you need to use one of the available rigs on Emotecraft's [GitHub](https://github.com/KosmX/emotes/tree/dev/blender). Please read the README.md.    
This guide is based on the `emote_creator` one as it has more features.  
It is expected for you to already be familiar with Blender in some way. If you are not, please read the [Blender Documentation](https://docs.blender.org/manual/en/latest/) first. I recommend reading the `User Interface`, `Editors`, `Scenes & Objects` and `Animation` sections.  

# How do I make emotes??
You animate, then go to the `Export` tab, change the contents of the variables to your liking and run the script. Your emote will be placed in the same directory as the rig.  
To make the animation loop, check the `Cyclic Animation` box in the action properties.  
If you don't want some bones to be exported, comment them from the export_bones list in the script. If you add some custom pivot bones, you have to add them to the list.  

The icon is created on export automatically.  

There is a switch in the settings bone's properties to enable vanlla mode, so the limbs move to imitate bends without bends.  

# You can
- Add new bones -- they will be exported as [custom pivot bones](./custom_pivot_points.md).
- Use fcurve modifiers, constraints.

# You may not
- Apply any translation to the bend bones other than pitch rotation. (for now)

# Limitations
- Drivers don't get exported.
- Easings may look incorrect, because they work differently in Blender compared to the game.


