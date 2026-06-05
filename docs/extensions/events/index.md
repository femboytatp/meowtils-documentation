# **Events**

---

Events allow you to hook into various things that happen in Minecraft. These will generally be used to tell your Extension when to run your code.

Meowtils events are very similar to Forge events, however there are a few notable differences which will be explained below alongside some examples.

!!! Warning

    In order for your Extension to be compatible with Lunar Client, you must only use Meowtils events. Any Forge events (@SubscribeEvent annotated) will only work on Forge or if you specifically inject Meowtils into "Lunar + Forge".

# Usage

---

Like Forge, an event method has to be a public method that returns void, the actual method name can be anything but generally you would name it something relevant such as **onClientTick**.

## Annotation

Like Forge, an event method requires an annotation in order to be discovered. In this case that would be @EventTarget which tells the Meowtils event bus that this is a method that should be called when the relevant event fires.

### Priority

As shown in the example below you are able to set event priority, same as Forge. It defaults to `NORMAL` if none are set.

- `HIGHEST`

- `HIGH`

- `NORMAL`

- `LOW`

- `LOWEST`

!!! Example

    ``` java
    @EventTarget(priority = EventPriority.HIGHEST)
    public void onClientTick(ClientTickEvent event)...
    ```

## Parameter

### Type

Like Forge your event requires a parameter, the type would be the event you are listening to.

!!! Example

    `ClientTickEvent`

### Name

The parameter name can be anything and it is just used for your event method to "access" the event.

!!! Example

    Normally you would name this "event" or "e".

    `public void (ClientTickEvent event)...`

## Properties

Certain events have properties that are important to know about. If an event has specific properties, they would be documented on that specific event page.

### Common properties

#### Phase

Event phases determine when events are fired, usually this would have **PRE** & **POST**, which means the event either fires before or after Minecraft has ran it's own code for this specific event.

#### Type

Similarly to phases, this determines when a specific event should fire. Usually this would be used for selecting whether or not you should fire your event during world load/unload, or which type of chat message you should listen to.

!!! Tip

    In order to prevent your events from firing more than wanted you should always strictly enforce properties. Generally you should only run `ClientTickEvent|RenderTickEvent` on **POST**, and `ChatReceivedEvent` with **CHAT**.

## Methods

Events will usually have their own methods, in the example below we will use `getPhase()` in ClientTickEvent to check the current tick phase.

!!! Info

    All events will have available methods documented on its own page.

## Cancelling

You can cancel events, which would prevent actions from being performed.

``` java
event.setCancelled(true);
```

!!! Note

    You should only cancel events when you know what you are doing and what it would lead to.

## Example

This is an example of a ClientTickEvent that would print a message saying "Hello, player!" in your own chat, every Minecraft tick (20 times a second).

!!! Note

    In this case we also check if the local player or world is null, since there is no point in sending a message if there is no chat visible. In some cases this will also prevent crashes, for example if you try to access a player that currently doesn't even exist.

``` java
@EventTarget
public void onClientTick(ClientTickEvent event) {
    if (mc.thePlayer == null || mc.theWorld == null || event.getPhase() != ClientTickEvent.Phase.POST) return;
    Meowtils.addMessage("Hello, player!");
}
```

As you can see, this is very similar to how a typical Forge event would be structured.