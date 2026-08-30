# BlockCraft

BlockCraft is a browser-based Minecraft replica built with HTML, CSS, JavaScript, and Three.js.

The project recreates the core Minecraft-style experience directly in the browser, including a procedurally generated voxel world, block mining and placement, crafting, combat, hostile mobs, and a dynamic day/night cycle.

> BlockCraft is an independent project inspired by Minecraft. It is not affiliated with, endorsed by, or associated with Mojang Studios or Microsoft.

## Features

* Procedurally generated voxel world
* Terrain generation with caves
* Procedurally generated trees
* Multiple block types

  * Grass
  * Dirt
  * Stone
  * Wood
  * Leaves
  * Snow
  * Planks
  * Coal Ore
  * Iron Ore
* Block mining and placement
* Mining progression and block crack effects
* 9-slot hotbar and inventory
* Crafting system
* Wooden, stone, and iron tools
* Combat system
* Zombies and spiders
* Player health system
* Death and respawning
* Dynamic day/night cycle
* Hostile mobs spawning at night
* First-person and third-person camera modes
* Mouse look with Pointer Lock support
* Click-and-drag camera controls when Pointer Lock is unavailable
* Block targeting outline
* Damage effects

## Controls

| Key / Input    | Action                             |
| -------------- | ---------------------------------- |
| `W A S D`      | Move                               |
| `Mouse`        | Look around                        |
| `Space`        | Jump                               |
| `Left Click`   | Mine blocks / attack mobs          |
| `Right Click`  | Place blocks                       |
| `1-9`          | Select hotbar slot                 |
| `E`            | Open / close inventory             |
| `F5`           | Toggle first-person / third-person |
| `V`            | Toggle mouse lock                  |
| `R`            | Return to spawn                    |
| `Click + Drag` | Look around without mouse lock     |

## Technology

BlockCraft runs entirely in the browser and does not require a build system.

* HTML5
* CSS3
* JavaScript
* Three.js

Three.js is loaded through the following CDN:

```text
https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js
```

## Running the Game

### Directly in a Browser

Clone the repository:

```bash
git clone <repository-url>
cd BlockCraft
```

Then open the HTML file in a modern web browser.

### Using a Local Server

For the best compatibility, run BlockCraft through a local HTTP server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## World Generation

The world is generated dynamically when the game starts.

Block data is stored using a JavaScript `Map`, allowing blocks to be added and removed during gameplay.

Procedural functions are used to generate terrain with varying heights, caves, trees, and ore deposits.

## Rendering

BlockCraft uses Three.js for 3D rendering.

Blocks are grouped by type and rendered using `THREE.InstancedMesh`, reducing the amount of individual mesh objects required for the world.

Block textures are generated at runtime using HTML canvas instead of relying on external texture files.

## Mining

The player can target blocks using a voxel raycasting system.

Different block types have different mining times. Pickaxes increase mining speed for stone and ore, while axes improve the mining speed of wood.

Some blocks also require a specific tool tier before they can be mined.

## Crafting

BlockCraft includes a crafting system accessible through the inventory.

Current recipes include:

* Planks
* Sticks
* Wooden Pickaxe
* Wooden Axe
* Wooden Sword
* Stone Pickaxe
* Stone Axe
* Stone Sword
* Iron Pickaxe
* Iron Sword

## Combat

Players can attack nearby hostile mobs using weapons.

Current sword damage values are:

| Weapon       | Damage |
| ------------ | -----: |
| Fist         |      2 |
| Wooden Sword |      4 |
| Stone Sword  |      6 |
| Iron Sword   |      8 |

Current hostile mobs:

* Zombie
* Spider

Mobs have their own health, movement speed, and attack damage.

## Day/Night Cycle

BlockCraft includes a dynamic day/night cycle.

During the night, the environment becomes darker and hostile mobs spawn throughout the world.

When daytime begins, the hostile mobs are cleared from the world.

## Project Structure

The project is currently designed as a compact single-file browser game.

```text
BlockCraft/
└── index.html
```

The HTML file contains the game's:

* Interface
* Styling
* World generation
* Rendering
* Player controller
* Physics
* Inventory
* Crafting
* Mining
* Combat
* Mob AI
* Day/night system

## Future Development

Potential future additions include:

* World saving and loading
* Water and fluid systems
* More advanced terrain generation
* Passive mobs
* Farming
* Hunger and food
* Additional weapons
* Armor
* Fire
* Additional ores and materials
* Structures
* Multiplayer
* Mobile controls
* Sound effects and music
* More detailed textures
* Additional performance optimizations

## License

BlockCraft is an independent project created for experimentation and learning.

Minecraft is a trademark of Mojang Studios and Microsoft. BlockCraft does not use Minecraft's original source code or assets.

---

BlockCraft is a Minecraft-inspired voxel game designed to run directly inside a web browser.
