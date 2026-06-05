# **RenderTickEvent**

---

This event fires each render tick, which is once per frame.

!!! Note

    You should always RenderGameOverlayEvent or RenderWorldLastEvent for render modules. It is recommended that you only use this event when you need to update something faster than what is possible with client tick.

## Parameter

`RenderTickEvent`

## Properties

### Phase

- **PRE** - Before Minecraft render tick.

- **POST** - After Minecraft render tick.

!!! Tip

    If you don't know which one to use, use **POST**. In most cases you will never need to use **PRE**.

## Methods

### Phase

``` java
getPhase()
```

Gets the current render tick phase.

### Partial ticks

``` java
getPartialTicks()
```

Progress between last and current tick, usually used for interpolation.

## Example

``` java
/*
We make sure to return if the player or world doesn't exist, while also enforcing post (end) phase of the render tick.
*/
@EventTarget
public void onRenderTick(RenderTickEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null) return;
    if (event.getPhase() != RenderTickEvent.Phase.POST) return;
    Meowtils.addMessage("Render tick called");
}
```