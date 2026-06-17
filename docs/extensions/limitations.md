# **Extension Limitations**

!!! Info

    **Extensions** are seen as additions loaded by **Meowtils** that provide a bridge between your code and **Meowtils**. They are treated as scripts with less limitations. They will have certain limitations due to how they are loaded.

## Mixins

??? failure "Not Supported"

    **Mixins** are not supported.

Since **Extensions** load at runtime by **Meowtils** you are unable to use certain things that are required to load before class transformation, while this applies to several things the most notable one is **Mixins**.

!!! Info

    In many cases you won't need Mixins at all, however if you do and are unable to find a way around this limitation, it is recommended that you load your own mod instead.

## Reflection

??? success "Supported"

    **Reflection** is supported.

**Reflection** is a powerful tool that, while not as powerful as **Mixins**, still provide a way to modify certain things that would have otherwise only been possible through **Mixins**. For many features that otherwise require **Mixins** this is a great workaround.

[Java Reflection API](https://docs.oracle.com/javase/8/docs/technotes/guides/reflection/index.html).

!!! bug "Important"

    In order to ensure compatibility with both **Lunar Client** and **Forge** you will need to include several mappings for fields.

!!! Tip

    You can find mappings in the `resources` directory in **Meowtils**, you can also use any mapping viewer as long as they include **SRG** & **MCP** mappings.