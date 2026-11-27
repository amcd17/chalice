# Chalice backlog (formerly Dark Chalice, before that Scryball)

Ideas parked for later, and the current design for reference.

## Versions
- v197-205: seeker ward moved to G (right click free), then Aegis on right click (40 shield, 4 s, 12 s cd, 30 m, on the teammate nearest the crosshair). Rascal blowgun on right click (dart marks one enemy 5 s: team sees outline through walls, takes 1.2x from his team, 10 s cd). Fire flask burns on walls too. Scimitar always one-handed, 50, no chalice penalty. All throwables 20 s. Drinking resets all the drinker's cooldowns. Rascal back to the grapple (RASCAL_DASH=false). Crusader G is now a holy book (team-tinted leather, gold bindings): lands, falls open, thin ring bursts 5 m, knocks enemies back, 25 to 10 dmg, pages flutter; grenade kept in code for the Brigand. Settings grouped within each class tab by Body / weapon 1 / weapon 2 / right click / G / Shift, every list checked against the sliders; new sliders for grapple range and speed, arbalest reload with the chalice, scimitar swing time. End screen fixed for Chalice (cup held, drinks, holder kills, betrayals; no ball columns).
- v195-196: Rascal reworked as a skirmisher (card: "Skirmisher"): throwing daggers are his main weapon at range (speed 55, grab two more in 1.2 s, cd 0.32, sliders), bots circle at about 10 m and throw, switch to the dagger up close or for an open back. Throwables on G, one per class (Alex: the seeker's ward is his own): rascal smoke bomb moved from right click to G (right click free), crusader grenade (bounces, 1.8 s fuse, 4.5 m, 90 to 15 damage, walls shelter, hurts the thrower, 14 s cd), lampist fire flask (2.6 m patch for 5 s, 20 dps, 14 s cd; bots step out of fire). HUD "G" bar under the ability. Alex wants no class identity tied to the cup. Test v196: Rascal 1.24, Crusader 0.91, Lampist 0.89, Seeker 0.88; thrown daggers are the top killing weapon (80); grenades rarely kill (frag 6, fire 1).
- v189-194: flintlock ball 110 m/s (slider) and 2.2 s reload. The Lampist's lantern heals instead of marking: teammates within 8 m in her sight heal 12/s while it burns (not her), gold ring shows the reach; her bots stay about 4 m from their own holder and light it when someone near is hurt. Smoke: enemies inside an enemy rascal's smoke take 1.15x damage (alongside the choke); enemies inside your own smoke get a red outline only you see (stencil outline). Rascal: backstab 2.5x (slider "Dagger from behind"); Shift is now the champion's dash (RASCAL_DASH, 3 s, slider) instead of the grapple; bots pick on the back line, the hurt and the busy, circle anyone squared up to them, wait at the edge of a fight over a loose cup, throw daggers at a crusader facing them, back off from a healthy crusader, dash to sidestep, escape and get behind. Hammer 55 (was 60). Blunderbuss pellets 13 (8 x 13 = 104, a point-blank one-shot on 100-health classes). Bot tests: rascal K/D 0.82 with grapple + 2.5x backstab, 0.59 with the dash (he gets shot crossing open ground); Alex is trying the dash himself. Size 0.92 / 120 health for the rascal tested as no change.
- v188: the Lampist, a 4th class (code key lampist), in Mixed games (4v4 gets one of each; class cap is now a quarter of the team). Pale woman in a ragged dress, bandaged eyes under an iron birdcage. 100 health. Flintlock (1): 35 damage, 1.5x headshot, 1.5 s reload, muzzle smoke. Blunderbuss (2): 8 pellets of 12, full damage to 4 m, nothing by 10.5 m, 3 s reload (5 s holding the chalice, one-handed). Lantern (right click with the flintlock out): 6 s of oil, 20 s to refill, can't relight until a quarter is back; enemies she can see within 25 m are marked for 3 s, shown to her team as a red outline through walls and smoke, and take 15% more damage from her team; the marked player gets a MARKED toast. Leap (Shift): forward and up, 6 s cooldown. Climbs twice as high. Bots: hang back about 10 m, blunderbuss under 5.5 m, lantern on enemies near her or the objective, leap to escape or travel; her team's bots see marked enemies through smoke and prefer them. Settings: Classes/Lampist tab. First 4v4 Chalice test (3 maps x2): Lampist K/D 1.38, Crusader 1.03, Seeker 1.03, Rascal 0.67; flintlock is the top killer (100 of ~480).
- v129: key 1 is always the primary. Magus: 1 staff, 2 scimitar (was the other way round). Crusader 1 hammer, 2 javelin; Skulker 1 daggers, 2 smoke.
- v128: class names (what players see): Knight is now the CRUSADER, Sorcerer the MAGUS, Goblin the SKULKER (briefly Gremlin in v127). The code still uses knight/sorcerer/goblin, and older notes here use the old names. The Skulker's model is redesigned: lean and hunched, grey-green skin, lighter-brown leathers and cloth wraps, team colour only on the deep hood, scarf, short ragged cape and chest sash; face in shadow with glowing eyes and a cloth mask; pointed ears out through the hood; crouched wrapped legs.
- v127: the Goblin is renamed the Gremlin everywhere players see it (menus, class card, HUD, kill feed, Tuning). The code still calls it goblin. (This doc still says goblin in older notes.)
- v126: goblin dagger lunge shortened to 1.2 m (Classic only), so the daggers land from about 3.4 m between centres, the shortest of the three (scimitar about 4 m, hammer about 4 m). Slider: Goblin dagger lunge.
- v125: the sorcerer's sword is now a two-handed scimitar (medium length, curved). Reach 2.7 m (dagger 2.3, hammer 3.1) and a short 1.5 m lunge, so it lands from about 4 m between centres (was over 6 m); Scryball's sword keeps its long lunge. Sliders: Sorcerer scimitar reach and lunge. Design rule (Alex): every class has a one-handed primary (usable while holding the chalice) and a two-handed secondary.
- v124: the knight's kite shield is a solid object against shots (raised in front knee to chin, hanging at his left side, or slung on his back); shots that miss it hit him (over the top: head; under: legs; sides). Teammates' shots pass through. Javelins stick in it. While charging, shots that hit it are batted aside. Melee blocking unchanged (raised shield stops swings from the front 90 degrees). Thrown dagger headshot lowered to 1.5x (75 damage, never a kill on its own).
- v123: Dark Chalice mode (default game), new main menu (title, turning chalice, Classic and Scryball), modes renamed (Classes is now Classic; the gridiron mode is now Scryball), 10-minute matches.
- v122: knight rebuild (kite shield, javelin, shield charge).
- v121: goblin rebuild (two daggers, smoke bomb, world-only grapple).
- v120: class health, set damage, headshots.
- v119: Jump height slider on the Tuning page (take-off speed follows from height and gravity).
- v118: original flat thistle and marigold insignias drawn in code, replacing the stock-art versions.
- v117: engraved thistle and marigold insignias from Alex's artwork.
- v116: Ember renamed Marigold, with a marigold insignia; thistle leaves level, no crosshatch.
- v114: teams renamed Thistle and Ember, with new colours and insignias.
- v113: the game is renamed DARK CHALICE (page title, menu logo, footer). The ball is still the scryball, and saved settings keep their old keys.
- v112: the sorcerer holds the staff in his right hand only; his left hand comes out (glowing) to aim and cast the ground ward. In third person the staff sits at his right side.
- v111: levitating no longer drops the left hand out.
- v110: sorcerer rebuild (bursts with lock-on, ground ward, two-handed sword) and animated clamber for everyone.
- v109: X no longer swaps weapons (1, 2 and the wheel).
- v108: 1.01 plus team deathmatch.
- **1.01** (12 November 2026): named by Alex. Main menu with Classic and Classes, team choice, own name and number, kick-off and pre-spawn choosers, gridiron knights with plumed (Dash) and winged (Levitate) helms, three maps (Basilica, Scrollwork, Mausoleum), Fuse rules with optional Pass to bank. The menu footer shows the version.

## Movement feel (13 Nov)
- Alex: low gravity and very fast movement are no longer the point; it should feel a bit slower, still slightly floaty like the original Halo games. Decided: leave movement as is for now; Alex will tune it himself on the Tuning page (Movement tab: move speed, jump height (added v119), gravity).
- Now: gravity 7.4, jump about 4.8 m high and 2.3 s in the air, base run 8.2 m/s.
- Suggested: jump about 2 m high and 1.3 s in the air (gravity about 9.5), base run about 6.5 m/s; projectile, ward and pass speeds re-checked against it. Classic stays fast (to confirm).
- Knock-on: every map was built around 4.8 m jumps. Upper levels, ledges and bot jump routes need re-checking; some will need steps or ramps. Clamber, levitation and the grapple become more important.

## Teams (v114-116)
- THISTLE (royal violet #7a4fe8, glow #8a5cff, UI #a98cff) and MARIGOLD (red-orange #e8461e, glow #ff5a24, UI #ff7048). Colours chosen 13 Nov for colourblind separation and to stand apart from the gold chalice. Both teams are wildflowers (Marigold briefly Ember in v114).
- Insignias (v118): original flat, one-colour thistle and marigold drawn in code (based on the general shapes of Alex's references, no copied artwork). Thistle: spike fan on a narrow collar, round bud with side spines, stem, two spiny leaves. Marigold: round ruffled head with its centre in negative space (a ruffled ring cut around a round heart), small cup, stem, two leafy sprigs. Tinted pale thistle and marigold-gold. On banners in every map, knights' tabards (slight glow) and gridiron belt buckles. Tried and dropped: Alex's stock art (engraved, v117) and auto-traced flat silhouettes.
- The chalice stays as the knight's class symbol and the game's emblem.

## Menu and modes (v100; reworked v123)
- v123: main page shows only the title, a slowly turning darkened-gold chalice on a tilt, and two modes: Classic (the class game: knight, goblin, sorcerer) and Scryball (the gridiron mode). No portraits, no text above the title. Game row: Dark Chalice (default), Oddball, Team deathmatch.
- Main menu: two modes, Classic and Classes. Shared settings sit below them (map, Pass to bank, bots, mouse sensitivity, tuning, controls, ball rules).
- Classes: selection screen with a Violet/Amber team toggle (the three class portraits switch to the team's colours), the class cards, name, number, and the Mixed / All knights / All goblins / All sorcerers option.
- Classic: selection screen with a violet and an amber gridiron knight; click one to join that team. Name and number underneath. Portraits show the sword in the right hand and the cannon on the left shoulder (menu pose only).
- Name and number are auto-generated the first time, then editable and remembered.
- The player can join either team. HUD accents, the YOU chip, first-person hands and the end screen follow the player's team.
- Kick-off: everyone waits 3 s at their base before the first spawn. The match clock starts at kick-off.
- Choosing before a spawn (kick-off and every respawn): Classic picks Dash or Levitate with 1 and 2. Classes changes class with 1, 2 and 3; if a teammate holds that class, they swap with you at their next spawn, so the team keeps one of each.

## Team deathmatch (v108, for testing)
- Main menu has a Game row: Oddball or Team deathmatch. Works with Classic, Classes and the single-class options.
- One point per kill, first to 25 or the time limit. No ball, no ball marker or radar dot. The rules box switches to deathmatch rules.
- Bots hunt the nearest enemy. Kit sorcerers keep about 6 m back, goblins grapple in from range.
- Test results (3v3 bots): most matches reach 25 in 2 to 4 minutes. The All sorcerers match on Mausoleum only reached 14-2 in 5 minutes: sorcerer bots kill slowly there (slow bolts, low ceilings). A data point for the sorcerer redesign.

## Ball rules (v91)
- Fuse (default): holding scores 1 point a second, live. Team fuse of 10 s when a team takes the ball; each caught pass adds 3 s back. The glass fills and grows unstable as the fuse burns. If it fills while held or thrown it detonates: carrier dies, that possession's points are taken back. Burns out harmlessly on the ground.
- Pass to bank (toggle, off by default): points go into a pot in the ball. A caught pass (or a teammate picking up a drop) banks the pot and empties the ball. Enemy grab wipes it. The pot is the timer: the ball detonates when it fills at 20 (one carrier holding 20 s). Re-catching your own throw neither banks nor resets.
- No fuse ring around the ball; the ball's fill and instability are the timer.
- Q requests a pass ("BALL REQUESTED"); bot carriers throw to an open caller 85% of the time.

## Classic mode: gridiron knights (v94-100)
- Everyone is a gridiron knight: knight helm and plume, sleeveless team jersey with numbers front and back, steel shoulder pads, bare arms with big biceps, team-coloured bracers, chainmail shorts, tall boots. Violet has the lighter skin tone, amber the darker.
- Sword (one-handed, edge leads the swing) plus cannon. 1 sword, 2 cannon, scroll wheel toggles (X dropped in v109). Run speed x1.22.
- Dash: burst in your movement direction, about 6 m, 3 s cooldown. Levitate: sorcerer-style hover with a glow under the boots. Bots get a random mix.
- Reading an opponent (v101): dashers keep the plain knight helm with its plume; levitators have no plume and wear tall upright feathered wings on the helm (modelled on Alex's winged-helm reference, 20% smaller).
- Hold block to stop swords; tap block (raised within about 0.6 s) to bat a cannonball aside, which then belongs to you.
- A two-handed stance exists behind a switch (centred grip, both hands); Alex has seen renders and has not chosen it.

## Classes mode: class kit (built in v70)
Knight beats goblin, goblin beats sorcerer, sorcerer beats knight.
- Knight: warhammer (slow, one-hit kill, smashes the goblin's block), shield (stops anything from the front), shockwave.
- Goblin: dagger (fast, two hits, lunges), block (stops daggers; a freshly raised block deflects bolts; breaks against the hammer), grapple.
- Sorcerer: crystal staff (fires bolts, two hits; staff strike up close), ward (pentagon of runes, 120 degrees, stops hammer, shockwave and bolts; daggers slip through), flight. Left hand held out low, plain round hand, while flying.
- Squad numbers on backs in the team chalice colour. Teammates show class symbol (chalice, dagger, crystal) + number + name overhead; enemies show nothing.
- Open: the hammer uses the sword's sideways swing animation; an overhead smash would read better.

## Class rethink (planning, 13 Nov; sorcerer built in v110)
Order: the sorcerer first, then the other classes.
Alex: the classes are more distinct than before but less fun to play. Classic mode has speed and simplicity; the classes felt good when they had three abilities each. Each class should become more independent, with a whole toolkit of its own, and matchups should still play differently.
- Plan: Alex plays full single-class matches (All knights, All goblins, All sorcerers on the Classes screen) to judge each kit on its own, without the counter triangle.
- Things to note per class: does the basic attack feel good to land and fair to be hit by; time spent attacking vs defending vs waiting; moments where a tool is missing; the most fun and most frustrating moments.
- Classic's speed and simplicity are the bar.

### Sorcerer redesign (Alex's design, built in v110)
- Weapon 1, crystal staff:
  - Left click: bursts of three bolts with a slight lock-on (a gentle curve toward the enemy nearest the crosshair, only within a narrow cone). Bolts faster than the current 15 m/s.
    - Kill time matched to a perfect Halo 3 battle rifle kill: three bursts, one every 0.75 s, about 1.5 s in all. Each bolt is one-eighth of a kill, so three full bursts (9 bolts) kill with one miss to spare. (Halo 3 BR: 3-round bursts at about 2 a second; 12 rounds = 4 bursts to kill with headshots, 21 rounds on body shots; there are no headshots here, so the time is matched, not the burst count.)
  - Right click: ground ward. Hold to preview a glowing circle where it will land, release to cast. The ward lasts 2.8 s. Needs its own cooldown (suggested about 8 s).
    - Affects enemies only: it slows enemy fighters and enemy projectiles inside it. Allies and allied projectiles pass through unaffected.
    - Visible as a ring on the ground with a beam of light rising around its edge, so everyone can see the space it covers, including that it slows projectiles.
    - It takes over the pentagon ward's job in the triangle.
- Weapon 2: the classic two-handed sword (1 for sword, 2 for staff, scroll wheel toggles; X no longer swaps), with normal hold-to-block against swords and daggers.
- Ability: levitate, unchanged.
- Clamber: jump at a ledge, push forward, and pull up onto it. The sorcerer's clamber is the baseline for every other class (they'll be set faster or slower relative to it).
  - Suggested baseline: reach up to about 1.5 m above the top of your jump; pull-up takes about half a second, with a short camera dip and lift.
  - Decided: automatic. You climb whenever you push into a ledge mid-jump.
  - Bots use it too.
- Removes the current pentagon ward.
- As built (v110), all values on the Tuning page:
  - Bolts 44 m/s, 3 per burst 0.07 s apart, a burst every 0.75 s. 8 bolts kill (kill time about 1.6 s plus travel). Lock-on picks the enemy within about 7 degrees of the crosshair and turns bolts 0.4 rad/s; in testing that lands a burst aimed 1.3 m off at 20 m.
  - Built in v112: the staff is one-handed (right); the left hand casts the ward, or holds the chalice in Dark Chalice.
  - Ground ward: 3.6 m radius, 5.5 m beam, cast range 26 m, 8 s cooldown. Enemies inside move at 0.4x, enemy shots at 0.25x. Hold right click with the staff out to preview, release to cast; the HUD bar under the crosshair shows RELEASE TO CAST, OUT OF RANGE or WARD RECHARGING. Slowed players see SLOWED.
  - Sword: 2 hits to kill any class (Classic's sword still one-shots gridiron knights). Hold block stops swords, daggers and the ball; the hammer breaks through; no projectile blocking.
  - Controls: 1 sword, 2 staff, wheel toggles. Spawns with the staff.
  - Clamber: the old instant ledge snap (any class, ledge up to 1.5 m above your feet, in the air) is now a 0.45 s pull-up with a camera dip, for every class at the sorcerer baseline. Per-class multipliers exist, all 1 for now.
  - Bots: sword under about 4 m, staff beyond 6.5 m; cast wards on enemies at range or at their own feet against incoming shots.
  - Test (3v3 bots, deathmatch to 25): All sorcerers reached 25 on every map (Basilica 134 s, Scrollwork 170 s, Mausoleum 214 s; Mausoleum was 14-2 in 300 s before). In mixed Classes the sorcerers got about a third of the kills.
- Projectile defence: the ground ward slows enemy projectiles passing through it, so a sorcerer can cast it at his own feet and sidestep incoming daggers and bolts. That makes the ward a choice between offence and defence.
- The triangle is being loosened overall; the slow field is the sorcerer's main tool against the knight.

### Goblin redesign (planned, not built)
- Role: the flanker. Wins up close and from behind; no block, so a raised guard beats him head-on.
- Grapple (Shift): kept, but too strong today (mobility, gap close and kill setup in one). Decided: hooks walls and floors only, never enemies.
- Slot 1, two daggers (Alex, 13 Nov): an attack strikes with both daggers in quick succession. Throwing the left dagger halves his attacks (one dagger per strike) until he draws a new one (about 1.2 s). No block.
  - Suggested numbers: each dagger hit a quarter, so a double strike is half and two double strikes kill (about 0.5 s). Thrown dagger: half to the body, a kill to the head. Throw then two single stabs also kills.
  - Controls: left click = double strike, right click = throw the left dagger (matches the other classes).
- Slot 2, smoke bomb (Alex, 13 Nov): one bomb, already lit when he pulls it out (no lighting animation; the fuse never goes off in hand). Click to throw; he switches back to the daggers. No bounce: it bursts where it lands. Throw distance matches a Halo 3 grenade, tuned for our low gravity. To smoke himself, he throws it at his feet. Cooldown 20 s to start.
  - Cloud about 5 m across, about 5 s. Enemies can't see through it; lock-on bolts can't target inside it. The goblin sees people inside as glowing outlines.
  - Decided: the goblin's whole team sees through his smoke; enemies (including enemy goblins) don't.
- Backstab bonus: an idea to try later, not in the first build.

### Fourth class ideas (parked, 13 Nov)
- Name decided (13 Nov): LAMPER.
- Lamper's lantern (13 Nov): Alex likes seeing through walls but worries it makes him an auto-pick and weak on open maps. Suggested instead: a ~6 m pool of light where enemies are exposed (about +20% damage taken, outlined only while in the light) and smoke burns away; the pole sets targets alight (exposed, glowing trail) instead of revealing them through walls. Alex is thinking about it; he wants classes to feel weird and interesting thematically.
- Lamper kit draft: snuffer (or mace) as one-handed primary, lantern in the left hand (right click), lamplighter's pole as two-handed secondary (longest reach, slow), Flash on Shift, about 110 health, slowest class. Look: older, steady figure, long soot-stained coat, wide-brimmed hat or hood, gloves, satchel of wicks, brass lantern burning in the team colour.
- A dashing class (Alex: would be helpful). Thematically odd options: Mothkin (moth-person; fluttering dash with wing dust; sickle, dust pouch, scythe; a natural rival to the Lamper; suggested favourite), Harlequin (tumbling jester with bells; dagger, juggled weights, bladed staff), Hareling (hare-folk; huge bounds; sickle-sword, sling, boar spear), Revenant (dead duellist; wisp dash through enemies; rapier, parrying dagger, executioner's sword).
- Lamplighter (Alex likes it): mace, a left-hand lantern on right click (reveals hidden enemies, burns away smoke, helps teammates heal sooner), oil flask in slot 2. Not a dash: suggested Flash on Shift (a blinding burst). Decided to wait and play the three classes in Dark Chalice first; build him if a gap shows (finding people, smoke).
- Built around Classic's omnidirectional dash, with two charges. Options discussed: Duellist (rapier, parry, hand crossbow), Ranger (longbow), Monk (staff, deflect), Runner (ball specialist; dash works while carrying). Left for now.

### Knight redesign (planning, 13 Nov; not built)
- Role: the anchor. Front shield is the hard counter to bolts and thrown daggers; slow, big, flankable.
- Slot 1 warhammer: left click swing, hold to charge a smash. Alex (13 Nov): weapons do set damage and each class gets its own health (replacing hits-to-kill per class).
  - Charged smash (Alex, 13 Nov): not an instant kill; damage scales with how long it's held, from a normal swing (60) up to 100 at full charge (about 1.2 s). At full: kills a goblin or sorcerer, leaves a knight on 50. No hammer glow and no charge meter: the charge reads from how far back the knight has wound the hammer (first person and third person), which keeps increasing until full. The small blast around the impact stays.
  - Suggested health: goblin 80, sorcerer 100, knight 150. Damage: bolt 12.5 (head ~19), dagger hit 25, thrown dagger 50 (head 100), sorcerer's sword 50, hammer 60, charged smash 150, javelin 60 (head 150). Not yet agreed.
- Right click: shield, stops everything from the front. Agreed: he moves at about 70% speed while it's up.
  - Alex: when raised it should block a substantial part of his view (a limiting factor), and be a proper kite shield with a sloped top.
- Slot 2: javelin (agreed). Thrown in a heavy arc. He can throw with the shield raised; the limit is the 3.8 s to draw another javelin (Alex).
  - Alex: a thrown javelin stays stuck where it lands (floor, wall or player) for 10 s. If it kills the player, it vanishes with the body. (If it hits someone who survives, it stays in them for the 10 s.)
- Shift: shield charge (Alex, 13 Nov), replacing the shockwave and holy ground. As he rushes forward, projectiles in his path are deflected.
  - Suggested: about 6 m in about 0.6 s, very little steering, stops early at a wall. Deflects shots from the front only (batted aside, not sent back). Anyone he hits is knocked back and briefly staggered, with small damage, so a hammer swing can follow. Cooldown about 10 s.
- Clamber: suggested about 1.3x the sorcerer's time.

### Headshots (planned, not built)
- Projectiles only: bolts, thrown daggers, cannon direct hits. Not melee.
- Head zone at the top of each hitbox (the goblin's is smaller).
- Bolts: head about 1.5x body, so body-only stays three bursts and all-head bursts can kill in two.
- Lock-on must pull toward the point nearest the crosshair, not the body centre, so head aim stays on the head.
- Thrown dagger to the head: possibly a kill outright.
- Distinct hit marker and sound. Bots mostly aim at the body, head chance by difficulty.
- Option for later: the knight's helm soaks some of the bonus.

## Dark Chalice (built v123, 13 Nov; first called Blood Chalice)
- As built: Game row option (default). Chalice starts in the middle of the map. Touch to pick up. Holder rules, fill/multiplier, Q to drink (2 s, standing still), E to pass (highlighted teammates within 8 m, fast toss, enemies in its path catch it), drain when dropped, ward slows passes, goblin grapple yanks a loose or flying chalice (can't be intercepted while yanked), knight charge knocks a loose or flying chalice away. Darkened gold chalice with black ichor sparkling in the holding team's colour, brimming motes at 3x, a beacon and a draining pool when loose. HUD: cup pips, multiplier, pot, drink bar, hints; marker and radar dot. Chalice tab on the Tuning page. Bots carry, escort, hunt the holder, chase, drink (waiting for a bigger cup), pass when hurt or asked.
- Bot test (3v3, 8 min): scoring works but kills come slowly, so 60 is rarely reached by bots in that time; Alex: 8-10 minute games are fine, default match length now 10 minutes.
- Name: DARK CHALICE (Alex). A gold chalice. The liquid: suggested black, sparkling ichor whose sparkles take the holding team's colour, getting more restless as it fills and spilling over at 3x. Avoids gore and reads as magic.
- Alex's idea for Classes: team deathmatch with one chalice. The holder carries it in the left hand and fights with the primary weapon in the right; no swapping to the secondary. Every kill the holder's team gets while it's held fills the chalice. The longer it's held, the bigger the score multiplier.
- What the holder gives up: knight loses the shield; goblin his left dagger (half damage, no throw); sorcerer keeps the staff in his right hand but loses the ground ward (the ward is his left-hand ability). Each class carries with its main weapon: hammer, daggers, staff.
- Agreed: carry with the primary weapon (hammer, daggers, staff); no secondary; no abilities while holding (no charge, grapple, levitate or ward). Clamber still works.
- Passing (Alex, 13 Nov): the holder can hand the chalice to a teammate, keeping the pot and the multiplier, e.g. when about to die. While holding, teammates in range are highlighted; press E to pass to one.
  - Range about 8 m with line of sight; the teammate nearest the crosshair is selected (brighter highlight). No pass-back limit (Alex: not a problem with human players).
  - Alex: an enemy who intercepts a pass gets the chalice. So the pass is a short, fast toss aimed at the teammate (about 0.4 s in the air), not a hand-to-hand handoff; any enemy whose body is in its path catches it.
  - Decided: an interceptor takes the chalice with the blood in it.
  - The multiplier: suggested it resets to x1 for the team that steals it (not yet agreed).
  - Alex: a well-timed ground ward slows an enemy's chalice pass in flight (like any enemy projectile), making interceptions possible.
  - Alex: a goblin's grapple can grab a loose chalice, on the ground or mid-air (the one exception to walls and floors only). Suggested: the hook yanks the chalice back to him; it can't take it from a holder's hand.
  - Alex: the knight's shield charge knocks a loose chalice away, on the ground or in mid-air (e.g. a pass). Suggested: it's batted off in the direction of the charge, still loose, keeping its blood, so anyone can grab it. Decided: it can never knock the chalice out of a holder's hand.
- Scoring (decided): banked by drinking. Kills fill the chalice; the holder drinks to bank it (suggested: hold a key about 2 s, standing still) and the cup empties.
- Alex (13 Nov): the multiplier tops out at 3x. The cup has a limit: once it's full, the team can't score any more until the holder drinks, which banks it and resets the chalice.
  - Decided: the multiplier rises only from kills. 1x until the cup is half full, 2x from half full, 3x from four-fifths full.
  - Decided: only the team holding the chalice scores. Kills by the other team score nothing; they have to take the chalice.
  - Suggested: the cup holds 10 kills. Kills 1-5 add 1 point each, 6-8 add 2, 9-10 add 3, so a full cup banks 17. A pass in flight still counts as your possession; a loose chalice belongs to nobody.
  - Alex (13 Nov): a loose chalice (dropped, holder killed, knocked away) drains while it's on the ground, one unit a second, then is empty. Suggested: it drains by one kill's worth a second (so a full cup empties in 10 s, and the multiplier steps back down as it drains); whoever picks it up, either team, gets what's left. Implies the holder's death drops it with its blood.
- Vulturing (13 Nov): mostly handled by drinking whenever you like, the full-cup rule, the drain, and the non-holding team scoring nothing. The remaining risk is a holder caught mid-drink. Build as designed; if it's a problem in testing: a faster drink (about 1.2 s), or a holder killed mid-drink banks part of the cup.
- Holder killed: the chalice drops with its blood and starts draining (follows from the drain rule).
- Decided: first to 60 points wins (suggested backstop: highest score when the match clock runs out).
- Alex: a Chalice tab on the Tuning page with every setting for the mode (cup size, multiplier steps, points per step, score to win, drink time, drain rate, pass range and speed, interception, etc.).
- Decided: Q drinks while holding the chalice (it banks the pot). Suggested: when not holding, Q still asks the holder for a pass.

## Maps: one per class
Each map leans toward one class. The other two still need a plan there, so picking a class for the map becomes part of the strategy.

### Basilica: the knight's map
- DONE (v81): great chandelier at 25 m; flight ceiling lowered from 36 m to 27 m.
- To do: cover on the sand to break long sightlines (nave of columns, tombs, pews), so fights happen at hammer range.
- To do: gates and tunnels as chokepoints for a shielded knight.

### Scrollwork: the sorcerer's map
- Upper levels are flat and open-edged, with flush brass edge inlays and no rails (v105):
  - Galleries along both long walls and two bridges across the hall at 4.2 m. Jump on from the floor; run straight off.
  - Four floating reading platforms at 7.6 m, hung on brass rods, each with a desk and candle.
  - The observatory beams around the orrery, lowered from 13.5 m to 11 m.
  - Jump chain, tested for every class: floor to bridge or gallery, then platform, then observatory, each a single jump. The long ramps up to the observatory remain.
  - Bots use the galleries, bridges and ramps but don't make the jumps between levels.
- To do: open the hall up (fewer, shorter stacks, clear lanes from the galleries).

### Mausoleum: the goblin's map (v81-82; restored to the 1.01 layout in v107)
- Flooded, overgrown crypt, 128 x 88 m, low 8 m ceiling except the rotunda.
- Rotunda: skull ossuary with eight low doors, a 6 m ledge, and six sheets of water falling from the oculus around the ball's dais (bots can't see through them).
- Ruins: collapsed rubble heaps with terraces at 1.8-4.6 m, rubble ramps along the tunnels, wall stubs to the ceiling for cover. Bots use them.
- Four landmarks, one per quarter, under collapsed ceiling patches with coloured light: fallen tree, toppled angel, fungus column, king's tomb.
- A flow rework (v104: low runnable walls, open rotunda, beams between tops) was tried and rejected. Alex: "Original Mausoleum is much better. The new one does not work at all." Don't redo it; any flow changes should keep the original's enclosed character.
- Pathfinding: the route table is built by a search from each waypoint instead of the all-pairs method; identical routes, kept from that work.
- Backlog, approved as a visual reference: the flooded rotunda from the first Bellringer mockup. It has an open oculus with teal daylight, two tiers of stone arches, a timber gallery, faded banners, and mossy piers rising from reflective water.

## Menu camera (v106)
- The menu's slow orbit is per map: high and steep inside Basilica's dome and under Scrollwork's ceiling, and round the edge of the rotunda drum in Mausoleum.

## Crowds (backlog)
Alex wants tiered seating around every map that players can't reach, full of clapping supporters in team colours, all three classes mixed.
- Approach: instanced low-poly fans (body, head, arms) in team colours with knight, goblin and sorcerer silhouettes; clapping and bobbing animated on the GPU; unlit materials. Thousands of fans for a few draw calls.
- Basilica: fill the existing arena tiers; fence off the top so players can't wander in.
- Scrollwork: add a raised spectator gallery behind railings around the hall.
- Mausoleum: undecided. Options offered: ghostly supporters on balconies ringing the rotunda, or skeleton crowds in the burial niches.

## Other open offers
- Knight shockwave knocks the ball out of an enemy carrier's hands.
- Grapple range 42 m could go to about 50 m.
- Fourth class: Warden suggested, not confirmed.
- Crash after passing to a teammate: not reproduced; error box added, waiting on details.
- Bots: teach goblin bots to take flanking routes (matters most on Mausoleum).
- Clambering: planned, automatic, bots use it; starts with the sorcerer as the baseline (see the sorcerer redesign).

## Outrider look (mock-up, not wired in)
- Buck kick rejected.
- Literal anthropomorphic horse: chestnut coat, dark mane and forelock, tall ears, hooves with feathering.
- Quilted checkered doublet in team colour and its dark, with stitched diamond quilting and a short flared skirt. Breeches to the knee.
- Team-coloured noseband and browband so his side reads from the front.
- Bandolier of sling stones from right shoulder to left hip. Bolas at the left hip. Flail in the right hand. Staff sling across the back.
- Model lives in buildBody as an inert 'outrider' branch. Not selectable yet.

## v135 (13 Nov): menu rebuild and rule changes
- Main menu: bigger wobbling chalice (black inlaid gems, white skulls), GAME MODE (Dark Chalice / Scryball / Scrum) with that mode's rules beneath, PLAY AS (Classes / Knights, any mode), MAP, BOTS, PLAY. Sensitivity, pass-to-bank and tuning in a collapsed SETTINGS.
- PLAY goes to the class page (or Knights team page). No controls page: the chosen class's controls show beneath the cards, plus the mode's keys.
- Portraits are live idle loops holding the primary weapon.
- Names: Oddball is now Scryball, team deathmatch is Scrum.
- Scryball fuse is per holder (10 s): passing resets it; detonation kills the holder and takes back only their points; re-grabbing your own drop keeps the fuse.
- Dark Chalice: drinking works on the move at 40% speed (tunable); a hit or jump breaks it. Dropped cup drains one kill a second. Rules text is Alex's wording; no "first to" line (set in settings).
- Version tag: the menu's bottom-right "Dark Chalice 0.N" must match the artifact version. Before every publish, set it to the next version number (last published + 1).

## v150 (13 Nov evening)
- Test focus: Chalice mode only, for now (Alex). Mode renamed "Chalice" in the menu; the game is still DARK CHALICE.
- Gridiron knights renamed Champions. Classes move slower (6.8 m/s, 1.8 m jump, gravity 11.5); Champions keep 8.2 / 4.77 / 7.4. World gravity follows the roster in play.
- Melee reach (feet to feet, measured): Skulker 3.1 (lunge 0.8), Crusader 3.5 (hammer range 2.5, lunge 0.3, short horseman's hammer), Magus 4.0 (scimitar range 3.1, lunge 0.1).
- Skulker 90 HP. Magus bolt 10 (was 12.5). Javelin 65; Crusader helm: javelin headshot x2 (130) vs him. Javelin redraw 2.5 s. Tapped hammer wind-up 0.1 s. Shield charge: one 0.4 s lunge from 32 m/s, about 8 m.
- Chalice bots: holder stays in the middle 55% of the map (was fleeing into corners, causing stalemates on Mausoleum), drinks at half-full when fairly safe, nearly full through danger, full always. Six-match result: 35-53 pts winners in 10 min, drinks avg 3.5 pts.
- Class results after v150 (3 Chalice matches): Magus K/D 1.39 (mostly bolts), Crusader 1.1, Skulker 0.58. Bots favour ranged; Skulker still weakest.

## v156 (13 Nov late): one rule for every class
- Rule: key 1 is a one-handed primary; the left-hand ability (right click / F) only works with it out. Key 2 is a two-handed secondary, slower to bring up (0.55 s vs 0.35 s back to the primary).
- Magus swapped: scimitar on 1 (one-handed) with the ward in the left hand; crystal staff on 2, held in both hands, bursts of 3 x 7 bolts 0.2 s apart. He holds the chalice with the scimitar. No more scimitar block.
- Crusader: shield only with the hammer out. Shift with the javelin out puts it away and charges with the shield up.
- Health unchanged: Skulker 90, Magus 100, Crusader 150.
- 3 Chalice matches: K/D Crusader 1.18, Magus 1.13, Skulker 0.76; damage per minute alive Magus 366, Crusader 281, Skulker 279.

## v157 (14 Nov): the class pattern
- Pattern for every class: Shift = movement, always usable. 1 = one-handed primary. Right click / F = control, with the primary out. 2 = two-handed ranged secondary, slow to raise (0.55 s).
- Skulker: one dagger (20 a slash, about every 0.27 s), no double strike. Right click throws the smoke bomb (no switch, 20 s cooldown). Slot 2: two throwing daggers, 40 each, right then left, 1.4 s to grab two more.
- Crusader: the shield is his thing; it works with the hammer or the javelin, but he can't attack while it's up. Javelin: plant and throw, 0.4 s wind-up plus 0.2 s follow-through at 30% speed. Shift cancels the throw and charges.
- Health +20% for a longer time to kill: Skulker 110, Magus 120, Crusader 180.
- 3 Chalice matches: damage/min alive Magus 391, Skulker 374, Crusader 335; K/D Crusader 1.6, Magus 0.93, Skulker 0.67.

## v158 (14 Nov): Crusader rework
- Right click on every class is now a team tool: Skulker hides (smoke), Magus slows (ward), Crusader protects (light).
- Crusader: no kite shield. Holding right click / F with the hammer out raises a wall of light shaped like a big kite shield (2.2 x 2.6 m, 1.5 m in front, team-coloured with a cross). It stops enemy shots and melee and enemies can't walk through it; allies and their shots pass. Drains a 4 s meter while up, recharges fully in 6 s after a 0.6 s pause. He can swing the hammer with it up and moves at 85%. A full charged hammer smash shatters it.
- Shift: Charge, a hard dash that ends in a 40 hammer blow plus knockback.
- Slot 2: Arbalest, one heavy bolt (65, 70 m/s, nearly flat, headshot x2), 2.5 s to wind back. (Internally still the 'javelin' projectile.)
- Javelin parked for a future class that could use it as a primary (Alex). The javelin model and sticking code are still in the file.
- 3 Chalice matches: Crusader K/D 2.03, 425 dmg/min, clearly too strong; Magus 0.78, Skulker 0.56.

## v159 (14 Nov morning)
- Renamed: Magus is now the Seeker, Skulker is now the Rascal (internal keys still sorcerer / goblin).
- Crusader: templar look (pale surcoat with a team-colour cross front and back, team-colour hem and cloak, flat-topped great helm with a brass cross, no plume). 150 health. Pious Charge does no damage (still bowls enemies aside). Arbalest bolt 40.
- Wall of light: heater outline like Alex's reference (peaked top, curved sides to a point), double rim, no symbol. 70% speed while up. Drains with time (4 s) and with damage: 100 damage soaked breaks it; cracks appear in three stages. Once broken or spent it's back after 20 s; released early it refills over 20 s. A charged hammer smash breaks it outright.
- Alex: different abilities should have their own cooldowns (light 20 s, smoke 20 s, ward, charge each separate).
- 3 Chalice matches: K/D Crusader 1.64, Seeker 1.07, Rascal 0.56; damage/min Seeker 448, Rascal 346, Crusader 325.

## v160 (14 Nov)
- Rascal: new fighting dagger after Alex's reference (long blade with a ridge, four-armed guard with forked tips, wrapped grip, spiked pommel). Throwing daggers stay small and plain.
- Weapon strip: when you switch, the bottom of the screen shows both weapons for 1.6 s, crossed swords over the primary and a crosshair over the secondary, current one lit.
- Crusader: 125 health. Surcoat now in the team colour with a pale cross and hem; plain steel armour (no team tint). Cloak removed but parked: Alex likes the idea.
- 3 Chalice matches: K/D Crusader 1.31, Seeker 1.19, Rascal 0.64.

## v0.161
- Done: Crusader cross matches hem width; Rascal dagger longer (0.56); stowing knives starts their reload.
- Done: left hand shows the team tool. Rascal holds the smoke bomb (hidden while on cooldown), Seeker's hand swirls with magic (dim while the ward recharges).
- Idea: Crusader left gauntlet glows faintly while the wall of light is charged, to match.
- Chalice regression (3 maps): K/D Crusader 1.13, Seeker 1.12, Rascal 0.82.

## v0.162
- Done: bot roles. Seeker hangs back about 13 m off the objective and kites anyone who closes (scimitar only inside 3.2 m). Rascal goes straight for the objective, breaks off after ~1.2 s in close or when hurt, smokes his getaway, and prefers Seekers as targets. Crusader holds a line a few metres out from a friendly holder or a loose chalice, and presses an enemy holder.
- Done: Seeker shows one pair of arms (the portrait showed two). New scimitar: damascus blade, stepped back edge, disc guard, banded grip, hooked pommel. Rascal knees now bend forward and his legs are thicker.
- Done: Crusader's gold holy symbol, held up in his left hand in first and third person. Faint glow when the light is ready, bright while raised, dark once shattered. Chest cross back to pale (and its bar now sits flat on the cloth).
- Watch: with the new roles, 2-map test K/D Seeker 1.42, Rascal 0.91, Crusader 0.81. Seekers at range are strong; the Crusader suffers most.

## v0.163
- Done: Crusader bots push forward behind the light onto any enemy they can see within 24 m of the objective, and fall back to the line once the light is low or shattered. 2-map test K/D: Seeker 1.15, Rascal 0.96, Crusader 0.94.

## v0.164
- Done: backstab. The Rascal's dagger does 1.5x (BACKSTAB_MUL) from more than ~110 degrees behind; "BACKSTAB" / "BACKSTABBED" toasts. Rascal bots flank: round the side to the target's back before striking, and grapple in behind them. ~13 backstabs per 4 min from two Rascals.
- Done: holy symbol smaller and pale gold.
- Watch: Rascal K/D dipped to 0.8 (2-map test) while he circles under fire. Ideas: only flank targets busy with someone else, or smoke before flanking.

## v0.165
- Done: Rascal bots lean on smoke. They smoke a target who's watching them before flanking, smoke the enemy holder's escort as they rush in, and still smoke their getaway. About 9 smokes per 4 min from two Rascals (the 20 s cooldown is the limit). 2-map test K/D: Seeker 1.27, Rascal 0.92, Crusader 0.90.
- Note: bots can't see through enemy smoke (smokeBlocks in target choice, every think, 0.12-0.22 s on normal); within 2 m (SMOKE_SEE) they can.
- Option: shorter SMOKE_CD if Alex wants smoke used even more.

## v0.166
- Done: smoke completely obscuring to the enemy. Solid core (writes depth once thick, so light walls and glows behind it vanish too), 42 puffs at full opacity, no thinning near the eye, SMOKE_SEE 0. Bots drop a target the moment smoke comes between them (checked every frame), except the Rascal who threw it keeps track of the one he smoked. No sword lock-on reticle through smoke. The thrower's own team still sees a thin haze.
- Done: crystal staff overheats. STAFF_HEAT 0.065 per bolt, cools 0.4/s after 0.5 s rest, 3 s lockout. Sustained fire overheats in about 4 s (5 to 6 bursts). Crystal runs from team glow to orange-white, flickers and smokes when overheated; HEAT bar under the crosshair with HOT / OVERHEATED countdown. Bots ease off at 78% heat unless the target is nearly dead, and switch to the scimitar if overheated with someone within 7 m. Tunable in settings.
- 2-map test K/D: Rascal 1.14, Seeker 0.97, Crusader 0.87.
- Open: should the thrower's own team also be blinded?

## v0.167
- Done: Seeker slots swapped. Slot 1 is the crystal staff (one-handed, left hand raised for the ward, right click / F casts with the staff out). Tap: one bolt, BOLT_DMG 8, BOLT_CD 0.3 (~27/s max). Hold past 0.15 s to charge for BOLT_CHARGE_T 1 s: up to BOLT_FULL 40, bigger and 40% faster, BOLT_HEAT_X 6 times the heat (a full charge is ~0.39 heat). Fires on release. Heat bar shows CHARGE %. Slot 2 is the scimitar, 50 a hit, 0.55 s to raise. Menu card and controls text updated. primW(f) gives each class's slot-1 internal weapon.
- Bots: tap with gaps of ~0.36 s on normal, charge 30% of the time beyond 14 m when heat is under 40%, ward with the staff out.
- Before (DPS ceilings): dagger ~65 (95 backstab), hammer tap ~55, old staff burst ~28, scimitar ~75.
- 2-map test K/D: Crusader 1.22, Rascal 1.08, Seeker 0.55 (26 kills, 47 deaths). Weak as intended, maybe too weak. Levers: tap damage, bolt rate, charged damage.

## v0.168
- Done: Rascal health 110 to 90 (CLASS_HP.goblin, menu card).
- Done (v0.169): time between staff bolts set to 0.36 s, from Alex's tapping (BOLT_CD).

## v0.170
- Done: charged staff releases a burst. Under half charge: one bolt. Half: two. Full: three. 0.08 s apart (BOLT_GAP). Damage per bolt scales 8 to BOLT_FULL 14 (full charge 3 x 14 = 42). Heat is charged once per release. Charged bolts are bigger, white-hot at the core, wider glow and a longer trail. Old saved values bfull 40 / bcd 0.3 / hpg 110 are ignored on load.
- 3-map test K/D: Seeker 1.04, Rascal 1.01, Crusader 0.96.
- Next: the maps. Measured how often two random standing spots can see each other: Basilica 44%, Scrollwork 29%, Mausoleum 6%. Target ~15-20%. Options given to Alex: shrink, break up the middle, add rooms/aisles, add height.

## Basilica side chapels (mockup, not published)
- Built behind BAS_ROOMS (off) in sideChapel(): four chapels at ring segments k 9, 15, 33, 39 (two per long side), each three segments wide, cut from all four seating tiers. Doorway off the first-tier walkway (y 5); a central ramp up to raised floors at y 10 on either side and across the back; walls to 17 m; timber trellis roof with leaves and hanging vines (collider, no flying in); three open windows in the cathedral wall (y 10.9-15.6) with shattered glass teeth, shards on the floor, night sky behind and moonlight beams; planters, two torches.
- Mockup sent: basilica_chapels_mockup.png. Door frame and blind arches don't render yet (single-sided).
- Openness with chapels: 44% to 40%. The open bowl is still the main problem; the chapels add routes and cover, not much blocking.
- Still to do if approved: bot navigation into the chapels, final dressing.
- Pending: throwing daggers 40 to 25 each (proposed, awaiting Alex).
- v0.171 published: throwing daggers 40 to 25 each (head 37.5); old saved 40 ignored. Basilica changes still off in the published build.
- Basilica walkway corridors (mockup, BAS_HALLS off): sideHall(k0, k1) on k 8-16 and 32-40. Inner wall on the podium edge with a broken stained-glass window per segment (sill 6.5, top 9.4, jumpable through); back wall on the seating edge except at the seating ramp (k 12/36) and chapel fronts; trellis roof at 10.6 (collider); ends open where the floor ramps arrive; middle doorway with a new ramp down to the sand. Torches every other segment. Mockup: basilica_halls_mockup.png. Openness with chapels + corridors: 34% (from 44%).
- Basilica centre garden (mockup, BAS_GARDEN off): gardenPavilion() over the dais. Timber posts with climbing vines, dense vine hedges (solid, block sight) on each side leaving the four ramps open, overgrown lattice roof at 6.2 (collider). Openness with chapels + corridors + garden: 24% (from 44%).
- Chalice shrine on every map (mockup, SHRINE_ON off): chaliceShrine() on the existing 2 m dais at the origin. Slow-turning pale green rune ring, faint glow, rising wisps, five circling motes, cold point light; brighter while the chalice sits there.
- Done locally (not yet published): Seeker keeps his staff (primary) when holding the chalice, left hand raised holding it (chHolderRules uses primW). Chalice 35% bigger in third-person hands and sat on each class's left hand (CH_HOLD). First person: cup bigger, fist round the stem, tipped toward you and to the side so the liquid shows.

## v0.172
- Published: Basilica chapels, walkway corridors and centre garden (flags on); chalice shrine on all maps; chalice hold changes (Seeker keeps staff, bigger cup, first-person stem grip tilted to show the liquid). Nav nodes added for chapel floors, corridors, under the trellis. Basilica test: no errors, 96 kills/10 min. Bots rarely go into chapels/corridors (no reason to yet).
- Published: new chalice HUD (chalHudDraw). Under the health bar: YOUR TEAM HAS THE CHALICE / ENEMY TEAM HAS THE CHALICE / THE CHALICE IS FREE / CHALICE DROPPED. Yours: outline cup filling in team colour, dashed lines + 2x/3x labels (silver past half, gold at 3x with the outline), pulse when full, "+N IN THE CUP" beside; under it CHALICE FULL, or for the carrier DRINK FROM CHALICE · Q (full), a quiet Q DRINK · E PASS (otherwise), DRINKING bar. Enemy: no cup, multiplier (1x dim, 2x silver, 3x gold, FULL pulsing) and "+N THEIR CUP". Old pip meter hidden; "first to 60" dropped from the line.
- Ideas: Seeker bots perch at corridor windows, Rascal bots flank through corridors/chapels.

## v0.173
- Throwing daggers 30 each. Ability greyed out while holding the chalice (still no Shift abilities for holders).
- Holder secondaries with trade-offs: Seeker scimitar one-handed at HOLD_SCIM_X 0.7 damage (normally two-handed now, longer grip, both hands in first and third person); Rascal throws one dagger at a time from the right hand; Crusader arbalest one-handed with HOLD_ARB_X 1.6 reload (4 s), lowered to his side to reload. Weapon label adds "· ONE-HANDED". Arbalest otherwise unchanged (two-handed, 40, 2.5 s).
- Staff heat like the Halo 3 plasma pistol: each tap adds STAFF_HEAT 0.06 x (1 + STAFF_RAMP 2 x heat), so about 10 rapid taps overheat it; a full charge overheats it outright. Lockout 3 s either way. Bots mostly half-charge.
- 2-map test K/D: Crusader 1.23, Rascal 1.07, Seeker 0.64. Seeker weaker after the heat change; levers: STAFF_RAMP, lockout, tap damage.

## v0.174
- Scimitar edge forward, blade leaning slightly inward (first and third person).
- Seeker fix: idle bots were swapping to their old primary ('melee') with no target, so Seekers had the scimitar out 45% of the time. Now they go back to primW (the staff): staff out 99%. Heat ramp eased: STAFF_HEAT 0.05, STAFF_RAMP 1.25 (14 taps to overheat), lock still 3 s.
- 3-map test K/D: Seeker 1.12, Crusader 1.11, Rascal 0.84.

## v0.175
- First-person one-handed scimitar (holding the chalice) turned edge-in (weaponModel rotation.y -0.7).
- Smoke vulnerability: anyone inside the other team's smoke takes SMOKE_VULN 1.15x damage (inEnemySmoke in damage(); setting under Classes). No on-screen cue yet.
- 2-map test K/D: Seeker 1.19, Rascal 1.01, Crusader 0.86.

## v0.176
- Hammer: tapped strikes now 0.8 s apart when clicking as fast as possible (MELEE.hammer.cd 1.0 to 0.73; the click itself adds ~0.07 s). New setting "Crusader: time between hammer strikes".
- Idea from Alex (parked for now): a three-hit combo (left angle, right angle, overhead down) 0.52 s apart, then a recovery.

## v0.177
- Rascal dagger slower: MELEE.dagger.cd 0.25 to 0.4.
- Staff heat bar turns red while charging and fills toward the heat the shot will leave (a full charge fills it).
- Chalice dais: the rune ring and circling motes are gone; the dais top glows pale green (brightest at the middle and edges), wisps still rise, cold light stays.

## v0.178
- Test after the slower dagger (v0.177, 3 maps): Rascal 0.59 (dagger kills 47 to 23), Crusader 1.41, Seeker 1.22. Suggested dagger 0.3 s.
- Settings: Classes tab split into sub-tabs Rascal / Seeker / Crusader / Shared, each class's weapon, ability and health settings together; Cannon tab renamed Champions. New slider "Rascal: time between dagger slashes".
- Esc on the pause screen goes back to the game (after 0.7 s; if the browser refuses to recapture the mouse, it stays paused rather than dropping to the windowed fallback).

## v0.179
- Pious Charge ends in a hammer swing again: on contact the target is stopped in front of him and staggered, then when the charge ends he swings automatically for SC_SWING_DMG 50 (tested: 125 to 75). The hammer glows white-hot through the charge and the swing (first and third person). Settings (Classes/Crusader): swing on/off, swing damage, contact damage, knockback (used when the swing is off), stagger, speed, time.

## Notes for later (from Alex)
- (done v0.181) The wall of light shown as him holding up the holy symbol.
- (done v0.181) Rascal: grapple and smoke bomb swap instead of the bomb dropping.

## v0.180
- Pious Charge distance setting (SC_DIST, default 8.85 m, 1 m longer than before; measured 8.85 m in the open). Peak speed is derived from distance and time. Replaces the old peak-speed slider.
- The Pious Charge swing knocks the target away at SC_SWING_KNOCK 5 m/s (the old contact knockback was 9). Setting "Pious Charge swing knockback".

## v0.181
- Done: the Crusader raises his holy symbol to cast the wall of light. First person: the symbol rises into view and blazes (the old bare glowing hand is retired in Classes mode). Third person: left hand held up at head height with the symbol, larger and bright.
- Done: Rascal's grapple swap. In first person the smoke bomb goes down first, then the grapple launcher comes up; putting the grapple away brings the bomb back after it.

## v0.182
- The wall of light carries the holy symbol traced on its face: the flared cross with pointed arms and the ring behind, glowing in team colour, fading with the wall.

## v0.183
- Wall of light offset 0.5 m to his left (LIGHT_SIDE, setting "wall of light offset to his left"); blocking, melee and movement checks all follow it.
- First person: the raised holy symbol is placed on the same line of sight as the symbol on the wall, so it sits inside it. Third person: held further out (0.74 m) and nearer his centre line.

## v0.184
- Wall of light 15% larger (LIGHT_HW 1.265, LIGHT_HH 1.495).
- Mausoleum test (2 x 10 min): scores 13-26 and 13-22 (nobody near 60), 69 and 86 kills, chalice held 92-96%, 8-10 drinks a match, fullest cups 5-7. K/D Crusader 1.40 (hammer 70 kills), Seeker 1.09 (only 24 kills; few Seekers drawn), Rascal 0.67 (dagger 29, knives 22; 44 backstabs).

## v0.185
- Chalice defaults: cup 6 kills, 2x from a third, 3x from two-thirds (1, 1, 2, 2, 3, 3 = 12 for a full cup). Rascal dagger 0.3 s. Old saved cup 10 / 0.5 / 0.8 and dagger 0.4 are ignored.
- Mausoleum test (2 x 10 min): 28-4 and 14-26; 15-17 drinks a match averaging 2.1-2.4 points; fullest cup 3 (bots drink at half when safe, so they never reach 3x). K/D Crusader 1.45, Seeker 1.00, Rascal 0.71 (dagger kills 29 to 35).
- Open: bots should hold the cup longer (drink at 4+ when safe); win target 60 is out of reach in 10 minutes.

## v0.186
- Win target 30 (old saved 60 ignored). Rascal dagger back to 0.25 s. Rascal health 100.
- Bot drinking: hold until the 3x line (4 kills) when safe, one short of full through some danger, full always, hurt banks early, and a match-winning drink is taken at once.
- 3-map test: Mausoleum 14-30 in 8:36, Basilica 33-2 in 4:46, Scrollwork 0-25 (time). Drinks average 5 points; fullest cup 5. K/D Seeker 1.57, Crusader 1.19, Rascal 0.60 (dagger 25, knives 32 kills).
- Rascal still weakest at any dagger speed or health tried; look at his bot behaviour next (flank circling, in-and-out retreats) rather than numbers.

## v0.187
- Rascal smoke no longer makes enemies take extra damage (that's the Lampist's job now). It chokes instead: SMOKE_DPS 4 a second in 0.5 s ticks to enemies inside, lingering SMOKE_LINGER 1 s after they leave (tested: about 18 over a cloud), kills credited to the thrower as SMOKE. Settings under Classes/Rascal.

## Next class: the Lampist (design agreed so far, mockup only)
- A pale, haunted woman with an iron birdcage locked over her head (was a weasel; scrapped): long ragged dress in dark team colour over a pale underskirt, frayed shawl, long black hair, hollow eyes with a pale glint, short chains from the cage collar.
- Slot 1: flintlock pistol in the right hand (one heavy, accurate shot, slow reload).
- Right click / F: the lantern in his left hand. Raised, it burns oil: enemies in range are revealed through walls to his team and take 15% extra damage while the oil burns; the marked know it.
- Slot 2: lamplighter's pole, two-handed, long reach; good at range, poor right up close.
- Shift: a diagonal leap forward; best clamber (ledge-climb) distance of any class.
- Healing saved for a later class.
- Models in the file (unused): makeLampist, makeLantern, makeFlintlock, makeLampPole. Mockup: lampist_mockup.png.

## Light and heavy weapons (Alex, 15 Nov; built by v0.213)
- Light weapons are one-handed and work while holding the chalice; heavy weapons are two-handed and can't be used with it.
- Light: hammer, staff, scimitar, dagger, throwing daggers, flintlock, javelins. Heavy: arbalest, blunderbuss, claymore/standard.
- Built: holding the chalice locks out the arbalest and blunderbuss (chHolderRules). The one-handed special cases are gone.
## Superseded: the Brigand (15 Nov). Split into the Champion and the Dragoon, below
- Battle standard as his primary (reach, sweeps several people); right click: raise it in both hands, it glows, he and nearby teammates move and attack faster (can't swing while it's up).
- Shift: dash. G: the grenade (already built, off the Crusader).
- Secondary undecided: javelins (light, usable with the chalice) or a gap-filler (repeating crossbow for sustained fire). Alex likes javelin as secondary so he can throw while holding the cup.
- Gaps in the current weapons: reach melee, sustained fire, lobbed/indirect fire, long-range zoom.
- Built parts not in use: Champion's two-handed sword with guard and parry, the thrown javelin (code now drives the arbalest), dash, shockwave slam, holy ground aura, shoulder cannon, levitate, lamplighter pole model, Lampist alternate heads (face, bulb, moth).
## Planned: new map, the Royal Garden (Alex, 15 Nov). Mockups and layout first
- A royal garden on a misty island, at the foot of a gothic arcane research cathedral.
- A large central tower with an archway through it at ground level; the chalice spawns under the arch.

- Open: N-S arch or a 4-way crossing under the tower; tower balcony or not. Layout and massing mockups sent.

## v0.188 to v0.214 (15 Nov): where things stand
- Class pattern for everyone: 1 primary, 2 secondary (0.55 s raise), right click / F team tool, G throwable (20 s recharge for all), Shift movement. Drinking from the chalice resets every cooldown the drinker has.
- Crusader: warhammer 55, arbalest (heavy), wall of light, holy book on G (lands open with fluttering pages, ring RELIC_R 5, push 14, damage 25 falling to 10), Pious Charge.
- Seeker: crystal staff, scimitar (one-handed, 50), Aegis on right click (40 HP bubble on an ally, 4 s, 12 s cooldown, range 30), ward on G (hold to aim), flight.
- Rascal: dagger (backstab 2.5x), throwing daggers (speed 55, reload 1.2), blowgun on right click held in his left hand (marks one enemy for his team, 5 s, +20% damage, 10 s cooldown), smoke on G (choke plus 15% extra damage; he sees enemies outlined inside it), grapple.
- Lampist (built): one-handed flamethrower after Alex's reference (bronze frame, brass canister, side gauge facing the player, pilot light). Burns only what the stream hits and sets them alight; 40 a second, range 7, 4 s of gas, lowers to her side to refill. Blunderbuss (heavy, 8 pellets x 13, two-handed tip-up reload). Lantern heal on right click (12 a second, radius 8). Fire wall on G (7 m wall across the throw, or along a wall it hits; 2.5 s afterburn). Blink on Shift (hold to aim, range 16, 6 s cooldown; can blink up onto floors above, shown with a blue arrow).
- Blink travel (v0.213): she crosses as a smoke streak over 0.3 s, untouchable, and can't fire for 0.35 s after arriving. Answer to the blink-in-and-blunderbuss worry.
- Map editor (v0.212): MAIN MENU > MAP EDITOR. Drafts save to the browser and never touch the live map. Prefabs (block, ramp, stairs, pillar, wall, bookcase, crate, hedge), copy/paste, undo, grab and turn. Copy for Claude puts the draft on the clipboard to paste into chat; Download file saves a .json (v0.214, through the artifact's downloads permission).
- End screen: Chalice columns (cup held, drinks, kills as holder, betrayals).
- Settings: every number grouped per class under Body, weapon 1, weapon 2, right click, G, Shift; spares under Shared.

## Next: Champion and Dragoon (agreed in outline, not built)
- Champion: two-handed sword (heavy, guard and parry already built), javelins (light), war cry on right click, dash, grenade on G (the old frag code).
- Dragoon gunslinger: two pistols (light, alternating; one while holding the cup), carbine (heavy, zooms when steadied), bandolier on right click (faster reloads and recharges for nearby allies). Shift: sprint on a charged meter; his jump is a powder jump on a recharge. G: a powder keg, suggested.
- Open from Alex: swap blink and grapple (Rascal blinks through his own smoke, Lampist gets grapple)? Bow class later.
- Multiplayer: host on itch.io or GitHub Pages, PeerJS with the host running the game. Plan not written yet.

## v0.214 to v0.217 (15 Nov afternoon)
- Aegis is armour with no timer: 40 points, draining 1 a second (AEGIS_DECAY) until it runs out or is shot off. Radar removed.
- Rascal blowgun: hold right click to raise and aim (slight zoom), release to fire. The blowgun drops out of his left hand before the grapple launcher comes up, and comes back after.
- R reloads everything: the flamethrower refills only with R or when it runs dry (lowered to her side), and a fresh trigger pull stops a refill. Blunderbuss holds 2 shots (BB_SHOTS, 0.45 s apart), R reloads both. Bots top up between fights.
- New HUD (classes mode): health bottom left with the class symbol, current/max HP and the blue Aegis bar; ability tiles bottom centre (F, G, Shift; ready, cooling with a rising fill and seconds, a half-second flash when ready, dim with a gold cup when the chalice blocks it, a pulse when you press a blocked key); weapons bottom right (the one in hand big with ammo/gas/heat, the other small above; 1H/2H tags on the left; a gold cup beside a 2H weapon you can't use). Your team is always on the left of the scoreboard. Kill feed stays top right. Weapon names stand in for weapon icons for now.
- Renames: wall of light is now Blessed Shield, holy book is Holy Repulse, the Seeker's flight is Float.
- Icons (in the HUD): Crusader Celtic cross; Blessed Shield (heater shield with cross), Holy Repulse (book with arcs on four sides), Pious Charge (nested arrows with speed streaks). Seeker crystal; Aegis (person in a hexagon), Ward (rune ring), Float (wind gusts). Rascal curved dagger; Blowgun (skull under two chevrons), Smoke (billowing cloud), Grapple (hook and rope). Lampist lantern; Lantern heal (lantern with a cross), Fire wall (solid flames), Blink (figure of smoke lines, then solid).
- Bot test after the change: blunderbuss kills went up (33 of the Lampist's 39); watch whether 2 shots is too strong.

## v0.218 to v0.221 (15 Nov evening)
- Right-click tool needs weapon 1 out; pressing it with weapon 2 out swaps back first (a tap tool goes off once the swap ends).
- Throwables work with either weapon: the left hand drops its tool (or lets go of a 2H weapon, which can't fire meanwhile), brings the throwable up, lets go (TOSS_REL 0.3 s). Rascal swaps in 0.25 s. Burning lasts 3 s.
- The Brigand (built v0.221, class key 'brigand', 5th class, key 5): kettle hat pulled down to his moustache, goatee, pale doublet (lilac Thistle, pale saffron Marigold) with team-colour sleeves and hose, javelins in a tall quiver, two powder grenades on his belt. 120 HP.
  - 1 Greatsword (2H, heavy): 60 damage, reach 3.3, 0.95 s between swings, wide sweep that carries into a second enemy for 60%.
  - 2 Javelins (1H): 3 carried, 45 damage (head 1.5x), stick where they land for 20 s; walk over one to take it back; one returns every 8 s. His weapon with the cup.
  - Right click Rally (sword out): lifts the sword flat overhead; teammates within 10 m (and him) get 20% move speed and 25% faster attacks and reloads for 6 s, slows lifted. 20 s cooldown.
  - Shift dash (5 s), G powder grenade (the old frag: 90 to 15 damage, radius 4.5, 1.8 s fuse).
  - No block; the buckler idea was dropped. First bot test: K/D 0.94.
- Next to discuss (Alex): right click always available with either weapon; a hold tool takes the left hand off a 2H weapon, which can still fire a loaded shot but can't reload.

## v0.222–v0.233 (15 Nov)
- Left-hand rule: right click works with either weapon; a held tool takes the left hand off a 2H weapon (loaded shot still fires, no reload). Throwables with either weapon.
- HUD v2 shipped. Class symbols and ability icons; Brigand icons from game-icons.net (credit on the class page). Seeker symbol: Alex's sun-and-staff, inverted. Aegis symbol: Alex's magic-shield.
- Aegis HUD: a glowing blue frame around the health bar that runs down right to left, with the Aegis symbol to the right of the bar.
- Right-click tile key shows a mouse symbol (was "F").
- Brigand: no block. Rally is now the left fist punched up with a gold shockwave (floor ring, waist ring, dome, flash at the fist); the javelin hand stays free, the greatsword can't swing while the fist is up.
- Dash bug: dashT never ran down, so dashes skidded far and braking was off afterwards. Now the burst lasts DASH_T and cuts speed to 35% at the end (Brigand dash about 5.6 m).
- Class page rebuilt: a five-character lineup (symbol over each, front-on portraits), click for a role line plus a row per weapon/ability. Match box: team size 1v1 to 6v6, Classes = All one class / Random mix / Custom (click slots to cycle classes; the enemy fields the same lineup). Max team size is 6.
- Menu portraits: Brigand rests the greatsword on his shoulder, Seeker holds the staff diagonally in both hands.

## v0.234–v0.248 (15 Nov, later)
- Aegis frame: splits at the right end, top and bottom lines drain right to left together.
- Right-click key label is the text "RMB".
- Respawn screen: the class lineup (portraits, symbols, 1–5) over the menu's orbit camera; mouse steers a ring cursor while captured, click picks. No picker at kick-off: you start as the class picked on the menu.
- Greatsword: fuller raised to stop flicker, quillon end caps removed. Menu portrait rests the flat of the blade on his shoulder.
- Rally: 2 s (fist up by 0.4 s, held, dropped over the last 0.6 s). First person shows a plain fist, forearm, bent elbow and upper arm.
- Status symbols over heads (teammates always, enemies only when seen): Rally gold, Aegis blue, heal green, marked red, burning orange, slowed violet, choking grey.
- Lantern: green + signs float up from it when lit (the green glow on the lantern itself was removed in v0.251). It heals the Lampist too.

## Backlog: melee blocking for classes (idea, not started)
- Bring back a block button for melee weapons, reusing the Classic champion's block/parry code.
- Needs a key (right click is the class ability; F is its trackpad alias, Q drink, E pass): C, V or middle mouse.
- Needs a guard pose per weapon, first and third person: greatsword, scimitar, dagger, warhammer.
- Left-hand rule: a 2H block uses both hands, so no block during Rally or while the Blessed Shield / Pious Charge is up.
- Balance: the Crusader already has the Blessed Shield; the Rascal is designed with no block. Suggested start: greatsword and scimitar only.
- Bots need block logic (adapt the Classic bots').

## v0.249–v0.256 (16 Nov)
- Respawn flow: the killed-by screen stays for 2 s, then the orbit camera and a CHANGE CLASS button that opens the portrait lineup. Digits 1 to 5 still pick directly.
- v0.250: cooldowns had stopped ticking (Pious Charge, ward, G, stun) because a comment swallowed the decrement line. Fixed. The death-screen cursor now roams the whole screen.
- v0.251: status chips bottom left, just above the health bar (v0.252 aligned them to the bar's left edge). Gold for good (Rally, lantern heal), red for bad (mark, burn, slow, choke), with seconds left; lantern heal and slow have no timer. Aegis keeps its blue frame.
- Overhead symbols now show only what you put on someone (your mark, your Rally or Aegis, your smoke). The Lampist sees a health bar over teammates she is healing, only for her own heals. Burning bodies get a rising flame instead of a symbol.
- v0.253: Rascal and Lampist swapped Shift abilities. Rascal blinks (hold to reach out and mark a spot, let go to blink; blowgun, bomb and left knife drop away). Lampist grapples (hook in her left hand, lantern goes down, Blunderbuss can't fire while it's up). Icons, tiles, class page text, controls and bots follow.
- v0.254–v0.255: blink hand is a plain ball hand with a slim arm from the bottom left, lowered.
- v0.256: chalice free throw. Tap E still passes. Hold E to show the arc and landing ring, let go to lob it to that spot (20 m/s, tunable); it lands loose.
- Swallowed-comment scan found lines not yet fixed: lantern raise offsets, arm visibility while ranged or floating, one dead line on a shield. Left alone on purpose, since fixing them could change how things look.

## Backlog: Twin Chalice mode (idea, not started)
- Each team defends a home chalice, kills pour into your own cup, and carrying the enemy's cup home steals its points. A capture-style mode, separate from Dark Chalice (one cup, team without it can't score).
- Alex's call (16 Nov): keep one chalice for the main mode. Snowballing is a worry but not yet measured; holding off on bot matches and fixes. If it needs fixing later: louder carrier for a fuller cup, a comeback respawn edge, a dropped cup resetting toward the middle.

## v0.257–v0.273 (16 Nov)
- v0.257: fixed a crash when Brigand javelins reloaded (my Rascal blink hand name collided with the javelin code; renamed to VM.blinkHand). Javelin regen itself was always fine, 1 per 8 s with or without the cup.
- v0.258: arcs on all G throwables (smoke bomb, holy book, fire flask, powder grenade): hold G to aim, release to throw.
- v0.259: on fire shows burning screen edges, no ON FIRE toast. The burn chip stays bottom left. HUD about 15% larger.
- v0.260: with the cup you can use both weapons. Abilities and gear (right click, G, Shift) stay locked. Weapon-slot HUD no longer locks.
- v0.261: Chalice tab has a "Weapons with the cup" group: a switch for the two-handed weapons (Crusader arbalest, Lampist blunderbuss, Brigand greatsword; off brings back the old rule), Brigand one-handed swing time (1.25x), arbalest and blunderbuss reload settings. Rascal's right dagger now leaves the hand after a throw with the cup. HUD weapon labels read 1H with the cup. Rally now also speeds swing animations and Lampist reloads (movement, cooldowns and dagger reload were already covered).
- v0.262–v0.265: Burdened and Empowered by the chalice. A step is 2.5%; kills 1-2 add one step each, 3-4 two each, 5-6 three each, so a full six-kill cup is 12 steps, 30%. Burdened slows move and attack speed, Empowered raises damage, both stack with the kill multiplier. Separate toggles and a per-step setting. Bottom-left chips show a small chalice with one to three chevrons (up and gold, down and red). Per-class jump height multipliers added to the Movement tab.
- v0.266–v0.268, v0.273: Seeker staff. A charge fires one bolt (8 damage tapped, 40 fully charged, bigger the longer you charge). The weapon gauge fills with the charge. Heat and charge turn the crystal white-hot (was orange-red); overheating no longer flickers, it smokes and fades back. No CHARGING text.
- v0.269–v0.270: the Seeker's scimitar is replaced by the Diamond Spear. Brigand javelin shape in silver, small diamond head in the team's crystal colour, held low, quick straight jabs. 40 damage, 4.4 m reach, 0.5 s between jabs, narrow cone, no lunge, dead zone under 1.6 m. First and third person jab animations. Tuning rows for damage, jab time, dead zone, cone, reach.
- v0.269: friendly fire master switch (off by default). The old cannon and sword rows only apply when it is on.
- v0.271: Diamond Spear headshot multiplier (1.25x, tunable). Aegis shows a faint blue rim on the screen of the player who has it. Lantern pluses are gold again. A healed teammate shows a gold + over a glowing gold health bar that flashes when full.
- v0.272: crystal staff head remodelled after the Seeker logo: floating orb, four prongs twisting up and curling in, two flares at the base.
- Not built or not tested in play: jab hits on live enemies, friendly-fire switch, aegis rim, new heal display. Bots still step in close with the Diamond Spear.
- Open: Rally does not yet speed the Brigand's javelin regen. Whether the Burdened step rate should stack with Rally or other speed effects has not been decided.

## v0.274–v0.282 (16 Nov)
- v0.274: Lampist eye wraps are a pale shade of the team colour. Burdened/Empowered stack with Rally (multiplicative). Aegis also shields the Seeker casting it.
- v0.275: fire wall throw preview now draws a bar where the wall will stand, not only where the flask lands.
- v0.276–v0.278: Blessed Shield is a wide curved arc (option 3 of the mock-ups), 2.5 m out, peaked top, squared sides and bottom. Allies and their shots pass through, enemies stay blocked (LIGHT_PASS switch, off). Projectile, melee and walking checks follow the curve.
- v0.279: Pious Charge shows the shield in front of him. Close melee hits on the raised Blessed Shield do 12 damage and push the attacker back (LIGHT_RETORT, LIGHT_REPEL, both tunable). Holy book ring, flash and pages are in team colour.
- v0.280: charge hits as wide as the shield he carries, crunch on impact (extra sparks, block sound, stronger shake). Shield cocks back in the windup, drives out leaning and stretched.
- v0.281: the Pious Charge carries the original narrow heater shield (2.2 m wide, pointed bottom), separate from the wide Blessed Shield. Pointed shape is my best guess at the old curve.
- v0.282: Crusader's first-person hammer moved 7 cm right.
- Not tested in play: charge impact feel, retort damage and push, curved shield collisions with live fire, holy book colours, the hammer shift.
- Housekeeping: a code comment on BLINK_RANGE still says "the lampist's blink" (it is the Rascal's Shift).

## Backlog: Rascal rework (agreed direction, not started, 17 Nov)
- Identity: smoke, vanishing, subterfuge. Grapple now belongs to the Lampist. Blink stays on the Rascal's Shift.
- Rule across classes: G acts on enemies (damage or hindering), right click helps allies.
- G, smoke bomb: larger (about 4 m, about 6 s), still visible to teammates, every enemy inside is outlined and marked in red for the whole team, mark lingers 2 to 3 s after they leave. Tuning rows for radius, life and mark. Shorter cooldown than 20 s to try. The 1.2x damage on marked targets would sit with this mark only if wanted.
- Blowgun retired. Right click is now the Shroud:
  - 5 s, about 5 m burst around him, his team (himself and the Chalice carrier included) goes mostly invisible: no outlines, overhead icons or names for enemies, faint team-colour ghost for allies. Visible as a shimmer to enemies within about 4 m.
  - Breaks for a player when they attack, use an ability or charge a weapon, with about 1 s of visibility after. Healing should not break it. Centralise the break rule in one function.
  - The cup is shrouded too. A Burdened carrier is slow, which balances it. Watch escort cases in bot tests.
  - About 15 s cooldown. Gold chip in the bottom-left row with a timer.
  - Blink: smoke at both ends, a small real cloud (about 1.5 m, 1 to 2 s) at the start and the landing spot that blocks sight, so he can cover his own getaway or arrival. Agreed 17 Nov. Possible later: a backstab cuts his Blink cooldown.
  - Swap (right click alternative to the Shroud): trade places with a teammate in smoke, rescue only (teammate under about 50% health or holding the cup), half-second smoke telegraph, no veto, tuning rows for threshold and cooldown. Not agreed, a candidate to test against the Shroud.
  - Ideas parked: decoy (dummy Rascal that draws aim), bag of rats on G (scurry out, bite, mark three enemies), ranged-only damage reduction.
- Bots: Rascal bots lean on grapple to flank; check what they do now and retune around Blink and the Shroud.
- Grapple on the Lampist: confirm it is in place and bot use.

## Backlog: universal backstab (agreed, not started, 17 Nov)
- Every class gets 1.5x melee damage from behind (about a 110 degree cone behind the victim). Melee only: no shots, bolts, flames or thrown weapons.
- Master toggle, default on or off to be decided. Per-class tuning rows. Rascal possibly higher (2x) to keep his identity.
- A cue for the victim (directional hit marker or toast). Bot test for one-hit kills from behind (hammer 55 becomes 82, charged smash 150, Diamond Spear 40 becomes 60).
- Crusader suffers most from flanks; the raised Blessed Shield's front arc is his answer.

## Backlog: platforms and input (ideas, not started, 16 to 17 Nov)
- Split screen (two humans, one screen): hard. Rendering is easy (two scissor viewports), the work is making PLAYER, viewmodel, HUD, shake, FOV, overhead icons, edge overlays and audio listener per-player. Player two needs a gamepad. A few sessions.
- Xbox gamepad, one player: small, about one session. Gamepad API writes into the same per-frame input state. Sticks, triggers, bumpers mapped to abilities, dead zone and sensitivity sliders, button names in hints, Start for pause. Rumble later. Crouch could sit on a stick click.
- Crouch: new mechanic, moderate. Lower eye and body height with a ceiling check, slower walk, hit height changes (balance), third-person pose per class is the biggest piece. Hold or toggle undecided. Tuning rows.
- Phone touch controls: moderate. Thumb stick and drag-look, ability buttons, landscape lock, HUD touch layout, low-quality mode for performance. Do after gamepad.
- Friends playing: share the artifact link (Share menu, you set access) or send the single HTML file (needs internet for three.js and fonts). Online play against each other is a separate, large job. A static host such as GitHub Pages is the clean link.

## Agreed 17 Nov (supersedes the entries above where they differ)
- Rascal Shroud (right click): about 5 m burst, 5 s, team and cup carrier mostly invisible (shimmer within about 4 m). The cup itself is NOT shrouded: the carrier hides but the cup stays visible. Breaks per player only (one teammate attacking never breaks anyone else's cloak) on attack, ability or charge; healing does not break it. Adds about 15% movement speed for the full 5 s even after the cloak breaks (positioning tool). About 15 s cooldown. Gold chip with a timer. Capped option: himself plus the two nearest allies. Ambush bonus dropped.
- Rally rework: attack and reload speed as now, plus ability and throwable recharge about 1.5x (never its own cooldown). Movement speed comes off Rally. This also covers the open Brigand javelin regen item.
- Blink clouds: smoke at both ends, small real cloud, no marks and no damage.
- Smoke bomb: ordinary cloud everyone sees, enemies inside are outlined and marked for the whole team. Teammates no longer see through it (current build lets the team look through).
- Swap and decoy stay as parked candidates. Swap, if built: rescue only (teammate under about 50% health or holding the cup), half-second telegraph.
- Universal backstab: melee only, 1.5x, master toggle, per-class rows.
- Rascal fighting dagger: serrated and curved, mock-ups sent (A sickle fang, B recurved barb, C wicked kris), choice pending. Likely A's curve in dark steel. Throwing daggers stay small, plain, silver.
- Chalice: the final kill that fills the cup is worth more (5 instead of 3, so a full cup is 14, tunable "final kill value"). Drinking kills the drinker: the pot banks, the holder dies with no enemy credit (counted as a sacrifice, not a normal death), the cup returns to its shrine empty after about 5 s. Prompt is "DRINK" with a drawn skull icon, with a clear warning. Master toggle "Drinking kills the drinker" (default on). The cooldown refresh on drink moves to its own toggle, default off. Bots need a rule for when to drink (kill threshold, or cornered). Check the 30 point win target with roughly 14 per cup.

- v0.283: Rascal fighting dagger: same hilt, blade 0.74 m (was 0.56), dark steel, ten teeth down one edge pointing back toward the hilt, gentle curve in toward the toothed edge, fine lighter groove down the middle. Throwing daggers unchanged.

## v0.284 (17 Nov): built from the agreed list
- Chalice: the kill that fills the cup is worth 5 (tunable, a full cup is 14). The cup HUD shows LAST KILL x5 and pulses rapidly one kill from full. Drinking banks the pot and kills the drinker: no enemy credit, not counted as a death, feed says DRANK THE CHALICE, the cup reforms at the shrine after 5 s. Prompt is DRINK with a drawn skull. Switches: drinking kills the drinker (on), drinking resets cooldowns (off), reform delay. Bots wait for a fuller cup before drinking (about 5 kills, or hurt with a decent pot).
- Rascal: blowgun gone. Right click is the Shroud: 5 s, 5 m, himself and nearby teammates vanish from enemy sight beyond 4 m (faint team-colour ghost for allies), 15% faster for the full 5 s, 15 s cooldown. Attacking, throwing or using Shift or G breaks it for that fighter only (healing, aegis, rally do not), then 1 s of visibility. An enemy outlined by smoke cannot hide. The cup stays visible. Gold chip with a timer. New right-click icon. Tuning rows for all of it.
- Smoke bomb (G): 4 m, 6 s, 14 s cooldown. A solid cloud for everyone, his team included. Every enemy inside is outlined for the whole team and stays marked 2.5 s after leaving (tunable). Damage and 15% vulnerability unchanged.
- Blink: small 1.5 m clouds for 1.6 s at both ends, sight-blocking only (no marks, no damage). Switch and sizes in tuning.
- Rally: movement speed removed (default 1, row kept). Rallied fighters recharge abilities, throwables, aegis and javelins 1.5x (not Rally itself).
- Backstab: every melee weapon does 1.5x from behind (switch and multiplier rows in the Shared tab). The Rascal dagger keeps its own 2.5x. Melee only.
- Not tested in play: shroud feel against real players, how often bots use it, the smoke-mark reveal against a cloaked team, the backstab on each weapon, balance of final-kill 5 and the drink sacrifice over a full match.
- Still open: swap and decoy for the right-click slot are parked; Seeker and others have no change; platform ideas not started.

## v0.285 (17 Nov)
- Cup is 7 kills: values 1,1,1,2,2,3,5 (15 in a full cup). Each kill's value is adjustable in the menu (Chalice tab, chp1..chp10, cup size chcup).
- Final-kill note: LAST KILL x5 with a rapid pulse.
- Burdened / Empowered: one step per point in the cup (2% each, 15 steps full), and four chevrons, one per distinct kill value reached (1x, 2x, 3x, 5x).
- Arbalest HUD shows 1 / 1, then RELOADING with a bar during the cooldown.

## v0.286 (17 Nov)
- Cup colours by tier as it fills: 2x bronze, 3x silver, 5x gold (outline, labels, multiplier). 5x marker added at the brim. LAST KILL note and pulse removed.

## v0.287 (17 Nov)
- Drain setting is now seconds per kill ("Dropped cup loses one kill every", 0.25 to 10 s, default 1 s). Drain pops the newest (highest) kill first.

## v0.288 (17 Nov)
- Chalice controls: hold F to drink, tap E to pass, hold Q to aim a throw and release to throw. While carrying the cup F no longer doubles as right click. Hints, help text and the controls list updated. Q still calls for a pass when you are not carrying the cup.
- Cup HUD redesign proposed (hero multiplier, 7-segment meter, key buttons, danger glow); waiting on Alex's go-ahead for a mockup.

## v0.289 (17 Nov): new cup HUD and Shroud shimmer
- Cup HUD rebuilt (mockups C to G, then Alex's notes). Top centre: a chalice drawn in the shape of the in-game one, liquid only (no tick lines, no labels). Outline is the tier colour (plain, bronze 2x, silver 3x, gold 5x, platinum when full). Liquid is the holder's team colour.
- Readout, in order of importance: tag (NEXT KILL, or THE CHALICE IS over FULL), the multiplier large, kills to the next tier, a rule, then the pot (+7 IN YOUR CHALICE). A teammate carrying shows CARRIED BY name.
- Pulse: the cup and the multiplier pulse, slow and small at 1 kill (about 2.3 s) and quick and larger when full (about 0.6 s). Off for reduced motion and when dropped.
- Enemy cup: soft red frame and glow, THEIR NEXT KILL, outline and number run from pale red to hot red as the cup fills (CH_HEAT), pot reads +7 IN THEIR CHALICE, full reads ENEMY CHALICE over FULL with no drink line.
- Dropped: CHALICE DROPPED in the large type, DRAINING POINTS with a bar filling to the next kill lost, then +N REMAINING. Neutral grey-violet liquid.
- Prompts: one pill low centre above the ability boxes: F DRINK (skull), E PASS, Q THROW. Drink dims below 5 points in the cup, lights in the tier colour, goes platinum when full. While drinking it shows a progress bar; while aiming it says RELEASE Q TO THROW.
- The old top banner (Your team has the chalice, Chalice dropped) is gone; only The chalice is free remains.
- Shroud: shrouded allies now show a dark blue-green shimmer shell (brighter at the edges, slow bands rising up the body) instead of the flat team-colour ghost. Enemies still cannot see them beyond about 4 m.
- Not tested in play: pulse rates, enemy heat ramp against the orange team colour, shimmer visibility in bright rooms, the dropped panel width on small screens.

## v0.290 (17 Nov): Shroud looks like faint smoke
- A shrouded ally, seen by their own team, is now a faint blue-green smoke figure: the body fades to 16% (GHOST_BODY, on its own copies of the materials) and a drifting smoke shell (noise-based, thicker at the edges) sits over it. Ink outlines hide while shrouded. All restored when the Shroud ends.
- Replaces the v0.289 glowing shell, which Alex found too solid.
- Open: an enemy within about 4 m of a shrouded fighter currently sees them as a normal, fully visible body. Alex has not said whether they should get a faint smoke too.

## v0.291 (17 Nov): renamed
- The game is now called Chalice (was Dark Chalice). Changed: page title, menu logo, version tag ("Chalice 0.291"), the tuning copy text, the map draft text and its download filename. Chalice mode keeps its name. Help text now lists the 5x tier.

## v0.292 (17 Nov): ability name
- Renamed Blessed Shield to Bulwark in the Crusader kit, help text, break toast, and tuning labels.

## v0.293 (17 Nov): ability guide and game file
- The class screen shows Team, Field, and Movement ability icons. Hovering or keyboard focus reveals a one-line description. Field abilities are named Holy Book, Slowing Ward, Marking Smoke, Wall of Fire, and Powder Grenade.
- Renamed the game file to `chalice.html`.


## v0.296 (17 Nov)
- Q uses the class throwable or aims the Seeker's ward. G aims the Chalice throw and requests a pass when empty-handed. F drinks and E passes.
- Marking Smoke is deep purple for Thistle and deep orange for Marigold. Enemies are outlined in red for the thrower’s team. The mark lasts six seconds after they leave the cloud. A skull and downward chevron mark enemies overhead.
- The enemy Chalice readout leaves out the carrier footer.

## v0.297 (17 Nov)
- Q uses the class throwable or Seeker ward while free, and aims and throws the Chalice while carrying it. G requests a pass when empty-handed. F drinks and E passes.
- Marking Smoke uses softer purple and burnt orange tints. The Rascal's smoke icon has more billowing clouds around its skull and chevron.

## v0.298 (17 Nov)
- Replaced the Rascal's unused blowgun viewmodel with a small, low-held wooden horse head carved from a stick. It fades into blue-green Shroud smoke when used, then wisps reform it as the Shroud cooldown finishes.

## v0.299 (17 Nov)
- Wired the new local menu into Game Setup, the pre-game lobby, kick-off, death, and respawn. Setup uses real map thumbnails. The lobby uses live class portraits and the same roster that spawns in the match.
- Renamed Scryball to Divination and Scrum to Skirmish in the game UI. Online and LAN are marked Soon.
- Centered health and status effects, moved abilities to the right and weapon readouts to the left, and added a flash as abilities recharge.

## v0.300 (17 Nov)
- Replaced the fingers on the Rascal's horse totem grip with one ball hand. All character model hands use balls, including first-person props.

## v0.301 (18 Nov)
- Editor flight no longer depends on mouse capture. Right drag turns the camera when capture is unavailable.
- The menu chalice shows a lit ruby. Each half of the cup's band now has a fifth gem, sapphire. When the cup fills, sapphire sweeps across each face from right to left and all five pulse together.

## v0.302 (18 Nov)
- Restored the original icy white sapphire glow on the full chalice and its HUD. The fifth gem still lights first, then the glow sweeps left and all five pulse.

## v0.303 (18 Nov)
- Made the skulls flush with the chalice bowl and lit the far-right gem of each menu band with the same icy white-blue as the full cup.

## v0.304 (18 Nov)
- Divination's menu ball holds a dark blue-green vortex. Skirmish shows the in-game claymore crossed with the crystal staff. Both turn continuously around a fixed center.

## v0.305 (18 Nov)
- Slid the menu claymore along its blade axis so its pommel sits level with the base of the crystal staff.
- Enlarged the menu chalice by 30%. Divination and Skirmish are marked Soon and their cards preview art on hover or focus. Centered the Divination ball in its ring and used a straight-on view to keep the Skirmish weapon bases level while they spin.

## v0.306 (18 Nov)
- Centered the crossing of the claymore and crystal staff in the menu ring. The Chalice HUD now shows the projected next kill and the points in the cup in two columns. Full cups retain the drink prompt for the carrier.

## v0.307 (18 Nov)
- Moved the class crest and abilities to the bottom left and weapons to the bottom right. Restyled the Chalice controls to match the HUD and removed the ordinary pickup toast.

## v0.308 (18 Nov)
- Mirrored the taper on the class health bar and its Aegis outline.

## v0.309 (18 Nov)
- Moved the Aegis icon to the status row above health. The blue outline still shows how much protection remains.

## v0.310 (18 Nov)
- Replaced the Tutorial page with seven clickable slides, illustrated with screenshots from a Chalice match. The last slide links to Game Setup.

## v0.311 (18 Nov)
- Crusader's Bulwark is planted in place, stays fixed while he moves, and is about 13% wider. The holy symbol flashes as it appears. Allies can still move and shoot through it.
- The Crusader's warhammer has a longer haft and a larger head, and is held with both hands when neither hand is needed for an ability animation.
- Holy Book opens once, then sends three shockwaves during its three-second effect.

## v0.312 (18 Nov)
- The Chalice carrier cannot attack or reload with a two-handed weapon. The game swaps to a one-handed weapon when one is available, and the HUD keeps the 1H / 2H labels visible and marks locked weapons.
- Removed the setting and reload / swing workarounds that let heavy weapons act one-handed while carrying the Chalice. The Crusader's final one-handed / two-handed weapon pairing awaits the mace design choice.

## v0.313 (18 Nov)
- Crusader carries a studded flail in slot 1. Its chain trails a sweeping overhead attack that can hit several enemies in front of him for 32 damage each at default tuning.
- The two handed Warhammer replaces the Arbalest in slot 2. It keeps its knockback and charged smash. The left hand leaves the shaft during ability animations.
- Picking up the Chalice puts away the Warhammer and draws the flail. A dimmed Warhammer row uses the same gold Chalice icon as the locked abilities.

## v0.314 (18 Nov)
- The studded flail swings out in a wider right-to-left arc. The chain straightens at full extension and bends again as the head drops.

## v0.315 (18 Nov)
- The flail chain starts uncoiling during the windup. The wrist eases into the cut so the head travels continuously into the sweep.

## v0.316 (18 Nov)
- The Seeker holds the Diamond Spear with both hands in first and third person. The left hand releases the shaft for abilities and returns to the grip afterward.
- Diamond Spear is a 2H weapon. Picking up the Chalice stows it and brings out the Crystal Staff.
- Restored the boxed 1H and 2H labels in the weapon HUD and class loadouts. A gold Chalice icon still marks locked weapons.

## v0.317 (18 Nov)
- The Diamond Spear sits straighter in both hands and extends to the centre of the reticle during a jab.
- Deployed Bulwark uses the Low Parapet design with five crenellations and glowing stone joints. Enemy shots can go through the gaps. Allied shots still pass through the wall.
- A tapped Warhammer attack plays its full 0.32-second wind-up. Releasing a held charge still goes straight into the swing.

## v0.318 (18 Nov)
- Rascal casts Shroud with a quick sweep of his empty left hand. Removed the wooden horse totem.
- Shroud makes first-person hands and weapons translucent and trails blue-green wisps around the edges of the view. This applies to the Rascal and any affected teammate.
- Shrouded fighters stay faintly visible to enemies at range. Shroud still limits the distance at which enemy bots detect a fighter.

## v0.319 (18 Nov)
- Mausoleum's rotunda uses weathered stone, and the broken burial niches contain rubble. Softened the waterfalls, foam, and oculus glare.
- Grounded the mushrooms on the terrace, fallen rubble, or the curved surfaces of the column drums.

## v0.320 (18 Nov)
- The Chalice rests on a low stone plinth in the centre of Mausoleum's rotunda. Its light fades when claimed and returns when the cup reforms at the shrine.

## v0.321 (18 Nov)
- Six tutorial slides teach the Chalice objective, shrine, gem scoring, drinking, carrying, and dropped state using new screenshots from Mausoleum.
- Mausoleum is the selectable match map. Basilica and Scrollwork stay available in the map editor.

## v0.322 (18 Nov)
- The tutorial has a Points tab with per-kill values, running totals, and a sapphire FULL row for the 15-point cup.

## v0.324 (18 Nov)
- The friendly HUD uses ruby for NEXT KILL +5. Sapphire appears when the chalice is full.

## v0.325 (18 Nov)
- Classes show teammate names beside the same class crests used in the HUD. Removed class squad numbers from name tags, armor, and setup. Champions keep their squad numbers.

## v0.326 (18 Nov)
- Dagger, greatsword, and Champions sword attacks clash when opposing strikes are in reach and close to landing. Both recoil without taking damage.
- Shroud uses the status chip above health for nearby allies and the Rascal who casts it.

## v0.327 (18 Nov)
- Shroud uses a hood dissolving into wisps on the Rascal's ability tile and the active status chip.

## v0.328 (18 Nov)
- The main menu has a Classes page with live portraits, health, loadouts, and ability descriptions. Browsing is separate from the match class choice.

## v0.334 (20 Nov)
- Hand rules for the Crusader, Lampist, Rascal and Seeker, following the Zealot. Left hands now stay on the weapon and leave it only for an ability or the cup.
- New shared carry (carryLeft, CARRY_LOW): the left hand reaches down to the cup, lifts it, lowers it on a drop, then returns to the weapon. The cup rides the hand through f.chHand for all five classes, not just the Zealot.
- Crusader: with the Holy Blunderbuss out the left hand sits at its fore point (model.userData.fore). The book, the charge and the raised shield still take the hand first. First person gains the foregrip hand.
- Lampist: the Furnace Lantern hold keeps its support grip, and the cup carry now rides the same hand through the reach, lift and lower.
- Rascal: his read on the Infernal Daggers. The fan stays in the right hand (the right arm now follows it, it used to hang at the old kit hold), the left hand does the sending: a quick wrist flick per knife thrown and a sharp whip back on the recall, in both views. trialRecall stamps w.recalledAt for the whip. The smoke bomb no longer floats over the left hand while the throwing kit is out.
- Seeker: with the Runic Repeater out the left hand carries the cup with the same reach and lift. Staff and spear holds are unchanged on purpose.
- No balance numbers changed, nothing to log in codex-weapon-niches.md.

## v0.337 (20 Nov)
- The Crusader's blessing reload went in: through the three-second reload the blunderbuss tips its bell up, the left hand traces the sign over it, a bead of light runs from the cross into the bell, and the cross lights with it. Both views. This entry is logged late, the version landed between other agents' builds.

## v0.341 (20 Nov)
- The Crusader's blessing actually moves his hand now, in first person. The reload path helper was called with the wrong argument list, so every point on the path collapsed to one static chest point and the hand sat still for the whole reload. Found with a throwaway hooked copy of the page, never shipped.
- The Lampist's feeding reload: the lantern dims a little with every shot and gutters nearly dark by the sixth. On the reload she rolls the launcher slightly right, her hand hovers just off the left glass side, golden-orange flame wisps curve from her palm into the cage, and the six lid dots relight one by one. Both views.
- The Seeker's wicking: on the three-second overheat her hand comes out low to the left, palm up, and the heat swings off the crystal and curves down into her palm while the crystal cools back to her colour. Both views, the wick arms built lazily over the staff pose.
- The Rascal's catch: the whip back already existed, now each returning knife snaps into the fan with a short pop and a small catch pulse of the hand, one per arrival. Both views.
- The Zealot's knitting: on the two-second recharge the left hand passes along the rifle's spine only as far as the furthest broken rib, and the ribs regrow in a wave behind the fingers, bone closing like frost. A full magazine walks the whole spine. Both views.
- The class portraits hold their primaries casually now: the Crusader with the Holy Blunderbuss low at his side, the Lampist with the current armory lantern, the Rascal with the three floating Infernal Daggers, the Zealot with the Skeleton Rifle low across the front. The Seeker keeps her staff.
- No balance numbers changed, nothing to log in codex-weapon-niches.md.

## v0.342 (20 Nov)
- The Lampist's reload no longer blinds you in first person. The game's fxSprite takes opacity as its third argument and has no scale argument; the feeding, wicking and knitting passed their intended sprite scale there and never set the scale, so every wisp and palm glow rendered at 1 by 1, which at viewmodel distance is most of the screen, additive. All those sprites now carry explicit scales.
- The Crusader's holy symbol hangs from his belt now, and the Lampist's lantern hangs from hers, both with a small sway. The hands pick them up only for the light, the charge and the heal, and put them back. First person shows the props only while the ability is in hand.
- The Rascal's three daggers in third person now match their first-person size (0.82 instead of 1.05 on the trial hold).

## v0.343 (20 Nov)
- The Rascal's daggers in third person halve again (0.41 on the trial hold) and the cluster is lifted 0.14 above his hand, so the blades hover over it instead of sitting through it.
- The furnace lantern loses the raised lid panel. The six shot dots are set straight into the peaked roof, up the rear slope, and the lantern's glass now dims with the ember as the fuel runs down.
- The Seeker's staff is held down lower in first person (base at -0.82), the crystal head is 30% smaller, and both her hands are on the shaft. The floating ward hand that used to hang out to the left whenever the staff was out is retired from that state; it only appears for the spear's cast moment.
- The Zealot's knitting pass rides 0.25 above the barrel axis instead of 0.05, clearing the spine rod and the rib knuckles it used to clip through.

## v0.344 (21 Nov)
- The Seeker's hands are visible on her staff: they were inheriting the staff's 0.7 scale and coming out smaller than the grip they sat on. Scaled past it and set to the camera side of the shaft. The staff also moves right, base at 0.40 instead of 0.24.

## v0.345 (21 Nov)
- Selecting a class no longer inherits the previous class's weapon slot: setClass resets the trial record, so a new class always starts on its primary. This is what auto-switched the Seeker to her melee.
- The Diamond Spear's first-person hands are scaled up past its viewmodel scale, same fix as the staff's, so the melee view reads too.

## v0.346 (21 Nov)
- One sword for every class (SHARED_SWORD, on). In the melee slot, tap left click to slash and hold to draw back, then release to lunge with a heavy blow. Slash 40 damage, 0.6 s between swings. Heavy 70 damage, 3 m lunge, 0.95 s recovery, and you move at 70% while it is drawn. Clash works for every class now. Bots slash, and go heavy to close a gap after a visible draw-back.
- Models are unchanged for now (hammer, flail, rapier, spear, bone sword). A single sword model needs a mockup.
- Tuning rows for the heavy blow are in the Match tab under Combat rules. Numbers are in the balance log and the handover.

## v0.347 (21 Nov)
- The melee slot is now the classic sword for all five classes, named Bastard Sword in the HUD and menus. Same rules as v0.346 (tap slash, hold for a heavy lunge). The pommel stone is the team colour. First and third person both use the new model; the Seeker and Zealot now share the generic melee view.
- Unequipped weapons are stowed on the body: the sword sheathed across the back (hilt over the right shoulder), the Runic Repeater holstered at the right hip.
- The Zealot's wool mantle and its tufts are gone.
- Not stowed yet: the primary weapon. Class page text for the Crusader, Seeker and Zealot is still stale.

## v0.335 (20 Nov)
- The Crusader's left hand actually reaches the blunderbuss fore now. trialModel wraps the gun in a group and the fore point (and the cross) lived on the inner gun, so the v0.334 pose code read nothing and the hand fell back to rest. The wrapper now carries both, the fore scaled to match the gun build. The cross that lights during the windup was disconnected the same way, it works again.

## v0.336 (20 Nov)
- The Crusader's holy symbol no longer shows while the Holy Blunderbuss is out, in either view. The old visibility check read `weapon === 'melee'`, which the trial system makes always true for him, so the symbol (with its own hand in first person) sat in the left hand regardless of the weapon. It now shows only when the equipped weapon leaves the left hand free: the trial melee or the repeater, or while charging or flashing.

## v0.348 to v0.350 (21 Nov)
- Runeblade ported into the game as the shared sword (first person, third person, back sheath). Sword moved to key 3, Repeater to key 2.
- Arcanist: Ward (RMB, 12 s dome on an ally, 14 s cooldown) and Crystal Grenade (Q, 2 s fuse, 10 shards).
- Lampist: Lightbath (RMB, 12 s heal field, 18 s cooldown).
- Per-class first-person hands, Skulker pale green.
- Rascal renamed Skulker, Seeker renamed Arcanist everywhere user-facing.
- All throwables set to 20 s recharge (Smoke was 14).
- Open: Ward and Grenade HUD icons, beam deflection, stale Crusader and Zealot class-page rows, Marigold Runeblade check, stow the primary weapon.

## v0.351 (21 Nov)
- The Arcanist's staff hands are visible in first person again. The cause was position, not scale: the v0.343 rest put the grip below the bottom edge of the viewmodel frame (the hands read at -1.3 and -1.9 in view space, where -1 is the frame edge). Per Alex the staff is held higher and further right, rest at (0.52, -0.62, -0.74), the hands ride higher on the shaft (local y 0.72 and 0.42) with the sleeve cuffs following. The hands now read at -0.30 and -0.77, the crystal sits upper right clear of the crosshair, and the staff base still enters from the bottom edge, so the low hold keeps its character.
- Venting with the left hand now drops with the staff. The first-person wick condition tested VM.staff.visible, a flag that never changes on a weapon swap (only its parent group's does), so the venting hand kept floating after switching to the pistol. The condition is now gated on the staff being the equipped slot, the same gate the third-person vent always had.
- The Arcanist's levitate hand sits lower and further back, rest at (-0.22, -0.22, -0.90), so her long sleeve stays inside the frame instead of grazing and clipping through its bottom edge.
- The Lampist's lightbath now reads as a faint warm dome shimmering around her rather than the green circle on the floor, and the same gold pluses that used to drift from her raised lantern drift off her hip lantern through the bath, in both views. Numbers untouched: 12 s, 18 s cooldown, the old reach and rate.

## v0.352 (21 Nov)
- The Arcanist reads two hands, not three. Her left hand now lifts off the staff whenever it is out doing something else, venting, levitating or casting, so the venting hand is her left hand moving off the shaft rather than a third hand appearing beside it. It returns to the grip the moment the vent or the cast is done.
- Per Alex the right hand sits lower on the shaft and the left hand higher.

## v0.353 (21 Nov)
- The Arcanist's vent is one hand, animated. Her left hand now travels off the staff grip to the palm spot when the vent starts, holds there while the heat drains into it, and travels back when the lockout ends. The separate venting hand is gone entirely.
- For levitate and the ward cast, the same left hand slides down the shaft out of the frame while the casting hand rises in, an animated swap rather than a pop.
- Her robe cuffs in first person are twice as long, the mouths still at the wrists, and the left cuff travels with the venting hand.

## v0.354 (21 Nov)
- The Arcanist's staff leans gently back toward the camera now, its forward tip eased from -0.30 to -0.18 radians, the crystal closer to the player and still upper right, both hands and the grip in frame.
- The sleeve cuff no longer separates from her hand ball while she vents: the left cuff rides the wrist at the same rigid offset it keeps at rest, through the whole travel out and back.

## v0.355 (21 Nov)
- The Arcanist is an elf: pale blue skin, open hood with a visible face, pointed ears, pale blue hands in both views, three crystal shards on the belt.
- The sword rests low at the bottom right and is drawn in from above on equip.
- Merged onto the other agent's v0.354 melee and staff work.

## v0.356 (21 Nov)
- The Arcanist's eyes are almond shaped, tilted up at the outer corners, not straight slits.

## v0.357 to v0.358 (21 Nov)
- Arcanist eyes 30% smaller.
- Fixed the Arcanist's first-person staff hands, which were still skin coloured; now pale blue.

## v0.359 (21 Nov)
- The sword swing is rebuilt in the game: three cuts in rotation, the heavy lunge, hit stop, camera roll and a viewmodel jolt on a hit. Tap windup 0.15 to 0.20 s.
- Not yet: finisher, parry, tip damage, third person swing.
- v0.360: sword parry (R). Marth-based window, 1.5 s whiff, flash + ping, 0.22 s freeze on catch, first and third person poses, bots parry.
- v0.361: forced right to left riposte after a parry, 1.35x damage on an opened enemy.
- v0.362: gentle first-person movement sway on all weapons.

v0.363 (21 Nov): new class HUD. Health bar sits on the left above the three ability tiles (insignia removed); weapons on the right with flat cream icons (embedded WICON, keyed by weapon name via WI_KEY); status chips show symbol + name for 2 s then shrink to symbol + draining bar, with a Settings toggle (localStorage dc-status-names, default on). Chalice UI: cup points chip beside each score (reserved dashed slot), bank fly animation when the cup is drunk, bottom-middle carry line ("YOU CARRY THE CHALICE  +n NEXT KILL") above the Q/F/E prompts. Old #chalHud panel hidden under body.nhud. Layout wrapper is #nhL; scale set in nhUpdate.

v0.364 (21 Nov): banking chime. sfx bankChime (bright bell, your team) and bankChimeEnemy (lower, their team) play from chalBankFly when the cup is drunk, alongside the points flying to the score.

v0.365 (22 Nov): new map Cathedral (MAP_ID cathedral, buildCathedral, selectable alongside Mausoleum). Two-level basilica 130 x 80 m: apse bases at x +-52..65 behind a chancel screen (main door + flank doors), pillared antechambers, flank corridors with stairs up to a +3 m mezzanine over each antechamber, nave with a 0.6 m chancel step, arcade, pews and toppled drums, a ring of 8 giant columns round the crossing, Chalice dais at centre, chapels with four landmarks (same block, different dressing), transept halls. Gallery at +6 m over the inner aisles and both transepts, chest-high parapets, two bridge spans over the crossing with a 7 m gap above the cup. Ten stairs. Stained glass via glassTex (lancets, two rose windows, dome oculus with a light beam). Flight cap at 18 m. Measured: median sightline 9.5 m, 7% over 40 m, no spawn-to-spawn sightlines. Bot match clean; bots reach the gallery and mezzanines. Menu art borrows the Basilica image for now.

v0.366 (22 Nov): weapon stack rebuilt to match the HUD mockup (#nhWp rows: big panel for the weapon in hand with slot numeral, icon, large count, name and a thin bar; slim rows for the other two with their own counts; team bar on the primary; locked primary fades with the cup icon). wpAmmo(p, slot) gives counts for any slot. No RELOADING text anywhere: the count stays and a thin bar fills during a reload (rifle, furnace, blunderbuss; blunderbuss wind-up uses the same bar). Runic Repeater shows numbers only, violet while charging, held or stowed. Arcanist staff keeps its heat bar and HOT/OVERHEATED.

v0.367 (22 Nov): bot fixes. (1) Nav: bots standing on the Cathedral spawn pads froze ~3 s because two nodes sat closer than the 1.2 m arrival radius; navTarget now skips nodes the bot is already within 1.5 m of, and botControl re-picks the next node the moment one is reached (reached needs |dy| <= 1.4, so a bot on a bench no longer counts a node below it as reached). (2) Lampist Flash Dash: also fires when hp < 45% and the target is within 9 m, and ~1.2%/frame sidestep when an enemy faces her at < 16 m and hp < 80%. (3) Gallery perches: botPerch() gives every even-id Arcanist/Zealot a node with y 4.5 to 9, 14 to 34 m from the objective with LOS to it, held 20 s (3 s retry when none). Only used when there is no target. Bot time at y > 5 is still only ~1% overall (5 to 8% for the perched bots). Measured, not fixed: bots almost never draw the shared sword (< 1% of alive time for every class but Skulker), because their roles keep them at range. Idle % in my harness is mostly bots waiting at goals, not a stuck metric. Harness: /home/claude/w5/au*.js (not on the Mac).

## v0.369 (22 Nov)
- Cathedral mesh audit: every piece buildCathedral() adds is now logged with its world bounds and support class in cathedral-mesh-audit.md, 297 pieces from the editor record. One flag: the fallen bell at the southwest landmark sat half-buried in its cover block, base at 1.03 against a block top at 1.5. It now lies on the stone, rim resting on the block, y 2.3 to 2.77. Everything else rests on the floor, a wall, a column, a slab, or is mounted glass or light by design. Capture shots for matching: mock-assets/shots/cath-gallery-side.png and cath-aisle-sw/se/nw/ne.png.

v0.368 (22 Nov): team lists show class crests (classCrest(k, team)); Skulker menu portrait daggers use the first-person build at half size with armWisps (P.pwisps animated in pose()).
v0.369 (22 Nov): (1) Title screen: #titleScr inside #menu, shown while #menu has class `titling`. The real makeChalice() turns in #titleCv (own renderer, stops drawing once dismissed), animChalice drives the ichor, gems strobe like wing lights (blue, ruby, jade, sapphire, out of step). Background is a slow black/navy/purple CSS shimmer. Any key, click or pad button calls dismissTitle() and shows the existing main menu. #ver is now always visible bottom right on every menu (railFoot copy removed). (2) Full gamepad support, one block under "Gamepad (Standard mapping)": padUiScreen() picks title/menu/pause/end/death picker; D-pad or left stick moves a focus ring (.padFocus, nearest item in that direction, held repeat), A selects, B backs out ([data-back], backLocal, lessonBack) or resumes from pause, left/right nudges sliders and selects. In a match: RT fire, LT Q, LB Shift, RB right click/F, X reload/parry (R), B and L3 pass (E), D-pad left call for pass (G), Y tap swap / hold sword, R3 and D-pad down sword, View scores, Start pause. Radial dead zones, curved look response, Settings: Controller look speed (dc-pad-sens) and invert Y (dc-pad-invert). padMode (last input) swaps HUD prompts to pad glyphs via K(); .padOnly/.kbOnly spans. Rumble on hits taken and kills (padBuzz). enableFallback stays silent in padMode. Verified with a fake pad in puppeteer: title to menu, setup, lobby, Ready Up, match, pause, resume, respawn picker. Not tested on real hardware. Also folded in the other session's Cathedral bell fix (y 2.77).

v0.369 fix (22 Nov): pad RT press now adds mpressed(0), so weapons that fire on the press (blunderbuss, daggers, repeater) fire from the trigger; right stick up now looks up (pitch sign was inverted in the original pad code). Selected or hovered gold buttons (.play, .setupBtn) glow via a drop-shadow on the parent (the clip-path would cut a box-shadow) and pulse.

v0.369 menu (22 Nov): the main menus (not the in-match menu) use the title shimmer as their background, with the rail and panel made see-through; the 3D map no longer shows behind them. Gold buttons are wrapped in .goldWrap so the hover/focus glow lights only the button.

v0.369 tuning (22 Nov): BB_SHOTS 3 (was 2; bbshots:2 added to TUNE_OLD_DEFAULTS so an old saved tuning value is dropped). TRIAL_REPEATER.gemRecharge 3 s (was 5). Crusader first person: blessFade now eases fpLeft back to fpLeftBase, so the left hand no longer stays floating above the bell after the blessing reload.

v0.369 pad fix (22 Nov): I.throwL used pressed.has(KeyQ), so LT never threw; now just(KeyQ). Same for the Shift nope flash while carrying the cup.

v0.369 Bumper Jumper (22 Nov, Alex chose it): LB jump, RB melee (draws the sword, then swings; hold for the heavy), RT fire, LT throwable (Q), X movement ability (Shift), A class action / drink (RMB, F), B reload and pass (R + E), Y swap / hold sword, D-pad slots, D-pad left call for pass, R3 sword, L3 pass, View scores, Start pause. PAD_GLYPH matches; death skip shows LB. Menus unchanged: A select, B back.

v0.369 pad layout (22 Nov, Alex chose, replaces Bumper Jumper): A jump, LB movement ability (Shift), RB class action / drink (RMB, F), RT fire, LT throwable (Q), X reload or parry with the sword out (R), B pass (E), Y tap swap / hold sword, R3 sword, D-pad slots, D-pad left call for pass, L3 pass, View scores, Start pause. Aim assist (aimAssist(), controller only, Settings toggle dc-pad-aa, on by default): friction 0.55 look speed while the reticle is within a cone of about 2.2x the target radius (0.025 to 0.14 rad) on a visible enemy within 45 m (LOS and smoke checked), and magnetism carries 35% of the target angular movement while steering. No bullet bending.

v0.369 sword and pad (22 Nov): the three first-person cuts (SWCUTS) now swing from the shoulder: the hand travels a quadratic arc (h: cocked, landing, end; m: control point) across the view, the blade lags (q^2.2) and whips through, the follow-through carries it out of view, recovery eases out. Wind-up is half the windup, hit timing unchanged. The old wrist-flick version is in /home/claude/w5/index.pre-swing.bak. Pad: <summary> headers are now focusable, so the tuning groups in the pause menu and Settings open with A; held left/right on a slider speeds up (x3 after 6 repeats, x10 after 20).

v0.369 thrust (23 Nov): the heavy (THRUST const above swEaseOut3). Charging coils the hand back towards the camera (coil [0.07, 0, 0.15]) with the blade pitched down to point forward (coilPitch -1.3), trembling at full. The thrust drives from the coil to ext [0, -0.03, -0.08] (pitch -1.52) on a q^2/q^3 ease, so the hand stays low right and the blade spans from the corner to the crosshair instead of shrinking into the distance; holds 0.12 s, then pulls back. Hit timing unchanged. Old version: /home/claude/w5/index.pre-thrust.bak.

v0.370 (23 Nov): menu v2. The approved dark and gold controller menu is in the game. Title close-up into the cup, camera pulls back as the canvas shrinks into a 46vh brand over the wordmark. Home column: Local, Online (SOON), Extras (Tutorial, Classes, Map Editor), Settings. Game setup is four boxes: map list, read-only options summary, play box with a dark chalice and ENTER LOBBY, team rosters in the game's Thistle `#a98cff` and Marigold `#ff7048`. Editable settings live on a new Options page (Match, Bots, Classes). Lobby is five class cards with real portraits, weapons, abilities, locked tags for classes a teammate holds when duplicates are off, and Ready Up. Respawn reuses the cards with Deploy. The team switch moved to Settings. Pause is Resume, Settings, Quit with the tuning panel behind Settings and the HUD hidden. Full time and death reskinned. One focus everywhere: gold bar or border, pad A/B. Not done: Classes/Tutorial/Settings inner pages keep the old panels; the player name has no field; the options use chip focus rather than a left/right stepper; a map change still reloads the page. Tested node --check, eslint no-undef, a 15 second live Chalice match on Mausoleum, and the full menu flow with a fake pad. Death and respawn checked with a temp-hook copy, not a real death. No balance changes. Detail in `codex-menu-v2-handover.md`.

v0.371 (23 Nov, built from the v0.370 menu-v2 copy): (1) Skeleton Rifle magazine 15 (was 24). TRIAL_RIFLE.capacity; the existing rifleammo slider (3 to 60, step 3) drags it live; rifleammo:24 added to TUNE_OLD_DEFAULTS so an old saved 24 is dropped. The rib cage now breaks in proportion to the magazine (eight ribs whatever the capacity) in all three places that count them. (2) The carrier's sword kills bank +1: SWORD_CUP_BONUS = 1 beside CH_CUP; chScoreKill(a, t, w) takes the weapon from kill(); the bonus applies only when w === 'sword' and a === CH.holder, between the roll and the push. No cap (max cup value 5, so 6 at most). Tuning row swordcup (0 to 3) on the Chalice tab under The cup. Probe: carrier sword kill banked 2 (rolled 1), rifle kill 1, teammate sword kill 1, carrier sword kill at kill 4 banked 3 (rolled 2). Lint clean, bot match ERRORS 0. Not committed: index.html also carries the other agent's uncommitted menu-v2 work.

v0.372 (23 Nov): the carrier sword-kill toast reads "+N  ·  BY THE SWORD" (N = what that kill banked, bonus included; "· LAST KILL" appended on the seventh). The top scoreboard cup slots (#cpotB / #cpotR) no longer show a dashed empty box: with no cup, each slot shows a solid grey box with the cup outline (CUP_MINI) in grey; when a team takes the cup it lights in that team colour with a soft glow and the pot count. Lint clean, bot match ERRORS 0.

v0.372 scoreboard fix (23 Nov, Alex): the cup slot is vertically centred in its score panel (align-self:center), always the same 56 px with the pot-number space reserved (the em is kept and hidden when empty), so the panel never resizes and the cup never shifts. Empty: transparent, dotted box border, cup outline drawn in dots (stroke-dasharray). Held: lights solid in the team colour with the pot count, as before.

v0.372 scoreboard fix 2 (23 Nov): both team score panels are plain rectangles (the enemy panel had a slanted clip-path edge and yours did not; removed in .tscore.blue/.red and the #topbar.flip variants). The cup slot was picking up the menu-v2 .slot rule (all:unset, 6px 10px padding, display font, cursor) because it shared the class name; it now uses .cpot.shown, so it is its intended 56 x 26 and sits exactly in the vertical middle of the panel. Watch for this: any HUD element with a class called slot will be restyled by the menu.

v0.372 tutorial (23 Nov): CHALICE_LESSONS rewritten for the current carry rules. Carrying: primary and class abilities locked, fight with the Runic Repeater and the sword, throw / drink / pass; new screenshot (TUTORIAL_SHOTS.carrying, Crusader on the Repeater with the lock marks). New slide after it, Sword / "By the sword": the carrier sword kill +1, carrier only (TUTORIAL_SHOTS.sword, the +3 BY THE SWORD toast). Points slide gains a line: the carrier sword kills bank one point more. The older shots (take, full, drink, drop, objective) still show the old HUD and the old flail/warhammer kit and want retaking. Not committed.

v0.373 (23 Nov): menu simplification ported into the game. LOCAL now opens Match Setup directly; the v0.370 Local game type page and the four-box setup are no longer on that path. Match Setup is the new three-column screen: the left column has the mode/match/bots lines, Map and Edit Game Options rows, the real Mausoleum plate, the mode-on-map caption, a loading bar and Start Game; the right column has the player count and the Thistle and Marigold rosters, larger, with class crests first. Edit Game Options is a wide row list with the bots sub-rows; Map is its own page. Start Game opens the new full-screen class select: class name, role, HP, line and ability descriptions on the left, the live portrait in the centre, the team roster on the right with class crests and class names only, the five crests along the bottom and READY at the bottom right. READY launches the existing 3 s kick-off. A second cup renderer sits behind Match Setup, Options and Map: dark bronze materials, large, tilted on the diagonal, spinning, and it starts from the home crest when you enter from the main menu. The in-match lobby, death and respawn still use the old renderMatchS so the match flow is untouched. Mockups remain in menu-redesign-mockup.html, match-setup-mockup.html and class-select-mockup.html. Tested: node --check, eslint no-undef, full menu flow at 1600x900 and 1280x720, and a live Chalice match on Mausoleum. No balance changes.

v0.374 (23 Nov): the Match Setup rosters show class names only, with the class crest and YOU or BOT, the same as the class select. Wren and Ash were placeholder names in the mockup, not game names; the generated bot names are gone from this screen. The in-match lobby still shows player names. Mockup roster updated to match.

v0.376 (23 Nov): Match Setup rosters show the generated bot names again, not class names and not class crests. Your team reads YOU plus the bot names; the enemy team reads the bot names. With bots off in Edit Game Options, the roster keeps the player and shows OPEN for the missing slots. Classes are only chosen on the class select, so nothing on Match Setup reveals a class. Mockup roster updated to generated-style names.

v0.377 (23 Nov, Alex): Cathedral removed from the menu map selection. PLAYABLE_MAPS is now mausoleum only, the Cathedral entry is gone from MENU_MAPS, and the legacy map button is gone. The map code and its editor data remain in the file; it cannot be chosen from the menu. The menu falls back to Mausoleum if a saved or linked map is no longer available.

v0.378 (23 Nov, from 0.377 / 5e53f04): (1) The sword cup bonus now pays any sword kill by the team holding the cup (SWORD_CUP_BONUS, team gate in chScoreKill), not only the carrier. Toast "+N  ·  BY THE SWORD" shows to the carrier and to the player who made the kill. Probe: carrier sword 2 (rolled 1), rifle 1, teammate sword 2, carrier sword at kill 4 banks 3. (2) chalSwordRise(team, amt): a sword glyph and "+1" pop in under that team cup box (#cpotB / #cpotR), hold a beat, rise into it (950 ms); the box shows the pre-bonus total (CHB.hold) until it lands, then bumps and shows the new total. Shown for both teams. (3) #toasts top 71% (was 60%). (4) #chalBot raised to 64 px (was 24). (5) The carry line leads with the cup outline (CUP_MINI) instead of the holder class icon. (6) Tutorial: Sword slide and Points note rewritten for the team rule. Lint clean, bot match ERRORS 0. Not committed.

## v0.437 (26 Nov): class select action navigation
- D-pad Down from a class goes to Ready/Deploy, and Right from the final class also reaches it. Up or Left from the action returns to the selected class. Ready has an explicit controller focus highlight.
- Removed the class name from the Ready button.
- Verification: script syntax, diff checks and a temporary Node navigation check passed. Live controller verification remains outstanding because local-file browser access is blocked.

## v0.436 (26 Nov): class picker navigation and portraits
- D-pad left/right follows class buttons in order and stops at the ends. Controller focus stays on the picked class after the menu rebuilds and starts on the selected class in the in-match picker.
- Removed the YOURS label from the selected crest.
- Class portrait camera moved back and aimed lower to include the full body and feet, with its aspect ratio set from each canvas.
- Verification: script syntax and diff checks passed. A temporary Node check confirmed class-row navigation reaches both ends without leaving the row. Portrait framing still needs live visual verification; local-file browser access remains blocked and ESLint is unavailable locally.

## v0.435 (26 Nov): class-change error and controller glitter
- Restored the local `oneHandedSword` declaration in `trialWorldView`, fixing the ReferenceError during class changes. Zealot melee now reaches the grip-aligned sword pose after his class-specific handling; its extra arms hide when switching to another weapon.
- Controller focus on START GAME now adds twinkling gold specks and a travelling shimmer, with a static reduced-motion fallback.
- Verification: extracted script passes `node --check`; `git diff --check` passes. A temporary Node harness exercised `trialWorldView` for all five classes through primary, melee and repeater slots using rendering stubs. ESLint is unavailable locally; live browser and visual checks remain blocked by local-file browser policy.

## v0.434 (26 Nov): gamepad Start Game focus
- The Match Setup START GAME button now gets a bright glow when selected by controller focus, matching its hover and keyboard-focus feedback. It was receiving the gamepad focus class, but its style did not include that class.

## v0.433 (26 Nov): persistent Lampist fire
- Active Furnace Lantern ground patches now keep seven bright flame tongues flickering in height, width, rotation and opacity until the patch expires. Their ground glow pulses gently so the hazard remains visible between fireball impact and expiry. Patch lifetime, radius and damage are unchanged.
- Verification: `node --check` passed on the extracted largest script. ESLint was unavailable and the browser blocked local-file testing, as noted in v0.432 below.

## v0.432 (26 Nov): impact, menus, weapon poses and controller aim
- Lampist Furnace Lantern impacts now make a wider, longer flame burst with a bright ground ring and central flare. The damaging surface patch, damage and splash numbers are unchanged.
- Gamepad focus now starts on PLAY at Home, then the primary action on the current menu page.
- The solo pre-match class select is the only class selection at kickoff. The kickoff countdown no longer reopens the class-card screen.
- Zealot's Bone Sword hand ball now sits around the leather grip; the active third-person sword and arms use one aligned pose.
- Skulker's three-blade fan sits higher above the hand and each blade drifts gently to strengthen the levitating read.
- Aim-assist target follow moved from 0.35 to 0.40. Friction, range and cone did not change.
- Verification: `node --check` passed. ESLint is not installed locally and `npx eslint` stalled; browser match testing was blocked when the browser policy refused the local `file://` URL.

### v0.438 · 26 November 2026

Cup progression: 1, 2, 3, 4, 5, 7, 10 points. Sword kills multiply the current value by ×2; per-gem points and ×1–×5 sword multiplier are exposed in Chalice tuning. Gold cup with two seven-gem rosettes, centre gem 7, attached stem, no middle band, and onyx skull inlays. Full cup turns gems and skulls sapphire with matching halos. Score target unchanged.

Validation: extracted game script passes node syntax and ESLint no-undef checks. Isolated scoring checks pass for ordinary kills, sword ×1/×2/×3/×5, full-cup cap, drain/refill and team gating. Live Chalice match and visual review remain pending because browser policy blocked the local file URL.

### v0.439 · 26 November 2026

Sword kill feedback shows the active multiplier: the points toast reads, for example, "+10 · SWORD ×2", and the rising sword icon displays "×2". Both follow the multiplier set in Options. The cup counter still adds the actual bonus points when the animation lands.

## Requested polish: Zealot splinter readability (26 Nov)
- Make the Bone Splinter effect more obvious in play. Alex requested this as a follow-up note while authorizing the Bellringer and class ability changes; do not silently change splinter damage.

## v0.440 (26 Nov): Bellringer and support/control kits, local first build
- Added Bellringer to class selection and bot pools at 150 HP, using the accepted archer/bell-helmet prototype. Shared sword and Repeater retained. Full bow charge takes 1.5 s and fires a travelling, piercing soundwave: 100 body / 150 head, no damage falloff. Tap release makes a short peal. Added positional bell windup and release sounds.
- Alarm Bell takes over the 10 m / 5 s team reveal. One thrown tuning fork arms 1 s after landing and triggers within 2 m with line of sight: 3 s silence and 20% slow on the triggering enemy, then breaks. Reused the old terrain grapple.
- Lampist fireballs now deliver 60 direct / up to 30 splash without lasting ground fire. Shield Lantern grants 50 temporary overshield for 8 s on an ally hit; a ground or enemy impact becomes a 0.65 m hovering pickup for allies, including Lampist, lasting 10 s. One waiting lantern per Lampist. Lightbath retained.
- Arcanist Ward is a stationary full sphere at the cast point, with friendly shots passing through and enemies free to enter. The staff orb now does 60 direct damage and leaves a 2.5 m field for 3 s at 20 damage/s, retaining its existing splash, charge, travel and forced overheat. Ward/Bulwark hits break the protection and consume the orb without a field. Crystal Grenade retained after Alex's follow-up question.
- Crusader Bulwark is 20% narrower and slightly shorter. Tap right click and release to protect self; hold at least 0.25 s to aim at an ally and release to protect them. It follows its target's position and facing. Friendly shots and enemy movement pass through; swords remain useful after crossing the wall.
- Recorded all provisional values in the playtest balance log in `codex-weapon-niches.md`. Updated `bellringer.md`; added the requested Zealot splinter-readability follow-up note without changing splinter balance.
- Verification: extracted largest script passes `node --check`; ESLint `no-undef` passes with browser globals declared; `git diff --check` passes. Temporary Node checks using the game's pinned Three.js r128 pass for both team character geometries, wave damage/headshots/piercing/wall stop, fork throw/landing/arming/single-use debuffs, ally/enemy lantern impacts, overshield values, and wall tracking. Local-file browser policy still blocks live Chalice match and rendered visual verification. Uncommitted and unpublished; existing changes from the other chats preserved.

## v0.441 (26 Nov): staff taps, grenade size and splinter visibility
- Arcanist tap damage 10 → 20, headshot 15 → 30, with the same 0.36 s interval. Saved old default damage migrates. Crystal Grenade visual model enlarged 20% without changing its combat properties.
- Added visible pale bone splinters to affected bodies; increased the Zealot-facing indicators' size, glow and spacing. No change to shatter damage or healing. Offensive replacement for shatter healing remains a design question.
- Syntax, ESLint no-undef, diff checks and targeted runtime checks pass. Live visual/play verification remains blocked by local-file browser policy. Unpublished.
- Follow-up: Arcanist tap/partial bolt speed 44 → 51 m/s; full orb remains 20 m/s.

## v0.442 (26 Nov): Belfry Market greybox
- Built the approved asymmetric church / fallen tower / market / catacomb plan in `buildBelfry`, with explicit spawns, custom bounds, a menu orbit camera and navigation. Plain stone, wood and team-tinted blocks; no art pass.
- All vertical routes use walkable ramps/stairs or ordinary jumps. Church crypt, well, cellar hatch and ossuary stairs connect the catacomb. Tower stump, scaffold and market gallery each have walking access. The shaft has a 2 m jump gap and a 0.8 m jumpable obstacle. The market grate is a one-way drop with a directed navigation link; no ladder or mantle-only route.
- Raised floor slabs are cut around every stair/drop opening. The underground cult chamber, bone hall, crypt, ossuary and south passage remain open under a separate street slab. Added a tiny overlap between slab strips after structural checks found strict collision seams at integer coordinates.
- The dais at x=0,z=0 is the highest surface under the cup spawn ray, at y=4.4. Tower tip and hanging bell are offset, and the bell has no collision.
- Not added to `PLAYABLE_MAPS` or `MENU_MAPS`. Explicit development preview: `index.html?map=belfry&preview=1`; editor: `index.html?map=belfry&edit=1`.
- Structural checks using actual game geometry, spatial queries and foot-navigation rules: 473 solid pieces, 12 ramps, 606 waypoints; all key landmarks reachable from both teams; ramp traversal checked excluding the intentional low jump obstruction; spawn floors/headroom and cup height checked; one-way drop cannot be walked up. Average graph path to dais across all eight spawns: Thistle 41.47 m, Marigold 40.59 m (about 2.2% difference). These distances do not establish combat balance.
- Live walk-through, screenshots, ten side-swapped Chalice bot matches and split-screen play remain unverified because the browser's local-file security restriction is still in force. Greybox stays hidden pending Alex's walk-through. No publishing or Git push.

## v0.443 (26 Nov): Bellringer hand and arm transitions
- Added a separate left ball hand in first person, tracking the striker during draw and returning after release. Right hand keeps the bow grip. Added a small bell jolt on firing.
- Fork and Alarm Bell now have a shared 0.82 s retrieve/throw/return animation, with the actual projectile released at 0.34 s. The held model disappears at release; it is not duplicated in the hand. These actions cancel a bow draw and temporarily occupy the left hand. Cooldowns begin on the actual release; Alarm Bell preserves the fork cooldown.
- Left hand reaches forward to aim/launch the old grapple, stays out while grappling, then returns. Grapple rope originates at that hand.
- Third-person Bellringer now uses moving sleeve/forearm segments and spherical hands, preserving the fixed round shoulderpads. Both hand poses follow the bow/other held weapon, with the left hand performing the same ability transitions. Removed duplicate static arm visuals.
- State and view rigs reset on death/class changes; silence or cup possession cancels an unthrown action. All hands remain balls without fingers.
- Verification: syntax and ESLint no-undef checks plus temporary Three.js r128 runtime checks for both rigs, draw tracking, held prop visibility, one projectile per timed release, independent cooldowns, interruption, grapple reach/hold/recovery and weapon slots. Rendered animation review and a live Chalice match remain blocked by browser local-file policy. Unpublished.

## v0.444: Bellstriker and Chalice HUD
- Renamed the Bellringer to Bellstriker. Raised the Bell-Bow in first person. The left hand supports it beneath the bell while the right draws the striker, throws and grapples. With the Repeater or sword out, the left hand handles abilities while the right keeps its weapon.
- The owner can retrieve a landed tuning fork with the field ability and throw it again immediately. One active fork at a time.
- The Chalice marker, score panel and carrier's scoreboard row show liquid in the carrier's team colour. Opponents see an ENEMY DRINKING toast when a drink starts and a live countdown. The dropped cup shows time until the next drain tick.
- Arcanist Ward radius increased from 2.0 to 2.6 m so allies have more room inside the sphere.
- Zealot Bone Sword shatter now grants 10% bonus damage per consumed splinter, up to 30%, in place of the flat damage bonus and heal.
- Bellstriker uses the original approved bell crest and dedicated Alarm Bell, Tuning Fork and Grapple icons from the reviewed mockup.
- First person weapon swaps now keep one left-hand pose visible. An active throw or ability takes over from the weapon support hand until its animation clears.

## v0.445: Gem HUD and progressive banking
- Mirrored score panels place both cup boxes beside the timer. Seven gem sockets sit under each team. The holder's outlines take their team colour. The next gem glows before the next-kill value.
- Drinking is committed, with a draining bar between the scoreboard and sockets. Each tick banks points, updates the cup pot, clears a gem and animates the deposit.
- Added the morning rules pass: first to 50, 10 minutes by default, sword kills fill two slots, 28-point full cup, close-range snatch, dropped-cup grace and rounded-up shared payout formula. Overtime accounts for ties and a live cup that can still affect the result.

## v0.446: Melee Chalice snatch
- An enemy melee kill on the carrier transfers the Chalice immediately. Primary, secondary and other non-melee kills drop it. A cup dropped on death can be picked up after landing.
- Added a V / R3 quick strike with the equipped weapon and a 10-damage hit. Hold Y or use the weapon slots to equip the full sword. Quick melee earns no By the Sword bonus.
- Raised quick melee to 15 damage for the first playtest.
- Made the regular hit marker larger and red, with a gold headshot marker and a larger, brighter red kill marker.

### 27 November 2026 · Sound preview integration

Integrated the approved sound study into the shared local build: low shotgun blast and sacred blunderbuss charge; sharp staff tap, charge and larger orb release; Furnace Lantern fire; individual Infernal Dagger throws and Skeleton Rifle shards; sword swing/impact, gem fill, drinking and bank release. PCM audio is embedded in index.html. Three one-shot variants avoid immediate repeats. Charges follow current tuning and stop on cancellation, death, pause or switching weapons. Existing Bellstriker sounds remain. No balance changes. Version/release edits left to the other person working in index.html.

Validation: extracted script passes node syntax and ESLint no-undef checks. Isolated audio checks verify all 13 embedded cue groups, charge timing/cancellation, drink loop and variation selection. Live Chalice match/audio review remains pending because browser policy blocks the local file URL; no alternate browser route was used.

## v0.447 (27 Nov): Belfry Market greybox rebuilt to plan v9
- Replaced the v0.442 greybox, which played as one flat open plaza. Layout now follows `mockups/belfry-market-plan-v9.html`: solid two-storey houses wall off tower lane, the square and tanners' lane, two more frame the market side of the square, and a collapsed house fills the west end of tower lane. Cover mixes waist height and 2.2 to 3 m pieces. Market and tanners' lane booths are solid with roofs, making 3 to 4 m alleys.
- No ladders. Every level change is a ramp or a switchback stairwell (two 2 m flights about 30 degrees with a 1.5 m landing): church crypt (6 m, railed hole in the nave), well pit and cellar pit (4 m, open to the sky, 1 m kerb as cover, open at the stair head), ossuary (4 m). The tanners' lane grate stays a one-way drop.
- New updraft lift (`BELFRY_LIFT`, `belfryLift()` called from `physics()` before gravity): a vent at about (-10.8, -9.7) lifts anyone about 6.5 m, then glides them onto the fallen tower ramp at (-8, -12.5), past the gap. Bots get a one-way nav link.
- Neutral materials only (stone, plaster, darker stone, wood). No team colours on the map, because more teams are planned.
- Church spawns moved clear of the crypt hole and the new pews.
- Checks: syntax, a lift ride test (lands on the ramp at y 9.3), nav graph of 773 nodes with every key spot reachable from both spawns (chamber, crypt, ossuary, both pit tops, grate bottom, tower tip, stump, lift landing, gallery), and 4- and 1.5-minute bot matches with no page errors. Bots used the lift, the tower tip, the gallery and the catacomb. Side balance not yet measured: the test player stood idle on team 0.
- Still hidden from the menu: `index.html?map=belfry&preview=1`.

## v0.448 (27 Nov): Bell-Bow weapon icon
- Added the Bell-Bow art to the primary weapon box (`WICON.bellbow`, `WI_KEY['Bell-Bow']`). Same method as the other icons: a side-on render of the in-game bow model in the cream icon palette, 200 px wide, bow longways with the bell where the model has it and the striker on the string, drawn back slightly so it clears the bell. Source PNG: `mockups/mock-assets/bellbow-icon.png`. Approved option A from `mockups/bellbow-icon-mockup-v2.html`.

## v0.449 Bell Rope throws straight, left-handed (27 Nov)
- The Bell Rope no longer flies on an arc (the arc could clip through walls). It uses the old grapple ray: it lands on whatever visible surface is under the reticle, within grapple range, then pulls you in.
- The bell travels out along the rope over 0.1 to 0.4 s (scaled by distance) before the pull starts.
- Aiming shows the old straight grapple marker with the "N m / OUT OF RANGE" readout. The arc guide is off.
- Always thrown with the left hand. With the Bell-Bow out, the bow flicks up over the right shoulder (0.12 s, `f.bellStow`) while the left hand holds the device up, then comes back 0.2 s after the throw. The bow can't fire while stowed. Third person slings it across the back.
- First person: the rope runs from the left side of the waist.
- traceBellRope and the arc branches in the grapple update are now unused; safe to delete later.
- HUD: the "V MELEE" reminder under the weapon box is hidden (`#nhQuick` display:none).
- Chalice model: added a thin inner lining to the bowl. The gem backs and the stem tip sat just through the outer wall and showed inside the cup. Ichor now starts at y 0.17, above the lining's floor.
