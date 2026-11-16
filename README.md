# Marble Rush 3D 🟡🔵🔴

A shared-screen, arcade-style **3D marble racing game** built for mobile Safari, iPads and desktop browsers. Set up **2–6 marbles** on one device and watch the obstacles determine the winner.

### ▶️ Play

**[Play Marble Rush 3D](https://m0998001.github.io/marble-rush/?v=6)**

No account or installation required. Each visitor plays a local session on their own device; the link does not connect friends into one online race.

## v0.5 — Home Screen icons and Pachinko as a stage

- **iOS Home Screen icon:** Added `apple-touch-icon.png` (180×180), 192×192 and 512×512 web app icons, and a web app manifest for standalone installation.
- **Install on iPhone or iPad:** Open the public link in **Safari** → Share → **Add to Home Screen** → **Add**. The icon and label **Marble Rush** appear on the Home Screen. If you previously installed the game, remove the older shortcut and add it again to update the icon.
- **Pachinko Palace is now a free stage, not a separate game mode.** Select Free for All or Teams, then choose Pachinko Palace under Course Type. Existing saved coin balances and unlocked courses remain intact.
- In Free for All Pachinko, the highest slot points win (time breaks ties). In Teams Pachinko, the highest **average slot score** wins. Other stages continue to use racing placement.
- Two game modes remain: Free for All and Teams. There are now **10 course types**, including Pachinko Palace.

## v0.4 — Visual track geometry repair

A phone screenshot revealed a major presentation defect in v0.3: the visual road was constructed from independently rotated rectangular segments. Those blocks were yawed in the wrong direction relative to the curved path, leading to jagged edges, disconnected-looking railings, and apparent gaps.

**The v0.4 renderer uses a different approach:**

- **Continuous road meshes:** The deck, underbody, shoulders, rail faces, top caps and lane lines are swept along exactly the same centerline as the marble simulation. No step-shaped deck sections or separated edge boards.
- **Correct curvature alignment:** Fixed a sign error in how rendered track objects rotate around the curved path.
- **Physical/visual correspondence:** Splitters, spinning arms, gates, side baffles and curved bowl barriers are drawn from the same endpoints as their collision segments.
- **Tunnel geometry:** Tunnel side walls and roof shoulders are continuous meshes that follow the track, replacing repeated disconnected boxes. Arched frames remain to communicate enclosure.
- **Less visual clutter:** Removed non-colliding overhead bars and reduced overly large peg decorations.
- **Clearer mobile screen:** Reduced the size of the iPhone race HUD, preserving more room for the course.

**Testing:** In addition to geometry seam/tangent calculations and render-path smoke checks for all ten environments, 1,200 simulated races passed across course types, 2–6 players and all three race lengths. These simulations cannot prove the visual quality or rendering performance of a physical iPhone. Screenshots and on-device feedback remain essential.

## Previous v0.3 updates



- **Curved courses:** Tracks now follow smooth, randomized, 3D S-bends. Cameras, guardrails, scenery, ramps and marbles follow the same track coordinates, not just a straight slope.
- **Real tunnel passages:** Funnel Frenzy and other later stages include tunnels with continuous side walls, overhead roof bands, arched ribs, and navigable entrances/exits. A dedicated **Tunnel Twister** course is free to try.
- **Active edge obstacles:** More bumpers mounted to the outside rail, plus short angled deflectors, so marbles encounter meaningful side-of-track interactions without being pinned against a wall.
- **Additional obstacles:** Moving spinner arms, short launch pads that send marbles on visible arcs, contoured hill ramps, booster plates, spring bumpers, and two-row peg slaloms.
- **Safer vortex bowls:** Formerly closed, trapping rings now have matching open curved walls with upstream and downstream gaps.
- **More complete courses:** A shallow start ridge gives each marble early contact, while hand-spaced slalom sections prevent consistently straight, obstacle-free lanes.
- **Mobile optimization:** Reduced WebGL pixel ratio and camera-based object culling for more practical phone performance.

Previously added in v0.2: **2–6-player limit**, **Pachinko board**, increased course diversity, gradual stuck recovery instead of teleporting marbles, and additional materials/scenery.

## Modes

- **Free for All** — First marble to the finish wins.
- **Teams** — Choose 2–4 teams; team average finishing points decide the winner.

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
| Pachinko Palace | Free | 7 scoring bins, dense pegs, high-score win conditions |

Pachinko Palace is a free **stage** in the course picker, available under Free for All and Teams. Existing players automatically receive this stage and Tunnel Twister without spending coins.

## Controls

Use **Start Racing**, choose a mode and 2–6 players, customize marbles, then preview or regenerate the course. During the race, drag the screen to orbit the camera, pinch/scroll to zoom, or tap a leaderboard name to follow a marble.

Marble cosmetics never affect racing performance. Earnable coins, unlocks and results are stored locally in the browser on that device; clearing site storage may erase them.

## Testing and limitations

Before this release, **1,500 simulated races** passed across the modes, nine tracks plus Pachinko, course lengths and 2–6 competitors, with no unfinished marbles in that run. A separate render/UI smoke test passed for all ten environments. These are automated simulation tests, **not** verification on an actual iPhone or iPad.

This is still a lightweight JavaScript/WebGL prototype with **lane-constrained physics rendered in 3D**, not a production Unity rigid-body project. Tunnel arches use open skylight cutaways to keep racers visible. Large curved ramps and launch animations are simplified, not fully realistic 3D ballistics.

## GitHub Pages

This game is static: the repository-root [index.html](index.html) serves the entire experience. In **Settings → Pages** set **Deploy from a branch → main → /(root)**. GitHub Pages publishes pushes to main automatically.

_No software license has been added; rights remain with the repository owner._
