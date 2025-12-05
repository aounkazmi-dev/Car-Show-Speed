# Car Racing Game in x86 Assembly

This is a simple **car racing game** implemented in **x86 Assembly** for DOSBox. The project demonstrates graphics programming, keyboard input handling, animation, collision detection, and basic multitasking for background music. The game is developed in multiple phases to progressively add features, presenting both programming logic and presentation skills.

---

## Features

### Phase 1: Start Screen
- Static background with road, grass, and borders
- Red car positioned in the center lane
- Randomly placed blue obstacle car
- Introduction screen showing:
  - Developer names
  - Roll numbers
  - Name of the game
- Instruction screen showing controls and gameplay instructions
- Main screen displays: *"Press any key to start the game"*

### Phase 2: Game Animation
- Red car moves forward automatically
- Arrow keys control movement:
  - **Left/Right**: Move lanes
  - **Up/Down**: Move forward/backward
- Blue obstacle cars appear randomly at intervals
- Coins appear to collect points
- Fuel icons appear to refill fuel
- Fuel bar decreases over time
- Timer ensures smooth movement (one step per key press)
- Infinite loop to continuously update animation
- Background remains static

### Collision and Score
- Collision detection with obstacle cars
- Visual spark effect on collision
- Ending screen displays:
  - Coins collected
  - Fuel left
  - Player name and roll number
- Score updates as coins are collected
- Fuel management and color-coded bar (optional for visual appeal)

### Additional Features
- Confirmation screen on pressing **ESC**:
  - "Do you want to quit?" with **Y/N** options
- Smooth transition between screens
- Background music using multitasking:
  - Separate process for game music
  - Optional sound effects for coin collection, fuel refill, and crash
- All screens and features are implemented using subroutines for clean and modular code
- Configurable global variables for screen positions, car speed, lanes, etc.
- Proper management of interrupts and stack to ensure DOSBox stability

---

## Controls

| Key          | Action                                   |
|--------------|-----------------------------------------|
| Arrow Keys   | Move car (Left, Right, Up, Down)        |
| ESC          | Pause game / Quit                        |
| Y/N          | Confirm exit during pause                |
| Space/Enter  | Continue from ending screen              |

---

## Installation

1. Install **DOSBox**: [https://www.dosbox.com](https://www.dosbox.com)
2. Clone this repo
3. Mount the project folder in DOSBox
4. Assemble and run the game using your preferred assembler (MASM/TASM/NASM)
   
```asm
; Example (TASM)
tasm main.asm
tlink main.obj
main.exe
