# **WorldEvent**

---

This event fires each time a world loads or unloads for you.

## Parameter

`WorldEvent`

## Properties

### Type

- **LOAD**

- **UNLOAD**

## Methods

### Type

``` java
getType()
```

Returns the type shown above.

### World

``` java
getWorld()
```

Returns **WorldClient**.

## Example

``` java
@EventTarget
public void onWorldLoad(WorldEvent event) {
    if (event.getType() != WorldEvent.Type.LOAD) return;
    Meowtils.addMessage("World loaded!");
}
```