# The Bellringer

Design brief, 23 November 2026. A sixth class for Chalice, not built yet. Mockup: `mockups/bellringer-mockup.html`.

## Who he is

A wandering medieval minstrel who fights with sound. He is the trapper: he prepares ground, waits, and springs it. Where the other classes are knights, cultists, a goblin, an elf and a blind lamp-bearer, he is the one bright, theatrical figure, which makes him easy to pick out across a room. The bright costume hides a grim detail: his ears are bound with cloth, because bellringers went deaf.

- Role: Trapper. 125 HP, the same as the Skulker. Fragile; his strength is preparation.
- Code key: to be chosen when built (the other classes keep old keys: `knight`, `sorcerer`, `goblin`, `lampist`, `brigand`).

## The look

From Alex's medieval-musician references:

- A two-colour tunic split down the middle: one half in the team colour (Thistle violet or Marigold red-orange), the other in cream, with a gold hem and collar.
- Hose that swap sides, so each leg contrasts with the tunic above it.
- Long pointed shoes, the strongest part of his outline at a distance.
- A bowl haircut under a round cap in the team colour with a cream brim.
- Ears bound with a cloth band running over the crown, with a faint stain at each ear.
- Eyes half closed, listening rather than looking.
- A leather belt with a sheath of three tuning forks at the hip and a small hand bell that swings as he walks.
- The bell-bow slung across his back when another weapon is out.

## The game's visual style, as it applies to him

Match the existing cast so he sits beside them without looking imported:

- Built from simple solids (cylinders, spheres, cones, lathed shapes) with a thin black outline, like every other class.
- Hands are plain balls, with no fingers, in every view.
- Team colour carries on cloth; metal and wood stay fixed: bronze bells, dark iron fittings, warm wood, brown leather.
- Readable silhouettes first, detail second. Every object he places in the world should be recognisable from across a room.
- Prose on his card follows the house voice: short, direct, no flourishes.

## His kit

Primary: the bell-bow (key 1)

- Alex's design. An angular bow: straight limb segments meeting at hard corners, square in section.
- A large bronze bell hangs mouth-down inside an eight-sided cradle at the centre of the grip, level with the string.
- The red-wood striker sits on the string. Hold to draw it back; release to snap it into the bell. There are no arrows; the bow fires sound.
- A quick strike is a short peal: about 35 damage up close, falling off fast.
- A full draw takes 1 s and sends a travelling note: about 75 damage, at a speed you can see and dodge.
- Every release shows the bell jolting and a ring of sound leaving it.

Field ability: tuning forks (Q)

- Three forks, thrown one at a time; each sticks upright where it lands and hums faintly.
- Only a note from his own bow sets them off. Striking any one rings all three, wherever they are.
- Enemies within 4 m of a ringing fork are silenced (no abilities) for 3 s and slowed 20%. His team is never affected.
- Any enemy damage breaks a fork, and he hears it go. They are thin and dark: a careful player finds them, a sprinting one does not.
- Forks last 30 s; each recharges in 12 s.

Class ability: Alarm Bell (right click)

- The Lampist's Marking Lantern, reskinned as a small bell that tinkles, with the same throw, animation and stats.
- It hovers for 5 s and reveals enemies within 10 m through cover, Shrouded Skulkers included. 12 s recharge.

Movement: Bell Rope (Shift)

- Aimed like the Marking Lantern: hold to see a spike of light where the far end will land. The far end can be higher, lower or level.
- Release, and a bronze bell on a cast-iron yoke slams down at his feet, a matching one plants at the spike, and the rope snaps taut between their tops. He is pulled along it.
- The yokes are knee-high, after Alex's photo of a yoke-mounted bell, with a small wooden lever in place of the photo's steam valve. On a ceiling the far yoke hangs like a church bell.
- The rope stays for about 15 s. Teammates ride it by walking in and holding jump. The bells ring when anyone uses it.
- Enemies can break it by shooting either bell or the rope. When it ends, both yokes sink into the ground with a dull clang. 15 s recharge.

## Sound

He is the class players should hear before they see. Each part has its own voice:

- The bow: a struck bell, short for a peal, long and ringing for a full note.
- The forks: a thin, steady hum, and a bright chord when struck.
- The Alarm Bell: a light tinkle.
- The rope: heavy clangs as the yokes land, and a ring each time someone uses it.
- His walk: the soft swing of the hand bell at his belt.

## Related decisions

- The Lampist loses her Marking Lantern and gets the Blinding Flare: a thrown lantern (the same model), a warm flash, then a gold afterimage that fades. It is stronger the more directly you looked at it, and it always breaks Shroud. The Alarm Bell takes over revealing enemies.

## Still open

- The code key and the name on his card.
- How bots should use the forks and the rope.
- His first-person view of the bow at rest and drawn.
