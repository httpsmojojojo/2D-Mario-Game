# 2D Mario Game Engine

Welcome to the 2D Mario Game Engine project! This repository contains the source code for a modular and flexible game engine designed to create a Mario-style 2D platformer. This is part of a class project for Object-Oriented Programming (OOP).

## Members

- 23BSCS003
- 23BSCS012
- 23BSCS026
- 23BSCS034
- 23-22BSCS042

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [File Structure](#file-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Running the Game Engine](#running-the-game-engine)
  - [Creating and Modifying Levels](#creating-and-modifying-levels)
- [Architecture](#architecture)
- [Contributing](#contributing)
- [License](#license)

## Overview

This game engine is designed to create and run 2D platform games, specifically a Mario-style game, with modular code for easy expansion. It supports custom levels, basic AI for enemies, animation, sound management, and collision detection, making it ideal for learning game development.

## Features

- **Animation Handling**: Manages smooth animations for characters, enemies, and environment.
- **Advanced Collision Detection**: Detects and handles collisions between players, enemies, and tiles.
- **Sound Management**: Plays background music and sound effects.
- **Input Handling**: Supports customizable keyboard input for player control.
- **User Interface (UI)**: Manages menus, HUDs, and other UI elements.
- **Map Loading and Rendering**: Supports multiple tile-based maps.
- **Extensible Structure**: Add new levels, entities, and power-ups with ease.

## File Structure
```plaintext
2D-Mario-Game
├── build
│   ├── classes
│   │   └── com
│   │       └── mojo
│   │           ├── graphics
│   │           │   ├── Animation.class
│   │           │   ├── ScreenManager.class
│   │           │   └── Sprite.class
│   │           ├── input
│   │           │   ├── GameAction.class
│   │           │   └── InputManager.class
│   │           ├── test
│   │           │   └── GameCore.class
│   │           └── tilegame
│   │               ├── GameEngine.class
│   │               ├── MapLoader.class
│   │               ├── TileMap.class
│   │               ├── TileMapDrawer.class
│   │               └── sprites
│   │                   ├── Creature.class
│   │                   ├── Fly.class
│   │                   ├── Grub.class
│   │                   └── Player.class
├── dist
│   ├── images
│   │   └── ... (game images)
│   ├── maps
│   │   ├── map1.txt
│   │   ├── map2.txt
│   │   ├── map3.txt
│   │   └── map4.txt
│   ├── README.TXT
│   └── SuperMarioGame.jar
├── images
│   └── ... (image assets)
├── maps
│   ├── map1.txt
│   ├── map2.txt
│   ├── map3.txt
│   └── map4.txt
├── mojo_projects
│   ├── private
│   │   ├── private.properties
│   │   └── private.xml
│   ├── build-impl.xml
│   ├── genfiles.properties
│   ├── project.properties
│   └── project.xml
├── src
│   └── com
│       └── mojo
│           ├── graphics
│           │   ├── Animation.java
│           │   ├── ScreenManager.java
│           │   └── Sprite.java
│           ├── input
│           │   ├── GameAction.java
│           │   └── InputManager.java
│           ├── test
│           │   └── GameCore.java
│           └── tilegame
│               ├── GameEngine.java
│               ├── MapLoader.java
│               ├── TileMap.java
│               ├── TileMapDrawer.java
│               └── sprites
│                   ├── Creature.java
│                   ├── Fly.java
│                   ├── Grub.java
│                   ├── Player.java
│                   └── PowerUp.java
├── build.xml
├── manifest.mf
└── README.md
```

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- IDE such as IntelliJ IDEA, Eclipse, or VSCode

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/httpsmojojojo/2D-Mario-Game.git
   ```
2. Navigate to the project directory:
   ```bash
   cd 2D-Mario-Game
   ```
3. Compile the code using `build.xml`:
   ```bash
   ant build
   ```

## Usage

### Running the Game Engine

1. Open the project in your preferred IDE.
2. Run the `SuperMarioGame.jar` file or execute the main class in your IDE:
   ```bash
   java -jar dist/SuperMarioGame.jar
   ```

### Creating and Modifying Levels

Levels are stored as `.txt` files in the `maps` directory. Each file contains data representing the layout of tiles in that level. You can create new maps by adding `.txt` files with tile data and then referencing them in the game.

## Architecture

The engine is divided into several packages, each focusing on a different aspect of the game:

- **Graphics** (`graphics`): Responsible for animations and rendering of game elements.
  - `Animation`: Manages frame-by-frame animations.
  - `ScreenManager`: Controls the game screen display.
  - `Sprite`: Represents visual objects in the game.
  
- **Input Management** (`input`): Handles user input from keyboard and mouse.
  - `GameAction`: Encapsulates an action triggered by a key press.
  - `InputManager`: Maps keys to game actions.

- **Core Gameplay** (`tilegame`): Contains core game logic and entity handling.
  - `GameEngine`: Main game loop and logic.
  - `MapLoader`: Loads and parses map data.
  - `TileMap`: Manages game tiles and their properties.
  - `TileMapDrawer`: Renders the map and objects.
  
- **Entities** (`sprites`): Represents all characters and objects in the game.
  - `Creature`, `Fly`, `Grub`, `Player`: Different types of entities with specific behaviors.
  - `PowerUp`: Represents power-ups and bonuses.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a detailed description of your changes.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
