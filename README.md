# Political Engine

Political correspondence, diplomacy and an experimental strategy campaign for
**Skyrim Special Edition + SkyrimNet**.

## (not very)Quick guide

**Letters**
- You can place an unlimited number of postal stations by choosing from all available station types (the owl option is recommended).
- You can configure the interval and chance of receiving letters, as well as choose the delivery method (courier or postal station). You can also completely replace the courier. This way, even vanilla letters that would normally be delivered by the courier will appear at the postal station.
- You can interact with the owl to write and send a letter to someone.

**Politics**
- For the best experience, installing the “[LC-Build](https://www.nexusmods.com/skyrimspecialedition/mods/18308)” mod is recommended. However, the plugin also supports assigning a custom faction or taking control of a vanilla one. Both can be done through MCM or PrismaUI.
- Starting with version 0.6.5, it is possible to gain control over a vanilla hold through dialogue (not letters).
- Other jarls may not recognize your rights of ownership. Your claims derive from world knowledge.
  
**Interactive Map**
_(well, you decided to become a Jarl)_
- You can move and hire troops.
- You have different relationship levels with other Jarls. This directly depends on memories and world knowledge.
- Each region generates income in the form of gold and resources. You can improve these values by constructing new buildings in the region.
- You can also establish various trade agreements with other Jarls. Successful trade improves relations.
  
**Battles**
- If you find yourself at war with another hold, you can always stop the war if you manage to negotiate a truce.
- Battles mostly take place in the field, but mod always uses a "City" battle as the final battle.
- You can assign equipment to your fighters by equipping a follower with the desired set and then hovering the crosshair over them. Then, in the settings under the "Combats" tab, you can find the option to copy the loadout of the character currently in your crosshair.


## Features

- SkyrimNet-driven political letters, player replies and ruler relationships.
- Postal stations, shared mail storage and optional vanilla courier replacement.
- PrismaUI settings, interactive campaign map and troop commands.
- Regional armies, treasury, resources, strategic buildings and NPC trade routes.
- Field battles and city engagements, with player-confirmed war declarations.
- Full NPC trading correspondence history, without physical NPC mail items.

This is an experimental campaign overlay, not a replacement for vanilla Civil
War ownership. Route lines are schematic; physical caravans are not implemented.

## Installation

Developed and built for Skyrim SE **1.6.1170** (VR supported) and SkyrimNet **Beta25** or later.
Use the matching SKSE and required dependency versions. The UI requires SkyUI,
MCM Helper and PrismaUI. Address Library is used by the native plugin. PapyrusUtil
provides the StringUtil functions used by scripts. SeverActions integration and
Fellburg are optional. GLENMORIL is not a runtime dependency of the packaged owl.
Other runtime versions and mod combinations require separate testing.

Install the base ZIP with your mod manager, then the matching Russian patch if
desired. Enable `PoliticalLetters.esp` and restart Skyrim. Letter language remains
prompt-controlled and independent of the UI language.

See [English instructions](docs/INSTALL.txt) or [Русская инструкция](docs/INSTALL-RUSSIAN.txt).

## Credits and distribution

Postal owl resources: **Vicn / GLENMORIL**. Topographic map: **T Cook**,
*Skyrim topographic map*, Nexus #36159. Skyrim resources: **Bethesda**.
See [credits and resource conditions](CREDITS.md).

Public downloads do not grant an open-source licence or unrestricted permission
to redistribute third-party assets. Source code is not published in this repository.

## Reporting issues

Include game, SKSE, SkyrimNet, PrismaUI and mod versions; reproduction steps;
whether the issue occurs on a separate test save; and relevant sanitized log
excerpts. Remove credentials, private conversations and personal information.
The plugin log retains its legacy filename `PoliticalLetters.log`.
