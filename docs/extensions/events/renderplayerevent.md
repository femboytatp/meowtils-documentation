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
/*
If a player is invisible this makes them visible again.
*/
@EventTarget
public void onRenderPlayer(RenderPlayerEvent event) {
    if (event.getStage() != RenderPlayerEvent.Stage.PRE) return;
    final EntityPlayer player = event.getPlayer();
        
    if (player.isInvisible()) {
        player.setInvisible(false);
    }
}
```