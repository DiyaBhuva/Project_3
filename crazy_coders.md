# 👾 Alien Shooter Game in C++

A console-based Alien Shooter game where you control a spaceship to shoot falling aliens. Developed using pure C++ with no external libraries.

---

## 🎯 1. Motivation

This game was created to:
- Strengthen understanding of arrays, structures, and functions in C++
- Implement real-time input handling using `kbhit()` and `getch()`
- Create a full-fledged console game with only basic C++ and Windows API
- Improve logic-building skills by handling multiple entities (player, aliens, bullets) at once

---

## ✨ 2. Features

- 👾 Aliens fall from the top randomly
- 🚀 Player can move left/right and shoot bullets
- 💥 Bullets destroy aliens on collision
- 🧠 Collision detection logic implemented from scratch
- 💾 High score saving and display using file I/O
- ⌨️ Real-time controls: Arrow keys to move, Spacebar to shoot, Escape to exit
- 📉 Game over when alien reaches the ship

---

## 🧰 3. Data Structures Used

- **Arrays**:  
  - To store positions of aliens and bullets
- **Struct**:  
  - To store player names and scores
- **File I/O**:  
  - For reading/writing scores to `hunter.txt`
- **Functions**:  
  - `gotoxy()`, `draw_ship()`, `move_ship()`, `draw_bullet()`, etc., used for modular code design

---

## 🧠 4. Logic & Game Flow

- **Shooting**: When space is pressed, a new bullet is created with ship's current x, y position
- **Bullet Movement**: Each bullet's y-coordinate decreases in each iteration
- **Alien Movement**: Each alien's y-coordinate increases every loop
- **Collision Detection**: If bullet and alien share same x, y — the alien is destroyed and score increases
- **Game Over**: If any alien reaches the player line
- **High Score**: Name and score are written to `hunter.txt` and sorted

---

## ❓ 5. Important Questions & Answers

| No. | Question | Answer |
|-----|----------|--------|
| 1 | What is the logic of shooting? | When the spacebar is pressed, a bullet's position is stored in an array. In the game loop, the bullet moves upward by reducing its y-coordinate. |
| 2 | How does the alien fall? | Aliens are randomly generated at the top and their y-coordinate increases in every loop iteration, simulating falling. |
| 3 | How is collision detected? | The bullet and alien positions are compared. If their x and y match, it’s a hit. The alien is removed and score increases. |
| 4 | How is input handled? | Using `kbhit()` to check if a key is pressed, and `getch()` to get the pressed key (left, right, space, escape). |
| 5 | What happens on game over? | If an alien reaches the ship’s row or bottom of screen, game over is triggered. Score is then saved. |
| 6 | How is high score saved? | After entering the name, the score is written to `hunter.txt`. All scores are read from file and sorted for display. |
| 7 | Why is `gotoxy()` used? | To move the console cursor to a specific (x, y) position for redrawing the ship, aliens, bullets. |
| 8 | What is the role of `Sleep()`? | It controls the speed of the game loop to slow down alien/bullet movement, simulating animation. |
| 9 | Why did you use structs? | To store the player’s name and score in a single object, making it easier to sort and manage. |
| 10 | How is flickering prevented? | Screen is redrawn every loop with updated positions using `gotoxy()` instead of clearing the whole screen. |

---

## 🏁 6. Ending Note

This game is a fun, lightweight project to test your **logical thinking**, apply your **C++ knowledge**, and explore **console graphics** without needing external libraries.

**Enjoy blasting aliens!** 🚀👾  
**Keep learning, keep building!** 💪
