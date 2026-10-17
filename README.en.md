# Air Logistics Tower / 航空物流塔

**English** | [简体中文](README.md)

A Factorio mod that adds air and interstellar logistics towers. Cargo planes and ships carry items and fluids within a planet and between planets, while every tower offers numbered storage sections, vanilla logistic and construction robot platforms, and automatic mining.

Current version **0.12.69** | Changelog: [CHANGELOG.en.md](CHANGELOG.en.md)

## Features

- **Numbered storage sections**: each tower keeps 5 item sections (9 rule slots on interstellar towers), shown as an icon with a count. Click an icon to take or insert items and to set a request amount or a supply reserve.
- **Robot platforms**: request sections are filled by logistic robots from chests; supply and storage sections are available to logistic and construction robots.
- **Two-way aircraft delivery**: planes carry cargo both ways between the two tower types on the same planet, dispatched by priority, fair rotation and strict full loads.
- **Interstellar transport**: an interstellar tower's hangar accepts both planes and ships, and ships handle cross-planet cargo and fluid transport.
- **Smart belt interfaces**: an interface learns whatever arrives on its belt, or outputs a filtered item, and can be controlled through red and green wires.
- **Automatic mining**: mines connected ore patches and springs, plus ocean fluids under the tower, filling free supply sections automatically.
- **Shared infinite research**: capacity, speed, cargo and fleet research is shared across a force.

## Compatibility

- Factorio **2.0.77** or newer, including 2.1.
- The interface is available in **English** and **Simplified Chinese**.
- On Factorio 2.0 the script driven item grids inside the tower window cannot be shown, because that GUI element was added in 2.1. Every other button, number, filter and readout works.
- Internal names of items, entities and technologies are unchanged, so existing saves keep working.

## Installation

1. Download the latest package from the [release](release/) folder, for example `air-logistics-tower_0.12.69.zip`.
2. Place the zip into Factorio's `mods` folder **without unpacking it**.
   - Windows: `%APPDATA%\Factorio\mods`
   - Linux: `~/.factorio/mods`
   - macOS: `~/Library/Application Support/factorio/mods`
3. Start the game, enable the mod in the mod list, then restart the game.

You can also install it from the in-game mod portal.

## Feedback

Please report problems in [Issues](https://github.com/pokn0/air-logistics-tower/issues) and include the relevant part of `factorio-current.log` together with the steps to reproduce.

## Author

pokn
