# **RenderGameOverlayEvent**

---

This fires each frame.

**Cancellable =** `false`

!!! Tip

    This should be used for rendering HUD overlays, which would be text in most cases.

## Parameter

`RenderGameOverlayEvent`

## Example

``` java
@EventTarget
public void onRenderGameOverlay(RenderGameOverlayEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null) return;
    if (mc.currentScreen != null) return;

    Meowtils.drawString("Example HUD text", 10, 10, 1, -1);
}
```