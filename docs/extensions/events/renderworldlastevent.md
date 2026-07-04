# **RenderWorldLastEvent**

---

Fires after world has been rendered, each frame.

!!! Tip

    This should be used to render things at a fixed position, such as on players or for example text above a specific block.

## Parameter

`RenderWorldLastEvent`

## Methods

### Partial ticks

``` java
float getPartialTicks()
```

Progress between last and current tick, usually used for interpolation.

## Example

``` java
/*
This draws a 3D ESP box on your own player.
*/
@EventTarget
public void onRenderWorldLast(RenderWorldLastEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null) return;

    for (EntityPlayer player : mc.theWorld.playerEntities) {
        if (player == null) continue;
        if (player != mc.thePlayer) continue; // Skip other players

        final Color color = ColorUtil.getColor(255, 255, 255); // White color

        Render.drawEntityBox(player, true, false, color, true, color, 0.1f, 0.1f, 0.1f);
    }
}
```