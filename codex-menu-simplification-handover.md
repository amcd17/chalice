# Menu simplification handover

23 Nov 2026. Ported into the game as v0.376.

## What is in the game

The local flow is now:

Home -> Local -> Match Setup -> Start Game -> Class Select -> Ready -> 3 second kick-off -> match.

The v0.370 Local game type page and the four-box setup are no longer on that path. The old screens are still in `index.html` as unused code, so nothing else that referenced them broke.

## Files

- `index.html`: the game, v0.376. All of the work is here.
- `menu-redesign-mockup.html`: the approved home and cup transition reference.
- `match-setup-mockup.html`: the approved setup, map and options reference.
- `class-select-mockup.html`: the approved class select reference.
- `mock-assets/map-*.webp`: map art used by the mockups.

The mockups remain useful as a visual reference. They are not loaded by the game.

## Match Setup

`renderG()` in `index.html` builds the screen.

- Left column: LOCAL GAME, MATCH SETUP, the mode/match/bots lines, Map and Edit Game Options rows, the real Mausoleum plate, the mode-on-map caption, the thin loading bar, Start Game.
- Centre: the menu cup renderer.
- Right column: player count and the Thistle and Marigold rosters. `namePanel()` shows YOU or the generated bot name with a YOU or BOT tag. No classes are shown; classes are picked on the class select. With bots off, only the player is listed and the other slots read OPEN. Your team is first.
- Back returns to the home menu.
- Map opens the new Map page. Choosing a different map reloads into `?menu=setup`, the same as the old setup did.
- Edit Game Options opens the wide options page. The existing options are kept and laid out as rows. Bots are shown as a sub-list when on.
- Start Game builds the lobby roster if needed and opens the class select.

## The menu cup

`#menuCupWrap` and `#menuCupCv` are a second, full-window renderer behind the menu. The home crest is still the title canvas; this renderer takes over on Match Setup and its sub pages.

- It uses `makeChalice()` with cloned materials: dark bronze bone and a gold trim, so the cup reads darker than the in-match cup.
- Setup: scale 8.2, centre lane, tilted on the diagonal (z -0.16, x 0.09), spinning at 0.55 rad/s, dim .34.
- Options and Map: smaller, dimmer, further back.
- Entering setup from the home screen starts the cup at the home crest position and size, then eases it to the centre lane. Returning home hides this renderer and the title crest takes over again.
- The renderer stops when the menu is hidden or the title is showing.

## Class select

`renderClassSelect()` in `index.html` builds the pre-game screen. The in-match lobby, death and respawn screens still use `renderMatchS()`, so a match in progress is unchanged.

- Left: class name, role, HP, one-line description, and the three abilities with symbols, key and the descriptions from `MENU_CLASSES`.
- Centre: the live 3D class portrait (`data-live-portrait`) at 520x680 in the canvas, scaled by CSS.
- Right: the player's team roster, with the team name and colour. Each row is a class crest, the class name and YOU or BOT. No portraits, no player names, no role text.
- Bottom: the five class crests, with locked classes dimmed when duplicates are off, and READY at the bottom right.
- READY calls `launch()`, which starts the match. The existing `KICKOFF_T = 3` countdown handles the three seconds.
- Back returns to Match Setup.
- The player's class swap still goes through `pickClass()` and `lobbyClassSwap()`.

## Layout

The shell width is widened for setup, map, options and the pre-game class select. The home column is 780px instead of 620px. At 1500px and 1340px the setup and class columns step down. The short-height rules keep the class crests and READY above the bottom hint.

Checked at 1600x900 and 1280x720.

## Testing

- `node --check` on the extracted script.
- `npx eslint g.js | grep no-undef` prints nothing.
- Home -> Local -> Match Setup -> Start Game -> Class Select -> READY -> live Chalice match, at 1600x900 and 1280x720.
- Match ran on Mausoleum with bots and the HUD active.
- No page errors. The only network 404 is the favicon.

## Still old

- The in-match pause, death and respawn screens are the v0.370 layouts.
- The Classes and Tutorial pages in Extras are unchanged.
- The options page uses the existing segmented controls inside the new rows, not the chevron rows from the mockup.
- The Map page reloads the document to change the map, as before.
- The loading bar on Match Setup is decorative. Start Game goes straight to the class select.
- The mockup files still exist and should be kept in sync if the layout changes again.
