# **Entrypoint**

This is your main point of entry, it is called once when your **Extension** is loaded.

!!! Info

    You are required to register modules, classes with events, and so on.

## Requirements

1. Create a class called `Main.java`.

2. Add a `public static` method that returns `void`.

3. Name it `init`.

!!! Example

    ``` java
    public class Main {
    
        public static void init() {
            // Register here
        }
    }
    ```

## What do you need to register?

!!! Tip

    You should init your own stuff here as well.

- [Modules](gui/module.md)

    !!! Example
    
        ``` java
        Extension.registerModule(new ExampleModule());
        ```

- [Events](events/index.md)

    !!! Example

        ``` java
        // Not needed for module classes - that is done automatically
        Extension.registerEvent(new ExampleHandler());
        ```

- [Commands](basic/commands.md)

    !!! Example

        ``` java
        CommandHandler.register(new ExampleCommand());
        ```

- [Slot Background](render/slot-background.md)

    !!! Example

        ``` java
        SlotManager.register(new ExampleSlot());
        ```

- [Name Icons](render/name-icons.md)

    !!! Example

        ``` java
        IconManager.register(new ExampleIcon());
        ```