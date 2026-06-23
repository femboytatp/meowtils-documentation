# **Auto Updates**

**Meowtils** will automatically update to the latest version available, if you aren't already on latest. This is convenient and requires no input from your part.

**If you want to disable auto-updates you can do so [HERE](../modules/meowtils/settings.md).**

!!! Tip

    It is recommended that you keep these enabled, or that you manually update each new version that is available. Outdated versions may contain fatal bugs, instability issues, performance issues, and outdated features.

## How do they work?

Each time you join a world for the first time the update checker will run, this contacts the GitHub API to check the latest version available from the [Meowtils Repo](https://github.com/femboytatp/meowtils).

### When enabled:

If your current version is older, it will download the new jar. When you close your game the old jar will get replaced by the new one, to apply the new update next time you launch.

This also downloads the [MeowtilsAutoUpdate.jar](https://github.com/femboytatp/meowtils-auto-update), which is what applies the update after your game closes. This will only be downloaded if you are missing it, not each update.

### When disabled:

This will just alert you in chat if you use an outdated version, and provide a link if you want to go download it manually.

!!! Note

    This requires you to properly replace the jar, which if using Lunar Client also requires you to rename it.
