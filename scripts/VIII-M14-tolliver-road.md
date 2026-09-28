# SCRIPT · Chapter VIII, Mission 14: Tolliver Road

*Production script (V8). Source of truth for story: `chapters/chapter-08-feedback.md`, Mission 14, read with M13 (the box) before it and M15 (the payphone) after it. This script turns the mission into the form the team builds from: numbered scenes, line IDs, delivery notes, input nodes with the flags they read and set, camera, audio, light and UI cues, and timing. Where this script and the chapter disagree, the chapter wins on story and this script wins on execution. Binding specs from the chapter are restated here in full. Canon used: bible §3.2 (the road), §5 (the crash), §11.1 (the switch), §11.3 (Clara's rules), §11.8 (Clara's help); `18-performance-and-direction.md`.*

**Conventions**
- **Line IDs:** `VIII14_<SPEAKER>_<nnn>`. Speakers:
  - ELL: Ellis, 19.
  - CLA: Clara, 21.
  - GRA: Grace at fourteen, as Ellis sees her tonight in the passenger seat. This is not the 1973 memory (IX M6, X M8).
  - NB: a notebook line. On-screen text, not recorded.
- The one line the chapter heads **GRACE/CLARA** is filed under GRA, because the chapter has it "in Grace's voice" and Grace's actor records it.
- **Cues:**
  - `SW:` switch;
  - `CAM:` camera;
  - `AUD:` audio;
  - `MUS:` band or music;
  - `UI:` HUD or prompt;
  - `SYS:` a system state.
- `CAM (Ellis):` is Ellis's perception. M14 has no other camera.
- **Flags** go in the tracked-state registry (`17-tracked-state-registry.md`). Every flag below is new with this script and needs an entry there.
- **Clara** (CLA) and **Grace** (GRA) are recorded and mixed like any person in the car. No processing.

**Flags read here:** none. M14 plays the same way for every player. Its entry state is fixed by M13 (below).

**Flags set here:**
- `tolliver_passes` (int, default 0): times the player drove past the turnoff before taking it.
- `tolliver_grace_reply` (`speed_limit` | `walk` | `silence`).
- `tolliver_looks` (int, default 0): looks at the passenger the player made, from the turn to the Bend.
- `tolliver_ages_seen` (a set of up to 5: `14`, `15`, `16_17`, `19`, `21`): the ages the player caught with their own look.
- `bend_stop` (`road` | `clay`).
- `oak_touch` (`player` | `rising`): how Ellis's hand reached the scar. Always set by the end of M14. Read by M15 (the bench: "Did you touch it?" / "Yeah.").
- `obs_tolliver_oak` (bool): the Observe line was written.
- `tolliver_road_driven` (bool, world state): set true on the turn.

**Entry state (from M13, 6:40 p.m.)**
- Ellis has taken the Valiant keys off the hook and gone down the porch steps into the dark. Wayne's last line, from the kitchen door: "It's gonna rain." It isn't.
- Wayne stays at the kitchen table in his hat with the two photographs on the oilcloth. M15 finds him there at 11:40 p.m.
- Clara vanished from the doorway when the photographs came out (Rule 13: Lorraine's face).
- Dry. No rain for a week.
- The help layer is active for Ellis. He isn't on medication yet (M17).

**Route (bible §3.2; binding for level design)**

Tolliver Road is a through road. Southbound from the South Fork road:

| Marker | Mile | What's there |
|---|---|---|
| The turnoff | 0.0 | On the left going south. Pickens Grocery on the corner. A green county sign: TOLLIVER RD. No sawhorse (gone since the fall of 1974). A SPEED LIMIT 45 sign past the mouth (the posted limit, bible §5). |
| The first bend | 0.5 | A gentle curve between fences. Nothing to see. |
| The church | 1.1 | On Ellis's side. Passed, never stopped at. |
| The Tolliver farm | 2.0 | On the right. (In IX M6 the Impala turns right out of the farm lane to go on toward the Bend.) |
| The HENSLEY mailbox | 3.7 | On the right, on a cedar post. A frame house set back. |
| The long straight | 3.7–4.0 | IX M6's "long straight before the Bend." Hensley's is 0.3 miles short of the oak. |
| Tolliver Bend | 4.0 | A blind right-hand curve, down toward the creek. A bank of red clay on the right and no shoulder: asphalt, then clay, then the ditch. The white oak on the outside of the curve. |
| Beyond | | The road climbs back to the Tanner Valley road east of Roy's: the back way home. Closed to the player tonight. |

Distances are real-scale. Level design may compress them (bible §3.1) as long as the order survives, the farm stays near the middle, and the Hensley-to-oak straight stays.

---

## MISSION 14 · TOLLIVER ROAD (6:50–8:40 p.m.)

**Whole-mission systems**
- `CAM:` In the car, the camera is at Ellis's eyes in the driver's seat for the whole mission. M14 has no exterior driving camera, no photo mode and no free camera: from outside the car the passenger could only be seen through glass (Rule 12), and a free camera is an objective one. The mission has no cuts, from the first frame to the stop at Pickens.
- `SW:` None. See 14.3.
- `MUS:` None. No score and no band anywhere in the mission.
- `UI:` SATURDAY. No date (nobody says it). No objective and no marker. The only prompts are the ones in the nodes below.
- `SYS:` The help layer is active. It gives one line in this mission (14.1) and nothing after the turn.
- `SYS:` The open-world turnoff rule (from Chapter II, Ellis brakes at the Tolliver Road turnoff and turns around with a line) is suspended for this mission.
- `SYS:` Traffic: ordinary Saturday night in town. On the South Fork road and Tolliver Road, none. No headlights come toward Ellis anywhere in M14.
- `SYS:` The radio is off and isn't offered (see Audio). High beams aren't offered: the Valiant runs on low beams all night. (The high beams on Tolliver Bend were the pickup's, bible §5.)
- `SYS:` Observe: one cue in the whole mission (14.5).
- `SYS:` Bounds: Hollow Ridge and the South Fork road as far as the church lot at the low-water bridge. At an edge (the church lot, the town line on US 19 or the Tanner Valley road, the Blake yard) Ellis turns the car around on his own, with no line, and the mission waits.
- **Timing.** Play time about 20 minutes: 14.1 three to four minutes, plus about three per drive-past; 14.2 and 14.3 about five; 14.4 one to three; 14.5 about two for the exchange, then the sit for as long as the player likes; 14.6 about four.
- **Story clock** (the HUD shows only the day, so this drives light and M15): the turnoff about 7:00, the farm about 7:04, the Bend about 7:08, rising at 8:30, Pickens at 8:40.

### 14.1 · THE TURN · COLD BRANCH ROAD TO THE TURNOFF · 6:50–7:00 P.M.
`CAM (Ellis):` The Valiant pulls out below the Blake house, the kitchen light on behind. Clara is in the passenger seat with her boots on the dash from the first frame. She has no entrance.
`SYS:` The player drives. No destination marker. The chapter's route, which the player can wander off and come back to:
1. down Cold Branch Road;
2. past Marlon's (Saturday night, the chalkboard lit, other acts on it);
3. across the tracks at Depot Street;
4. south onto the South Fork road, the way he's driven it a hundred times, with one road always on the left that he never takes.

`AUD:` Engine, dry tires, the town. Clara says nothing on the drive.

`CAM (Ellis):` The mouth of Tolliver Road on the left. Pickens Grocery dark on the corner, one bulb lit over its pay phone. No sawhorse.
`SYS:` Trigger: 150 m before the turnoff, or 5 s before it at the car's speed, whichever comes first. First southbound approach only.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_CLA_001 | CLARA | Not that way. | A direction, the way you'd give one ("Left at the church."). Boots on the dash, eyes on the road ahead. Match her I M1 read of the same line. There's nothing extra in it tonight. |

`SYS:` This is help (bible §11.8: directions), and it's biased, away from the Bend. It's the first of her help that fails.

**Node N14.1a · the turnoff** (repeatable; sets `tolliver_passes`)

| Input | Result |
|---|---|
| Take the turn | Go on below. |
| Drive past | `tolliver_passes` +1. The South Fork road goes on to the farmhouse and the low-water bridge (dry tonight), and nothing happens. At the church lot by the bridge Ellis turns the car around on his own and drives back north. The turnoff comes up again, on the right. Clara says nothing on any later approach. No timer: the mission waits. |

`SYS:` A turn taken from the south is a right turn. Everything below runs the same.

`CAM (Ellis):` He turns anyway. His head leads into the turn, as a driver's does. The headlights swing across the green county sign, TOLLIVER RD, and the road narrows to a strip of old asphalt with no center line, between fences and dark pasture, going south and down toward the South Fork.
`SYS:` During the turn, with the passenger out of frame, she changes from Clara (21) to Grace (14) under the rules in 14.3. If the player holds the view on her through the turn, the change waits for their first look away.
`SYS:` `tolliver_road_driven = true`.

### 14.2 · WHO'S IN THE CAR · THE TURN TO THE FIRST BEND · 7:00 P.M.
`SYS:` Look 1, age 14. The look rules and the fallback glance are in 14.3.
`CAM (Ellis):` There's someone else in the passenger seat.
- A girl of fourteen, in a jean jacket that fits her, a child's size, with a horse sewn on the pocket, crooked.
- Muddy riding boots. A ponytail.
- She's turned to her window, looking out at the pastures: a fourteen-year-old who's been riding all afternoon and is annoyed about something.
- Grace. The same likeness and clothes as the M13 school picture and the IX M6 Impala. She's dry tonight; in IX M6 she's wet.

`SYS:` 3 s after the change, whether or not the player has looked, Ellis rolls his window down an inch without thinking about it. She smells like a horse. His left hand goes to the crank, one inch, and back to the wheel. The camera stays on the road. The window stays down an inch until Pickens.
`SYS:` GRA_010 plays 6 s after the change, or once the player's first look has held for 1 s, whichever comes first.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_GRA_010 | GRACE | You drive like an old man. | To her window, not to him. A kid sister's dig, bored and a little pleased with it. A real fourteen-year-old: sillier and meaner than Clara, and she doesn't soften it. |

**Node N14.2a · the answer** (sets `tolliver_grace_reply`)

`UI:` Two phrasings, small, for 6 s. Holding the silence input, or no input, is silence. The answers are Ellis at sixteen.

| Option (the player sees) | Ellis says | ID | Delivery |
|---|---|---|---|
| "Speed limit's forty-five." | Speed limit's forty-five. | VIII14_ELL_010 | Instant and literal, a brother defending his driving. (Tolliver Road is posted 45, bible §5. He doesn't play that.) Sets `speed_limit`. |
| "You want to walk?" | You want to walk? | VIII14_ELL_011 | The old threat nobody ever carries out. Deadpan. Sets `walk`. |
| Silence | (nothing) | (no line) | He drives. Sets `silence`. |

The next two lines play whichever option was taken. Neither answers him.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_GRA_011 | GRACE | Dolly threw a shoe. Mr. Tolliver said he'd get it Monday. | News from her afternoon, told as a grievance. Still mostly to the window. |
| VIII14_GRA_012 | GRACE | You're gonna be late. | Singsong, pleased about it, and not sorry. |

- `SYS:` 4–6 s between the lines, the way she'd have said them on a Thursday three years ago, in this car's older brother. If the player drives fast the gaps shrink.
- `SYS:` All three Grace lines finish before the church. They may run past the first bend: she's fifteen by then, and the voice doesn't change.
- Nothing more is said until the farm. The Tolliver farm is two miles ahead.

### 14.3 · OLDER · THE FIRST BEND TO THE HENSLEY MAILBOX · 7:01–7:07 P.M.
Every time the player looks at the passenger seat, she's older. The player can't catch the change happening. It has always already happened when they look.

**Node N14.3a · the looks** (free and repeatable from the turn to the Bend; sets `tolliver_looks`, `tolliver_ages_seen`)

| Look | Age | Where | What the player sees |
|---|---|---|---|
| 1 | 14 | after the turn | Grace, as in 14.2. |
| 2 | 15 | at the first bend | Her hair longer. Nothing else the player can name. (18 §6: the player should doubt the first change.) |
| 3 | 16 or 17 | past the church | The jacket is bigger now, a grown-up jacket, the same one: the same horse, the same crooked stitching, the same pocket. The face is halfway. One build that reads as either age; don't settle it. |
| 4 | 19 | at the Tolliver farm | Behind her, through her window: lights on in the farmhouse, Floyd's green truck in the yard, the empty paddock where Dolly stood for twenty years. Her face most of the way to Clara: the girl on the church steps in M13's wedding portrait, with Grace's eyes. |
| 5 | 21 | between the farm and the Bend | Clara. Dark hair to her shoulders, Lorraine's cheekbones, Grace's eyes, the gap, Grace's jacket in an adult size, Ellis's red flannel under it. Boots up on the dash. |

- Carried through all five: the gap in her front teeth, Grace's gray-green eyes, the crooked horse patch.
- Under the jacket she wears a shirt of Grace's until 21, when it's his red flannel.
- `SYS:` Each look the player makes adds 1 to `tolliver_looks` and adds that age to `tolliver_ages_seen`. Fallback glances (below) add nothing.

`SYS:` Between look 4 and look 5, with the passenger out of frame and Ellis looking at the road, she says one more thing, in Grace's voice.
- The window opens at the farm gate, once she has been out of frame for 1 s. If the player is looking at her, the line waits.
- It must finish before the HENSLEY mailbox. She can't reach 21 until it has.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_GRA_020 | GRACE/CLARA | Daddy'll kill us both. | Looking straight ahead through the windshield. Out before she means it, the way Grace would have said it: flat, a fact the whole family knows. She doesn't take it back: no breath after it, no laugh, no look at him. Nobody leans on "Daddy." |

- `UI:` Subtitles show this line with no speaker name. GRACE/CLARA is the chapter's heading, and it isn't a label to print. Every other line is labeled as usual: ELLIS, GRACE, CLARA.
- `SYS:` Ellis says nothing on this stretch. He doesn't answer "Daddy."

`CAM (Ellis):` Past the farm, on the right, a mailbox on a cedar post: HENSLEY. A frame house set back in the dark with one porch light on. (IX M5 pays the porch light: "Opal Hensley's porch light was the only one on.")

**THE PASSENGER. Binding camera spec.**
- **Ellis's perception only.** She exists in the driver's-eye camera and nowhere else. No objective shot, exterior camera, photo mode or free camera.
- **Never a mirror or a reflection.**
  - The rearview mirror shows the road behind and nothing of the cabin.
  - Reflection probes and screen-space reflections exclude her at every age.
  - The cabin glass carries no interior reflection in this mission. At dusk, with the dash lamps low, that reads as true.
  - She is never seen through glass. An empty seat in the glass would be the objective camera, which this mission doesn't have.
- **Never closer between cuts.** There are no cuts on Tolliver Road; the looks are head turns.
  - The eye point is fixed at Ellis's head: no lean, no zoom, no change of FOV, no aim-in.
  - Her head is never nearer Ellis's eyes than it was at look 1, in any pose, at any age.
  - She never leans toward him, and on a look-back she's never facing him.
- **Head turns are human.** Look speed is capped at a driver's; no whip-pan.
  - While the car moves, a look held for 2.5 s ends on its own: Ellis's head goes back to the road over 0.5 s, because he's driving. Stopped, there's no cap.
  - While a look is held, the steering holds the lane. On Tolliver Road the car can't leave the pavement or touch a fence.
- **Framing.** The horizontal FOV in the car is 70° at most. The passenger, boots on the dash included, sits 45° or more off Ellis's straight-ahead eye line. Looking at the road, she's fully out of frame, edges included.
- **What counts as a look.** Her head inside the middle half of the frame for 0.25 s. Glimpses at the edge don't count.
- **The look-away and look-back rhythm.** Road, glance, road: a driver's rhythm. A change happens only when all three of these hold:
  1. she has been fully out of frame (her current pose and her next pose, plus a 10° margin) for at least 1.5 s;
  2. the car has crossed into the next age zone since the player last saw her;
  3. for 21, VIII14_GRA_020 has finished.
- **The look-back.** A flick away and back never changes her. On the look-back she's already settled in an ordinary pose (looking out her window, looking ahead, hands in her jacket pockets). She's never mid-motion and never looking at the camera. No transition animation exists, and none is ever built.
- **Age zones:**
  - Z0, before the turn: Clara, 21.
  - Z1, the turn to the first bend: 14.
  - Z2, the first bend to the church: 15.
  - Z3, the church to the farm: 16 or 17.
  - Z4, the farm to the end of GRA_020: 19.
  - Z5, from there to the Bend: 21.
- **Repeat looks in one zone.** The chapter says every look finds her older, so a second look in the same zone finds her a half-step further toward the next age (hair, jacket fit, face blend). She never reaches the next age inside a zone. In Z5 she's Clara and stays Clara.
- **Fallback glance.** The five ages are the mission's reveal (the chapter's clue ledger marks it *revealed*), so they mustn't be missable.
  - If the player hasn't looked in a zone by the point where that zone's glance is due, Ellis glances on his own. Due points: Z1, 2 s after GRA_010; Z2 and Z3, the zone's midpoint; Z4, before GRA_020's window opens; Z5, before the HENSLEY mailbox.
  - The fallback uses the same head-turn speed and angle as the player's look, holds 1.2 s, and goes back to the road.
  - It follows every camera rule above. It doesn't count toward `tolliver_looks` or `tolliver_ages_seen`.
- **On the way back** there are no changes. She doesn't get any younger.
- **No switch grammar.** No look and no change uses any part of `SW_CUE`: no narrowing, no frame-stutter, no depth-of-field pull, no `RMB_SWITCH` or `RMB_FAIL`, no HUD fade. The failed catch on Clara belongs to M4 and M10, and a third one here would be a false one. Nothing marks the change: no sound, no light, no music. (Rule 12; bible §12, rule 6.)
- **Accessibility.** One press of *look at passenger* performs the same glance: same speed, same angle, same 2.5 s cap.

### 14.4 · THE BEND · 7:08 P.M.
`SYS:` From the HENSLEY mailbox, the long straight. Speed eases to 30 mph at most, and to 20 at the curve, whatever the throttle. It plays as Ellis lifting his foot. The car can't leave the road on the outside of the curve, and the player can't hit the oak.
`CAM (Ellis):` Two miles past the farm the road starts to curve right, down toward the creek, blind, with a bank of red clay on the right and no shoulder at all. The asphalt just stops, the clay starts, and then the ditch.
`SYS:` It's in the steering before it's in the headlights. The road drops and the wheel needs more angle about 1 s before the curve shows in the low beams. This is the steering model only; there's no haptic pulse.
`CAM (Ellis):` Tolliver Bend. The headlights come around, and there it is, on the outside of the curve: a white oak, big, old, with a long scar on the trunk at the height of a car door, where the bark has grown back over it crooked, thick and folded, like a badly healed arm.

**Node N14.4a · where he stops** (sets `bend_stop`)

| Input | Result |
|---|---|
| Brake in the road (no one's coming) | `bend_stop = road` |
| Brake half onto the clay | `bend_stop = clay` |
| No brake by the end of the stop zone | Ellis stops on his own, in the road. `bend_stop = road` |

- The stop zone runs from the curve's entry to the point where the beams would leave the oak. Wherever he stops in it, the headlights stay on the oak.
- `SYS:` Ellis switches off the engine. The headlights stay on. `AUD:` The engine ticks.
- 3 s later he gets out. The player can walk.
- **The passenger side.** Tonight the Valiant's passenger side is the side away from the oak. The chapter's "the side that was nearest the tree" belongs to 1973: the Impala rotated and its passenger side hit the oak (bible §5). Don't park the Valiant's passenger door against the tree.

`CAM (Ellis):` Clara gets out of the passenger side.
- **Rule 1 staging.** The passenger door never opens. The camera is on Ellis's own door and his boots on the clay.
- When the camera comes up from his exit, she's already out on the passenger side, and the door is shut.
- Precedent: VIII M10, where she fixes his collar and the collar doesn't move. A door she opened would have to move.

`SYS:` On foot the player can walk as far as the headlights reach, about 30 m. At the edge, Ellis turns back on his own.

**Node N14.4b · Touch** (optional; sets `oak_touch = player`)
- `UI:` At the trunk, facing the scar: *Touch.*
- `CAM (Ellis):` His right hand on the bark at hip height. The bark is rough, and then, on the scar, smooth and ridged, like a knuckle.
- `AUD:` A dry hand on bark, then the smoother, ridged sound of the healed wood.
- Haptics, where the platform has them: a fine rough texture, then slow ridges. Never a pulse.
- The prompt stays while Ellis is at the trunk. No timer. If the player never takes it, N14.5b covers it on the way up.

### 14.5 · "I MADE YOU" · THE OAK · 7:10–8:30 P.M.
`CAM (Ellis):` Clara is standing a few feet away, in the headlights, with her hands in her jacket pockets.

**Blocking**
- She stands off the Valiant's axis at the edge of the beams, lit from the side, the same way Ellis is.
- The lamps are never behind her head.
- She casts a shadow like anyone in his view. It never touches his and never falls across the scar. (Nobody's shadow touches hers, as in VI's cold open.)
- When Ellis faces her, the car's lamps are off to his right. No light comes at him low from the left.

`SYS:` The exchange starts when Ellis faces her from within 3 m of the trunk, with or without the Touch. It waits as long as the player likes.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_ELL_030 | ELLIS | I made you. | Worked out, and said like a fact about an engine. Curious, not wounded (18 §2). |

`CAM (Ellis):` She looks at him.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_CLA_030 | CLARA | Does that make me less real? | Curious, not wounded (18 §2). A real question; she'd like to know. |
| VIII14_ELL_031 | ELLIS | I don't know. | Honest. Nothing added. |
| VIII14_CLA_031 | CLARA | Well. Holler when you know. | Dry. A big sister closing a subject she's bored of. |

`CAM (Ellis):` He doesn't have an answer.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_ELL_032 | ELLIS | You've got her eyes. You've got Mama's teeth. | Looking at her face and naming parts. Plain. "Mama" here; he says "my mother" to Riley in M15. |
| VIII14_CLA_032 | CLARA | I've got your shirt. | A tease, quick and light. On the line she plucks at the red flannel under the jacket, his shirt. |
| VIII14_ELL_033 | ELLIS | Why'd you come? | A plain question. He wants the answer. |
| VIII14_CLA_033 | CLARA | You asked me to. | Simple, the way you'd remind somebody they asked you to pick up milk. Nothing leaned on. |
| VIII14_ELL_034 | ELLIS | When? | Quick. He really doesn't know. |

`CAM (Ellis):` Clara looks at the oak. At the scar at the height of a car door.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_CLA_034 | CLARA | Right here. | To the scar, off his eyeline. Placing it, the way you'd say where you parked. Don't underline it; the player does that. (18 §7 names this line as one of the three things M14 must get right.) |

`SYS:` After a 2 s beat, Ellis sits down on the clay with his back against the oak, under the scar. No timer from here on.
`CAM (Ellis):` Clara sits down beside him, not touching him. She never touches anything, and her back doesn't touch the trunk either.
- She sits only in view, in one continuous move. If she's out of frame when he sits, she stays standing until the player's view finds her, then comes over and sits. (Rule 12: never closer between cuts.)

8 s after she sits:

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_CLA_040 | CLARA | Button your jacket. | An order. Practical, bossy, fond, and the subject changed. It isn't help: the chapter's help ledger lists nothing after "Not that way." |

`CAM (Ellis):` He buttons it. No cars come. The creek at the bottom of the hill. Frogs, early, it being March. The Valiant's headlights on the two of them and the tree.
`SYS:` From here the story clock runs fast and unseen. On rising it reads 8:30. The light is already full dark by now (see Light), so nothing visible changes with the clock.

**Node N14.5a · Observe** (optional, once; sets `obs_tolliver_oak`)
- `UI:` The Observe cue, 10 s after "Button your jacket." It stays until he gets up.
- `CAM (Ellis):` He turns his head to the scar beside and above him in the headlights, and writes in his memo book.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| VIII14_NB_040 | NOTEBOOK | *The bark grew back over it like a hand over a mouth.* | On screen, in his pencil hand. Not voiced. It joins the notebook pool that Chapter IX's leaked pages are built from (bible §11.5). |

**Node N14.5b · getting up** (timing only, no timer; may set `oak_touch = rising`)
- When the player gets up (any movement input), Ellis gets up. There's no prompt.
- If `oak_touch` isn't set yet, his hand goes back to the trunk to push himself up and lands on the scar: rough, then smooth and ridged, like a knuckle. The same foley and haptic as N14.4b, shorter. Sets `oak_touch = rising`.
- Why: in M15 he tells Riley he touched it and what it felt like, so by the end of M14 he always has.
- Idle on the walk back: he rubs his left forearm once, without looking at it (bible §6.1: it aches before rain; the rain is an hour off).

`CAM (Ellis):` Clara walks back to the car with him, in view, like a person. She's at the passenger door as he opens his. When the camera comes back from his own door and seat, she's in the passenger seat with her boots on the dash.
- Rule 1 again: the passenger door never opens.
- She's never seen through the glass.

### 14.6 · BACK UP TOLLIVER ROAD · PICKENS GROCERY · 8:30–8:40 P.M.
`SYS:` The first throttle input turns the Valiant around in the curve on its own (a three-point turn), heading north. He doesn't drive home. The road south of the Bend is closed tonight, and if the player turns south again, Ellis turns back around on his own.
`CAM (Ellis):` He drives back up Tolliver Road the way he came, and Clara rides with him, and she doesn't get any younger.
- The looks still work, and every look finds her at 21.
- The HENSLEY porch light, the farm, the church, the first bend.
- `SYS:` No lines, no help, no Observe.

`CAM (Ellis):` At the bottom of Tolliver Road, where it meets the South Fork road, there's a closed store with a pay phone on the wall outside under a light. Pickens Grocery, as M15 describes it:
- cinderblock, with a tin awning;
- two gas pumps;
- a hand-lettered sign: PICKENS GRO · GAS · BAIT · CLOSED SUN;
- the pay phone under one bulb, and a moth at the bulb;
- a bench under the awning.

`SYS:` The last 50 m steer in on their own. He stops by the pumps. The player can't turn onto the South Fork road.
`CAM (Ellis):` Hold through the windshield on the pay phone under the bulb. Clara is in the passenger seat, 21, boots on the dash, out of frame unless the player looks. Engine off; it ticks.
`SYS:` The mission ends on a 4 s hold. No card.

---

## Exit state into M15 (binding for the M15 script)
- **Where and when.** Pickens Grocery, the foot of Tolliver Road, 8:40 p.m. The Valiant is stopped by the pumps with the engine off. Ellis is at the wheel.
- **Clara.** In the passenger seat, 21. From Riley's side in M15, he's alone (Rule 3).
- **Weather.** Dry, with cloud building. The rain starts during Riley's drive in M15, "about halfway." By the time she reaches Pickens, the Valiant is ticking in the rain.
- **Wayne.** At the kitchen table in his hat with the two photographs, where M15 finds him at 11:40.
- **Flags.** `oak_touch` is always set. `tolliver_road_driven = true`. The rest are as played.
- **8:40 to 8:52.** Ellis places the call. M14 doesn't show it. M14 fires no switch; M15 opens on the ring in Riley's kitchen on Cutler Street. If M15 bridges the two with a switch, the call is its carrier (bible §11.1: a phone line).
- **M15 lines that stand on this mission.** Their IDs belong to the M15 script. They're quoted here so nothing in M14 contradicts them.
  - ELLIS: "The store at the bottom of Tolliver Road." / "It's closed." (Pickens is closed.)
  - ELLIS: "I drove it. The road. All the way to the bend." (He drove to the Bend and back the same way.)
  - ELLIS: "I was driving." / RILEY: "I know." He says it as his own. It isn't staged as a revelation.
  - RILEY: "Stay there." Practical, not tender (18 §2).
  - On the bench, if Riley asks: "Did you touch it?" / "Yeah." / "What was it like?" / "Like a knuckle." `oak_touch` makes "Yeah." true on every playthrough.
  - What he can tell her about the road (the girl who got older every time he looked, the HENSLEY mailbox, the curve with no shoulder, the oak) is on the route for every player.
- **After.** The Valiant stays at Pickens. Roy tows it back Sunday afternoon (M15).

---

## Binding audio spec
- **No score** anywhere in M14. Diegetic sound only (18 §5).
- **No rain.** The chapter keeps this mission dry.
  - M13 ends on Wayne's "It's gonna rain." and "It isn't."
  - The first rain in a week starts during Riley's drive in M15.
  - So: no rain, no thunder, no wet tires, no wipers.
  - "Rain on Tolliver Road (Mar 20)" in `11-open-world-evolution.md` is M15's rain at Pickens.
- **Engine and road.**
  - The Valiant's slant-six: a slow, honest car. Dry tires.
  - On Tolliver Road the tire note turns coarser (old asphalt, no center line), with grit at the edges.
  - From 14.2, the inch of open window on Ellis's side: a thin, steady hiss of air on the left.
  - At the Bend, engine off: the block and exhaust ticking as they cool, dying away over about three minutes.
- **Radio.** None.
  - The Valiant's AM radio is off from the first frame and isn't offered. The radio plays what the chapter says it plays (18 §5), and the chapter gives it nothing.
  - Nothing by the Blakes is audible anywhere in M14, through Marlon's door included.
- **Voices.** Clara and Grace are mixed as a person in the passenger seat: the car's own acoustic, right front, the same chain as Ellis.
  - No reverb, filter, pitch or formant shift, breathiness, doubling or whisper.
  - The ages get no voice treatment, and there's no voice morph. The passenger speaks in Grace's voice (GRA_010–012, GRA_020) or Clara's (CLA_001 before the turn; the oak), never a blend.
  - At the oak both voices are open air, from where each of them is: a few feet off, then beside him on the ground.
  - Clara doesn't hum. Nothing is playing.
- **The change.** Silent. No sting, no whoosh, no tone, and none of the switch sounds (`RMB_SWITCH`, `RMB_FAIL`, the ambience narrowing).
- **The Bend.**
  - The creek at the bottom of the hill.
  - Frogs: spring peepers, early, it being March. No summer insects.
  - No cars, ever, and hardly any wind.
- **Pickens.** The bulb's hum, and a moth ticking against it. M15 hears it down the phone line: "a moth hitting a light."
- **Haptics.** No pulses in M14. The soft double pulse and the single hard pulse belong to the switch. The Touch texture is the only haptic.

## Binding light spec
- **Clock and sky.**
  - Sunset is about 6:50 p.m. (Eastern Standard; in 1976 daylight saving began April 25).
  - The mission runs from last light into full dark: dusk at the turn, dark at the Bend.
  - Cloud builds from the west all evening (M15's rain). No moonlight, and no stars by the Bend.
- **Town.** Streetlights coming on. Marlon's chalkboard lit.
- **The turn.** The last usable daylight. The headlights swing across the green county sign, and its letters light in the beams. No flare.
- **Tolliver Road (Z1–Z3).**
  - The pastures are dark shapes under a gray-blue sky. The fences are in the headlights.
  - The cabin is dark except for the dash lamps, which are dim.
  - **The passenger's face must read at every look.** Dash spill and the last of the sky, soft and even, the same at every age.
  - No rim light, no glow, and no light that belongs only to her.
- **The farm (Z4).** Warm farmhouse windows. Floyd's green truck in their spill. The paddock fence in the headlights, and nothing behind it.
- **The Hensley house.** One porch light on (IX M5 pays it). The house set back and dark.
- **The Bend.** Low beams only. The curve is black until the beams come round, and then the oak:
  - pale bark;
  - the scar at car-door height in raking light, the beams striking it at 30–45° so the thick, folded healing throws its own shadows;
  - to the eye it reads like a badly healed arm.
- **"Like a knuckle."** At the Touch the framing is close enough that the ridges under his fingers read like a knuckle. His hand's shadow is the only shadow on the scar.
- **The clay.** It shows red only where the beams hit it.
- **The sit.**
  - The two of them and the tree in the Valiant's beams, lit from the front and low.
  - The lamps sit off-center in his view (the car to his front right), with no bloom and no flare streaks.
  - Period glass. Beyond the beams, black.
- **High beams.** Never (bible §5: they were the pickup's).
- **No light from the left.** Nothing comes at Ellis low from the left in this mission. The reflex planted in VII M15 and paid in X M8 isn't touched here.
- **Pickens.** One bulb over the pay phone. The tin awning, and the pumps in the bulb's spill. The store dark.

---

## Clara's rules in this mission (bible §11.3)

| Rule | How M14 keeps it |
|---|---|
| 1. No effect on the objective world | The passenger door never opens for her (14.4, 14.5). Her boots leave nothing on the dash. She sits without touching him or the trunk. |
| 2. Only Ellis speaks with her | Nobody else is in the mission. |
| 3. Never in an objective shot | M14 has no objective, exterior or free camera. |
| 4. Tater never reacts | Tater is at the house. |
| 5. Grace's room | Doesn't arise. |
| 6. Nothing Ellis couldn't know | "Right here." and "You asked me to." are his own "I'm right here. Stay with me," said at this tree (bible §5). "Daddy'll kill us both" is his own sentence from the car (IX M6). |
| 7. Never the cemetery | The church on Tolliver Road is passed on Ellis's side and never stopped at. |
| 8. Not long in a room with Wayne | Wayne isn't in the mission. |
| 9. The switch fails on her | No switch fires in M14. |
| 10. Never "go" | Her seven lines and the GRACE/CLARA line contain no "go" in any form. The mission's one "gonna" is Grace's, at fourteen, before the first change (VIII14_GRA_012). |
| 11. Vehicles and third parties before the midpoint | Doesn't arise (after V M16). |
| 12. No horror grammar | No mirror, window or reflection. Never closer between looks. No cuts on the road. No sting. |
| 13. Vanishing | She never vanishes in M14. The ages are found on look-backs: Rule 13's "gone when the camera comes back from looking somewhere else," applied to who is in the seat. |

## Staging calls (execution; the chapter leaves these open)
- **Rain.** None in M14 (see Audio). The rain rig isn't used for this mission.
- **Free looks against five fixed ages.** The ages are zoned to the chapter's landmarks. Repeat looks in a zone find her a half-step older. A fallback glance makes sure every player sees all five.
- **"Sixteen or seventeen."** One build that reads as either.
- **The optional Touch.** M15 assumes he touched the scar, so his hand finds it when he gets up.
- **Clara getting out.** The passenger door can't open for her (Rule 1), so her exit is never seen.
- **"Not that way."** Played once, on the first approach, and never again on a return approach.
- **Grace's "gonna"** stays verbatim. It's Grace's line at fourteen, not Clara's.

---

## Performance and recording notes
- **One performer or two: two.**
  - The chapter separates them: the girl in the seat is Grace ("Grace."), the "Daddy" line comes "in Grace's voice," and it's Clara who gets out at the Bend.
  - 18 §2 casts them apart: Grace is an actual thirteen-to-fourteen-year-old; Clara is the adult actor with Lorraine's face.
  - Grace's actor voices GRA_010–012 and GRA_020. Clara's actor voices CLA_001 and the oak. Nobody voices the ages in between.
- **Clara's actor.**
  - Record CLA_001 in the car shell with Ellis's actor, her boots up. Match her I M1 "Not that way."
  - Record the oak as a two-hander with Ellis's actor, in the blocking: a few feet apart and standing for CLA_030–034, then side by side on the floor for CLA_040, so the distance is in the sound.
  - Record "Right here." with her head turned to the scar.
  - She's a person, never a mystery (18 §1). Nothing wistful or knowing, and nothing meant twice. Take several of CLA_030 and CLA_034 and use the least performed.
  - Capture: look 5 (21) and the oak.
  - Look 4 (19) is her likeness styled two years younger, toward the 1953 wedding portrait (18 §2 uses her likeness for it). Keep Grace's eyes and the gap.
- **Grace's actor.** The same actor as IX M6 and X M8.
  - Record GRA_010–012 in the car shell, dry, with her head turned to her window.
  - Record GRA_020 facing forward, inside a run of her ordinary lines. Don't flag it to her as a reveal.
  - Record GRA_011 in the same session as IX M6's "Dolly threw a shoe. Mr. Tolliver had to hold her." Read the shared first sentence the same way both times; IX pays it.
  - Keep the contractions as written. M14's "Daddy'll" is hers; IX M6's "Daddy'd" is Ellis's. Don't make them match.
  - She must sound like a real fourteen-year-old, and specifically not like Clara (bible §6.2).
  - Capture: looks 1 and 2. Fifteen is the same face with longer hair.
  - Look 3 (16 or 17) is a blend of the two actors' scans, in the grown-up jacket.
- **The aging, for makeup and VFX.**
  - Five held idle poses, one per look.
  - The half-steps between them are blends of hair length, jacket fit and face.
  - No transition asset.
  - Subtle age makeup and VFX (18 §6). The first change should leave the player unsure they saw it.
- **Ellis's actor.**
  - Record ELL_010 and ELL_011 in the car shell with Grace's actor in the seat if the schedule allows. It's the brother bit coming back on reflex, played at nineteen. Don't pitch up to sound sixteen.
  - The oak lines are plain and busy-minded, not brooding (18 §2). No tears are written, so don't add them.
  - Efforts: the window crank, getting out, the sit, buttoning the jacket, the hand on the trunk to rise.
- **Wardrobe.** Ellis's jacket must button: the line says so.
- **The rain rig: off.** M14 is dry (see Audio).
  - Keep the rain machine off for every M14 session, including car-shell days shared with IX M6 or with X M8's 1973 stems, which are both wet.
  - Record M14 first, or re-dress the shell dry: no wet glass, no drip, no wipers.
  - An M14 stem with rain in it is a reject.
  - The rig is next needed for M15 (rain on the tin awning at Pickens).
- **Foley and ambience.**
  - Peepers and a small creek, recorded in early spring.
  - A real slant-six ticking down after shutdown, three minutes of it.
  - A hand on white oak bark, and on a healed callus of oak.
  - A Valiant window crank, one inch.
  - Boot heels on a dash.
