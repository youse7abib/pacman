# 🎮 Pac-Man Game

A classic Pac-Man game built with vanilla JavaScript and HTML5 Canvas.

## 🕹️ Play Online

**[Play the game here](https://youse7abib.github.io/pacman/)** - Click to start playing instantly in your browser!

## ✨ Features

- **Classic Gameplay**: Navigate Pac-Man through a maze while collecting food and avoiding ghosts
- **Smooth Movement**: Responsive controls with direction buffering for seamless gameplay
- **Smart AI Ghosts**: Four different colored ghosts with randomized movement patterns
- **Score System**: Earn 10 points for each food pellet collected
- **Lives System**: Start with 3 lives, lose one when caught by a ghost
- **Level Progression**: Complete levels by eating all food pellets
- **Game Over & Restart**: Automatic restart functionality after game over

## 🎯 Game Rules

1. **Objective**: Eat all the white food pellets to complete the level
2. **Avoid Ghosts**: Don't let the ghosts catch you!
3. **Lives**: You have 3 lives. Lose all lives and it's game over
4. **Scoring**: Each food pellet = 10 points
5. **Level Complete**: Collect all food to advance to the next level

## 🎮 How to Play

1. Click the demo link to start playing
2. Use arrow keys or WASD to control Pac-Man
3. Eat all the white dots while avoiding the colored ghosts
4. Complete the level by eating all food pellets
5. When game over, press any key to restart

## ⌨️ Game Controls

**Arrow Keys or WASD**
- Up Arrow / W - Move Up
- Down Arrow / S - Move Down
- Left Arrow / A - Move Left
- Right Arrow / D - Move Right
- Any Key - Restart after Game Over

## 🔧 Technical Details

### Game Specifications
- **Board Size**: 21 rows × 19 columns
- **Tile Size**: 32×32 pixels
- **Canvas Size**: 608×672 pixels
- **Frame Rate**: 20 FPS
- **Movement Speed**: 8 pixels per frame (tileSize/4)
- **Technologies**: HTML5 Canvas, Vanilla JavaScript, CSS3

### Collision Detection
The game uses AABB (Axis-Aligned Bounding Box) collision detection for precise hit detection between Pac-Man, ghosts, walls, and food pellets.

### Direction Buffering
The game implements direction buffering to allow smooth direction changes:
- Player input sets `nextDirection`
- Before each move, the game attempts to change direction
- If blocked by a wall, maintains current direction
- Prevents jarring movement and improves gameplay feel

## 📁 Project Structure

```
pacman-game/
│
├── index.html          # Main HTML file
├── style.css           # Styling for the game
├── main.js             # Game logic and mechanics
└── Assests/            # Game assets (images)
    ├── wall.png
    ├── blueGhost.png
    ├── orangeGhost.png
    ├── pinkGhost.png
    ├── redGhost.png
    ├── pacmanUp.png
    ├── pacmanDown.png
    ├── pacmanLeft.png
    └── pacmanRight.png
```

## 🎨 Customization Guide

### Change Wall Color

In `main.js`, locate the `loadImages()` function:
```javascript
wallImage.src = "./Assests/wall.png"; // Change to your image
```

### Adjust Game Speed

In the `update()` function:
```javascript
setTimeout(update, 50); // Lower number = faster game
```

### Modify Game Board

Edit the `tileMap` array in `main.js`:
- `X` = Wall
- `O` = Empty space (no collision)
- `P` = Pac-Man starting position
- ` ` (space) = Food pellet
- `b` = Blue ghost
- `o` = Orange ghost
- `p` = Pink ghost
- `r` = Red ghost

### Change Lives or Scoring

```javascript
let lives = 3;        // Starting lives
score += 10;          // Points per food pellet
```

## 🐛 Bug Fixes Applied

### Direction Change Issue
**Problem**: Pac-Man wouldn't respond to direction changes during movement

**Solution**: Implemented direction buffering system with `nextDirection` property and `tryChangeDirection()` method

### Ghost Reset Bug
**Problem**: Ghosts not resetting properly after collision

**Solution**: Fixed `resetPositions()` function by adding parentheses to `ghosts.values()`

## 🚀 Future Improvements

- Add power pellets for eating ghosts
- Implement ghost AI with different personalities
- Add sound effects and background music
- Create multiple difficulty levels
- Add high score system with local storage
- Implement ghost "scared" mode
- Add bonus fruits for extra points
- Create start screen with instructions
- Add pause functionality
- Implement different maze layouts

## 📝 License

This project is open source and available for educational purposes.

## 👨‍💻 About

Developed as a learning project to practice JavaScript and HTML5 Canvas game development. Feel free to explore the code and learn from it!
