# Chalice: the whole game in one place

Current build: v0.389, 23 November 2026. Read this first, then `AGENTS.md` for the working rules. `scryball-backlog.md` is the long, version-by-version history; the `codex-*` files go deep on one topic each.

## What it is

A first-person medieval-fantasy class shooter, played against bots. Two teams, Thistle (purple) and Marigold (orange), five classes, one shared sidearm and one shared sword. It started as a remake of a Halo 3 oddball variant Alex made, and the feel still leans on Halo: quick health regen, burst rifles, a slightly floaty jump, and kills timed against a perfect battle-rifle kill.

The whole game is one file, `index.html`: three.js r128 from a CDN, every image embedded, no build step. It runs by opening the file in a browser.

- Repo: `https://github.com/amcd17/chalice` (branch `main`).
- Live site: `https://chalice-game.vercel.app/`. A push to `main` publishes it. Only commit or push when Alex asks; he pushes from his own terminal.

## Modes

- Chalice (the main mode). Kills only count while your team holds the cup. See the rules below.
- Divination. The original oddball: hold the crystal ball to score, pass it before it destroys you.
- Skirmish. Team deathmatch, mostly for testing.

## Maps

Mausoleum (the round crypt, the default), Basilica, Scrollwork and Church are in the menu. Cathedral is built (`buildCathedral`) but taken off the list until its layout is reworked; see `cathedral-mesh-audit.md` and the two Cathedral mockups in `mockups/`.

## The cup rules

- A cup holds 7 kills. In order they are worth 1, 1, 1, 2, 2, 3 and 5, so a full cup is 15. First team to 30 wins.
- The holder carries it. Hold F to drink: that banks everything in the cup for the team and kills the drinker (no death counted, no credit to the enemy). The holder moves at 40% speed while drinking.
- Tap E to pass to a teammate within 8 m. Hold Q to aim a throw.
- A dropped cup loses its newest kill every second until someone picks it up.
- Sword bonus: while your team holds the cup, every kill made with the sword, by anyone on the team, adds one extra point. A sword glyph rises into the team's cup box with "+1", and the killer sees "BY THE SWORD".
- The carrier loses his class primary and movement ability while carrying; the sword stays usable.

All of these are live sliders on the Chalice tab of the Tuning menu.

## Health and movement

Health starts to refill 4 s after the last hit and comes back fast, Halo style. Class speed varies a little: Skulker 1.12, Crusader 0.94, everyone else 1.0.

## The classes

Every class has the same layout: 1 primary, 2 Runic Repeater, 3 the sword; right click is the class ability, Q the field ability, Shift the movement ability. Damage figures below are what lands in play.

Crusader (code `knight`), Guardian, 145 HP
- Holy Blunderbuss: winds up 0.45 s, then eight pellets. 88 damage within 2 m, 73 at 4 m, knocks the target back. Two shots, then a 3 s reload.
- Bulwark (class): a wall of light in front of him for up to 4 s. Blocks enemy shots and movement; allies pass through. Recharges in 18 s.
- Holy Book (field): three shockwaves over 3 s that push enemies back. 12 s.
- Pious Charge (movement): raises the cross, then charges through enemies.

Arcanist (`sorcerer`), Controller, 130 HP
- Crystal Staff: tap for a quick bolt, or charge for a stronger one. Charging builds heat; overheat locks it.
- Ward (class): a glass dome on one ally for 12 s that mirrors every enemy projectile.
- Crystal Grenade (field): sticks to surfaces and enemies, bursts after 2 s. Stuck to an enemy, it kills them. 12 s.
- Float (movement): hold to float until the charge runs out.

Skulker (`goblin`), Rogue, 125 HP
- Infernal Daggers: 30 damage each, four throws a second. They stick in enemies and come back after the third throw or on R.
- Shroud (class): he vanishes for 6 s; enemies lose him beyond 4 m. His own attack breaks it, and that attack hits 25% harder for half a second. Recharges in 12 s. His alone, not the team's.
- Poison Smoke (field): blocks sight; enemies inside are 15% slower and take 4 damage a second. 12 s.
- Blink (movement): hold to mark a spot, release to vanish in smoke and reappear there.

Lampist (`lampist`), Healer, 130 HP
- Furnace Lantern: arcing fireballs, 40 on a direct hit and up to 20 splash, leaving surface fire that burns anyone standing in it. Six shots, then a 3 s reload.
- Lightbath (class): raises the lantern; a field of light travels with her for 12 s, healing her and nearby teammates. 18 s.
- Marking Lantern (field): thrown, hovers for 5 s and reveals enemies within 10 m through cover, Shrouded Skulkers included. 12 s.
- Flash Dash (movement): up to 5.25 m forward, 4.25 m other ways. 3.5 s.

Zealot (`brigand`), Vanguard, 135 HP
- Skeleton Rifle: 15 rounds, five three-round bursts. Each hit lodges a bone splinter in the target, up to 3, for 6 s. A Bone Sword hit on a splintered enemy shatters them all for extra damage and heals him 12.
- Rally (class): punches his fist up; a shockwave gives teammates within 10 m 20% move speed and 25% faster fire, reload and sword swings for 6 s, and clears slows. Enemies can see who is rallied (gold icon overhead, glow and embers at the feet); a rallied player gets a gold screen edge. 18 s.
- Powder Grenade (field): bouncing grenade on a short fuse. 12 s.
- Sprint (movement): hold Shift moving forward for 30% speed, up to 1.75 s.
- Bone Sword: his own look for the shared sword (key 3). Same numbers as everyone's; it is the blade that shatters his splinters.

Shared by everyone
- Runic Repeater: six 18-damage shots, up to four a second. Each spent gem comes back 3.75 s after it was fired.
- Bastard Sword: tap to slash, hold and release for a heavy lunge, R to parry. A parry opens the enemy for a 1.35x riposte. Usable while carrying the cup.

## Controls

Keyboard and mouse: left click fire, right click class ability, Q field ability (or aim a cup throw), Shift movement ability, 1/2/3 weapons, R reload (parry with the sword out), F drink, E pass, G call for a pass, Tab scores, Esc pause.

Gamepad (bumper jumper, Alex's layout): A jump, LB movement ability, RB class ability (drink while carrying), RT fire, LT throwable, X reload or parry, B pass, Y swap (hold for the sword), R3 sword, D-pad left call for a pass, View scores, Start pause. Light Halo-style aim assist, with a Settings toggle. Every menu works on the pad.

## How the game got here

- Scryball. A gridiron oddball game with a Y2K synth look: hold the ball to score. Classes arrived around v70 (knight, goblin, sorcerer).
- v113 to v123: renamed Dark Chalice, reskinned as medieval fantasy, and the Dark Chalice mode became the default: a cup that fills with kills.
- v128: the names players see changed (Crusader, Magus, Skulker). The code keys never changed, which is why the code still says knight, sorcerer, goblin and brigand.
- v188: the Lampist joined as the fourth class; the Brigand (now the Zealot) followed.
- v0.284: the cup rules took their current shape (7 kills, 1-1-1-2-2-3-5, drinking costs your life).
- v0.291: renamed Chalice.
- v0.347 to v0.348: every class's melee replaced by one shared sword on key 3; the Runic Repeater became everyone's key 2.
- v0.360 to v0.362: sword parry and riposte, weapon sway.
- v0.367 to v0.378 (22 to 23 Nov): bots taught the new kit; title screen with the turning in-game chalice and winking gems; full gamepad support; the sword swing and thrust rebuilt; Rifle magazine cut to 15 and the sword cup bonus, so the game gives a reason to close in; the cup box scoreboard; Menu v2 from another agent.
- v0.379 to v0.389 (23 Nov): Blunderbuss back to two shots; Lantern buffed; Repeater 3.75 s; splinters 6 s; swap classes with bots; the menu cup zooms between home and Match Setup; class cards rewritten (TEAM abilities now CLASS); Rally and Shroud reworked into two distinct jobs; every Q ability on 12 s, Bulwark and Rally on 18 s; folder sorted into `mockups/` and `old/`; darker, side-lit home and title cup; Back at the bottom of Match Setup and class select; class select shows the map camera; the Zealot carries his Bone Sword again.

## Balance, last measured

Six bot matches on Mausoleum at v0.378 (before the latest changes): kill/death ratios Crusader 1.45, Skulker 1.21, Arcanist 1.05, Zealot 0.87, Lampist 0.67. The Repeater was the top killer, then the Blunderbuss, then the sword. One team won 5 of 6, which is unexplained. Every change since has been aimed at those numbers, so a fresh run is due. Log every balance change in `codex-weapon-niches.md`.

## Open work (backlog, not to be built until Alex asks)

- Zealot splinter UI (mockup in `mockups/zealot-splinter-mockup.html`). Agreed: a SPLINTERED status with pips and a timer, plus a count over the enemy for the Zealot; no damage preview.
- Remove the dead blowgun dart code (nothing fires darts any more).
- Cathedral: a more natural layout and the floating artefacts.
- A Trapper class (a launcher primary was the favourite idea).
- Retake the tutorial screenshots, including the Sword slide.
- Scrollwork II.
- A fresh balance run, which should also count how often each ability is used, and check for a spawn-side bias on Mausoleum.
- Two handover notes (`codex-weapon-niches.md`, `codex-handover-hands.md`) were replaced by much shorter versions at 16:40 on 23 Nov; Alex is deciding whether to keep those or restore the full ones.

## Where things live in the code

Search by name. The main ones:

- Classes and kits: `MENU_CLASSES` (the cards), `loadoutRows` (weapon text), `TRIAL_LOADOUT`, `CLASS_HP`, `CLASS_SPEED`.
- Weapons: `TRIAL_REPEATER`, `TRIAL_FURNACE`, `TRIAL_RIFLE`, `TRIAL_DAGGERS`, `TRIAL_SPLINTER`, `BB_*` (Blunderbuss), `BOLT_*` (staff), `SWORD_SLASH`, `SWORD_HEAVY`, `trialTickWeapons`, `damage`.
- Abilities: `rallyCry`, `castShroud` and `breakShroud`, `LIGHT_*` (Bulwark), `LB_*` (Lightbath), `*_CD` constants for the Q abilities.
- Cup: `CH`, `CH_CUP`, `CH_PTS`, `chScoreKill`, `chTake`, `chDrop`, `SWORD_CUP_BONUS`, `chalSwordRise`.
- Menus: `localMenu`, `MENU_MODES`, `MENU_MAPS`, `CHALICE_LESSONS` (tutorial), `titleLoop`, `menuCup`.
- Gamepad: `padUiScreen`, `padUiTick`, `PAD_GLYPH`, `aimAssist`.
- Tuning: `TUNES` rows; saved values sit in localStorage, and `TUNE_OLD_DEFAULTS` drops old saved defaults whenever a number changes.

## Folder

- Top level: `index.html`, `AGENTS.md`, this overview, and the handovers agents use now.
- `mockups/`: mockups for pending or recent work, with `mock-assets/`.
- `old/`: built, superseded or abandoned files. Reference only.
- `_to_delete/`: safe to delete.
