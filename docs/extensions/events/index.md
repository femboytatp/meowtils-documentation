# **Events**

Events allow you to hook into various things that happen in Minecraft. These will generally be used to tell your Extension when to run your code.

Meowtils events are very similar to Forge events, however there are a few notable differences which will be explained below alongside some examples.

!!! Warning

    In order for your Extension to be compatible with Lunar Client, you must only use Meowtils events. Any Forge events (@SubscribeEvent annotated) will only work on Forge or if you specifically inject Meowtils into "Lunar + Forge".

# Usage

Like Forge, an event method has to be a public method that returns void, the actual method name can be anything but generally you would name it something relevant such as **onClientTick**.

## Annotation

Like Forge, an event method requires an annotation in order to be discovered. In this case that would be @EventTarget which tells the Meowtils event bus that this is a method that should be called when the relevant event fires.

``` java
@EventTarget
```