# Basilica redesign: build plan

The visual plan is `basilica-plan.html` and `mock-assets/shots/basilica-plan.png`. The drawing is schematic. This note has the real numbers from `chalice.html` and the order I would build it in.

## The problem

The arena floor is 40 by 26. The first tier runs at 5 m, the seating rises to a top tier at 12.5 m, and the top tier is the upper level. It is open around the long sides, so two players on opposite tiers have a long, clean line, and the floor is a Seeker range. The chapels hang off the tier but do not shape the fight.

## What exists already

- `N = 48` around the ellipse, `ARENA_A = 40`, `ARENA_B = 26`.
- Podium at 5 m, first tier walkway from 42 by 28 to 50 by 36 at 4.5 to 5 m.
- Four seating steps, tops at 7.5, 10, 12.5, 12.5, from 50 by 36 out to 66 by 52.
- Top tier at 12.5 m, 62 by 48 to 66 by 52.
- Four chapels at `ROOM_K = [9, 15, 33, 39]`, two per long side. Platforms at 10 m, roofs at 17 m, ramps down to the 5 m walkway.
- Cathedral wall at 66 by 52 to 67.5 by 53.5, up to `CATH_WALL = 34`. Dome above.
- Nav already has nodes on the top tier at 12.5 every 15 degrees, on the chapels' raised floors at 10, and along the corridors at 5.

The drawing compresses the seating ring so the rooms read. Build to the numbers above, not to the drawing.

## Phases

Each phase gets a flag, so it can be switched off and compared with the current map.

### 1. Ground cover (`BAS_COVER`)

- Rood screens at x = ±12, in two pieces each: z -19 to -4 and z 4 to 19. Height 8.5 m, thickness 1.2 m. Central gap of 8 m, aisle gaps beyond 19 m. Add a lintel over the central gap at 5.5 m so it reads as an arch.
- Rood loft: solid screen from 8.5 to 13 m over the same span, so the top tier cannot see over it into the crossing.
- Dais arcade: four low wall segments on a circle of 8.4 m at 3 m high, leaving the four ramp openings. Keep the trellis.
- Colonnade: eight columns at 26 by 17, angles 22.5 + 45k. Radius 0.8 m, height 8 m, with a simple capital.
- Pews: four blocks at x ±24, z ±11, 12 by 4.5 m, 1.1 m high, with slat lines. Solid collision.

### 2. Top tier rework (`BAS_TOPBAY`)

- Cut the top tier into three bays per long side, between the chapels. Pull the middle bay back 1.2 m toward the wall, and put a 1.5 m buttress at each joint. The tier stays at 12.5 m.
- Parapet along the inner edge at 1.2 m, with crenels. Today the tier has no rail.
- Hang banners from the roof between bays, from 17 down to 13 m, offset so there are gaps. They cut the cross-arena line and leave the floor alone.
- Stairs from each chapel platform at 10 m up to the tier at 12.5 m, at the back of the chapel. The chapel becomes the vertical link.

### 3. Bridge and drop (`BAS_BRIDGE`, `BAS_DROP`)

- Bridge at the +x apse end, across the short axis, at 12.5 m. Width 2.2 m, length as needed to meet the two tier ends. A 2.5 m gap near the far side. A low parapet on one side only.
- Choir box at the north end of the bridge: a 6 by 5 m room with an organ front for cover.
- Drop at the -x end: a hole in the tier down to the first tier at 5 m, with a rubble pile. One way. If a 7.5 m drop feels too harsh, drop to the chapel platform at 10 m instead and use its ramp.
- No second bridge. The loop is the point.

### 4. Nav and bots

- Add nav nodes along the new bays at 12.5, on the bridge, and at the top of each new chapel stair.
- Do not add a node back up the drop.
- Bots need a link from the chapel platform to the stair, and from the bridge to both tier ends. Test a full loop with bots before tuning anything else.
- Check the bridge is wide enough for two bots to pass. If not, widen to 2.6 m.

### 5. Spawns and cup

- Spawns on the first-tier walkway outside each chapel door, at 5 m, under the chapel front. Not inside the room.
- Cup stays on the dais, inside the arcade. Check that drops settle against the arcade or the pews, not the open floor.
- Check the beacon is still visible from the tier and the bridge, without a clean shot at the dais.

### 6. Dressing and light

- Stone and timber for the screens, pews and bridge. The choir box gets an organ front and a rail.
- Banners in the existing cloth material, dark red.
- Dust shafts from the dome, darker aisles. The bridge can take a shaft so it reads as a landmark.
- Keep the vines and the trellis. They tie the new work to the old map.

## Budgets to test

- Floor line 30 m maximum, 34 m down the two aisles.
- Gallery bay line 20 m maximum, 22 m down into the aisle.
- No clear 52 m line between the two galleries.
- Waist cover within 3 m of any 10 m of travel.
- Every route to the cup has at least two entrances.

## Risks

- Screens to 13 m may block too much of the tier's view and flatten the upper level. Test both 11 m and 13 m lofts.
- The bridge can become the only fight. Watch whether the drop and the chapel stairs are used as much as the bridge.
- Bots may not use the tier or the bridge without explicit links. Budget time for the nav pass.
- The top tier is already at 12.5, so do not add a second gallery inside the arena. Use the tier.
- Fall from 12.5 to 5. Decide early whether that hurts, and dress the landing either way.

## Order

1. Flags and the screenshot test at the current map.
2. Ground cover, screens first. Play a few rounds with no other change.
3. Top tier bays and parapet.
4. Chapel stairs and nav.
5. Bridge, then the drop.
6. Spawns, cup, dressing.
7. Tune sightlines and bot links.

Test in Chalice mode first, then Divination and Skirmish. Bump the version in `#ver` when it ships.
