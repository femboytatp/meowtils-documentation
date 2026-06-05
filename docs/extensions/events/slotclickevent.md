# **SlotClickEvent**

---

This event fires each time you click a slot in an inventory.

## Parameter

`SlotClickEvent`

## Properties

### Type

#### Click type

- **CLICK_NORMAL**

- **CLICK_SHIFT**

- **CLICK_HOTBAR**

- **CLICK_MIDDLE**

- **CLICK_DROP**

- **CLICK_DRAG**

- **CLICK_DOUBLE**

#### Button type

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

### Clicked button

``` java
getClickedButton()
```

Returns clicked button.

### Click type

``` java
getClickType()
```

Returns click type.

### Replace click

``` java
getReplaceClick()
```

Gets whether click should be replaced with middle click or not.

### Clicked button