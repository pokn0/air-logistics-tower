# Changelog

**English** | [简体中文](CHANGELOG.md)

The internal names of items, entities and technologies never change, so existing saves keep working after an update.


## 0.12.88 / 0.12.89
- 2.0 branch: the hangar take and store buttons moved out of the height limited scroll pane (a clipped button also loses part of its hit area) and an unnecessary pre-check was dropped.
- 2.0 branch: clicking a hangar button now logs the element name and tower lookup result, so an unresponsive button can be traced.
- The 2.1 branch is unchanged.
## 0.12.86 / 0.12.87
- 2.0 branch: the hangar take and store buttons no longer fail silently; they move one aircraft or show the reason (no aircraft in the backpack, hangar full, hangar empty, backpack full).
- 2.0 branch: storing also accepts the aircraft held on the cursor.
- The 2.1 branch is unchanged.
## 0.12.84 / 0.12.85
- 2.0 branch: the hangar is click based again (click the aircraft icon to take one, click + to store one from the backpack) and no longer opens the logistics chest window with its request panel.
- 2.0 branch: added names for the hidden section containers, so the native grid window no longer shows Unknown key.
- Sections still open the native item grid (a plain container, grid only); sections set to a robot mode use a logistics chest entity, so their window includes the engine's logistics panel.
- The 2.1 branch is unchanged.
## 0.12.82 / 0.12.83
- 2.0 branch: each configured section has a chest icon button that opens the engine's own item window (the same grid the base game shows for chests and turrets), so items can be moved by hand.
- 2.0 branch: the hangar gets the same button, opening the native two slot aircraft grid with the aircraft filters in place.
- The buttons only appear on versions without script driven inventory grids; the 2.1 branch is unchanged.
## 0.12.80 / 0.12.81
- Fixed the section placement of the new hint text and aircraft tooltip localisation (they had been written under the wrong section and showed as Unknown key).
- The 2.0 branch offers clickable aircraft icons in the hangar (one aircraft per click) and a hint where the player backpack grid used to be; the 2.1 branch keeps the native inventory grids.
## 0.12.78 / 0.12.79
- 2.0 branch: when the inventory grid cannot be created, the hangar becomes clickable aircraft icons (one aircraft per click) with live counts, and the player backpack area shows a hint.
- The first failure now writes the engine's reason to the log, which tells whether the element exists at all on that version.
- The 2.1 branch is unchanged and keeps the native inventory grids.
## 0.12.76 / 0.12.77
- Fixed the 2.0 tower window missing the player backpack and aircraft slot grids: a 2.1 only event had been mistaken for a 2.1 only element, so the whole class of inventory grids was skipped.
- Both branches now attempt to create the grids, with a retry that drops 2.1 only options.
- 2.0 has no such event, so drag and drop inside the grids is handled by the engine; the immediate refresh and aircraft type check do not run, and reopening the window shows current counts.
- 0.12.76 is the 2.1 branch, 0.12.77 the 2.0 branch.
## 0.12.74 / 0.12.75
- Fixed a render cadence defect introduced in 0.12.71: after aircraft movement moved to every second tick, the draw throttle still compared the raw tick modulo, so aircraft whose phase made the residue odd **never matched a render window** and stopped redrawing for long stretches in adaptive/performance render mode.
- It now compares the render window index, so each window redraws exactly once at any movement cadence, and the per-aircraft phase still spreads the load.
- 0.12.74 is the 2.1 branch, 0.12.75 the 2.0 branch; same code, only `factorio_version` and the dependency differ.
- The 2.0 branch also carries the full port: nine 2.1 only APIs now go through capability probes and compatibility layers; a 40 tower mixed scenario delivered 199200 items over 3600 ticks with every invariant assertion passing.

## 0.12.73
- Added a Factorio 2.0.77 build: all nine 2.1 only APIs now go through capability probes and compatibility layers, while 2.1 keeps using the native calls.
- Covers the GUI inventory event and elements, control behavior output networks, fluid capacity/add/remove, fluid filters, whole-stack inventory transfers and the logistic chest reader.
- On 2.0.77 `run-package`, `run-interstellar`, `run-robots`, `run-hangar` and `run-supply` all pass.
- On 2.0 the item grids in the tower window are hidden and interface fluid filters do not apply; everything else behaves the same.

## 0.12.71
- Late game performance: aircraft routes are now advanced once every 2 ticks (an effective 30 Hz), with two ticks of travel resolved per step, so speed, path and arrival order are unchanged.
- Reference save (115 towers, 444 aircraft): average update 13.54 to 12.38 ms (-8.6%), improved in all three alternating rounds, minimum frame 9.05 to 6.62 ms.
- Cost: aircraft positions update every 0.033 s, which can look slightly steppy at high speed, and arrivals resolve up to 1 tick later.
## 0.12.70
- Fixed 0.12.68 onward failing to load on 2.1: `factorio_version` is back to `2.1`, because Factorio requires an exact major.minor match.
- 2.0-only APIs such as `output_networks` and `get_fluid_filter` are now capability probed and degrade instead of crashing.
- Recorded a measured late-game baseline (115 towers, 444 aircraft) for future optimisation work.
## 0.12.69
- Fixed an error that stopped the mod from loading on the stable Factorio 2.0 branch.

## 0.12.68
- Added support for Factorio 2.0.77; interface and circuit features that require 2.1 are hidden automatically.

## 0.12.67
- Reduced repeated inventory reads during spoilage preservation, lowering the per tick cost.

## 0.12.66
- The aircraft list is no longer rebuilt and fully sorted on every launch and landing, noticeably lowering dispatch cost.

## 0.12.65
- Text change: "recovery storage details" is now simply "recovery storage".

## 0.12.64
- Planet logistics towers hide the fluid transport settings they cannot use, for a cleaner window; interstellar fluid transport is unchanged.

## 0.12.63
- Fixed connected ore patches sometimes disappearing as a group after the centre patch was exhausted.

## 0.12.61
- Deleting or clearing a whole surface now reclaims its towers and interfaces directly instead of spawning a large amount of dropped items.

## 0.12.60
- Reused the tower state already validated each tick, lowering routine maintenance cost.

## 0.12.59
- Dispatch now compares priority and distance first and skips candidates that cannot win, reducing stock reads; fairness and full-load rules are unchanged.

## 0.12.56
- Parked aircraft skip redundant rendering updates; flight and animation behaviour is unchanged.

## 0.12.55
- Fixed a shortfall where blue chest requests could only use a small part of the stock when recovery storage had built up.

## 0.12.54
- Every resource on the mining panel now has its own checkbox; while unchecked it mines nothing, consumes no ore or mining fluid, and creates no section.

## 0.12.53
- Towers are no longer scanned one by one while no aircraft is in flight.

## 0.12.52
- Fixed the red chest variant used for promethium asteroid chunks being delayed while robots still had pickups pending.

## 0.12.51
- Fixed an item transfer loop that could hang the whole game in rare cases.

## 0.12.57 / 0.12.58 / 0.12.62
- Internal performance work with no behaviour change.
