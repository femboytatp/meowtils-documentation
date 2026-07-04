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
Stage getStage()
```

Returns the stage as shown above.

### Partial ticks

``` java
float getPartialTicks()
```

Progress between last and current tick, usually used for interpolation.

### Renderer

``` java
RenderPlayer getRenderer()
```

Returns `RenderPlayer`.

### Player

``` java
AbstractClientPlayer getPlayer()
```

Returns `AbstractClientPlayer`.

### Position

#### X

``` java
double getX()
```

Returns X pos.

#### Y

``` java
double getY()
```

Returns Y pos.

#### Z

``` java
double getZ()
```

Returns Z pos.

### Yaw

``` java
float getYaw()
```

Returns yaw.

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