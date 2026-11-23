# Chalice menu and setup: handoff notes

This note goes with `menu-mockup.html`. It covers what each screen does, the exact copy, the icons, what is real and what is placeholder, and what has to change in `chalice.html` to wire it in.

## Files

- `menu-mockup.html` is the whole mockup in one file: HTML, CSS, JS, the portraits as base64 WebP, and the SVGs. No build step, no network except the Google fonts.
- `mock-assets/icons/` holds every icon as a standalone SVG: the five rail icons, the three mode emblems, the five class symbols, the padlock, and the big menu chalice.
- `mock-assets/shots/` holds 1280x900 screenshots of the local menu, game setup, kick-off, respawn and death screens, plus a size sheet for the new icons.
- The mockup footer says Chalice 0.295 to match the game at the time of writing.

## Opening the mockup

Open the file directly. The top bar switches screens:

- `A · MENU` is the rail menu.
- `G · SETUP` is the new game setup page.
- `S · PRE-GAME` is the lobby, with `KICK-OFF`, `DEATH` and `RESPAWN` sub-tabs.

Query parameters for jumping straight to a state:

- `?opt=A&nav=local` or `online`, `tutorial`, `settings`, `editor`
- `?opt=G&map=scrollwork&size=6&firstTo=40&len=15&bots=off&dupes=on&custom=on`
- `?opt=S&phase=dead` or `respawn`, `?opt=S&team=marigold`
- `?mode=divination` or `skirmish`

## Flow

1. `LOCAL` in the rail shows the game types: Chalice, Divination, Skirmish. Picking one is the only choice here.
2. `GAME SETUP` opens the setup page. It holds the map and every match rule.
3. `ENTER LOBBY` opens the pre-game screen. It shows the chosen map and a read-only match summary, then class, team, name, and ready up.
4. In play, dying shows the death screen. Both buttons lead to the respawn page, which is class selection plus deploy. Enemy classes are visible there.

`ONLINE` is the old friends screen, marked SOON. `TUTORIAL`, `SETTINGS` and `MAP EDITOR` are unchanged in structure.

## Screen notes

### Rail menu

Order: LOCAL, ONLINE (SOON), TUTORIAL, SETTINGS, MAP EDITOR. Icons: keep, globe, book, sliders, hammer. The footer shows the version.

The local page keeps the menu on the left and the turning chalice on the right. The mode cards are intentionally compact: no tags, small emblem, one line of description. `GAME SETUP` is a gold bar the same width as the cards.

### Game setup

Left column is the map list: three tiles, each with a 190x104 thumbnail of the map art, the map name and one line. The selected tile has a gold border, a gold left edge and a PICKED tag. Clicking a tile changes the selection and the lobby banner.

Right column has two groups. Each heading sits above its box, the same way MAP sits above the map tiles.

MATCH:

- MODE, with a CHANGE button that returns to the local page
- FIRST TO: 20, 25, 30, 40
- GAME LENGTH: 5, 10, 15 min

BOTS:

- ENABLED: On or Off
- TEAM SIZE: 1v1 to 6v6, shown when bots are on
- ALLOW DUPLICATES: Off or On
- CUSTOM CLASSES: Off or On. When on, five class buttons pick which classes bots may use. At least one stays on.

With bots off the box says "No bots. Open slots wait for players." Bottom bar repeats the summary and has BACK and ENTER LOBBY.

### Pre-game, kick-off

Top left is the map banner: KICK-OFF, map name, description. Top right is now a read-only match summary with four values: TEAM SIZE, FIRST TO, BOTS, GAME LENGTH. There is no round counter and no wave language.

Below: class list on the left in alphabetical order (Brigand, Crusader, Lampist, Rascal, Seeker) with number keys 1 to 5 in that order, class sheet in the middle (portrait, name, loadout, abilities), teams on the right.

Class rows show a solid padlock with no box around it when a class is taken on your team, plus the count if it is taken twice. OPEN when free. With duplicates off, the team cap applies: at 4v4 there is one of each class per team, and picking a taken class swaps with that teammate.

The ready bar holds the countdown at ON HOLD until every human is ready. Bots count as ready. At kick-off there is a DEPLOY button beside READY UP.

### Death screen

Card over a dimmed field. Copy: YOU DIED, Killed by Wren, "Go back in as Crusader, or pick a different class first." Buttons CHANGE CLASS and READY TO RESPAWN. Under them: RESPAWN IN 0:03. No wave wording anywhere.

Both buttons open the respawn page. CHANGE CLASS also pulses the class list once.

### Respawn

No map banner and no match box. Class list, class sheet, teams, and a respawn bar with the timer, the current class and DEPLOY. Enemy classes are shown here too. The team switch is hidden because you cannot change sides mid match.

## Copy deck

- Modes: Chalice, Divination, Skirmish.
- Chalice: "Kills only count when your team controls the chalice. The more kills, the greater the multiplier. Drink to score before it's too late."
- Divination: "Hold the crystal ball to increase your score. Pass before it destroys you and the points you just earned."
- Skirmish: "Fight to the death. The team with the most kills wins."
- Roles: Crusader GUARDIAN, Seeker CONTROLLER, Rascal ROGUE, Lampist HEALER, Brigand VANGUARD.
- Local header: LOCAL GAME / Select Game Type.
- Setup header: GAME SETUP / Match Settings.
- Buttons: GAME SETUP, ENTER LOBBY, BACK, CHANGE, READY UP, DEPLOY, READY TO RESPAWN, CHANGE CLASS.
- Settings row: "Divination: pass to score".
- Ability keys: team on RMB, field on Q, movement on Shift.

## Data the screens need

`mode`, `map`, `bots` (on or off, difficulty, duplicates and the custom class pool), `teamSize`, `firstTo`, `gameLength`, `classKey`, `team`, `playerName`, `ready` per human, and the roster with each player's class.

Defaults in the mockup: Chalice, Basilica, Normal, 4v4, first to 30, 10 minutes.

## Icons

New in this pass:

- `rail-local.svg`: castle front with two towers, gate and windows.
- `rail-online.svg`: wireframe globe.
- `mode-divination.svg`: crystal ball with a magic whorl and two motes.
- `mode-skirmish.svg`: two crossed swords, solid blades, crossguards and pommels.
- `class-rascal.svg`: the game's original dagger, restored. No new Rascal symbol is proposed.
- `lock.svg`: padlock used on taken class rows.

The rest are the game's own symbols and icons, extracted from `chalice.html`.

## What is placeholder

- Map art is the stylised SVG from the mockup, not screenshots of the real maps. The real setup page should show actual map renders.
- The menu art on the local page is one SVG chalice in the mockup, whatever mode is picked. In game it is a turntable of the real 3D asset for the selected mode: the chalice for Chalice, the crystal ball for Divination, and two crossed weapons for Skirmish. Use the game models so the menu matches what players see in play.
- Portraits are real renders captured from 0.294 at 200x262, one set per team.
- Ability names, descriptions and icons are copied from the game.
- Names, scores, the killer name and every timer are mock values.
- The ready-up countdown in the mockup is 5 seconds. The game kick-off timer is `KICKOFF_T`.

## Decisions already made

- No rounds. No "Round 1" line, no round setting.
- No waves. The game calls the respawn delay `RESPAWN_WAVE`; the timer can stay, the word should go.
- Map and match rules live on the setup page. The lobby shows them, it does not edit them.
- Class can change at kick-off and on every spawn, with no match-long lock.
- With duplicates off, the class cap still swaps you with a teammate rather than blocking the pick. With duplicates on it is ignored.
- Enemy classes are visible from kick-off onward.
- With bots off, rosters fill with OPEN slots, the summary reads BOTS Off, and the ready text drops the bots line.
- With duplicates on, taken classes show a count instead of a padlock, and no swap is implied.

## Open questions

- "Round size" came up but there are no rounds. It was read as team size and dropped. If it meant a round clock, say so.
- Should the chosen map, bots, size, first to and length persist between sessions in localStorage?
- First to is a free choice now. Modes may want different defaults, such as 25 for Skirmish.
- Does the ready-up check stay optional behind the settings switch that the mockup shows?
- Bot settings (on or off, duplicates, custom class pool) are not persisted yet in the mockup. They probably should be saved with the rest.
- Custom classes in the mockup remap a bot to the first allowed class when its own class is switched off. Real bots should pick from the pool with some sense of team balance.

## Wiring notes for chalice.html

- The game builds its menu and lobby in the same file. The mockup assumes the menu lives off-canvas or in a DOM layer above the renderer; keep the existing canvas and HUD untouched.
- Reuse `NH_IC.sym` for class symbols and `NH_IC.ab` for ability icons rather than duplicating SVG in the game. The new mode, rail and lock icons can be added to the same tables.
- Use `classCap()` with the chosen team size, and keep the swap behaviour.
- The cup values, 7 kills to fill and 30 to win, are game rules and do not change here. The wording moves from "bank" to "score" in the menu and tutorial; the game's own HUD text may still say bank.
- Rename the mode strings wherever the game shows Scryball and Scrum.
- Dying should open the death screen first, then the respawn page on CHANGE CLASS or READY TO RESPAWN. The respawn page is the class picker that the game already uses at spawn.
- The ready-up countdown should gate `KICKOFF_T`, not replace it.
- Test in Chalice mode first and bump the version in `#ver` when this ships.
