# Changelog

**English** | [简体中文](CHANGELOG.md)

The internal names of items, entities and technologies never change, so existing saves keep working after an update.


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
