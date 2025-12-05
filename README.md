# Car Game in x86 Assembly

This is a simple car racing game implemented in **x86 Assembly** for DOSBox. The project demonstrates:
- Graphics programming in DOS (VGA mode)
- Keyboard input and hardware interrupts
- Animation and smooth movement
- Collision detection, scoring, and fuel mechanics
- Basic multitasking for background music

## Features

**Phase 1: Start Screen**
- Static background with road, grass, and borders
- Red car in center lane
- Blue obstacle car placed randomly
- Introduction and instruction screens

**Phase 2: Game Animation**
- Red car moves forward automatically
- Left/right/up/down arrow keys move the car
- Randomly appearing blue cars
- Coin collection and fuel management
- Fuel bar with dynamic decrease over time
- Collision detection with visual spark

**Additional Features**
- Start screen with developer names and roll numbers
- Confirmation screen on pressing ESC
- Ending screen showing coins collected, fuel, and messages
- Background music (multitasking)
- Optional sound effects for coins, fuel, crash

## Controls
- **Arrow Keys**: Move car
- **ESC**: Pause game / Quit
- **Y/N**: Confirm exit
- **Space/Enter**: Continue from ending screen

## Installation
1. Download DOSBox: [https://www.dosbox.com](https://www.dosbox.com)
2. Clone this repo
3. Mount the project folder in DOSBox
4. Assemble and run the game using your preferred assembler (MASM/TASM/NASM)
   
```asm
; Example (TASM)
tasm main.asm
tlink main.obj
main.exe
