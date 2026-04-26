# NickBot

#### Rerolls nicks for you until a good one is found.

!!! Note

    To stop the NickBot simply press ESC.

---

## Delay

Time to wait until rerolling a nick.

!!! Tip

    It is recommended that you optimize delay with the ignore limbo kick option, to make it as efficient as possible without losing too much time to limbo kicks.

## Start

Starts the NickBot when clicked.

## Auto accept good

Will automatically accept the nick if you get a good one, otherwise it will just leave the book open for you to manually accept it.

## Ignore limbo kick

If you get kicked to limbo (usually due to spam) this will automatically go back to lobby, and continue rolling nicks.

## Legacy nicks

Searches for legacy nicks, these are extremely rare.

## Four char

Searches for 4 character nicks.

## Max char

Searches for nicks that have the maximum amount of allowed characters (16).

## Plain text

Searches for nicks that only contain text, ignores underscores.

## Custom words

Uses your custom word list.

## Commands

**/nickbot** - Shows all NickBot commands.

**/nickbot start** - Starts the NickBot.

**/nickbot add** - Add word to the list.

**/nickbot remove** - Remove word from the list.

**/nickbot list** - Show all words currently in the list.

### List syntax:

?meow - _If the nick contains meow._

=meow - _If the nick equals meow._

<meow - _If the nick starts with meow._

\>meow - _If the nick ends with meow._

!!! Example

    /nickbot add ?Ninja will check if a nick contains the word ninja, and if so flag it as a good nick.
