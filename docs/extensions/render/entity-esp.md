# **Render Entity ESP**

!!! Note

    When rendering visuals in your world you should use [RenderWorldLastEvent](../events/renderworldlastevent.md).

``` java
Render.drawEntityBox(
    Entity entity, 
    boolean is3D, 
    boolean fill, 
    Color fillColor, 
    boolean outline, 
    Color outlineColor, 
    double expandX, 
    double expandY, 
    double expandZ
)
```

### entity

The entity to draw an ESP for.

### is3D

If it should draw a 3D ESP box, if false it will draw a 2D box.

### fill

If it should fill the box.

### fillColor

The color fill should have, if enabled.

### outline

Outlines the box, always true for 2D ESP.

### outlineColor

The outline color.

### expandX

Visually expands the box in X direction.

### expandY

Visually expands the box in Y direction.

### expandZ

Visually expands the box in Z direction.

!!! Tip

    This automatically aligns the ESP boxes with the entity bounding boxes, however you can expand it if you want it to be more accurate as it sometimes varies. For example it is recommended that you expand it by 0.1 for players.

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
        if (player != mc.thePlayer) continue;

        final Color color = ColorUtil.getColor(255, 255, 255);

        Render.drawEntityBox(player, true, false, color, true, color, 0.1f, 0.1f, 0.1f);
    }
}
```