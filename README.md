# Graphical Game

A simple 2D desktop game developed with Java and the Processing library.

The player moves horizontally using the mouse, avoids falling obstacles, collects items, and tries to reach the end of the level without losing all three lives.

## Gameplay

The player is positioned near the bottom of the game window and follows the horizontal movement of the mouse.

During the game:

* Colored blocks act as obstacles.
* White blocks act as collectible items.
* Collecting an item increases the score.
* Hitting an obstacle removes one life.
* The player starts with three lives.
* The game ends after three collisions.
* The player wins when all game objects have passed through the screen.

The current score and remaining lives are displayed at the top of the window.

## Features

* Simple mouse-based movement
* Random obstacle placement
* Random collectible placement
* Collision detection
* Score tracking
* Life tracking
* Win and game-over screens
* Custom player and background images
* Object-oriented Java structure

## Built With

* Java 17
* Processing
* Maven

## Project Structure

```
graphical-game/
├── src/
│   └── main/
│       └── java/
│           ├── Main.java
│           ├── Display.java
│           ├── Brick.java
│           ├── Item.java
│           ├── Human.java
│           └── Interface.java
├── background.jpg
├── man.jpg
├── pom.xml
└── .gitignore
```

## Main Classes

### Main.java

Contains the main game loop, window configuration, collision detection, score calculation, life management, and win or game-over logic.

### Display.java

Draws the obstacles and collectible items and updates their vertical positions during the game.

### Brick.java

Represents the colored obstacles and handles their size, color, random position, and placement validation.

### Item.java

Represents the white collectible items that increase the player's score.

### Human.java

Stores basic player dimensions.

### Interface.java

Defines the shared method used to create and position game objects.

## Requirements

Before running the project, make sure the following tools are installed:

* JDK 17 or newer
* Maven
* IntelliJ IDEA or another Java IDE
* Processing Core

## Installation

Clone the repository:

```
git clone https://github.com/mahdiramezanif/graphical-game.git
cd graphical-game
```

The current `pom.xml` does not include the Processing Core dependency. Add the following dependency inside the `<project>` element:

```xml
<dependencies>
    <dependency>
        <groupId>org.processing</groupId>
        <artifactId>core</artifactId>
        <version>4.5.5</version>
    </dependency>
</dependencies>
```

After updating `pom.xml`:

1. Open the project in IntelliJ IDEA.
2. Import or reload it as a Maven project.
3. Wait for Maven to download the required dependencies.
4. Make sure `background.jpg` and `man.jpg` remain in the project root directory.
5. Open `Main.java`.
6. Run the `main` method.

## Controls

| Action     | Control                     |
| ---------- | --------------------------- |
| Move left  | Move the mouse to the left  |
| Move right | Move the mouse to the right |

## Game Rules

1. Avoid the colored falling blocks.
2. Collect the white falling blocks.
3. Each collected item increases the score.
4. Each collision with an obstacle removes one life.
5. The game ends when the player loses all three lives.
6. The player wins by surviving until all objects leave the screen.

## Possible Improvements

The project can be expanded with features such as:

* A restart button
* Multiple difficulty levels
* Increasing object speed
* Sound effects
* Background music
* More obstacle types
* Additional levels
* A high-score system
* Keyboard controls
* Improved collision handling
* A start menu
* Better separation between game logic and rendering

## Contributing

Contributions and suggestions are welcome.

To contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit your changes.
5. Push the branch to your fork.
6. Open a pull request.

```
git checkout -b feature/my-change
git add .
git commit -m "Add my change"
git push origin feature/my-change
```
