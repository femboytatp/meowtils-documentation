---
tags:
  - Legit
---

# **SniperWarning**

#### Warns you of certain players that may be snipers.

---

## Ping sound

Plays a sound for warnings.

## Check gear

Checks gear for snipers.

**Applies to:**

- Chainmail Armor + Iron Sword

## Check name

Checks if a player has a blacklisted name, and if so warn them for being a potential sniper.

**Applies to:**

``` title="Sniper names"
mcalt_,
mcalts_,
hassalt_,
dogalt_,
mal_,
bym_,
jy6_,
lf_,
wg_,
ggnekito,
dahai_,
tzi,
nicegen,
opalalts,
msmc,
myau,
vape,
snipe,
nicealts,
rave,
alt,
client,
hack,
hax,
fernan,
watchdog,
anticheat
```

!!! Bug

    This may not be 100% accurate, it only checks if a name contains typical phrases that indicate a cheater or sniper.

## Check stats

This checks stats of players to detect potentially suspicious accounts. First it checks their clutch ratio, then it checks their balance between final kills and final-kill-death ratio.

A low final kill count while also having a high FKDR may indicate a suspicious account.

!!! Failure

    This requires you to have the Stats module enabled.