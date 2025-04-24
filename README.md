<div align="center">
  <h1>🏀 NBA Game </h1>
  <p>Test your NBA knowledge by filling in a grid with players who have played on both teams shown. One goal: complete the grid!</p>
  <p><strong>Inspired by:</strong> <a href="https://www.hoopgrids.com/">Hoop Grids</a></p>
  <p><strong>Maker:</strong> AAYUSH BADOLA</p>
  <p><strong>CS50 Final Project</strong></p>
</div>

---

## 📜 Table of Contents
- [Game Overview](#game-overview)
- [Required Libraries](#required-libraries)
- [How to Play](#how-to-play)
- [Project Structure](#project-structure)
  - [main_game.py](#main_gamepy)
  - [test_game.py](#test_gamepy)
  - [dependencies.txt](#dependenciestxt)

---

## 🏆 Game Overview
This Python script implements the **NBA Team Match** game, a 3x3 grid-based game where NBA teams are displayed as row and column headers. Your objective is to find players who have played for both teams at each intersection.

- Uses the **NBA API** to fetch real-time team and player data.
- Features a **terminal-based interactive interface** with colorful formatting.

---

## 📦 Required Libraries
Ensure you have the following libraries installed:

```bash
pip install nba_api numpy pandas pyfiglet tabulate termcolor
```

Dependencies:

```plaintext
nba_api
numpy
os
pandas
pyfiglet
random
re
sys
tabulate
termcolor
time
typing
```

---

## 🎮 How to Play
1. Run the script:
   ```bash
   python main_game.py
   ```
2. Follow on-screen instructions.
3. Enter a player’s name along with the corresponding grid position.
4. To quit, press `CTRL+C` or `CTRL+D`.

---

## 📂 Project Structure
```
NBA-Team-Match/
│-- main_game.py
│-- test_game.py
│-- dependencies.txt
```

### `main_game.py`
This is the main script containing:

- **Game logic**: Core mechanics of the game.
- **NBA API integration**: Fetches real-time data.
- **Grid system**: Displays the 3x3 grid.

### `test_game.py`
- Contains unit tests for core functions using `pytest`.
- Ensures accurate validation of user input and game logic.

### `dependencies.txt`
- Lists required Python packages for running the game.
- Run the following command to install:
  ```bash
  pip install -r dependencies.txt
  ```

---

<div align="center">
  <h3>🔥 Ready to play? Clone the repo and start guessing! 🔥</h3>
</div>

```bash
git clone https://github.com/your-username/NBA-Team-Match.git
cd NBA-Team-Match
python main_game.py
```
