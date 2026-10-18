# PAYDAY 2 Mod Pack

My PAYDAY 2 mods folder, packaged so it can be dropped into a fresh install. It covers HUD and lobby information, quality-of-life fixes, and a few mods I wrote myself.

Runs on SuperBLT (64-bit). Last updated October 2026.

## Contents

| Path in `mod_pack.zip` | What it is |
|---|---|
| `WSOCK32.dll` | SuperBLT hook DLL. Goes in the game folder, next to `payday2_win64_release.exe`. |
| `mods/` | 30 mod folders plus `mods/saves/` (my settings for the mods below). Goes in the game folder. |

## Installation

1. Back up your current `mods` folder and `WSOCK32.dll` if you have them.
2. Download `mod_pack.zip` and extract it.
3. Copy `WSOCK32.dll` and the `mods` folder into the PAYDAY 2 install folder, usually `C:\Program Files (x86)\Steam\steamapps\common\PAYDAY 2`.
4. Launch the game. SuperBLT may ask to update itself on first start; accept it.
5. Set the keybinds under **Options > Mod Keybinds**. They are not part of the pack (see [Keybinds](#keybinds)).

Settings for VanillaHUD Plus, Void UI Scoreboard, Lobby Player Info, BerserkerQOL, AnimSkins Tuner and a few others come preconfigured from `mods/saves/`. Delete a mod's save file to reset that mod to its defaults.

## Mods

### Framework and libraries

| Mod | Folder | Author | Description |
|---|---|---|---|
| [SuperBLT](https://superblt.znix.xyz/) | `base` | Hoppip, ZNix | Lua hook loader that every other mod depends on. Works together with `WSOCK32.dll`. |
| [BeardLib](https://modworkshop.net/mod/14924) | `BeardLib` | Simon W, Luffy | Library for custom assets and menus. Required by AnimSkins. |
| [Simple Mod Updater](https://pd2mods.z77.fr/simple_mod_updater.html) | `Simple Mod Updater` | TdlQ | Update checker for TdlQ's mods (Lobby Player Info, Drag and Drop Inventory). Since paydaymods.com shut down, they can only update through this. |

### My mods

Written or maintained by me. They are not on ModWorkshop; the source is on GitHub where linked.

| Mod | Folder | Description |
|---|---|---|
| [AnimSkins](https://github.com/JP-mercier/AnimSkins) | `AnimSkins` | Animated glowing weapon skins (Eldritch Rose, Crackle, Crystal, Interstellar, Inversion, Molton, Nebula, Nightwave, PaP Galaxy, Purple, Scribble, Shatter, Starfall, Inversion Universal). Shown on your own first-person weapons only; other players see nothing different. Skins made by Siuna. Requires BeardLib. |
| [AnimSkins Tuner](https://github.com/JP-mercier/AnimSkins) | `AnimSkins Tuner` | In-game controls for AnimSkins: skin per weapon slot, glow brightness, bloom, scroll speed and direction, and reactive glow (stealth ember, assault surge, weapon heat). Found under **Options > Mod Options > AnimSkins Tuner**. |
| [ECM Rush Announcer](https://github.com/JP-mercier/ecm-rush-announcer) | `ECM Rush Announcer` | During an ECM rush, announces in chat whose turn it is to place the next ECM (GREEN > BLUE > RED > YELLOW), with a warning before the current one runs out. Only players with ECM Specialist aced (pager jamming) are counted. Arm it with its keybind. |
| Lobby ECM Check | `Lobby ECM Check` | Shows in the lobby which players actually have ECM Specialist aced. Lobby Player Info's ECM icon only counts Shinobi points, which can reach 38 without the ace; this resolves the unclear cases from what was seen in earlier heists. Requires Lobby Player Info. |
| [Lobby Recreate](https://github.com/JP-mercier/payday2-lobby-recreate) | `Lobby Recreate` | Press the keybind in a broken lobby, as host or client. You leave, host a new lobby with the same contract and settings, and everyone from the old one is invited. |
| [Chat Translator](https://github.com/JP-mercier/PD2-Chat-Translator-by-powware-in-3.0) | `Chat Translator` | 64-bit update of [powware's Chat Translator](https://modworkshop.net/mod/29967). Click a chat message to translate it, and type in any language. Uses Google Translate. |

### HUD and interface

| Mod | Folder | Author | Description |
|---|---|---|---|
| [VanillaHUD Plus](https://modworkshop.net/mod/25629) | `VanillaHUD Plus` | Test1, Kamikaze94, BangL | Continuation of WolfHUD. Adds HUD information panels and menu/lobby quality-of-life changes while keeping the vanilla look. |
| [Void UI Scoreboard Standalone](https://modworkshop.net/mod/30948) | `Void UI Scoreboard Standalone` | Xeletron, Fanged Hex, VxWolf | The end-of-heist scoreboard from Void UI, without the rest of Void UI. |
| [Name Label Fading](https://modworkshop.net/mod/35185) | `Name Label Fading` | Luis_De | Fades player name labels when they are near the center of the screen, so they don't block your aim. |
| [Endscreen XP List](https://modworkshop.net/mod/42283) | `Endscreen XP List` | zReko | Keeps every XP bonus line visible on the end screen instead of replacing them one after another. |
| [XPNotifier](https://github.com/vilanz/xp-notifier) | `XpNotifier` | vilanz | Shows a notification with the XP gained when a heist ends, with optional total and base XP. |
| [Drag and Drop Inventory](https://pd2mods.z77.fr/drag_and_drop_inventory.html) | `Drag and Drop Inventory` | TdlQ | Rearrange masks and weapons in the inventory by dragging them. |
| [Peer mod list highlighter](https://modworkshop.net/mod/39250) | `Peer mod list highlighter` | irbizzelus | Highlights chosen mods in other players' mod lists and on the Crime.net lobby screen. Add mods to the list in `lua/base.lua`. |

### Lobby and multiplayer

| Mod | Folder | Author | Description |
|---|---|---|---|
| [Lobby Player Info](https://pd2mods.z77.fr/lobby_player_info.html) | `Lobby Player Info` | TdlQ | Shows each lobby player's perk deck and skill point distribution. |
| [Infamy in Lobby](https://modworkshop.net/mod/41881) | `Infamy in Lobby` | Shane | Opens the infamy menu while in a lobby, so you can go infamous without leaving. |
| [Infinamy Multiplayer](https://modworkshop.net/mod/49324) | `Infinamy Multiplayer` | Dyrax | Sends your real infamy rank above the vanilla cap. Players who also have the mod see it; everyone else sees the capped value. |
| [Chat Commands](https://modworkshop.net/mod/30259) | `ChatCommands (no tp)` | ChildOfSorrow | Slash commands in chat: `/pm`, `/kick`, `/ban`, `/restart`, `/terminate`, `/fps`, `/mods`, `/profile`, `/playtime` and more. Type `/help` for the list. Host-only commands check that you are the host. This copy has the `/tp` command removed. |

### Gameplay and quality of life

| Mod | Folder | Author | Description |
|---|---|---|---|
| [BerserkerQOL](https://github.com/rockymoto517/BerserkerBlocker) | `BerserkerQOL` | Rockymoto517 | For Berserker builds. Blocks teammate effects that push your health back up: Crew Chief health/armor, Maniac absorption, Quick Fix damage reduction, Forced Friendship absorption, Combat Medic revive HP and team AI boosts. Can be set per skill set. |
| [pecm bug fix](https://github.com/bbqglgl/PAYDAY2_pecm_bug_fix_mod) | `pecm bug fix` | BigMouse | Fixes Hacker pocket ECM jamming being cut short by network timing when several players trigger it close together. |
| [Bag Carrying Tilt Removal](https://modworkshop.net/mod/16487) | `Bag Carrying Tilt Removal` | Seven | Removes the camera tilt while carrying a bag. |
| [No Screen Shake](https://modworkshop.net/mod/22471) | `No Screen Shake` | Sydch | Removes camera shake. |
| [Low Violence Mode](https://modworkshop.net/mod/14602) | `Low Violence Mode` | Schmuddel | Removes dead bodies and blood decals right away. |
| speedyxp | `speedxp` | Hejoro | Removes the waiting time on the end screen, so you can continue right away. |
| Disable Job Heat | `Disable Job Heat` | Javgarag | Turns off job heat, the XP bonus or penalty for how often a heist has been played lately. |
| [30 FPS Bind](https://modworkshop.net/mod/52691) | `30 FPS Bind` | [6IX] | Keybind that switches the frame cap between 30 and your normal limit. |
| Downloadable Content | `unlock_all_dlcs` | tsk.xz | Unlocks DLC content on the client. |

### Debug

| Mod | Folder | Author | Description |
|---|---|---|---|
| DRAW | `(P) draw v4 purple` | hoppip | Keybind that toggles drawing physics hitboxes within 10 m in purple. For looking at collisions and hitboxes. |

## Keybinds

These mods do nothing until a key is assigned under **Options > Mod Keybinds**:

- ECM Rush Announcer: arm/disarm the announcer for the current heist
- Lobby Recreate: recreate the lobby
- 30 FPS Bind: switch the FPS cap
- DRAW: switch hitbox drawing

## Updating

Mods with an update source (SuperBLT, BeardLib, VanillaHUD Plus, BerserkerQOL, Infamy in Lobby, XPNotifier, and the TdlQ mods through Simple Mod Updater) check for updates on launch, and SuperBLT notifies you when one is out. For the others, download from the links above. My mods get updates through their GitHub repos.

## Notes

- This is a client-side pack: nobody else in the lobby needs it. Infinamy Multiplayer only shows your real rank to players who also run it.
- Mods are unofficial and not supported by Overkill / Starbreeze. Use at your own risk.
- Credit for third-party mods goes to their authors, listed above.
