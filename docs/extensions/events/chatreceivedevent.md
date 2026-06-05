# **ChatReceivedEvent**

---

This event fires each time a message appears in your chat.

## Parameter

`ChatReceivedEvent`

## Properties

### Type

- **CHAT** - Normal chat messages.

- **SYSTEM** - System messages.

- **ACTION_BAR** - Action bar messages above hotbar.

!!! Tip

    In most cases you should only use **CHAT**, which is what is normally used by default in Forge mods.

## Methods

### Component

``` java
getComponent()
```

Gets the **IChatComponent** of the message.

### Type

``` java
getType()
```

Gets the current type of message.

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