# Chalice
(Called Dark Chalice until v0.291.)

First-person medieval-fantasy class shooter against bots. One file: `index.html` (three.js r128, no build step). Start with `chalice-overview.md`: the whole game, current numbers, history and open work. Version-by-version history: `scryball-backlog.md`.

## Folder layout
- Top level: the current build (`index.html`), `chalice-overview.md`, and the notes agents use now (`scryball-backlog.md`, `codex-weapon-niches.md`, `codex-sword-handover.md`, `codex-handover-hands.md`, the menu and git handovers, `cathedral-mesh-audit.md`).
- `mockups/`: mockups for work that is pending or recent, with `mock-assets/` beside them. New mockups go here.
- `old/`: built, superseded or abandoned mockups, test pages and handovers. Reference only.
- `_to_delete/`: safe to delete.

## Rules from Alex
- Bump `<div id="ver">Chalice 0.N</div>` on every change that gets published.
- Test in Chalice mode first.
- Send a mockup before any big visual or map change.
- Don't build new things unprompted. Backlog items stay backlog until asked.
- Record every balance adjustment in the playtest balance log in `codex-weapon-niches.md` so the next agent can pick it up.
- Never add a flashbang.
- Character hands are simple balls, with no articulated fingers in any view.
- Don't tie class identity to the cup.
- Prose and UI text: direct, human voice. No em dashes, no bold for emphasis, no words like leverage, robust, comprehensive, seamless, delve.
- Append `//` comments only at the true end of a line (a comment mid-line can swallow code).

## Before handing a change back
1. Extract the largest `<script>` block to a temp file `g.js`.
2. `node --check g.js`
3. `npx eslint g.js | grep no-undef` should print nothing.
4. Open the page in a browser and play a Chalice match.

## Roster
Crusader (`knight`), Arcanist (`sorcerer`), Skulker (`goblin`), Lampist (`lampist`), Zealot (`brigand`).

## Where things live (search by name)
- Chalice: `CH`, `CH_CUP`, `CH_PTS`, `chMult`, `chScoreKill`, `chTake`, `chDrop`, `CH_DRAIN` (kills per second internally, shown in the menu as seconds per kill).
- Cup HUD: `chalHudDraw` (top centre panel plus the F/E/Q prompt pill `#chalSub`), `CH_HEAT` (enemy colour ramp), `CH_TIER_COL`. Shroud smoke on allies: `GHOST_SH`, `GHOST_BODY`, `setGhost`.
- HUD v2: `NH_ST` (status chips), `NH_IC` (icons), `nhAbilities`, `nhAmmo`, `nhUpdate`.
- Tuning menu: `TUNES` rows and `TUNE_TABS`. Saved values are in localStorage key `scryball-tune`; `TUNE_OLD_DEFAULTS` migrates old saves.
- Smoke: `popSmoke`, `updateSmokes`. Shroud: `castShroud`, `breakShroud`, `isCloaked`.
- Melee and backstab: `resolveMelee`. Viewmodels: `buildVM`, `updateVM`. Bodies: `buildBody`, `updateBodies`.
- Combat feed: `kill(t, a, w)`, `pushFeed`.

## Cup rules in short
7 kills fill the cup. Values 1,1,1,2,2,3,5 (15 total), editable in the menu. Controls while carrying: hold F to drink, tap E to pass, hold Q to aim a throw. Drinking banks the pot and kills the drinker (no death counted, no credit to enemies). A dropped cup loses its newest kill every N seconds. First team to 30 wins.
