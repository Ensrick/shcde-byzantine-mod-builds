# Byzantine units for Stronghold Crusader: Definitive Edition (dev builds)

Test builds of a fan mod that adds Byzantine units to Stronghold Crusader: Definitive Edition.
This repository only holds the builds; the mod's source code is not published here.

**v0.1.0-dev.2 is an early development build for volunteer testers. Nothing in it has been
confirmed to work in game yet.** Please test on disposable maps, and back up any map or save you
care about first.

## Changes in v0.1.0-dev.2

New since v0.1.0-dev.1:

- New weapons, armour and helmets for six units, most of them models by other artists (see the
  credits file):
  - Varangian: a steel helmet, toned-down lamellar, and new axes and a round shield for the Danish
    axe and one-hand axe loadouts. The sword-and-shield Varangian keeps his earlier look until the
    new sword's licence is confirmed.
  - Cataphract: a face-mask helmet with a plume, long lamellar horse barding, a triangular pennon
    on the lance and an ornate mace for the mace riders.
  - Vanguard: sulitsa javelins, an arming sword, a kite shield and a steel helmet; his throw now
    starts from the ready hold.
  - Sentinel: a recurve bow with arrows and a quiver, a hand axe for melee and a steel helmet. He
    stows the bow while he digs or climbs a ladder.
  - Icon Bearer and Fire Siphoner: polished brass helmets and softer brass coats.
- Team colour: the Cataphract's plume and pennon and the Vanguard's shield now show their owner's
  colour.
- Border Rider: a shadow under the horse, and four horse colours.
- Varangians speak with their own recorded voice lines instead of the Swordsman's.
- The unit pictures on the Byzantine tab show the new gear too, apart from the sword-and-shield
  Varangian's.

## What is in this build

| Folder in the zip | Version | What it adds |
|---|---|---|
| `BepInEx\plugins\ByzantineUnits` | 0.1.20 | A Byzantine troop tab in the Map Editor, and the art for the Vanguard, Sentinel, Fire Siphoner, Cataphract, Icon Bearer and Varangian (three weapon loadouts) |
| `BepInEx\plugins\ByzantinePreview` | 0.1.8 | The art for the Hoplite and the Border Rider, and the Hoplite's voice lines |

Each Byzantine unit runs on a stock unit. It moves, fights and costs exactly what that stock unit
does, but looks different. Only units placed with the Byzantine buttons change; every other unit
keeps its normal look.

| Byzantine unit | Runs on the stock |
|---|---|
| Hoplite | Pikeman |
| Sentinel | Archer |
| Vanguard | Skirmisher |
| Border Rider | Horse Archer |
| Cataphract | Knight |
| Varangian | Swordsman |
| Icon Bearer | Healer |
| Fire Siphoner | Fire Thrower |

In this build, Byzantine units can only be placed in the Map Editor. The Imperial Garrison, where
they will be recruited in a normal game, is not included yet.

## Requirements

- Stronghold Crusader: Definitive Edition on Steam.
- BepInEx 5 (version 5.4.23.4), for example from the
  [SHCDE BepInEx bootstrapper](https://gitlab.com/rawra-stronghold-crusader/shcde-bepinex/-/releases).
- The SHCDE Script Extender 2.10.4: download `SHCDESE_2.10.4.zip` from its
  [official release page](https://gitlab.com/rawra-stronghold-crusader/shcde-script-extender/-/releases/v2.10.4) and follow its install notes. This build was made
  and checked against version 2.10.4; other versions are untested.

If you already play other Script Extender mods, you probably have both.

## Install

1. Close the game.
2. Find the game folder: in Steam, right-click Stronghold Crusader: Definitive Edition, then choose
   Manage, then Browse local files.
3. Extract `shcde-byzantine-mod-dev-v0.1.0-dev.2.zip` into that folder, so that the `BepInEx` folder in the zip merges with the
   game's own `BepInEx` folder. Windows' "Extract All" suggests a new subfolder; change the
   destination to the game folder itself.
4. Check that these two files now exist in the game folder:
   - `BepInEx\plugins\ByzantineUnits\ByzantineUnits.dll`
   - `BepInEx\plugins\ByzantinePreview\ByzantinePreview.dll`
5. Start the game. The file `BepInEx\LogOutput.log` in the game folder should contain
   `Byzantine units 0.1.20 waiting for the Script Extender` and
   `Byzantine animation preview 0.1.8 waiting for the Script Extender`.

The zip also places this file, `Byzantine-mod-README.md`, and `Byzantine-mod-CREDITS.md` in the game folder.

## How to test

1. Open the Map Editor with a new or disposable map.
2. Open the troops menu. A new tab showing a bronze shield and a spearhead sits after the Bedouin
   tab. Click it.
3. It shows ten buttons: Hoplite, Sentinel, Vanguard, Border Rider, Cataphract, Varangian (Danish
   axe), Varangian (sword and shield), Varangian (one-hand axe), Icon Bearer and Fire Siphoner.
   A dimmed button means that unit's art or placement did not load; please report it with your
   log.
4. Click a button, then click the map to place the unit. While you place it, the cursor should
   show the Byzantine unit. Shift, Ctrl and Alt place 5, 20 and 50 units, as usual.
5. Next to it, place the stock unit it runs on (see the table above) from the normal troop tab.
   The stock unit must keep its normal look.
6. Save the map, load it again, and check that every unit kept its look.
7. Play the map and give the Byzantine units orders: walk, run, fight, use ladders and dig moats
   where the stock unit can, and let some die. Check that every animation shows the Byzantine art,
   faces the right way, and has no flicker or stock frames mixed in.
8. Hoplites and Varangians: listen for their new voice lines when you select them and give orders.
   Stock Pikemen and Swordsmen keep their normal voices.
9. Cataphracts and Border Riders come in four horse colours (bay, black, iron grey and chestnut).
   For each of the two units, every four a player gets use each colour once, in a shuffled order.
10. Idle Hoplites should look to the right and then to the left (their alert idle).

A small separate panel on the troop tabs has a **Cheer** button. It is a development tool: for a
few seconds, idle Hoplites, Sentinels, Cataphracts and Varangians (and some stock units) play
their victory animation, so that art can be checked.

## Known issues and untested areas

- Nothing has been tested in game yet. Every step above is something we need checked.
- Unit stats, costs and behaviour are still those of the stock unit. Balance changes are not
  active.
- Units can only be placed in the Map Editor; there is no recruitment in a normal game yet.
- It is unknown whether the Byzantine look survives starting a game from an editor map. If other
  units of the same stock type suddenly look Byzantine, or Byzantine units turn stock, please
  report it.
- The new tab's position and look have not been checked against the real game screen, at any
  resolution.
- Fire Siphoner, Icon Bearer, Sentinel and Varangian show no team colour yet, so it is hard to tell whose they are. Border Rider, Cataphract, Hoplite and Vanguard have team colour.
- Only the Hoplite and the Varangian have their own voices; the other units still use their stock
  unit's voice. Neither has a victory line yet, and the Hoplite's ladder lines are unverified.
- Multiplayer is untested; please test in single player only. The Hoplite and Varangian voices are switched off in multiplayer.
- These log lines are expected in this build: `Optional spear impacts unavailable; native combat
  sounds remain` and `Imperial Garrison add-on is absent`.
- Maps and saves made with this build should still open without it, with the placed units shown
  as their stock units. This is untested.

## Uninstall

1. Close the game.
2. Delete these two folders from the game folder:
   - `BepInEx\plugins\ByzantineUnits`
   - `BepInEx\plugins\ByzantinePreview`
3. Optionally, also delete `BepInEx\config\ByzantineUnits.cfg`,
   `BepInEx\config\ByzantinePreview.cfg` (BepInEx writes them at the first start),
   `Byzantine-mod-README.md` and `Byzantine-mod-CREDITS.md`.

## Report a bug

Open an issue at https://github.com/Ensrick/shcde-byzantine-mod-builds/issues. Please include:

- the build (v0.1.0-dev.2) and what you did, step by step;
- what you expected, and what happened instead;
- a screenshot, if it is something you can see;
- the file `BepInEx\LogOutput.log` from the game folder, from the session where it happened. It
  can contain your Windows user name in file paths; you may remove that before posting.

## Credits

- Mod by Ensrick.
- The base characters, animations and horse come from free CC0 packs by Quaternius
  (quaternius.com), and some weapons and shields from models by other artists. The full list, with licences and our changes, is in
  `Byzantine-mod-CREDITS.md` in the download, and in `CREDITS.md` in this repository.
- The Hoplite voice lines were made with ElevenLabs.

This is an unofficial fan mod. It contains no game files, and it is not made or endorsed by
Firefly Studios.
