# **Stats**

#### Display game stats for players.

---

## API

### Hypixel

Uses the Hypixel API for fetching stats. Requires an API key.

An API key can be obtained by going to their [Developer Dashboard](https://developer.hypixel.net/)

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

Prints stats for all players in chat, this requires you to use AutoWho or run /who manually.

## Chat options

### Auto-check certain players

This automatically fetches stats and prints them in chat for some players, for example if they mention you or if they were denicked.

### Use team colors

Colors the names for chat stats based on the team they're on, rather than their rank.

## Urchin

### Check Urchin API

Will check if a player is in the Urchin blacklist. Does not require an API key.

### Ignore self

Ignore checking & rendering Urchin icon for yourself.

## Bedwars

Customize Bedwars stats.

## Skywars

Customize Skywars stats.