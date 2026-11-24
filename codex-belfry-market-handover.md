# Handover: build the Belfry Market greybox

You are building a new map for Chalice, a single-file browser game (`index.html`, three.js r128, no build step). It's a playable **greybox**: plain boxes and ramps, with no art pass yet. The point is to walk it at real scale and run bot matches to check balance.

Read `AGENTS.md` first. The layout was approved by Alex on 24 Nov 2026. The visual plan is `mockups/belfry-market-plan.html` (open it in a browser; the buttons switch between street level and the catacomb). The design write-up is `claude/belfry-market.md` in the CHALICE project.

## 1. What the map is

An asymmetric 3v3 Chalice map, about 96 × 68 m. A village square where the bell tower has fallen across into the night market, with a catacomb underneath. The chalice sits on a dais in the middle of the square, under the bell hanging from the tip of the fallen tower.

- **Thistle (team 0), the church, west.** They spawn inside a large church with pillared aisles. They own the height: the fallen tower is a ramp from 8 m down to 4 m, ending over the dais. The church's south wall has collapsed into a rubble slope down to tanners' lane. A crypt stair inside the church leads to the catacomb.
- **Marigold (team 1), the market, east.** They spawn in a covered market hall, which has an upper gallery with a balcony 4 m up overlooking the square. They own the cover: stall alleys and tanners' lane. An ossuary stair leads to the catacomb. A scaffold at the tower tip lets them climb onto the ramp.
- **Catacomb, contested.** A bone hall runs from the church crypt (west) to the ossuary (east), through a large cult chamber under the dais. There are two ways up to the square: the well (Thistle's side) and a cellar hatch (Marigold's side). A passage runs south from the chamber to a spot under an open grate in tanners' lane, and the grate is one way down.

## 2. How maps are built in `index.html` (read these first)

- `MAPS` and `PLAYABLE_MAPS` (about line 3992). Add `belfry:'Belfry Market'` to `MAPS`. Add it to `PLAYABLE_MAPS` only when it's ready to show in the menu. Until then, load it with `?map=belfry&edit=1`, since `MAP_ID` accepts any `MAPS` key in edit mode.
- `ARENA_X`, `ARENA_Z` and `mapOut()` (about line 4006) are chains of `MAP_ID === ...` checks. Add a branch for each.
- The builder dispatch is at about line 6077 (`EDREC.on = true; if(MAP_ID === 'cathedral') buildCathedral(); ...`). Add `else if(MAP_ID === 'belfry') buildBelfry();`.
- **Building blocks:**
  - `addBox(cx, cz, w, d, y0, h, style)` makes a solid axis-aligned box. Style is `'stone' | 'blue' | 'red' | 'wood' | 'none'`.
  - `mkOBB(...)` makes a rotated box.
  - `ramp(x0, z0, x1, z1, width, y0, y1, mat, base)` makes a walkable slope. Note that `ramp()` multiplies by the map scale `MS`, so set `MS = 1` at the top of your builder, as `buildMausoleum()` does.
- `buildChurch()` (about line 5331) is an existing **greybox** with rooms, arches, a courtyard and a mezzanine. Copy its style.
- `SPAWNS` (about line 6078). Every existing map mirrors team 0 and team 1 with `s = ±1`. **This map is not mirrored**, so list each team's spawn points explicitly, with 6 to 8 per team at the right floor height.
- Bot navigation is `buildNav()` (about line 6153). Add an `else if(MAP_ID === 'belfry')` branch that calls `addNode(x, y, z)` on a grid at each floor height, plus a node partway along each long ramp (see the mausoleum branch). Links are made automatically by `walkable()`. **Keep the node count under about 1,500**, because the route table is all-pairs and grows with the cube of the node count.
- `MENU_CAM` (about line 16512) is the orbit camera used on the menu, before kick-off, while dead, and in the spare quarter of 3-player split screen. Add `belfry:[rx, rz, height, lookY]`.
- `MENU_MAPS` (about line 15158) holds the map card text for the menu, and the menu art is in the same area.
- **The chalice home is fixed at world (0, 0).** `chalHome()` takes the highest surface below y 30 at x 0, z 0. Put the dais at the origin, and **don't put any solid (the bell, the tower tip) directly above (0, 0)**, or the chalice will spawn on top of it.
- There's no ladder mechanic. The class jump is 1.62 m high, and `MANTLE` lets you pull up onto ledges 1.5 m above your feet (3 m for the Lampist). Every vertical connection must be a ramp, stairs (ramps), a mantle-height step or a drop.

## 3. Heights (suggested)

The game treats very low y as out of the world (fall reset under y −20, projectile cleanup under −8), so keep everything at y ≥ 0. Put the catacomb at the bottom:

| Level | y (floor) |
|---|---|
| Catacomb floor | 0 (ceiling about 3.2) |
| Street, square, market, lanes | 4 |
| Church floor and churchyard | 6 (2 m above the square) |
| Market hall gallery and balcony | 8 |
| Fallen tower ramp | 12 at the stump end down to 8 at the tip |
| Tower stump top | 12 |

The street ground is a slab: solid boxes from 0 to 4 everywhere except over the catacomb, where it's a 0.6 m slab from 3.4 to 4 with the openings listed below.

## 4. Coordinates (from the plan; 7 px = 1 m, dais at the origin, −z is north)

All values are in metres. They're centres or min/max corners. Treat them as a starting point and adjust for feel.

- **Bounds:** x −51 to +45, z −34 to +33. The map is not centred on the dais, so write a custom `mapOut` box; for `ARENA_X`/`ARENA_Z`, use the larger half-extents (about 52 and 35).
- **Church (Thistle):** min (−49.4, −20.6) to max (−29.4, 20.0), floor y 6.
  - Two rows of pillars at about x −44.5 and −34.8.
  - Altar on the west wall.
  - Doors in the east wall facing the lychgate, at about z −5.
  - **South wall** (z 20) collapsed between x −45 and −34: a rubble ramp from y 6 down to y 4, running south-east out to tanners' lane, through a break in the churchyard wall at x about −23.4, z 20 to 28.
  - Crypt stair down to the catacomb at about (−39, 7), inside the church.
- **Churchyard:** from the church to the wall at x −23.4. Tall tombs, gravestones, a yew in the north yard at about (−39, −24). Lychgate (a gate you walk through) at (−23.3, −4.9).
- **Tower stump:** centre (−26.4, −27.3), about 7.7 × 7.7 m, top at y 12. Climb it from the churchyard side, for example with an internal stair ramp.
- **Fallen tower ramp:** from (−22.6, −27) at y 12 down to (−1.1, −5.6) at y 8, about 3 m wide.
  - A gap of about 2 m at (−11.4, −18.3) that you jump. It must be within the class jump: about 6.7 m of flat distance at full speed, so 2 m is easy.
  - A low wall (about 1 m high) across it at (−6.4, −13.3).
  - The tip ends about 5 m short of the dais, at (0, −4.6), so it is not above (0, 0).
- **Bell:** a visual only, hanging off the tip at about (0, −4.6), y 6 to 7. No collision, or a small one not above (0, 0).
- **Scaffold (Marigold's climb onto the tip):** at about (2.7, −1.7). It's a stack of mantle-height boxes (1.4 m steps) from the square (y 4) up to the tip (y 8).
- **Square:** min (−19.4, −12) to max (13.4, 12.3), y 4.
  - Dais at (0, 0): a round platform about 3.7 m across, 0.4 m high.
  - Keep a clear ring with a radius of about 6.5 m around it.
  - Cover pieces (each about 1.2 to 1.6 m high, 1.5 to 3 m wide): market cross (−12.9, −1), bell frame (12.3, 9.9), toppled stall (10.7, 0, rotated about −28°), and carts and crates at (−13.6, −7.1), (7.1, 7.1), (7.1, −6.3) and (−3.1, 8.1).
- **Well (Thistle's way up from the catacomb):** at (−10.3, 6.9). An opening in the street slab with stairs inside it (no ladder exists), from y 0 up to y 4.
- **Cellar hatch (Marigold's way up):** at (4.6, 10.9), built the same way as the well.
- **Tower lane (north of the square, under the shaft):** rubble chunks (1.2 to 1.8 m high) at about (−17.4, −18.6), (−11.7, −13.7), (−8.6, −26.6), (−1.7, −22), (5.4, −17.4).
  - A broken belfry section you can walk through at (11.7, −27.4), about 7 × 6 m: three walls and an arch.
- **Tanners' lane (south):** min (−19.4, 18.3) to max (16.3, 26.9), y 4. Covered stalls (roofs 2.6 m up, with posts) along it.
  - **Open grate** at (0.1, 20): a 2 m opening in the street with a grate model at its edge. Dropping in lands you in the catacomb's south passage at y 0. It's one way, so no stairs back up.
- **Market quarter (Marigold):** from x 16.3 east.
  - Stall rows with awnings (low boxes and roofs) and lantern alleys north and south of the hall.
- **Market hall:** min (31.1, −11.7) to max (43.4, 12.6), floor y 4.
  - Spawn inside.
  - **Upper gallery** along the west side at y 8 (about 3.4 m wide), with a stair ramp up inside the hall at about (37, 6).
  - **Balcony** sticking out of the west wall at (30.3, 0), about 2.3 × 7 m, with a 1 m parapet. It overlooks the square and the top of tanners' lane.
  - Big doors west, onto the square side.
- **Ossuary stair (Marigold down to the catacomb):** at about (25.7, 7.3), from y 4 down to y 0.
- **Catacomb (y 0):**
  - **Church crypt:** min (−43.1, 2.6) to max (−26, 11.1).
  - **Bone hall:** about 4.5 m wide, from the crypt east along z about 7, rising toward the chamber and continuing east to the ossuary.
  - **Ossuary room:** min (22.6, −3.1) to max (31.1, 9.7).
  - **Cult chamber:** under the dais, centred about (0, 1), an oval about 16.6 × 13 m (radii 8.3 by 6.6). It has four pillars at about (±6, −3) and (±6, 4.6), a ritual circle on the floor and a small altar at its south side. A grate in its ceiling under the dais shows the chalice above, but is solid to walk on.
  - **Well and hatch stairs** come down into the bone hall either side of the chamber.
  - **South passage:** about 3.4 m wide, from the chamber's south side to the drop point under the open grate at (0.1, 19.7).
  - **Distances:** crypt to well and ossuary to hatch should both be about 16 m, so the tunnel is contested. Measure once built and adjust the stair positions to keep them even.
  - Lighting: dark, with candles in the chamber.

## 5. Spawns

- **Thistle:** 6 to 8 points inside the church nave, y 6.01, spread between the pillars, about x −44 to −34, z −10 to 10. Facing yaw: east, toward the square.
- **Marigold:** 6 to 8 points inside the market hall, y 4.01, about x 34 to 42, z −8 to 8. Facing yaw: west.
- **Check:** both spawns should be about 30 m of walking from the dais. Measure the real paths (Thistle out the doors and lychgate, Marigold out the hall doors) and move spawns until they're within about 10% of each other.
- `respawn()` sets yaw with a per-map ternary (`MAP_ID === 'church' ? ...`), so add a branch: team 0 faces +x, team 1 faces −x.

## 6. Bot navigation

- Add node grids:
  - every 4 m at y 0 inside the catacomb rooms and passages only
  - every 4 m at y 4 on the street
  - y 6 in the church and churchyard
  - y 8 on the gallery
  - a line of nodes down the fallen tower ramp, either side of the gap.
- Add nodes in the middle of each ramp and stair (the mausoleum branch does this with `RAMPS`).
- The one-way grate drop works by itself: `walkable()` allows drops (`maxDrop`) but not climbing back. Check that bots use the catacomb at all. If they never do, add `NAV_EXTRA` links or nodes at the stair tops.
- Check that bots can reach the tower tip (via the scaffold and from the stump) and the gallery.

## 7. Testing (sandbox harness, see `claude/handover.md`)

- `python3 mk.py` builds `test.html`. Serve it on port 8765. `node t6.js` runs a bot match and must end `ERRORS 0`. Point it at the new map with `?map=belfry` (the harness loads `test.html?test`, so add the map param, or set localStorage `scryball-map` to `belfry` in `evaluateOnNewDocument`).
- Take screenshots from inside each spawn, from the tower tip, from the gallery balcony, in the cult chamber, and from the dais.
- **Balance:** run at least 10 bot matches in Chalice mode with Thistle and Marigold swapped (switch `MY_TEAM` or swap which side spawns which team), and record the win rate per side. Report back if one side wins more than about 60%.
- Check that the chalice spawns on the dais, not on the tower or the bell.
- Check split screen still works on this map (`node sp6.js 4` with the map param).

## 8. Don't

- Don't do an art pass yet. Use `MATS.stone`, `MATS.wood`, `MATS.blue` and `MATS.red` and simple shapes, like `buildChurch()`.
- Don't mirror anything. The two halves are deliberately different.
- Don't put a solid above (0, 0).
- Don't add a ladder mechanic without asking Alex. Use stairs.
- Don't add it to `PLAYABLE_MAPS` (the menu) until Alex has walked it.
- Alex pushes to GitHub; agents commit locally only. Bump the version in `#ver`.

## 9. Open ideas (not in scope unless Alex asks)

- Hitting the bell makes it toll across the map, giving away the shooter's position (a natural fit for the planned Bellringer class).
- Swapping ends at half time if bot balance comes out uneven.
