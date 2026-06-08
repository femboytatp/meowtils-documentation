# Sending Messages

---

## Chat messages

### **Client**

These messages only appear clientside, for yourself.

---

#### Message with prefix

``` java
addMessage(String message)
```

Prints a message with the Meowtils prefix.

---

#### Message without prefix

``` java
addCleanMessage(String message)
```

Prints a message without the Meowtils prefix.

---

#### Debug message

``` java
debugMessage(String message)
```

Prints a message if debug mode is enabled.

!!! Note

    Debug mode is toggled with the `/meowdebug` command.

---

### **Server**

These messages are sent to the server, same as if you were to type a message in chat and send it.

---

#### Message with prefix

``` java
sendMessage(String message)
```

This sends a message to the server with the prefix `Meow »`.

!!! Note

    This only sends messages to party chat, configured for **Hypixel**. This means it may not work on all servers and should generally be avoided unless this is your intention.

---

#### Message without prefix

``` java
sendCleanMessage(String message)
```

Sends specified message to the server.

---

## Log messages

These are log messages that will not appear in chat, but in your log.

!!! Tip

    You should always log important things, which will help with debugging.

---

#### Info

``` java
info(String msg)
```

!!! Info

    Info log messages should be used for general things, for example to log actions such as what player you fetched stats for.

---

#### Warn

``` java
warn(String msg)
```

!!! Info

    Warn log messages should be used for important things, or potential issues.

---

#### Error

``` java
error(String msg)
```

!!! Info

    Error log messages should be used for things that fail, but aren't potentially game-breaking.

---

#### Fatal

``` java
fatal(String msg)
```

!!! Info

    Fatal log messages should be reserved for game-breaking issues that are fatal to your Extension, or even the whole game.

---