# **SlotClickEvent**

---

This event fires each time you click a slot in an inventory.

## Parameter

`SlotClickEvent`

## Properties

### Type

#### Click type

_This is the type of action when clicking a slot._

- **CLICK_NORMAL**

- **CLICK_SHIFT**

- **CLICK_HOTBAR**

- **CLICK_MIDDLE**

- **CLICK_DROP**

- **CLICK_DRAG**

- **CLICK_DOUBLE**

#### Button type

_This is the mouse button type when clicking a slot._

- **BUTTON_LEFT**

- **BUTTON_RIGHT**

- **BUTTON_MIDDLE**

## Methods

### Gui container

``` java
getGuiContainer()
```

Returns current guiContainer.

### Slot

``` java
getSlot()
```

Returns current slot.

### Slot id

``` java
getSlotId()
```

Returns current slot ID.

### Click type

#### Get

``` java
getClickType()
```

Returns click type.

#### Set

``` java
setClickType(int clickType)
```

Sets the current click type.

!!! Example

    ``` java
    event.setClickType(SlotClickEvent.CLICK_MIDDLE);
    ```

!!! Warning

    When changing click type you should make sure the button type is also set in a way that would align with how a vanilla client behaves.

### Clicked button

#### Get

``` java
getClickedButton()
```

Returns clicked button.

#### Set

``` java
setClickedButton(int clickedButton)
```

Sets the current clicked button.

!!! Example

    ``` java
    event.setClickedButton(SlotClickEvent.BUTTON_MIDDLE);
    ```

!!! Warning

    When changing button type you should make sure the click type is also set in a way that would align with how a vanilla client behaves.

### Replace click

#### Get

``` java
getReplaceClick()
```

Gets whether click should be replaced with middle click or not.

#### Set

``` java
setReplaceClick()
```

Replaces all clicks with middle clicks.

!!! Tip

    This is usually used to replace your clicks with middle clicks. This prevents the clientside pick-up animation for items and allows you to click items faster since you no longer hold items, makes more of a difference when your latency is higher.

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