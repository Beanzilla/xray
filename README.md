# Xray

See thru stone and other materials.

## What's in the box

- API for adding nodes to see thru
- Redesigned internals from my xray in [oretracker](https://content.minetest.net/packages/ApolloX/oretracker/)
- Adds a formspec for adding/removing nodes so you can individually customize it
- Toggled by `/xray` chat command. (this means oretracker will disable it's xray mod in place of this one, since it will be more advanced and ultimatly better)

## How the new mod works

> How the old mod works... (Just to show what's the major difference)

This mod will build a "blank node" for each node you wish to make invisible (each blank will have it's own "id" which is used to keep drops and such the exact same) it will support making new "blank node"'s while in-game.

> I manually made a "blank node" for each node (where each node had it's own xray equal, but I manually defined it)

This mod then scans within a designated area for the nodes you wish for it to make invisible (swaping any with their "blank" counterparts)

> The old mod then scans within a designated area for the nodes I've defined (swaping any with their "blank" defined counterparts)

**Note this mod automatically creates the needed "blank node" without needing ME to define it first (thus more efficient and customizable)**

## Mods/Games supported

- MTG
- MCL (so long as they match the simular MCL2 format they should work)
- NC

> Oh, and any mod/game... (since you can customize it, you can add nodes while in-game, even supports adding node based on what you're looking at)

## Settings

All settings will be located in `minetest.conf` after first run (then you can edit and save those settings from there and restart if needed to enjoy)

- xray.interval_rate (how fast does the mod update, recommended 1.0 for once per second)
- xray.display_range (how far do nodes need to be to count as being affected, recommended is 8 for 8 nodes around the player)
- xray.extended_interval_rate (applied to those of "elite" status, typically you'd set this to say half the value of xray.interval_rate, 0.5 by default)
- xray.extended_display_range (applied to those of "elete" status, typically set to 1.5 times (150%) the value of xray.display_range, 12 by default)

> All values have a minimum of 0 or 0.0 (can't be negative)

## Privledges

Something new added to this mod is an `xray_extended` priv, this priv is by default only given to `server` or singleplayers.

It by default provides a more improved field of viewing nodes (display_range) and updates twice as fast (interval_rate).

> Of course you could change these, since it's in the settings. (not sure why you'd punish "elite" players like admin or staff, but you could)
