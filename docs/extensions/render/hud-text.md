# **Render HUD Text**

!!! Note

    When drawing text on screen use [RenderGameOverlayEvent](../events/rendergameoverlayevent.md).

``` java
Meowtils.drawString(String text, int x, int y, float scale, int color)
```

Draws a string on screen, font will depend on what is selected in the [Settings Module](../../modules/meowtils/settings.md).

## Render several lines

``` java
int y = 10;
for (String line : lines) {
    Meowtils.drawString(line, 10, y, 1, -1);
    y += Meowtils.offsetString(1);
}
```

If we want to render a list of strings from an array we can easily do so this way.

``` java
Meowtils.offsetString(float scale)
```

This will automatically calculate the required offset depending on font type and text scale.

## Full example

!!! Tip

    You should check **Minecraft.getMinecraft().currentScreen** to limit drawing your text so it only shows up when you want it to, like in the example below which will only draw the text when no GUI is open.

``` java
@EventTarget
public void onRenderGameOverlay(RenderGameOverlayEvent event) {
    if (mc.theWorld == null) return;
    if (mc.currentScreen != null) return;

    final String[] lines = {
            "Meow!",
            "Meow2!",
            "Meow3!"
    };

    int y = 10;
        
    for (String line : lines) {
        Meowtils.drawString(line, 10, y, 1, -1);
        y += Meowtils.offsetString(1);
    }
}
```