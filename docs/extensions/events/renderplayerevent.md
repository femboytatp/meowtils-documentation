# **RenderPlayerEvent**

---

Fires when players are rendered.

## Parameter

`RenderPlayerEvent`

## Properties

### Stage

- **PRE** - Before players render.

- **POST** - After players render.

## Methods

### Stage

``` java
getStage()
```

Returns the stage as shown above.

### Partial ticks

``` java
getPartialTicks()
```

Progress float between last and current tick, usually used for interpolation.

### Renderer

``` java
getRenderer()
```

Returns **RenderPlayer**.

### Player

``` java
getPlayer()
```

Returns **AbstractClientPlayer**.

### Position

#### X

``` java
getX()
```

Returns X double.

#### Y

``` java
getY()
```

Returns Y double.

#### Z

``` java
getZ()
```

Returns Z double.

### Yaw

``` java
getYaw()
```

Returns yaw float.

## Example

``` java
@EventTarget
public void onRenderPlayer(RenderPlayerEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null || event.getStage() != RenderPlayerEvent.Stage.POST) return;
    Meowtils.addMessage("All players have been rendered!");
}
```