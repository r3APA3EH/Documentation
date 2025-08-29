# Looping
This section includes information on how you can loop an animation.

## Return to tick
This method comes first because it was added by us for the Bedrock format   
It was ported from playerAnimator and has the same functionality.

```json5
{
  "loopTick": 0.4 // In seconds
}
```

## Hold on last frame
As the name suggests, it makes the animation "hold" on the last frame.

```json5
{
  "loop": "hold_on_last_frame"
}
```

## Play once
Using this method, the animation won't loop; it will just play once.

```json5
{
  "loop": "true" // or "play_once"
}
```

## Loop
The most boring method, the animation simply starts from the beginning when it ends.

```json5
{
  "loop": "true" // or "loop"
}
```
