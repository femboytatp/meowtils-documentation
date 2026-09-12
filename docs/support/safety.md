# **File Safety**

!!! Warning

    The only official places to download **Meowtils** is:   
    - [meowtils.dev](https://meowtils.dev/)   
    - [github.com/femboytatp/meowtils](https://github.com/femboytatp/meowtils)   
    - [tatp.wtf](https://tatp.wtf/)

Like everything else, you should always be careful when running unknown files. In certain cases they may perform malicious actions. The file type **Meowtils** is commonly shipped as (_.jar_, also known as a java archive) can be malicious, especially when you launch it as a mod which will automatically grant it the same permissions as **Minecraft has itself**. This is why it is very important you should only download it from a trusted source.

## Obfuscation

**Many mods & clients are obfuscated**, while this is usually a protective measure for auth & protecting their own code from being re-used/copied, it also means the real functionality of the code is being hidden and it may perform harmful actions - without your knowledge. This is not a warning sign in itself, especially if the service you use is paid, however it is something to note and you should never run anything you don't trust completely.

### Meowtils

**Meowtils** code itself is not obfuscated in any way, however it is compiled with vanilla obfuscation (also known as "notch" obfuscation), applying to Minecraft **class**, **field** and **method** names. All of these & what they do exactly can be checked by you, the **Meowtils.jar** even contains a '.csv' file with all of the mappings.

## Meowtils Injectable

!!! Info

    This is not yet released.

We provide an **.exe** file for full runtime-injection. Internally this does nothing different from the regular **Meowtils.jar** other than a few smaller launch differences, mainly attaching to the JVM at runtime and transforming classes again. Due to how it behaves, it might be flagged by anti-virus programs, without actually being harmful.

## Exclude in Anti-Virus

You may be required to add an exclusion for **Meowtils** specifically, especially if you want to use the **.exe** version of it.

### Windows Defender
1. Open Windows Security

2. Go to Virus & threat protection

3. Click Manage settings under "Virus & threat protection settings"

4. Scroll down and click **Add or remove exclusions**

5. Click **Add an exclusion > File**

6. Navigate to your Downloads folder and select the **Meowtils** exe.

## Other Anti-Virus programs:

[Exclude in Norton](https://support.norton.com/sp/en/us/home/current/solutions/v3672136)

[Exclude in McAfee](https://www.mcafee.com/support/?page=shell&shell=article-view&articleId=TS102056)

[Exclude in Avast](https://support.avast.com/en-us/article/antivirus-scan-exclusions/)

[Exclude in AVG](https://support.avg.com/SupportArticleView?l=en&urlName=avg-antivirus-scan-exclusions)

[Exclude in Bitdefender](https://www.bitdefender.com/consumer/support/answer/13427/)

[Exclude in Kaspersky](https://support.kaspersky.com/common/windows/12978)

[Exclude in ESET](https://support.eset.com/en/kb2903-exclude-files-or-folders-from-scanning-in-eset-windows-home-products)

[Exclude in Malwarebytes](https://support.malwarebytes.com/hc/en-us/articles/360038479234-Add-exclusions-in-Malwarebytes-for-Windows)