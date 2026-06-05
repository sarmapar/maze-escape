# Slime Maze Escape

A browser-based maze game built in a single HTML file. No installs, just open it and play!

You're a slime who escaped a lab. The scientists are not pleased and they've flooded the place to stop you. Navigate the maze, solve the logic gate puzzles blocking your path, and get out before you dissolve.

**[Play it here](https://www.sarmapar.com/maze-escape/)**

## How to play

- **Move** — WASD or arrow keys (click and hold on mobile)
- **Open a gate** — walk up to a gold barrier and press Enter/Space, or click it
- **Solve the puzzle** — pick operators for each row so the inequalities work out for the right colors, then confirm
- **Escape** — find and reach the ★ on the outer edge

### Game modes
- **Practice** — no flood, just explore
- **Normal** — flood pauses while you're solving a gate
- **Challenge** — flood never stops

## What's in it

- Procedurally generated mazes
- Gate puzzles in two modes: basic booleans (`&&` `||`) or logic gates (`AND` `OR` `XOR` `NAND` `NOR` `XNOR`)
- A flood that rises from the center and speeds up over time
- Colored smoke effects on solved gates that apply buffs and debuffs (speed, slow, reverse controls, darkness, freeze, waterproof)
- Smooth canvas animations
- Built-in, interactive tutorial
- Mobile-friendly with click/touch controls

## Technical Details

Everything runs in a single `index.html` using vanilla JS and the HTML5 Canvas API. The maze is generated using depth-first search, which picks a direction and keeps going until it hits a dead end, then backtracks — this is what creates long winding corridors. The flood uses breadth-first search starting from the center, calculating the distance to every cell so it spreads outward evenly like ripples in water. Player effects use radial gradient color interpolation to blend between red, purple, and blue in real time.

## Built with

Built with support from [Claude Code](https://claude.ai/claude-code). I handled the game design, creative direction, and a lot of the tweaks directly in VS Code. Claude generated with the math-heavy canvas work like gradient calculations, color interpolation, and animation logic. This project involved a lot of back and forth, which is honestly a pretty fun way to build something.


## Thank you
Thank you to my playtesters who gave ideas on UI design and information to include in the tutorial. Any feedback is appreciated, simply open an issue and I will get back to you! 

*gl;hf!*
