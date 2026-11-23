# Menu simplification handover

23 Nov 2026. Mockups only. Nothing in this handover is ported into the game.

## What this is

The simplified local flow Alex asked for:

Home -> Local -> Match Setup -> Start Game -> Class Select -> Ready -> 3 second countdown -> match.

It replaces the v0.370 four-box setup page and the Local "Select Game Type" page once it is approved. The current game still uses the v0.370 menu v2.

## Files

- `menu-redesign-mockup.html`: the home menu and the cup exit transition.
- `match-setup-mockup.html`: Match Setup, Map and Edit Game Options.
- `class-select-mockup.html`: the pre-game class select and countdown.
- `mock-assets/map-*.webp`: the real map art for the plate and map list.
- `mock-assets/thistle_*.png`: class portraits, used only for the large centre figure.
- `mock-assets/icons/class-*.svg`: class crests, used in the rosters and the crest row.

Run a static server from the repo root, for example `python3 -m http.server 8788`, then open:

- `http://127.0.0.1:8788/menu-redesign-mockup.html`
- `http://127.0.0.1:8788/match-setup-mockup.html`
- `http://127.0.0.1:8788/class-select-mockup.html`

## Flow wiring

- LOCAL on the home menu runs the exit transition and lands on Match Setup. The old Local game type page is skipped.
- Start Game opens the class select.
- Back on Match Setup returns to the home menu. Back on Map and Options returns to Match Setup. Back on the class select returns to Match Setup.
- Ready on the class select locks in and runs the 3 second countdown, ending on MATCH STARTING.

## Match Setup

Layout at 1600x900:

- Left column 540px: MATCH SETUP, mode, match summary, Map row, Edit Game Options row, Mausoleum plate, caption, loading bar, Start Game.
- Centre lane: the chalice.
- Right column 430px: player count and the Thistle and Marigold rosters.
- At 1440 the columns are 500 / lane / 390. At 1280 they are 430 / lane / 350.

The plate is the real Mausoleum image. Under it: CHALICE ON MAUSOLEUM, FIRST TO 30, 10 MIN. Then a thin loading bar. Then Start Game. There is no small READY text.

Bots live in Edit Game Options as an ENABLED row with difficulty, duplicates and custom classes in a sub-list. Turning bots off removes the sub-list.

## The chalice

The cup is the same `buildChalice()` mesh from the menu mockup.

- Scale 8.2, about 700px tall at 900px high. That is double the previous 4.2.
- Tilted on a diagonal axis: the pivot sits at z -0.16 and x 0.09, and the cup spins around its own axis. The rim leans and the gems travel on a diagonal.
- Spin 0.55 rad/s. Dim 0.46, canvas opacity 0.78, with a larger gold halo.
- `fitCup()` measures the plate and the right column, then shifts the cup into the centre lane and caps its scale if the lane is too narrow.
- It bobs slowly and takes a small parallax from the pointer.

## The transition

The home menu cup starts above the wordmark. On LOCAL:

1. The wordmark, rows and footer fade out over 0.35 s.
2. The cup travels down to the middle of the screen, tilts onto the diagonal, spins up and zooms to scale 10.5 over 1.25 s.
3. The browser goes to Match Setup when the zoom finishes.
4. Match Setup opens on a close camera with the cup at scale 10 and pulls back to its centre lane over about a second.

There is no black overlay. The previous version ramped a full-screen black layer over the last part of the exit, which made the two screens look like separate fades. It is removed. The next page is prefetched so the cut goes from the huge cup straight into the Match Setup cup. The pages are still two documents, so a real port should do this with one renderer that survives the screen change.

## Class select

Layout at 1600x900:

- Left: class name, role and HP, the one-line description, and the three abilities. Each ability shows its symbol, name, TEAM/FIELD/MOVEMENT label, key and a short explanation.
- Centre: large class portrait over the Mausoleum background, with a crest watermark and floor glow.
- Right: THISTLE roster, 440px wide, rows 72px tall. Each row is a class crest icon, the class name, and YOU, READY or LOCKED. No portraits and no role text in the roster.
- Bottom centre: the five class crests, locked classes dimmed.
- Bottom right: READY. It switches to READY locked and shows the chosen class underneath.

The ability descriptions are copied from `MENU_CLASSES` in `index.html` so the mockup and the game say the same thing. If an ability changes in the game, update the four strings in the `CLASSES` array at the top of `class-select-mockup.html`.

## Sizes checked

1600x900, 1440x900 and 1280x720. The roster, crest row, READY button and class details stay clear of each other at all three. At 1280 the class details panel narrows and the roster drops to 360px.

## What is not done

- Not ported into `index.html`. The game at v0.372 still has the v0.370 menu v2: four setup boxes, the Local game type page, and the lobby class cards.
- Home Extras, Settings and Online are still the old mockup panels.
- The loading bar is decorative. Start Game goes straight to the class select.
- The transition crosses two HTML documents. There is no single persistent canvas yet.
- The rosters and match values are static. Only 3v3 is shown. Only Mausoleum and Cathedral are enabled in the map list.
- No gamepad focus is wired in these three mockups; keyboard and mouse only.

## Next step

Wait for Alex to approve the flow, then port it into the real menu. The likely order is: one persistent cup renderer for both screens, Match Setup with the three rows and the plate, class select with the swapped roster, then the countdown into the existing match start.
