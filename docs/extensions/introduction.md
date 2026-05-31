# **Extensions**

---

An Extension is an external file that is loaded by Meowtils, it acts as a bridge that allows you to add features. They could be compared to scripts, except with less limitations.

These will show up in a new category called **Extensions**.

!!! Danger

    Extensions have very few limitations, they have the same permissions as Minecraft does. This means they may contain unwanted or malicious code.
    
    Only download Extensions from trusted sources.

!!! Tip

    It is not required to have previous Minecraft modding experience in order to develop Extensions; However it is heavily recommended as it is very similar to this, and these docs make the assumption that you have at least **some** knowledge.

## Usage

To use an Extension, simply put it in the **extensions** folder located in the **meowtils** folder in your game directory. You can also open this folder ingame by doing `/extensions`.

!!! Note

    Extensions end with .meowtils

### Loading

Extensions that already exist in your folder are automatically loaded when launching your game. 

You can also add, remove, or swap Extensions during runtime and then do `/reload` to load them.
