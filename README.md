# 🟢 Slime Maze Escape

A browser-based maze escape game — no installs, no dependencies, just a single HTML file.

You play as a slime who has escaped a laboratory. The scientists are not pleased. Navigate through a procedurally generated maze, solve logic gate puzzles to unlock barriers, and reach the exit before the flood rises from the center and dissolves you.

---

## How to Play

- **Move** — WASD or arrow keys (or click/hold to move on mobile)
- **Open a gate** — walk up to a gold barrier and press Enter/Space or click it
- **Solve the puzzle** — choose operators for each inequality row so the right colored values pass
- **Escape** — find and reach the ★ on the outer edge of the maze

### Game Modes
| Mode | Description |
|------|-------------|
| **Practice** | No flood — explore freely |
| **Normal** | Flood pauses while solving a gate puzzle |
| **Challenge** | Flood never stops |

---

## Features

- Procedurally generated mazes with guaranteed solvability
- Logic gate puzzles in two difficulty modes: **basic boolean** (`<` `>` `≤` `≥`) and **logic gates** (`AND` `OR` `XOR` `NAND` `NOR` `XNOR`)
- Rising flood mechanic that accelerates over time
- Colored smoke gate effects that apply buffs/debuffs to the player (speed, slow, reverse controls, darkness, freeze, waterproofing)
- Smooth canvas animations — particle effects, radial gradient auras, door slide animations, color-blending effects
- Interactive built-in tutorial for the gate puzzle system
- Mobile-friendly with touch and click-to-move controls
- Three-page intro, in-game cheatsheet, and operator reference

---

## Technical Details

Built entirely in a **single HTML file** using the HTML5 Canvas 2D API and vanilla JavaScript — no frameworks, no build step, no dependencies. Everything from maze generation to particle rendering runs in a `requestAnimationFrame` game loop.

Highlights:
- BFS-based flood fill for maze generation and flood depth tracking
- Per-effect color interpolation using radial gradients (red → purple → blue based on remaining durations)
- Darkness effect with an expanding light radius as it fades out
- Gate puzzle evaluation supports both symbolic operators and named logic gates via a shared `evalConnector` function

---

## Running It

Just open `index.html` in any modern browser. No server required.

---

## Built With

This project was built with support from **[Claude Code](https://claude.ai/claude-code)** (Anthropic's AI coding assistant). The creative direction, game design decisions, playtesting, and many of the code tweaks were done directly — Claude handled the math-heavy rendering work (canvas animations, gradient calculations, color interpolation, game loop timing) and implemented features based on iterative feedback. A collaborative process where both sides contributed meaningfully.

---

*Can you escape before you dissolve?*
