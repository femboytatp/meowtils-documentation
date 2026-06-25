# **RenderStringEvent**

---

Fires each time a string is rendered.

## Parameter

`RenderStringEvent`

## Methods

### String

#### Get

``` java
getString()
```

Returns the current string.

#### Set

``` java
setString(String string)
```

Sets the current string.

## Example

``` java
/*
This visually replaces your name with "Meow".
*/
@EventTarget(priority = EventPriority.LOWEST)
public void onRenderString(RenderStringEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null || event.getString() == null) return;
    final String playerName = mc.thePlayer.getName();
    final String text = event.getString();

    if (text.contains(mc.thePlayer.getName())) {
        event.setString(text.replace(playerName, "Meow"));
    }
}
```