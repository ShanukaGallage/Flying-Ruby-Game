# Flying Ruby

Flying Ruby is a 2D arcade game inspired by the classic pipe-dodging gameplay
of *Flappy Bird*. It is written in C++ with [raylib](https://www.raylib.com/)
and uses custom artwork, music, and sound effects.

The game includes:

- Two progressively faster levels
- A score and high-score counter
- Animated player character
- Scrolling backgrounds and ground
- Background music, sound effects, pause, and an about screen
- A level-completion screen and final win state

## Requirements

- Windows
- Visual Studio 2022 with the **Desktop development with C++** workload
- raylib installed and configured for the Visual Studio project

The solution targets Visual Studio toolset `v143` and supports Win32/x86 and
x64 Debug and Release configurations.

## Running the game

The repository contains prebuilt x64 binaries in `x64/Release`. Run the game
from the repository root so the executable can resolve the `images/`, `fonts/`,
and `sounds/` directories:

```powershell
& ".\x64\Release\Flying Bird.exe"
```

Alternatively, open `Flying Bird.sln` in Visual Studio, select an x64
configuration, build the solution, and run the project with the repository
root as the working directory.

## How to play

### Movement and actions

| Key | Action |
| --- | --- |
| `W` / `Up Arrow` | Move up |
| `S` / `Down Arrow` | Move down |
| `A` / `Left Arrow` | Move left |
| `D` / `Right Arrow` | Move right |
| `Space` | Start the game or advance to the next level |
| `P` | Pause or resume gameplay |
| `M` | Toggle music |
| `I` | Open or close the about screen |
| `Enter` | Restart after game over or return to the menu after winning |
| `Q` | Quit from the game-over screen |

Pass through the gaps between the pipes to increase your score. Colliding
with a pipe, the boundary, or the ground ends the run.

### Level goals

- **Level 1:** Reach 30 points.
- **Level 2:** Reach 50 points to win the game.

The game speed increases during play, making later sections more difficult.

## Project structure

```text
Flying Bird.cpp       Main game loop and gameplay logic
Flying Bird.sln       Visual Studio solution
Flying Bird.vcxproj   Visual Studio project configuration
images/               Sprites, backgrounds, UI, and icon assets
fonts/                Fonts used by the game
sounds/               Music and sound effects
x64/Release/          Prebuilt 64-bit Release executable and runtime DLLs
```

All asset paths are relative to the process working directory. Keep the
`images`, `fonts`, and `sounds` directories beside the executable when
distributing or running a build.

## Development notes

- The game window is 800 × 600 pixels and runs at a target of 60 FPS.
- The game currently contains two levels; the win screen advertises Level 3 as
  coming soon.
- The Visual Studio project expects raylib to be available in the local
  development environment; raylib binaries are not vendored in this repository.

## Developers

- Shanuka
- Sanadi
- Sasivarnasarma
- Bevindu
