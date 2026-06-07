# **PlayerInteractEvent**

---

Fires each time the player interacts with a block in the world .

## Parameter

`PlayerInteractEvent`

## Properties

### Action

- **LEFT_CLICK_BLOCK**

- **RIGHT_CLICK_BLOCK**

## Methods

### Action

``` java
getAction()
```

Returns current action as shown above.

### Player

``` java
getPlayer()
```

Returns EntityPlayerSP.

### World

``` java
getWorld()
```

Returns WorldClient.

### Pos

``` java
getPos()
```

Returns BlockPos.

### Facing

``` java
getFacing()
```

Returns EnumFacing.

## Example

``` java
/*
Sends a message when you right-click a chest.
*/
@EventTarget
public void onPlayerInteract(PlayerInteractEvent event) {
    if (event.getAction() != PlayerInteractEvent.Action.RIGHT_CLICK_BLOCK) return;

    final BlockPos blockPos = event.getPos();
    final TileEntity tileEntity = mc.theWorld.getTileEntity(blockPos);

    if (tileEntity instanceof TileEntityChest) {
        Meowtils.addMessage("Right clicked chest!");
    }
}
```