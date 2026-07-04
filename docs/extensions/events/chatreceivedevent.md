# **ChatReceivedEvent**

---

This event fires each time a message appears in your chat.

## Parameter

`ChatReceivedEvent`

## Properties

### Type

- **CHAT** - Normal chat messages.

- **SYSTEM** - System messages.

- **ACTION_BAR** - Action bar messages (above hotbar).

!!! Tip

    In most cases you should only use **CHAT**, which is what is normally used by default in Forge mods.

## Methods

### Component

``` java
IChatComponent getComponent()
```

Returns the `IChatComponent` of the message.

### Type

``` java
byte getType()
```

Corresponding to current message type.

!!! Tip

    It is recommended to use the type enums shown above instead of a byte.

## Example

``` java
@EventTarget
public void onChatReceived(ChatReceivedEvent event) {
    if (event.getType() != ChatReceivedEvent.CHAT) return; // Enforces normal chat messages only
    final String msg = event.getComponent().getUnformattedText();
        
    if (msg.contains("Meow")) {
        Meowtils.addMessage("Someone said Meow!");
    }
}
```