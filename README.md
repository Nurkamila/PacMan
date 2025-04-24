# Pac-Man Game (Java Swing)

## Project Overview 
A classic Pac-Man game built using Java Swing, featuring:
* Player-controlled Pac-Man movement (arrow keys)
* Ghosts with randomized AI movement
* Collision detection (walls, ghosts, food)
* Score tracking and lives system
* Level reset upon completing food collection

## Features
**1. Game Elements**
* **Pac-Man:** 
    * Moves in 4 directions (Up/Down/Left/Right) with sprite changes.
    * Collides with walls, ghosts, and food.
* **Ghosts:**
    * Four ghosts (blue, orange, pink, red) with randomized movement.
    * Reset positions when Pac-Man loses a life.
* **Walls & Food:**
    * Maze layout loaded from a **```tileMap```** string array.
    * Food pellets increase score when collected.

**2. Game Logic**
* **Scoring:** +10 points per food pellet.
* **Lives System:** 3 lives; game ends when all are lost.
* **Level Progression:** Resets when all food is eaten.

## Game Mechanics
**Controls**
* **Arrow Keys:** Change Pac-Man's direction.
* **Auto-Respawn:** Game restarts automatically after game over.
**Ghost Behavior**
* Ghosts move randomly but reverse direction on wall collisions.
* Special case: Ghosts at row 9 (center tunnel) always move upward.

## Technical Implementation

**Classes**

1. **```App.java```:**
    * Initializes the JFrame window with fixed dimensions.
    * Starts the ```PacMan``` game panel.

2. **```PacMan.java```:**
    * Extends ```JPanel``` and handles game logic, rendering, and input.
    * Uses ```Block``` inner class for all game objects (Pac-Man, ghosts, walls, food).

**Key Methods**

* ```loadMap()```: Parses ```tileMap``` to create walls, ghosts, and food.
* ```move()```: Updates positions and checks collisions.
* ```paintComponent()```: Renders all game objects.

**Assets**

* ```pacmanUP.png```, ```pacmanDown.png```, ```pacmanLeft.png```, ```pacmanRight.png``` (Pac-Man sprites).
* ```blueGhost.png```, ```redGhost.png```, ```orangeGhost.png```, ```pinkGhost.png```, ```scaredGhost.png``` (Ghost sprites).
* ```wall.png``` (maze walls).

## How to Run
**Prerequisites**
* Java JDK 8+
* IDE (IntelliJ, Eclipse) or command-line compilation.

**Steps**
1. Clone the project:
```
git clone [your-repository-url]
cd PacManJava
```
2. Run the game:
* Compile and execute **```App.java```**.
* Or use your IDE's run button.

## Dependencies
* Java Swing: Built-in GUI library.
* No external libraries required.

![alt text](https://github.com/Nurkamila/PacManJava/blob/master/GAME.png?raw=true))
