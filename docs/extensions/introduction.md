# **Extensions**

---

An Extension is an external file that is loaded by Meowtils, it acts as a bridge that allows you to add features. They could be compared to scripts, except with less limitations.

Modules from extensions will show up in a new category called **Extensions**.

!!! Danger

    Extensions have very few limitations, they have the same permissions as Minecraft does. This means they may execute unwanted or malicious code.
    
    **ONLY DOWNLOAD EXTENSIONS FROM TRUSTED SOURCES**

!!! Note

    These docs make the assumption that you have at least **some** past experience with java and Minecraft in general.

## Usage

To use an Extension, simply put it in the **extensions** folder located in the **meowtils** folder in your game directory. You can also open this folder ingame by doing `/extensions`.

!!! Info

    Extensions end with .meowtils

### Loading

Extensions that already exist in your folder are automatically loaded when launching your game. 

You can also add, remove, or swap Extensions during runtime and then do `/reload` to load them.

## Standards

Generally you should only register one module per extension, and not combine several unrelated features into one extension.

!!! Tip

    It is recommended that you follow standards for clarity and for your own convenience.

## What is an Extension file?

Like a jar, a Meowtils extension is an archive of compiled java class files. This is the same thing a regular Forge mod would be, except with a different file extension (.meowtils not .jar) and content requirements.

### Decompiling

You can use any java decompiler to decompile an Extension to verify what the code is, and exactly what it is doing.

There are many programs that can be used for decompiling, but also some online websites. [This is an example of an online decompiler](https://www.javadecompilers.com/) which doesn't require any downloads at all.

!!! Tip

    Some decompilers may only allow files with the .jar file extension, in that case you can temporarily rename it from **Extension.meowtils** to **Extension.jar** and it should work. This will not corrupt the file.