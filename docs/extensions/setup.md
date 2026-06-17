# **Setup**

**Extensions** are very similar to a typical Forge mod, you can easily convert a Forge project to build a **Meowtils** extension however a simple example project will be provided below.

!!! Note

    If you need help, ask [**HERE**](../support/request-help.md).

---

### 1: Download project

[Download the **ExampleExtension**](https://github.com/femboytatp/meowtils-documentation/releases/download/ExampleExtension/ExampleExtension.zip).

### 2: Extract the project

Your operating system likely has a tool to extract .zip files already, if not you will have to download one.

[7-Zip](https://www.7-zip.org/)

### 3: Open the project

[IntelliJ IDEA](https://www.jetbrains.com/idea/) is the recommended program to use. You can follow any Forge modding guide if you want to use something else.

### 4: Add Meowtils as a library

1. [Download Meowtils](https://tatp.wtf/download/).

2. Add the Meowtils.jar to the **libs** folder at root in your project.

3. Rename the jar to match what you have defined in the **build.gradle**, by default this will be `meowtils.jar`.

!!! Tip

    If using [IntelliJ IDEA](https://www.jetbrains.com/idea/) you will be able to view the decompiled Meowtils.jar in your sidebar, this can be used as a reference.