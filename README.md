# Really Cool Game

A 2D platformer built with [Godot 4](https://godotengine.org/). The player runs and jumps across a tile-based level.

**Status:** Early development. Features and structure are subject to change.

## Controls

| Action     | Keys                         |
|------------|------------------------------|
| Move left  | `A` or `Left Arrow`          |
| Move right | `D` or `Right Arrow`         |
| Jump       | `Space`, `W`, or `Up Arrow`  |

## Getting Started

### Requirements

- Godot 4.7 or later (the project uses the Mobile renderer and Jolt Physics, both included with Godot)

### Running the Project

1. Clone the repository:
```bash
   git clone https://github.com/erichyoon/reallycoolgame.git
```
2. In Godot, select **Import** and choose the `project.godot` file in the cloned directory.
3. Press **F5** or select **Run Project**. The game launches from `main.tscn`.

## Project Structure

```
reallycoolgame/
├── project.godot         # Project settings and input mappings
├── main.tscn             # Main scene: player, camera, and level
├── character_body_2d.gd  # Player movement, gravity, and jumping
├── icon.svg              # Player sprite and project icon
└── Screenshot ... .png   # Tileset image used by the level
```

## Implementation Overview

- **Player:** A `CharacterBody2D` node with a sprite, a rectangular collision shape, and a `Camera2D` with position smoothing.
- **Movement:** Defined in `character_body_2d.gd`.
  - Horizontal speed: `800`
  - Jump velocity: `-900`
  - Gravity: uses the project's default physics settings
- **Level:** A `TileMapLayer` built from the tileset image, with collision enabled on solid tiles.

Movement can be tuned by adjusting the `SPEED` and `JUMP_VELOCITY` constants in
