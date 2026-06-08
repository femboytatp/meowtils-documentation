# **ClientTickEvent**

---

This event fires each client tick, which would normally be 20 times per second.

## Parameter

`ClientTickEvent`

## Properties

### Phase

- **PRE** - Before Minecraft ticks.

- **POST** - After Minecraft ticks.

!!! Tip

    If you don't know which one to use, use **POST**. In most cases you will never need to use **PRE**.

## Methods

### Phase

``` java
getPhase()
```

Returns the current tick phase.

## Example

``` java
/*
We make sure to return if the player or world doesn't exist, while also enforcing post (end) phase of the tick.
*/
@EventTarget
public void onClientTick(ClientTickEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null) return;
    if (event.getPhase() != ClientTickEvent.Phase.POST) return;
    Meowtils.addMessage("Client tick!");
}
```