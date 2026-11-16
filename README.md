# Marble Rush 3D 🟡🔵🔴

A shared-screen, arcade-style **3D marble racing game** built for mobile Safari, iPads and desktop browsers. Set up **2–6 marbles** on one device and watch the obstacles determine the winner.

### ▶️ Play

**[Play Marble Rush 3D](https://m0998001.github.io/marble-rush/?v=4)**

No account or installation required. Each visitor plays a local session on their own device; the link does not connect friends into one online race.

## What's new in v0.3

- **Curved courses:** Tracks now follow smooth, randomized, 3D S-bends. Cameras, guardrails, scenery, ramps and marbles follow the same track coordinates, not just a straight slope.
- **Real tunnel passages:** Funnel Frenzy and other later stages include tunnels with continuous side walls, overhead roof bands, arched ribs, and navigable entrances/exits. A dedicated **Tunnel Twister** course is free to try.
- **Active edge obstacles:** More bumpers mounted to the outside rail, plus short angled deflectors, so marbles encounter meaningful side-of-track interactions without being pinned against a wall.
- **Additional obstacles:** Moving spinner arms, short launch pads that send marbles on visible arcs, contoured hill ramps, booster plates, spring bumpers, and two-row peg slaloms.
- **Safer vortex bowls:** Formerly closed, trapping rings now have matching open curved walls with upstream and downstream gaps.
- **More complete courses:** A shallow start ridge gives each marble early contact, while hand-spaced slalom sections prevent consistently straight, obstacle-free lanes.
- **Mobile optimization:** Reduced WebGL pixel ratio and camera-based object culling for more practical phone performance.

Previously added in v0.2: **2–6-player limit**, **Pachinko mode**, increased course diversity, gradual stuck recovery instead of teleporting marbles, and additional materials/scenery.

## Modes

- **Free for All** — First marble to the finish wins.
- **Teams** — Choose 2–4 teams; team average finishing points decide the winner.
- **Pachinko Palace** — Marbles fall through a dense peg board into seven point slots (100 / 250 / 500 / 1000 / 500 / 250 / 100). Highest score wins, with finishing time as the tie-breaker.

## Available racing themes

| Course | Coin price | Highlights |
|---|---:|---|
| Pegboard Paradise | Free | Curved carnival board, side bumpers and staggered pegs |
| Tunnel Twister | Free | Covered tunnels, narrow inside walls, curved corners and launch pads |
| Funnel Frenzy | 300 | Funnel-like open bowl arcs, spinning obstacles and enclosed tunnels |
| Factory Frenzy | 800 | Spinner arms, spring bumpers and ramp launchers |
| Cosmic Chaos | 1,500 | Magnetic obstacles, neon tunnel corridors and high-speed jumps |
| Jungle Jumble | 2,000 | Tropical ramps, foliage and offset peg fields |
| Glacier Glide | 2,500 | Sliding patches, crystalline scenery and ice tunnels |
| Magma Mayhem | 3,200 | Volcanic jump pads, spring bumpers and slaloms |
| Coral Cove | 4,000 | Reef-themed obstacles, currents and underwater tunnels |

Pachinko is a free **game mode**, separate from the nine racing courses. Existing players automatically get Tunnel Twister unlocked, without losing coins or previously unlocked content.

## Controls

Use **Start Racing**, choose a mode and 2–6 players, customize marbles, then preview or regenerate the course. During the race, drag the screen to orbit the camera, pinch/scroll to zoom, or tap a leaderboard name to follow a marble.

Marble cosmetics never affect racing performance. Earnable coins, unlocks and results are stored locally in the browser on that device; clearing site storage may erase them.

## Testing and limitations

Before this release, **1,500 simulated races** passed across the modes, nine tracks plus Pachinko, course lengths and 2–6 competitors, with no unfinished marbles in that run. A separate render/UI smoke test passed for all ten environments. These are automated simulation tests, **not** verification on an actual iPhone or iPad.

This is still a lightweight JavaScript/WebGL prototype with **lane-constrained physics rendered in 3D**, not a production Unity rigid-body project. Tunnel arches use open skylight cutaways to keep racers visible. Large curved ramps and launch animations are simplified, not fully realistic 3D ballistics.

## GitHub Pages

This game is static: the repository-root [index.html](index.html) serves the entire experience. In **Settings → Pages** set **Deploy from a branch → main → /(root)**. GitHub Pages publishes pushes to main automatically.

_No software license has been added; rights remain with the repository owner._
