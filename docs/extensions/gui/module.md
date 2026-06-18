# **Module Setup**

Modules will show up in a new category called **Extensions**, they will behave like any other module in **Meowtils**. You will also be able to add components to a module if you want to add settings.

!!! Tip

    You should generally make one **Extension** per module, to keep features separate. This is seen as the standard, however it is up to you as adding several modules to an **Extension** is still possible.

## Requirements

1. Must extend `wtf.tatp.meowtils.extension.Extension`

2. Contain `@Config public boolean enabled = false;`

    _This is used for your module state. In this case we set it to false by default, which is the standard._

3. Contain `@Config public int key = 0;`

    _This is used for your module toggle bind. In this case we set it to 0 by default, which means no key is bound to it._

## Example

``` java
public class ExampleModule extends Extension {

    @Config public boolean enabled = false;
    @Config public int key = 0;

    public ExampleModule() {
        super("ExampleModule", "Meowtils"); // Module name & author (you)
        // Register components & tooltip here!
    }
}
```

[Download the **ExampleExtension**](https://github.com/femboytatp/meowtils-documentation/releases/download/ExampleExtension/ExampleExtension.zip).

### Module name

Change the module name to something relevant.

### Author

Set the author (which would be you, or you + credits). This shows up in the tooltip.

!!! Tip

    If you don't want an author tag you can put it as `null`.