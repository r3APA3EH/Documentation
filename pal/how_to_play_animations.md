---
sidebar_position: 3
---

# How to play animations

```
        PlayerAnimationFactory.ANIMATION_DATA_FACTORY.registerFactory(ANIMATION_LAYER_ID, 1000,
                player -> new PlayerAnimationController(player,
                        (controller, state, animSetter) -> PlayState.STOP
                )
        );
```
Here is an example of how you register an animation layer for every player!  
You do this in your client init.  
Here the ANIMATION_LAYER_ID is the ResourceLocation/Identifier for you layer.  
The number after that is the priority of your animation.  
1000 priority is for cosmetic stuff like emotes, very low values are for idle animations, and values higher than that like 1500+ are for important gameplay animations.  

Here is how to get an animation layer and play an animation for a specific player:
```
		PlayerAnimationController controller = (PlayerAnimationController) PlayerAnimationAccess.getPlayerAnimationLayer(
                player, ANIMATION_LAYER_ID
        );
        controller.triggerAnimation(animationID);
```
That's the most basic way to do it.  
But there are a lot of other ways to play animations  
Take a look at the `replaceWithFade` method and the `PlayerRawAnimationBuilder` class!  

You should put your animations in `assets/<namespace>/player_animations`  
The animationID of your animation will be a ResourceLocation/Identifier with your mod's namespace and the path will be the name of the animation set in the animation file.  
Keep in mind that the name of the file itself has nothing to do with what the ID will be.  
