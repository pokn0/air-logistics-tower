## 0.14.5
- 2.0 build, same code as 0.14.4.

## 0.14.4
- The partition tab shows the tower diagram again with items and fluids together; the ship tower fluid interfaces moved onto the hull and the circuit page only appears once a wire is attached.
## 0.14.3
- 2.0 build, same code as 0.14.2.

## 0.14.2
- Fixed the window buttons and inputs not reacting: the window event registrations were overridden by a later one and are now forwarded from a single entry point.
## 0.14.1
- 2.0 build, same code as 0.14.0.

## 0.14.0
- Reworked the tower window into three tabs (partitions, logistics, circuits); partitions are a list with one editor form on the right.
- The title bar shows a coloured running state and the common values are grouped together.
## 0.12.99
- Fixed air towers gaining fluid interfaces after copy, cut or blueprint; empty rules are no longer stored and affected towers clean up automatically.

## 0.12.98
- 2.1 build, same code as 0.12.99.
## 0.12.97
- Fixed blank hangar and backpack grids: GUI elements are added with method syntax, since passing the parent explicitly is rejected on some engine versions.
- A created grid now verifies that its inventory really bound; if not, it is replaced by clickable icons instead of leaving an empty area.

## 0.12.96
- 2.1 build, same code as 0.12.97.
## 0.12.95
- Blueprints now save belt and fluid filters; planet tower fluid rules had been left out.
- When the event carries no entity mapping, towers are matched by position so the tags are still written.

## 0.12.94
- 2.1 build, same code as 0.12.95.
## 0.12.93
- Fixed the hangar + button and aircraft icon doing nothing.

## 0.12.92
- 2.1 build, same code as 0.12.93.

## 0.12.91
- Hangar buttons accept any aircraft the tower can park.

## 0.12.90
- 2.1 build, same code as 0.12.91.

## 0.12.89
- Hangar buttons moved out of the scroll pane so the click area is not clipped.

## 0.12.88
- 2.1 build, same code as 0.12.89.

## 0.12.87
- Hangar actions report the outcome and accept the aircraft on the cursor.

## 0.12.86
- 2.1 build, same code as 0.12.87.

## 0.12.85
- Hangar back to click based access; added names for the section containers.

## 0.12.84
- 2.1 build, same code as 0.12.85.

## 0.12.83
- 2.0: every configured section opens the native item grid.

## 0.12.82
- 2.1 build, same code as 0.12.83.

## 0.12.81
- Fixed the section placement of the new locale entries.

## 0.12.80
- 2.1 build, same code as 0.12.81.

## 0.12.79
- 2.0: hangar uses clickable icons with hints.

## 0.12.78
- 2.1 build, same code as 0.12.79.

## 0.12.77
- 2.0: the tower window attempts inventory grids.

## 0.12.76
- 2.1 build, same code as 0.12.77.

## 0.12.75
- 2.0 build: nine 2.1 only APIs replaced with compatibility layers.

## 0.12.74
- Fixed the aircraft render cadence so large fleets keep redrawing.

## 0.12.73
- First Factorio 2.0.77 build.


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
