# Marble Rush 3D 🟡🔵🔴

A shared-device 3D marble racing game for iPhone, iPad, and desktop browsers. **Up to six players** choose their marbles, then watch a fresh obstacle course play out.

## ▶️ Play now

**[Play Marble Rush 3D](https://m0998001.github.io/marble-rush/?v=3)**

Choose **Start Racing**, select a mode, set 2–6 players, choose marble skins, and launch. This is a browser game: people you share the link with can play their *own local races* on their devices; it is not online multiplayer.

## Game modes

- **Free for All:** first marble to reach the finish wins.
- **Team Battle:** choose 2–4 teams. Team averages reward strong finishes even with uneven team sizes.
- **Pachinko Palace:** marbles fall through staggered peg fields. End slots score **100 / 250 / 500 / 1,000 / 500 / 250 / 100**. The highest score wins; fastest time breaks a tie.

## Course collection

| Course | Coins | Theme |
| --- | ---: | --- |
| Pegboard Paradise | Free | Carnival pegs, splitters, bumpers |
| Funnel Frenzy | 300 | Solid vortex rims and spinning fans |
| Factory Frenzy | 800 | Metal sweepers, boosters and spring bumpers |
| Cosmic Chaos | 1,500 | Magnetic attractors and neon scenery |
| Jungle Jumble | 2,000 | Jungle canopy and mossy slalom fields |
| Glacier Glide | 2,500 | Icy skid patches and frozen pillars |
| Magma Mayhem | 3,200 | Volcanic towers and spring launchers |
| Coral Cove | 4,000 | Undersea bubbles, coral and flowing rings |

Pachinko Palace is a **free game mode**, not a purchasable course.

## What changed in v0.2

- Reduced the maximum player count from 16 to **6**.
- Rebuilt problematic splitters as short chevrons; matched rotating-arm direction to their physics.
- Made visible vortex rims solid, and introduced matching collision shapes for new bumpers and springs.
- Removed the former stuck-marble **forward teleport**. Instead, marbles get gradual steering and acceleration to escape jams.
- Added **Pachinko mode**, seven score bins, and a results screen ranked by points.
- Added **four unlockable stage families** with separate decorations and obstacle libraries.
- Added subtle contact plinks and new scenic structures.

### Testing

The new simulation has completed **324 seeded tests** across nine play environments and three race lengths (all six marbles finished in those tests), plus later regression passes. It has **not** yet been fully profiled on physical iPhones or iPads; visual/physics polish and edge cases may remain.

## Controls and progression

- Camera follows the pack automatically. **Drag** to orbit, **pinch/scroll** to zoom, or **tap a leaderboard name** to follow a competitor.
- Earn coins and unlock courses and cosmetic marble skins. Marble appearance does not affect physics.
- Coins, unlocks, and records are stored **locally in your browser on each device**. Clearing site data can reset progression.

## Running or deploying

The site is a static, dependency-free WebGL + JavaScript app: **[index.html](index.html)** is all that GitHub Pages needs. In repository **Settings → Pages**, publish the `main` branch from `/(root)`. For a local desktop preview, open `index.html` in a recent browser.

## Prototype limitations

The game uses a custom lightweight WebGL renderer and plane-constrained marble physics presented in 3D, not a production Unity build with full rigid-body interactions. Some power-up graphics are painted floor decals or non-solid force fields rather than physical walls. Sharing the link does **not** create a cross-device multiplayer session.

_The project is currently distributed without a license; all rights remain with the repository owner._
