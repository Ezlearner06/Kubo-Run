# KUBO RUN

**Run. Trick. Escape.**

A fast-paced, minimalist browser trap-platformer where every obstacle is deviously planned and your only ally is your own ghost. Master classic platforming instincts and outsmart puzzle traps with the signature **KUBO ECHO** mechanic.

![Play in browser](https://img.shields.io/badge/play-in%20browser-ffb24d)
![License](https://img.shields.io/badge/license-MIT-blue)

## Play

Open `index.html` directly in any modern web browser, or serve the directory locally:

```bash
npx serve .
# or
python -m http.server 8080
```

Then visit `http://localhost:3000` (or `http://localhost:8080`).

## Controls

| Key | Action |
|---|---|
| **← → / A D** | Move left / right |
| **↑ / W / Space** | Jump (variable height + coyote time) |
| **E** | **KUBO ECHO** (record & replay your recent ghost path) |
| **R** | Restart level |
| **M** | Mute / unmute audio |
| **T** | Toggle dark / light theme |
| **F** | Toggle fullscreen |

On mobile and touch devices, the game automatically presents responsive, translucent on-screen buttons: direction arrows on the left, and **ECHO**, **Restart**, and **Jump** on the right.

## Signature Mechanic: KUBO ECHO

Activate **KUBO ECHO** once per level by pressing **E** (or tapping the on-screen **ECHO** button):

1. **Replay Buffer**: The game continuously logs your recent movement window (last ~3 seconds).
2. **Ghost Projection**: When activated, a luminous, translucent Kubo Echo spawns at your past location and faithfully replays your actions.
3. **Echo Switches**: Special holographic **Echo Switches** only respond to the touch of your Echo.
4. **Puzzle Solving**: Walk across an Echo Switch, reposition yourself by the gate, press **E**, and let your Echo hold the switch while you sprint through the open gate!

### Echo Rules
- **One use per level**: Indicated by the `ECHO ● READY` / `ECHO ● USED` status badge.
- **Purely local**: Operates smoothly within solo play with zero backend requirements.
- **Resets on retry**: Death or level restarts cleanly reset your Echo ability.
- **Safety**: Echo cannot steal exit gates or prematurely end levels—it exists to solve timing and cooperative switch puzzles.

## Features

- **30 Handcrafted Levels**: Carefully balanced progression from tutorial gauntlets to mind-bending Echo gauntlets.
- **19+ Trap & Mechanic Types**: Collapsing floors, concealed pop spikes, falling crushers, crumbling platforms, tracking floor gaps, fake escape doors, reverse control fields, moving platforms, conveyor belts, high-impulse springs, spinning saws, telegraphed laser beams, teleporters, buttons, gates, blinking platforms, pendulums, turrets, and **Echo Switches**.
- **Computer Graphics Polish**:
  - Alpha-blended ghost trails and radiant energy auras
  - Smooth hermite/linear position and velocity interpolation
  - Expressive player squash and stretch physics
  - Layered rendering with screenshake, blood splatter particles, and iris scene transitions
- **Procedural Web Audio**: 100% synthesizer-driven 8-bit sound effects (jumps, thuds, deaths, lasers, chime echoes)—zero external audio assets needed.
- **Progress Persistence**: Deaths and level unlock progress saved locally in browser `localStorage`.
- **Themeable & Responsive**: Clean Dark & Light modes with dynamic canvas adaptation for both desktop and mobile screens.

## Architecture

Built entirely with standard Web standards:
- **HTML5 Canvas 2D**: Crisp 960×540 canvas with automatic high-DPI scaling.
- **Vanilla JavaScript (ES6+)**: Zero bulky libraries, zero build steps.
- **Vanilla CSS3**: Modern glassmorphic styling, responsive safe-area scaling, and fluid animations.
- **Vercel Analytics**: Lightweight privacy-friendly analytics via ESM import map.

## License

MIT — see [LICENSE](LICENSE).
