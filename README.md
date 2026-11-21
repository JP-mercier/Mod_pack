# PAYDAY 2 Mod Pack

My PAYDAY 2 mods folder, packaged so it can be dropped into a fresh install. It covers HUD and lobby information, quality-of-life fixes, and a few mods I wrote myself.

Runs on SuperBLT (64-bit). Last updated November 2026.

## Contents

| Path in `mod_pack.zip` | What it is |
|---|---|
| `mod_pack/WSOCK32.dll` | SuperBLT hook DLL. Goes in the game folder, next to `PAYDAY2.exe`. |
| `mod_pack/mods/` | 32 mod folders plus `mods/saves/` (my settings for the mods below). Goes in the game folder. |

## Installation

Never installed a PAYDAY 2 mod before? Follow these steps in order. It takes about five minutes, and nothing in the game's own files gets changed: the mods sit next to them and can be removed at any time.

### What you need

- PAYDAY 2 on PC (Windows), through Steam.
- The game closed while you install.

### 1. Open your game folder

In Steam, go to your **Library**, right-click **PAYDAY 2**, then **Manage > Browse local files**. A File Explorer window opens on the game folder. You are in the right place if you see `PAYDAY2.exe` in it.

The usual location is `C:\Program Files (x86)\Steam\steamapps\common\PAYDAY 2`, but it can be on another drive if you installed the game elsewhere.

Keep this window open.

### 2. Back up mods you already have (skip if this is your first time)

If the game folder already has a `mods` folder or a `WSOCK32.dll` file, you have mods installed. Rename `mods` to `mods_old` and move `WSOCK32.dll` to your Desktop, so you can go back if needed.

### 3. Download the pack

At the top of this page, click `mod_pack.zip` in the file list, then click the **Download raw file** button (the down arrow on the right). The file is about 13 MB and lands in your `Downloads` folder.

### 4. Extract the zip

In `Downloads`, right-click `mod_pack.zip` and choose **Extract All...**, then **Extract**. This creates a `mod_pack` folder. Open it: inside are exactly two things, `WSOCK32.dll` and a `mods` folder.

### 5. Copy them into the game folder

Select `WSOCK32.dll` and `mods` (click one, Ctrl+click the other), copy them (Ctrl+C), go to the game folder window from step 1 and paste (Ctrl+V). If Windows asks for administrator permission, click **Continue**.

Copy those two items, not the `mod_pack` folder itself. When you are done, the game folder looks like this:

```
PAYDAY 2/
├── PAYDAY2.exe
├── WSOCK32.dll        <- new
├── mods/              <- new
│   ├── base/
│   ├── saves/
│   ├── VanillaHUD Plus/
│   └── (the other mods)
└── (the game's own files)
```

### 6. Start the game

Launch PAYDAY 2 from Steam as usual. The first start can take a little longer. If SuperBLT says an update is available, accept it.

To check that it worked, go to **Options** in the main menu: you should see **Mod Options** and **Mod Keybinds**. If they are there, the mods are loaded.

### 7. Set your keybinds

A few mods do nothing until you give them a key. Set them under **Options > Mod Keybinds** (the list is in [Keybinds](#keybinds) below).

### Removing the mods

Delete `WSOCK32.dll` and the `mods` folder from the game folder. The game is back to normal on the next start. (Steam's **Verify integrity of game files** does not remove them, since they are not game files.)

### If something goes wrong

| Problem | Fix |
|---|---|
| The game looks normal and there is no **Mod Options** | `WSOCK32.dll` is not right next to `PAYDAY2.exe`. Usually the files ended up one folder too deep, like `PAYDAY 2\mod_pack\WSOCK32.dll` or `PAYDAY 2\mods\mods\`. Compare with the tree in step 5. |
| The game won't start, or an error mentions a missing DLL or `MSVCP` | Install the [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe), then try again. |
| Your antivirus blocks or deletes `WSOCK32.dll` | That file is SuperBLT, the mod loader. If you'd rather not trust my copy, download the same file from [superblt.znix.xyz](https://superblt.znix.xyz/) and use it instead. |
| The game crashes | The crash report is in `%LOCALAPPDATA%\PAYDAY 2\crash.txt` (paste that path in the File Explorer address bar), and the mod logs are in `mods\logs`. The last lines usually name the mod at fault. Right after a big game update, mods can break until their authors update them. |

Settings for VanillaHUD Plus, Void UI Scoreboard, Lobby Player Info, BerserkerQOL, AnimSkins Tuner and a few others come preconfigured from `mods/saves/`. Delete a mod's save file to reset that mod to its defaults.

## Mods

### Framework and libraries

| Mod | Folder | Author | Description |
|---|---|---|---|
| [SuperBLT](https://superblt.znix.xyz/) | `base` | Hoppip, ZNix | Lua hook loader that every other mod depends on. Works together with `WSOCK32.dll`. |
| [BeardLib](https://modworkshop.net/mod/14924) | `BeardLib` | Simon W, Luffy | Library for custom assets and menus. Required by AnimSkins. |
| [Simple Mod Updater](https://pd2mods.z77.fr/simple_mod_updater.html) | `Simple Mod Updater` | TdlQ | Update checker for TdlQ's mods (Lobby Player Info, Drag and Drop Inventory). Since paydaymods.com shut down, they can only update through this. |

### My mods

Written or maintained by me. They are not on ModWorkshop; the source is on GitHub where linked. Each mod's folder in `mods/` has the same name as the mod.

| Mod | Description |
|---|---|
| [AnimSkins](https://github.com/JP-mercier/AnimSkins) | Animated glowing weapon skins (Eldritch Rose, Crackle, Crystal, Interstellar, Inversion, Molton, Nebula, Nightwave, PaP Galaxy, Purple, Scribble, Shatter, Starfall, Inversion Universal). Shown on your own first-person weapons only; other players see nothing different. Skins made by Siuna. Requires BeardLib. |
| [AnimSkins Tuner](https://github.com/JP-mercier/AnimSkins) | In-game controls for AnimSkins: skin per weapon slot, glow brightness, bloom, scroll speed and direction, and reactive glow (stealth ember, assault surge, weapon heat). Found under **Options > Mod Options > AnimSkins Tuner**. |
| [ECM Rush Announcer](https://github.com/JP-mercier/ecm-rush-announcer) | During an ECM rush, announces in chat whose turn it is to place the next ECM (GREEN > BLUE > RED > YELLOW), with a warning before the current one runs out. Only players with ECM Specialist aced (pager jamming) are counted. Arm it with its keybind. Can also hide the generic ECM timer messages other players' mods post (off by default, on your screen only). |
| [Lobby ECM Check](https://github.com/JP-mercier/payday2-lobby-ecm-check) | Shows in the lobby which players actually have ECM Specialist aced. Lobby Player Info's ECM icon only counts Shinobi points, which can reach 38 without the ace; this resolves the unclear cases from what was seen in earlier heists. Works on its own; with Lobby Player Info installed, it also corrects that mod's team skills box. |
| [Lobby Recreate](https://github.com/JP-mercier/payday2-lobby-recreate) | Press the keybind in a broken lobby, as host or client. You leave, host a new lobby with the same contract and settings, and everyone from the old one is invited. |
| [XP Total HUD](https://github.com/JP-mercier/payday2-xp-total-hud) | In heists, a label with the XP the day pays if it ends now (the same total XPNotifier showed), the last gain, the level you will be once the day pays out, an XP bar for that level, and a log of XP awards with what gave each one. In the main menu profile box and in lobbies, total level XP and XP left to infamy. Position is adjustable under **Options > Mod Options > XP Total HUD**. |
| [Chat Translator](https://github.com/JP-mercier/PD2-Chat-Translator-by-powware-in-3.0) | 64-bit update of [powware's Chat Translator](https://modworkshop.net/mod/29967). Click a chat message to translate it, and type in any language (`tl help` lists the language codes). Optional auto-translate of incoming messages (`tl auto`, off by default). PAYDAY terms like ECM, pager or dozer come out as each language's official in-game names. Uses Google Translate. |
| [Recent Players Invite](https://github.com/JP-mercier/payday2-recent-players-invite) | Adds a **Recent** tab to the Social Hub with the players you played with: join their lobby, invite them to yours, or message them. |
| [Chat Input Fix](https://github.com/JP-mercier/payday2-chat-input-fix) | Keeps the chat box you are typing in visible: on the end screens it no longer hides behind the payday screen (and then sends your old text with the next message), and during the "is joining" pause you can see what you type. A message you were typing when the screen changes (lobby to heist, heist to end screen) is kept and the chat reopens with it. |

### HUD and interface

| Mod | Folder | Author | Description |
|---|---|---|---|
| [VanillaHUD Plus](https://modworkshop.net/mod/25629) | `VanillaHUD Plus` | Test1, Kamikaze94, BangL | Continuation of WolfHUD. Adds HUD information panels and menu/lobby quality-of-life changes while keeping the vanilla look. |
| [Void UI Scoreboard Standalone](https://modworkshop.net/mod/30948) | `Void UI Scoreboard Standalone` | Xeletron, Fanged Hex, VxWolf | The end-of-heist scoreboard from Void UI, without the rest of Void UI. |
| [Name Label Fading](https://modworkshop.net/mod/35185) | `Name Label Fading` | Luis_De | Fades player name labels when they are near the center of the screen, so they don't block your aim. |
| [Endscreen XP List](https://modworkshop.net/mod/42283) | `Endscreen XP List` | zReko | Keeps every XP bonus line visible on the end screen instead of replacing them one after another. |
| [Drag and Drop Inventory](https://pd2mods.z77.fr/drag_and_drop_inventory.html) | `Drag and Drop Inventory` | TdlQ | Rearrange masks and weapons in the inventory by dragging them. |
| [Peer mod list highlighter](https://modworkshop.net/mod/39250) | `Peer mod list highlighter` | irbizzelus | Highlights chosen mods in other players' mod lists and on the Crime.net lobby screen. Add mods to the list in `lua/base.lua`. |

### Lobby and multiplayer

| Mod | Folder | Author | Description |
|---|---|---|---|
| [Lobby Player Info](https://pd2mods.z77.fr/lobby_player_info.html) | `Lobby Player Info` | TdlQ | Shows each lobby player's perk deck and skill point distribution. |
| [Infamy in Lobby](https://modworkshop.net/mod/41881) | `Infamy in Lobby` | Shane | Opens the infamy menu while in a lobby, so you can go infamous without leaving. |
| [Infinamy Multiplayer](https://modworkshop.net/mod/49324) | `Infinamy Multiplayer` | Dyrax | Sends your real infamy rank above the vanilla cap. Players who also have the mod see it; everyone else sees the capped value. |
| [Chat Commands](https://github.com/JP-mercier/payday2-chat-commands-no-tp) | `ChatCommands (no tp)` | Helmut (based on ChildOfSorrow's Chat Commands) | Slash commands in chat: `/pm`, `/kick`, `/ban`, `/restart`, `/terminate`, `/fps`, `/mods`, `/profile`, `/playtime` and more. Type `/help` for the list. Host-only commands check that you are the host. This copy has the `/tp` command removed. |

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

Mods with an update source (SuperBLT, BeardLib, VanillaHUD Plus, BerserkerQOL, Infamy in Lobby, and the TdlQ mods through Simple Mod Updater) check for updates on launch, and SuperBLT notifies you when one is out. For the others, download from the links above. My mods get updates through their GitHub repos.

## Notes

- This is a client-side pack: nobody else in the lobby needs it. Infinamy Multiplayer only shows your real rank to players who also run it.
- Mods are unofficial and not supported by Overkill / Starbreeze. Use at your own risk.
- Credit for third-party mods goes to their authors, listed above.
