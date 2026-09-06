# **File Safety**

!!! Info

    The only official places to download **Meowtils** is:
    - [meowtils.dev](https://meowtils.dev/)
    - [github.com/femboytatp/meowtils](https://github.com/femboytatp/meowtils)
    - [tatp.wtf](https://tatp.wtf/)

Like everything else, you should always be careful when running unknown files. In certain cases they may perform malicious actions. The file type **Meowtils** is shipped as (_.jar_, also known as a java archive) can be malicious, especially when you launch it as a mod which will automatically grant it the same permissions as **Minecraft does itself, which is a LOT**. This is why it is very important you should only ever download it from a trusted source.

## Obfuscation

**Many mods & clients are obfuscated**, while this is usually a protective measure for auth & protecting their own code from being re-used/copied, it also means the real functionality of the code is being hidden and it may perform harmful actions - without your knowledge. This is not a warning sign in itself, especially if the service you use is paid, however it is something to note and you should never run anything you don't trust completely.

### Meowtils

**Meowtils** code itself is not obfuscated in any way, however it is compiled with vanilla obfuscation (also known as "notch" obfuscation), applying to classes & fields &  method names. All of these can be remapped manually by you, the **Meowtils.jar** even contains a '.csv' file with all of the mappings.

## Meowtils Injectable

We provide an **.exe** file for full runtime-injection. Internally this does nothing different from the regular **Meowtils.jar** other than a few smaller launch differences, mainly attaching to the JVM at runtime and transforming classes again. Due to how it behaves, it might be flagged by anti-virus programs.

## Exclude in Anti-Virus

### Windows Defender
1. Open Windows Security

2. Go to Virus & threat protection

3. Click Manage settings under "Virus & threat protection settings"

4. Scroll down and click **Add or remove exclusions**

5. Click **Add an exclusion > File**

6. Navigate to your Downloads folder and select the **Meowtils** exe.