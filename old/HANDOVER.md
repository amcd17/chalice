# Dark Chalice: handover (v0.293, 17 Nov 2026)

Read AGENTS.md first for the rules. This file is the state of the project. `scryball-backlog.md` is the full running log. Where it disagrees with this file, this file wins, and later backlog entries win over earlier ones.

## What it is
The game file is `chalice.html`.
A first-person medieval-fantasy class shooter against bots, one HTML file, three.js r128. Design intent from Alex: less chaotic, more chess-like arena combat. Movement is slightly floaty, like the early Halo games, not fast. Games run about 10 minutes. Teams are Thistle (violet) and Marigold (red-orange).

The mode that matters is Chalice. One player carries the chalice. Each kill adds to the cup. Drinking banks the pot. First team to 30 wins. Test everything in Chalice first.

## Chalice rules as built
- The cup holds 7 kills. Values: 1,1,1,2,2,3,5, so a full cup is 15. Every value, the cup size and the win target are menu rows.
- Controls while carrying the cup: hold F to drink, tap E to pass, hold Q to aim a throw and release to throw. F still doubles as right click when you are not carrying the cup.
- Drinking (F) banks the pot and kills the drinker. No enemy gets credit, it isn't counted as a death (it's a sacrifice), the feed says DRANK THE CHALICE, and the cup reforms at its shrine after about 5 s. Toggles: drinking kills (on), drinking resets cooldowns (off), reform delay.
- The holder can use both weapons but no abilities or gear (right click, G, Shift). Light weapons are one-handed and usable with the cup. Heavy weapons are two-handed and not.
- Burdened (slower) and Empowered (more damage) scale with points in the cup, 2% a point, 15 steps when full. Four chevrons show on the status chips, one per kill value reached. Both stack with Rally and the kill multiplier. Both have toggles.
- Cup HUD (v0.289, top centre, function `chalHudDraw`): a chalice drawn in the shape of the in-game one, liquid only. Outline is the tier colour (plain, bronze 2x, silver 3x, gold 5x, platinum when full); the liquid is the holder's team colour. Readout order: tag, big multiplier (the value of the next kill), kills to the next tier, then the pot ("+7 IN YOUR CHALICE"). The cup and the multiplier pulse, slow and small when near empty, quick and larger when full. A teammate carrying shows "CARRIED BY name".
- Enemy cup: soft red frame and glow, "THEIR NEXT KILL", outline and number run from pale red to hot red as it fills (`CH_HEAT`), "+N IN THEIR CHALICE". Full reads ENEMY CHALICE over FULL.
- Dropped cup: "CHALICE DROPPED" in the large type, "DRAINING POINTS" with a bar to the next kill lost, then "+N REMAINING".
- Prompts: one pill low centre above the ability boxes (F DRINK with skull, E PASS, Q THROW). Drink dims under 5 points and lights up as the pot grows.
- A dropped cup loses its newest kill every N seconds (menu: "Dropped cup loses one kill every", default 1 s). It drains the top kill first. Internally `CH_DRAIN` is kills per second; the menu shows seconds per kill.
- Bots drink when the cup is nearly full, or when they are hurt and holding a decent pot.

## Classes (what is built)
- Crusader (`knight`): warhammer 55 dmg, arbalest (heavy, 1 bolt then auto reload, HUD shows 1 / 1 and RELOADING), Bulwark on right click (wide curved arc, allies pass through, enemies blocked, close melee hits on it do 12 and push the attacker back), holy book on G, Pious Charge on Shift (carries the original narrow heater shield). Weakest to flanks.
- Seeker (`sorcerer`): crystal staff (charge for one large bolt, glows white-hot as it heats), diamond spear (heavy), Aegis on right click (shield bubble on an ally, also covers the Seeker), ward on G, flight.
- Rascal (`goblin`): dagger (serrated, curved, dark steel, 2.5x backstab), throwing daggers, right click is the Shroud (5 s, about 5 m, his team goes mostly invisible, 15% faster, breaks per player when they attack or use an ability, cup stays visible; shrouded allies show to their own team as faint blue-green smoke: the body fades to `GHOST_BODY` and a drifting smoke shell `GHOST_SH` sits over it; an enemy within about 4 m currently sees a normal body, undecided), G is a 4 m smoke bomb that outlines and marks every enemy inside for the whole team, Shift is Blink with small smoke clouds at both ends. Identity: smoke, vanishing, subterfuge.
- Lampist (`lampist`): flamethrower (one-handed, limited gas), blunderbuss (heavy, 8 pellets), lantern heal on right click, fire wall on G, grapple on Shift (grapple belongs to the Lampist, Blink to the Rascal).
- Brigand (`brigand`): greatsword (heavy), javelins (light, regen), Rally on right click (attack and reload speed, plus about 1.5x faster ability and throwable recharge for allies; no movement speed).
- Shared: every melee weapon gets 1.5x damage from behind (master toggle, per-class rows).
- Class pattern: 1 primary, 2 secondary, right click helps allies, G acts on enemies, Shift is movement. G recharges in 20 s by default.

## Design rules Alex has stated
- All character model hands are simple balls. Never add articulated fingers, including on first-person props.
- Never tie a class's identity to the cup objective.
- Never add a flashbang.
- Friendly fire has a master toggle, default off.
- Each map is themed to a class: Basilica (Crusader), Scrollwork (Seeker), Mausoleum (Rascal). A Royal Garden map is planned (mockups first).
- Every number that affects play should be a tuning row, grouped per class.

## Not tested in real play yet
Shroud feel against humans, how often bots use it, backstab on each weapon, balance of the 5-point final kill and the drink sacrifice over a full match, Pious Charge impact feel, curved shield collisions against live fire, the Arbalest HUD display, the pulse rates on the cup HUD, the enemy cup heat ramp, the Shroud shimmer in bright rooms, the shape of the original narrow shield, bot behaviour with a shrouded Rascal escorting the cup.

## Open and parked (don't build unless Alex asks)
- Right-click alternatives for the Rascal: swap (rescue only, never forced on a teammate) and a decoy.
- Bag of rats on G for the Rascal.
- A debuff for enemies walking through the Bulwark.
- Arc previews for javelins and throwing daggers.
- Scaling the scoreboard and kill feed with the HUD.
- Twin Chalice mode.
- Platform ideas: split screen, Xbox gamepad for one player (with crouch), phone touch, friends and online play (host on GitHub Pages or itch.io).
- Housekeeping: a stale comment on `BLINK_RANGE` says "the lampist's blink" (it is the Rascal's). Some old comment lines may still be swallowing code, so check any `//` that sits mid-line.

## How Alex likes to work
Short direct answers. He asks questions about the design before wanting code. For anything big or visual, send a mockup first and wait for a choice. He tests in the browser and reports what feels off.
