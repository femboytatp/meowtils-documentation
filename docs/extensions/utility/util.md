# **Click Utility**

---

## Left Click

``` java
Util.leftClick()
```

Safely left clicks, uses the Minecraft bind for attack key.

## Right Click

``` java
Util.rightClick()
```

Safely right clicks, uses the Minecraft bind for use key.

## Open Folder

``` java
Util.openFolder(File dir, String id)
```

Will open the selected folder if supported.

`File` - The path.

`id` - Name used for notifications.

## Format Timestamp

``` java
Util.formatTimestamp(long ms)
```

Uses unix timestamp, returns a string with the formatted time.

**Format:** `yyyy-MM-dd HH:mm`

## Format Time

``` java
Util.formatTime(int seconds)
```

Returns a string with seconds & minutes formatted, including `s` & `m` as suffix.

## Loaded Class

``` java
Util.isClassLoaded(String path)
```

Checks if a java class is loaded, this is useful if you need to detect another mod for example.

## Parse Int

``` java
Util.parseIntFromString(String string, int start)
```

Parses ints from a string by checking everything after your starting point, breaks at the end of the value.

!!! Example

    If the string we want to parse a value from is `Kills: 9` we would put the start at `7`.

## Play Sound

``` java
Util.playSound(Util.Sound sound, int volume)
```

There are a few pre-defined sounds you can use for convenience.

    PING
    PING_DEEP
    PING_MEDIUM
    LEVEL
    ANVIL
    MEOW
    ANVIL_BREAK
    ERROR
    ERROR_DEEP
    CRIT