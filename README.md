# Cyborg Chronicles

A top-down roguelike shooter built in Unity with C#. Final exam (maturita) project at SSPŠ, Prague, developed October 2022 to February 2023.

## The game
Every run generates a new floor. Clear the rooms, collect power-ups, find the boss room and beat the boss. Once a floor is clear, a lift down opens to the next one.

- **Procedural floors:** a 13x13 grid grown in random "veins" from the starting room. One dead end becomes the boss room and the others become item rooms. A minimap marks them (yellow for items, red for the boss).
- **Enemies:** stationary turrets, walking shooters and flyers, all built on a shared `GenericEnemy` base for health and damage.
- **Bosses:** Duke of Flies and the Turret Boss, spawned in the boss room.
- **Power-ups:** damage, fire rate, health, shot speed and movement speed.
- **Menus:** main, options, pause and death screens.

## Controls
- **WASD:** move
- **Arrow keys:** shoot
- **Esc:** pause

## Running it
Unity **2021.3.11f1**. Open the project folder in Unity Hub, load `Assets/Scenes/MainMenu.unity` and press Play. The game scene is `SampleScene`.

## Code layout
- `Assets/Player/`: player movement, shooting with cooldowns, power-up pickups
- `Assets/Enemies/`: the `GenericEnemy` base, three enemy types, two bosses, projectiles
- `Assets/Rooms/`: floor generation (`RoomGen`), doors, rocks, room detection, the next-floor lift (`LowerLevelGen`)
- `Assets/Menu/`: menu scenes and in-game menus

## Credits
- **Vojtěch Hronek** ([GamesH007](https://github.com/GamesH007)): player controller, shooting, all enemies and bosses, power-ups, doors, rocks, item and boss rooms, floor progression, pause, death and options menus, animations and scaling (62 of 68 commits).
- **Adam Majer** ([MajerAdam](https://github.com/MajerAdam)): the first version of the room generator, the minimap, and the main menu UI.
