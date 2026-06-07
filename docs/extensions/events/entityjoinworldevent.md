# **EntityJoinWorldEvent**

---

This event fires each time an entity joins your world.

## Parameter

`EntityJoinWorldEvent`

## Methods

### Entity

``` java
getEntity()
```

Returns the **Entity**.

### World

``` java
getWorld()
```

Returns the **World**.

## Example

``` java
/*
This lists all players that join in chat.
*/
@EventTarget
public void onEntityJoinWorld(EntityJoinWorldEvent event) {
    if (event.getEntity() instanceof EntityPlayer) {
        final EntityPlayer player = (EntityPlayer) event.getEntity();
        if (player == null) return;

        Meowtils.addMessage("Player joined: " + player.getName());
    }
}
```