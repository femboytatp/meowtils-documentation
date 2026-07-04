# **KeyInputEvent**

---

This fires each time you press a key.

**Cancellable =** `true`

!!! Note

    This only applies to keybinds that are set in **Minecraft settings**.

## Parameter

`KeyInputEvent`

## Methods

### Key

``` java
KeyBinding getKey()
```

Returns the pressed `KeyBinding`.

## Example

``` java
@EventTarget
public void onKeyInput(KeyInputEvent event) {
    if (event.getKey() == mc.gameSettings.keyBindAttack) {
        Meowtils.addMessage("You pressed attack key!");
    }
}
```