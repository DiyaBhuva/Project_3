# 👾 Alien Hunter - C++ Console Game

---

## 🎯 1. Game Motivation

The idea behind **Alien Hunter** is to build a retro-style **console-based shooting game** using only **C++**, without any external libraries like SDL or graphics engines. The goal was to enhance core programming skills such as:

- Mastering arrays and data handling
- Applying file I/O concepts
- Real-time keyboard handling
- Understanding game loops and animations in console environments
- Exploring logic building through fun gameplay

This project is also meant to explore how engaging interactive applications can be made using just the console window and basic language features.

---

## ✨ 2. Game Features

- 🚀 Spaceship controlled by arrow keys
- 👾 Randomly falling aliens from the top
- 🔫 Bullet shooting with spacebar
- 💥 Bullet vs Alien collision detection
- 📈 Real-time scoring and high-score tracking
- 🎮 Restart option after game over
- 💾 High score file (`hunter.txt`) is automatically saved and sorted

---

## 🧱 3. Data Structures Used

| Data Structure | Usage |
|----------------|-------|
| **Arrays**     | - 2D array for spaceship shape<br>- 2D arrays for aliens and bullets |
| **Structs**    | `Player` struct for storing name and score |
| **Files**      | Text file for reading and writing high scores |
| **Loops**      | Continuous game loop, nested loops for rendering |
| **Conditionals** | Game state control, collision checks, and input handling |

---

## 🧠 4. Logic Questions & Answers

### 🚀 Ship Control
**Q:** How is the spaceship movement controlled?  
**A:** Using `kbhit()` and `getch()` to detect left/right arrow keys and moving shipX accordingly.

### 💥 Bullet Mechanics
**Q:** How does bullet firing and movement work?  
**A:** When spacebar is pressed, a bullet's x and y are initialized. In every loop iteration, its y is decreased to move it upward.

### 👾 Alien Mechanics
**Q:** How are aliens falling?  
**A:** Aliens are initialized at random x positions at the top and their y increases over time, simulating fall.

### 🎯 Collision Detection
**Q:** How is collision detected?  
**A:** Bullet and alien coordinates are checked — if they match, a collision is registered.

### 💾 File I/O
**Q:** How are scores stored and retrieved?  
**A:** High scores are saved in a text file (`hunter.txt`) using `fprintf/fscanf`. After game over, scores are read, sorted, and displayed.

### ⌛ Game Over Logic
**Q:** When does the game end?  
**A:** When an alien collides with the spaceship or reaches a certain y position (bottom of screen).

---

## 🔧 5. Game Requirements

- OS: **Windows**
- Language: **C++**
- Headers Used: `iostream`, `conio.h`, `windows.h`, `time.h`, `stdio.h`, `stdlib.h`, `string.h`

> ❗ Note: It uses Windows-specific console APIs (`SetConsoleCursorPosition`, `Sleep`, `Beep`) which won't work on Linux/Mac.

---

## 🎮 6. Game Controls

| Key       | Action              |
|-----------|---------------------|
| `←` / `→` | Move ship left/right|
| `SPACE`   | Shoot bullet        |
| `ESC`     | Exit game           |

---
---

## 🔎 7. Important Functions

| Function Name | Purpose |
|---------------|---------|
| `gotoxy(x, y)` | Move cursor in console window |
| `drawShip()`   | Draw spaceship at current x position |
| `drawAlien()`  | Draw all aliens |
| `drawBullet()` | Move and draw all bullets |
| `bulletHit()`  | Check if a bullet hit an alien |
| `playAH()`     | Main game loop function |
| `writeHighScore()` | Save high score to file |
| `readHighScores()` | Read scores from file and display |

---

## 📚 8. Concepts Practiced

- Console-based game development
- Real-time input handling using `kbhit()` and `getch()`
- Cursor manipulation using `SetConsoleCursorPosition()`
- Collision detection logic
- Use of structs, arrays, loops, and conditionals
- File I/O for persistent game data

---

## 📈 9. How High Scores Are Stored

- After game over, user enters name.
- The score is written to `hunter.txt`.
- On next run, scores are read, sorted, and displayed.
- Sorted by score using `sort()` function and custom comparison.

---

## ✅ 10. How to Compile and Run

```bash
g++ AlienHunter.cpp -o AlienHunter
./AlienHunter
---



## ❓ 11. Important Questions & Answers (For Presentation)



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

| 10 | How is flickering prevented? | Screen is redrawn every loop with updated positions using `gotoxy()` instead of clearing the whole screen. 


---



## 🏁 14. Ending Note



This game is a fun, lightweight project to test your **logical thinking**, apply your **C++ knowledge**, and explore **console graphics** without needing external libraries.



**Enjoy blasting aliens!** 🚀👾  

**Keep learning, keep building!** 💪



---
