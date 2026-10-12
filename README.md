# Political Engine

Political correspondence, diplomacy and an experimental strategy campaign for
**Skyrim Special Edition + SkyrimNet**.

This repository contains public release documentation only. The implementation
source is maintained separately in a private repository. Download the mod from
this repository's **Releases** section, not GitHub's automatic source-code ZIP.

## Current release: 0.6.3

Upload these two assets to the release tagged `v0.6.3`:

- `PoliticalEngine-v0.6.3-beta25.zip` — complete base installation, English UI.
- `PoliticalEngine-v0.6.3-Russian-patch.zip` — Russian UI override; install after
  the base. The product name remains **Political Engine** in both languages.

The archives are staged locally in `release-assets/v0.6.3/`. That directory is
ignored by Git: attach the ZIPs to a release instead of committing them as files.

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

Developed and built against Skyrim SE **1.6.1170** and SkyrimNet **Beta25**.
Use the matching SKSE and required dependency versions. The UI requires SkyUI,
MCM Helper and PrismaUI. Address Library is used by the native plugin. PapyrusUtil
provides the StringUtil functions used by scripts. SeverActions integration and
Fellburg are optional. GLENMORIL is not a runtime dependency of the packaged owl.
Other runtime versions and mod combinations require separate testing.

Install the base ZIP with your mod manager, then the matching Russian patch if
desired. Enable `PoliticalLetters.esp` and restart Skyrim. Letter language remains
prompt-controlled and independent of the UI language.

See [English instructions](docs/INSTALL.txt) or [Русская инструкция](docs/INSTALL-RUSSIAN.txt).

## Updating from Political Letters

Version 0.6.3 is the continuation of the latest Political Letters v2.41.
Legacy technical names, including `PoliticalLetters.esp`, DLL, scripts, settings
and serialization keys, deliberately remain unchanged for save compatibility.

Replace existing files without making an intermediate save. Do not rename the
ESP or change its load-order position, clean the save, or enable duplicate copies.
Back up both `.ess` and its matching `.skse` co-save and test the update on a copy.
Offline checks passed; they do not guarantee compatibility with every save/mod.

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
