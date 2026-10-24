# Political Engine

Political correspondence, diplomacy and an experimental strategy campaign for
**Skyrim Special Edition + SkyrimNet**.

## (not very)Quick guide (updated, thanks to Whyregister)

  Political Engine  adds a turn-based strategy layer on top of Skyrim: holds are realms, each realm is split into districts, and you play one realm (your "Fellburg") against the others. The real world keeps going — battles are fought in real time, and rulers write you letters through SkyrimNet.

**The core loop:**

  1. Turn starts. Your 8 turn points refill and treasury income lands.
  2. Spend points. Move troops, recruit, build, send scouts.
  3. Turn ends — when you press End/skip, spend all 8 points, or the deadline hits. NPC realms then take their turn (build, trade, recruit, move).
  4. Battles that your moves started are offered as real-time fights you travel to, or resolved by auto-battle.
  5. Letters and delegations run alongside: diplomacy, trade deals, war declarations and peace offers.

  It never changes vanilla ownership, Civil War quests or the real jarls — it is a political layer on top. Settings live in MCM → Political Letters; the map and management panel open from MCM (General → Open PrismaUI control panel) or your hotkey, Numpad − (key 74).

**Reading the map**
  The map shows approximate borders — not vanilla quest boundaries. Each hold has a stronghold (the city) plus field districts such as Solitude Coast, Sea of Ghosts Coast or Heljarchen Plains.

**Mouse action**
  What it does
    Click a district - Select it; the side panel shows its details
    Double-click your district - Start a troop move from it
    Right-click a district - Open its menu (patched on this install so it works on field districts, not just strongholds)
    Drag - Pan the map

  Each district badge lists the troops in it, one row per realm, in that realm's color; a city shows a garrison total. ?? means fog of war is hiding the count (fog is off by default).
The side panel has six tabs for the selected district: Overview, Economy, Buildings, Diplomacy, Army (recruit) and Positions (appointments). MCM → General → Map display toggles labels, city names, trade routes, delegations and opacity.

**Turns and turn points**

  You get 8 turn points per turn, and they refill only on the timer — every 24 game hours by default. End/skip turn does not refill them; it just lets the enemy act sooner.
  • Your turn ends when you press End/skip, spend all 8 points, or reach the deadline. After that the map says "Waiting for daily refresh" and nothing can move until the next refill.
  • Battles delay enemy responses, not your refill.
  • Waiting (the vanilla wait/sleep menu) is the fastest way to reach the next refill.
  
## **Action**

**Point cost**
  Move troops -1 per 8 soldiers, max 8
  Move the whole group (leave nobody behind) - All 8
  Recruit - 1 per 8 soldiers, plus 100 treasury gold each
  Build or upgrade - 2
  Scouts - Their own, smaller cost
  
  The interval is MCM → War Campaigns → Strategic turn interval. Lowering it speeds the campaign up.
    
**Moving and reinforcing troops**
  Troops move one adjacent district per order. To reinforce somewhere farther away, hop through each district in between, one order per hop.
  1. Double-click a district holding your troops. It becomes the source and its neighbors highlight.
  2. Click a highlighted neighbor. The move dialog opens.
  3. Pick the troop group and count. The dialog shows the point cost.
  4. Press Move troops. Cancel movement backs out.
  5. 
   The Move troops button on the district panel does the same thing.

**Rules that silently cap or block a move:**
  • One soldier stays behind unless you have all 8 points, which moves the entire group and spends all 8.
  • No moves while a battle is pending, the enemy turn is queued, or after your turn has ended.
  • Passage: a neutral ruler with negative relations charges 2 treasury gold per soldier entering. At −50 or below, passage is refused. Your own land and enemy land are free.
  • Enemy cities can't be entered while that enemy still holds field districts. Take the countryside first.
  • Scouts move separately and reveal only the district they are in (this matters with fog of war on).
  
If a move fails, the bar at the bottom of the map says why: Not enough turn points, Pending battle, Enemy turn pending or Waiting for daily refresh.
Battles

Moving into an enemy-held district starts a battle. You can fight it in real time or let auto-battle resolve it.

**Real-time field battle:**
  1. The game finds open, navmeshed ground in that district and says "Field battle prepared in … Approach your army's marked staging area to begin." You get a journal objective.
  2. Walk or ride to the marker. Combat starts when you arrive.
  3. Soldiers arrive in waves: at most 8 per side are on the field at once, and replacements keep coming until a side's committed troops run out. A lull is not the end. Wait for the result message.
  4. You get a casualty report, for example "victory for Moonstone Castle … lost 6; Dawnstar lost 139". With war history on, the opponent's commander gets a memory of it.
  5. Auto-battle simulates the fight from abstract army levels (both 20 by default), not real NPC gear.

  Campaign pacing: an engagement is offered every 6 game hours and can be deferred. The first three engagements are field battles; after that, results and reserves decide whether it becomes a siege. Bodies are capped at 30 (oldest removed first, never while you're looting).

**Tips:**
  • Press F3 before a battle to turn off SkyrimNet's GameMaster. Otherwise it starts side conversations between soldiers mid-fight.
  • Say one battle line to your allies first, such as "Hold the line, more are coming." Their dialogue otherwise picks up from your last line before the battle.
  • Troop commands (follow, hold, attack, retreat, plus a hold-Mouse4 command wheel) are off by default. Turn them on under MCM → Troop Commands.
  • After a lost field battle, the loser's other districts in that hold may drop to 0. In your Dawnstar battle, Dawnstar lost 139 of the roughly 150 soldiers it fielded, which looks like the hold's whole army. Undefended districts are cheap to take next turn.
  
**Economy, recruiting and buildings**

Each district earns about 100 treasury gold a day, scaled by prosperity, and produces abstract resources: grain, timber, ore, fish, crafts, alchemy. Confirmed trade routes move goods and gold daily, and war suspends them. None of this is real inventory.

**Recruiting (side panel → Army):** select one of your districts, pick a count, and pay 100 treasury gold per soldier plus 1 point per 8. Soldiers exist as numbers and only spawn during battles. Archers need an Archery Range in that district, and mages need a Battlemage Tower. Every side also regains 6 troops per game day on its own.

**Building (side panel → Buildings):** each build or upgrade costs 2 points plus gold and resources. Buildings have 3 levels and pass to whoever captures the district. No world models appear.

**Building**
  **Effect per level**
    **Marketplace**
      Income +25%
    **Farm**
      Grain +6/day
    **Sawmill**
      Timber +6/day
    **Mine**
      Ore +4/day
    **Fish ponds**
      Fish +5/day
    **Workshop**
      Crafts +3/day
    **Alchemy garden**
      Alchemy +2/day
    **Fortifications**
      Defense +15%
    **Barracks**
      Recruit price −10%
    **Armory**
      Dwarven / Orcish / Ebony melee weapons
    **Archery Range**
      Recruit archers; better bows and arrows
    **Battlemage Tower**
      Recruit mages; better mana, perks and spells
      
  Ordering a ruler to build (by letter or conversation): use the exact names above. "Fishery" fails where "Fish ponds" works, because the name is checked exactly. NPC realms build at most once every third strategic turn, using their own treasury.

**Letters, diplomacy and positions**

Rulers write to you through SkyrimNet. On a set interval of game hours, the AI decides whether anyone should write, so an interval passing doesn't guarantee a letter. 
Each sender then waits about 2 game days before writing again unprompted, though that pause is lifted while you are actively corresponding with them.
  • Delivery: the vanilla courier by default. Alternatively, place a postal station (mailbox, dovecote or owl post) from MCM → Delivery; every station shares the same mail.
  • Replying: your reply goes out as outgoing mail, and the ruler answers on the next decision check. The panel keeps the last 10 exchanges per ruler.
  • Relations: each ruler gets a score built from SkyrimNet memories, dialogue and letters. It sets the tone of their letters, plus passage tolls and refusals (see Moving troops).
  • War: declare war with the outgoing-mail checkbox. An NPC's declaration only becomes eligible once you've read their letter, and you confirm before a campaign starts.
  • Peace: after 3 straight defeats, the losing side may offer peace on its turn. You must accept for the war to end.
  • Trade: a deal must be signed by a steward, governor or ruler. NPC realms also trade among themselves.
  • Delegations: outgoing, incoming or a wartime neutral meeting. Discuss terms with the envoy, then finish the meeting in the panel.
  • Positions tab: appoint NPCs (steward, governor, commander, housecarl and so on). This is a political position only; their vanilla AI and quests stay the same.
  
To add someone as a letter writer: aim at them, open MCM → General → Add targeted NPC. Jarls are included automatically. Test targeted NPC forces a letter right away.

**Troubleshooting**

  **Can't move or recruit** - Out of points, turn already ended, or a battle is pending. Read the bottom bar; wait for the 24-hour refresh
  **Build order "failed"** - Wrong building name (use the exact list), not enough gold/resources, or under 2 points
  **Move capped one short** - Points below 8 keep 1 soldier behind
  **Battle never starts** - Go to the staging marker; the site needs open, navmeshed ground
  **NPCs cheer "that's the last of them" too early** - Battles come in waves; wait for the result message
  **Right-click does nothing on field districts** - The map patch was reverted, usually by a mod update or reinstall. Re-apply it
  **Allies argue mid-battle** - SkyrimNet GameMaster; press F3 to toggle it

**Logs:** Political Engine writes to Documents\My Games\Skyrim.INI\SKSE\, not the normal Skyrim Special Edition folder:
  • PoliticalLetters.log: turns, NPC moves, construction, battle results. If the issue relates to a core mechanic (script) or a crash, you may also need to provide the Papyrus0.log file and a crash log, if one exists.

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
