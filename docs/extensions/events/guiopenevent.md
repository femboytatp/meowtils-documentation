# **GuiOpenEvent**

---

This event fires each time the player opens a **GuiScreen**.

## Parameter

`GuiOpenEvent`

## Methods

### Gui

``` java
getGui()
```

Gets current **GuiScreen**.

## Example

``` java
@EventTarget
public void onGuiOpen(GuiOpenEvent event) {
    if (event.getGui() instanceof GuiChest) {
        Meowtils.addMessage("Player opened chest!");
    }
}
```