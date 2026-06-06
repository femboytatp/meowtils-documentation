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
/*
This replaces all clicks in a chest with a left + shift click, making it so
you always directly shift-click items into your inventory.
*/
@EventTarget
public void onSlotClick(SlotClickEvent event) {
    if (event.getGuiContainer() instanceof GuiChest) { // Limited to chests only
        event.setClickedButton(SlotClickEvent.BUTTON_LEFT); // Left click
        event.setClickType(SlotClickEvent.CLICK_SHIFT); // Shift click
    }
}
```