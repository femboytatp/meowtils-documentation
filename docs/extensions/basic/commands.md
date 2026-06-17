# **Commands**

---

## Extends

``` java
import wtf.tatp.meowtils.handler.command.ClientCommand;
```

### Overrides

``` java
getName()
```

String, should return your command name.

``` java
process(String[] args)
```

This method is called each time the command is ran, args would be the additional command arguments provided.

``` java
getAliases()
```

Array of command aliases, this lets you assign several aliases to the parent command.

If not overriden it will be left empty.

``` java
tabCompleteNames()
```

Boolean, lets you tab-complete player names in your world if it returns true.

If not overriden it will be false.

## Registering

You will need to register your commands on init.

!!! Example

    ``` java
     CommandHandler.register(new ExampleCommand());
    ```

## Example

``` java
public class ExampleCommand extends ClientCommand {

    @Override
    public String getName() {
        return ("examplecommand");
    }

    @Override
    public void process(String[] args) throws CommandException {
        Meowtils.addMessage("Command ran!");
    }

    // Optional; Don't override if you won't use this
    @Override
    public List<String> getAliases() {
        return Arrays.asList("examplecommand2", "examplecommand3");
    }

    // Optional; Don't override this if you don't need it
    @Override
    public boolean tabCompleteNames() {
        return true;
    }
}
```