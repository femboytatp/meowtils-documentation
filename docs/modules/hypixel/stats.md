---
tags:
  - Legit
---

# **Stats**

#### Display game stats for players.

---

## API

### Hypixel

Uses the Hypixel API for fetching stats. Requires an API key.

An API key can be obtained by going to their [Developer Dashboard](https://developer.hypixel.net/).

### Abyss

Uses the [Abyss Overlay](https://github.com/Chit132/abyss-overlay) API for fetching stats, does not require any API key.

!!! Warning

    We simply provide the alternative for you to use this, but they likely do not intend for their API to be used this way, and if abused they might IP ban you.

    As long as it is used normally (loading stats ingame) you shouldn't run into any issues as this is what their overlay already does.



## Clear cache

To prevent rate limits, stats are cached. This allows you to clear that cache but it is not recommended to do so unless you run into issues with old invalid stats.

## Cache duration

Lets you set how many minutes stats will be cached for.

## Fetch cooldown

This is the delay between requests, a higher delay may prevent issues with rate limits but it would also mean it will take more time until all stats have loaded.

## Display mode

**Modes:** _Full, Compact, Lowercase_

Changes how stats look in tab.

## Display

### Tablist

Will show stats in tab.

### Nametags

Will show limited stats in player nametags, similar to how levelhead would work in other mods.

### Chat

Shows stats for all players in chat, this requires you to use AutoWho or run /who manually.

## Chat options

### Auto-check certain players

This automatically fetches stats and sends them in chat for some players, for example if they mention you or if they were denicked.

### Use team colors

Colors the names for chat stats based on the team they're on, rather than their rank.

## Urchin

!!! Info

    In order to use the Urchin API you need your own API key.

    **How to obtain an API key:**

    1. Join [Urchin Discord](https://discord.gg/urchin)

    2. Verify with your username, this assumes you have linked your discord to your username on Hypixel.

    3. Run /info then /dashboard to generate your API key with their discord bot.

### Check Urchin API

Will check if a player is in the Urchin blacklist. Does not require an API key.

### Ignore self

Ignore checking & rendering Urchin icon for yourself.

### Show name icons

Will show Urchin icons in nametag & tablist for players that are in the Urchin blacklist.

### Show in chat

Will send a message in chat if a player is blacklisted on Urchin, requires AutoWho or manually running /who.

This only applies to games that support the /who command.

### API key

Your Urchin API key.

## Bedwars

### Enabled

If bedwars stats should show for players.

### Level

Their bedwars level (star).

### Final kills

The amount of final kills they have.

### FKDR

The final-kill-death ratio of a player.  
_Calculation: final kills / final deaths._

### WLR

The win-loss ratio of a player.  
_Calculation: wins / losses._

### Winstreak

The winstreak they have.

!!! Info

    This will only be displayed for players that actually have a winstreak visible, as players are able to hide winstreaks from the API. This might not show up for everyone.

### Clutch ratio

The clutch ratio of a player.  
_Calculation: 1 - final deaths / beds lost._

## Skywars

### Enabled

If skywars stats should show for players.

### Level

Their skywars level (star).

### Kills

The amount of kills they have.

### Wins

The amount of wins they have.

### KDR

The kill-death ratio of a player.  
_Calculation: kills / deaths._

### WLR

The win-loss ratio of a player.  
_Calculation: wins / losses._