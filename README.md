# HumbleBot Wants To Retire Alive
 
A pygame game for the University of Helsinki Python Programming MOOC — Part 14 final project.
 
## How to Play
 
You are HumbleBot, a robot with one dream: **retire alive**. Collect coins to build your wallet, avoid the monsters, and reach the retirement door before they eat you.
 
### Controls
 
| Key | Action |
|-----|--------|
| ← → ↑ ↓ | Move HumbleBot |
| R | Restart after game over |
| Q | Quit the game |
 
### Goal
 
Collect **a certain amount of coins, your joy to find out how many,** to become retirement eligible, then walk into the **door** in the centre of the screen. The door will stay locked until you have enough in your wallet.
 
### Watch out
 
- Monsters chase you and get faster as more spawn
- The more coins you collect, the greedier you are, **the more difficult it'll get to reach the door** due to two mysterious side-effects, so choose your route wisely
- If a monster catches you before you retire, it's game over

## Features
 
- Player-controlled sprite with arrow keys and screen boundaries
- 100 collectible coins that wriggle around the screen
- 5 monsters that hunt the player
- Wallet counter and debug HUD showing player speed and max monster speed
- Robot grows in slows as wallet increases
- Retirement win condition — reach the door with wallet ≥ ?? coins
- Game over and retirement screens with restart option

## Requirements
 
```
pygame
```
 
Install with:
 
```bash
pip install pygame
```
 
## Running the Game
 
```bash
cd src
python main.py
```
 
The following image files must be present in the `src/` folder (included in the repo):
 
- `robot.png`
- `monster.png`
- `coin.png`
- `door.png`
## Project Structure
 
```
src/
├── main.py          # All game logic
├── robot.png
├── monster.png
├── coin.png
└── door.png
```
 
## Known Limitations
 
- The `lives` variable is tracked but not yet used — HumbleBot currently has one shot
- Coins can wander off screen edges

## Received Peer Reviews

### First 08/05/2026
Overall Impression: This is a fantastic and nice game:) The concept of retiring alive is funny, and the risk and reward mechanic where collecting coins makes the robot bigger and slower is a brilliant gameplay design.  

Code Quality: The code is excellently structured. You made great use of pygame sprite and group classes, which goes beyond the basic level. The logic is cleanly divided into separate classes and functions, making it very readable.  

Suggestions for Improvement:  As you mentioned in the limitations, adding simple boundary checks (like if self.rect.x < 0:) inside the Coin class's update would prevent them from going off-screen.  In the Game class, pygame.FULLSCREEN is written on its own line and isn't passed to set_mode, so it doesn't actually trigger fullscreen I think.  

Overall, it's a fantastic job!
 
