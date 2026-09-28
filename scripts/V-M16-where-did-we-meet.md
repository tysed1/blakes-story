# SCRIPT · Chapter V, Mission 16 · Where Did We Meet?

*Production script (V8). Source of truth for story: `chapters/chapter-05-velocity.md`, Mission 16, the game's midpoint. This script turns the mission into the form the team builds from: numbered scenes, line IDs, delivery notes, the held-embrace node with the flags it reads and sets, camera and audio cues, and timing. Where this script and the chapter disagree on story, the chapter wins. Where they disagree on execution, this script wins. Binding specs from the chapter are restated here in full. Canon it answers to: bible §11.3 (Clara rules), §11.4 (the objective camera; this mission is authored break #1), §11.8 (Clara's help and `clara_tests`); `18-performance-and-direction.md` §2, §6, §7.*

**Conventions**
- **Line IDs:** `V16_<SPEAKER>_<nnn>`. Speakers: ELL, CLA, RIL, CAL, DEA, WAY, MAR (Marlon), LOC (the local man), GRA (Grace, 1973; one sound in 16.5).
- **Cues:**
  - `SW:` switch;
  - `CAM:` camera. `CAM (Ellis):` is Ellis's perception, the default whenever the camera is with him. `CAM (objective):` is the camera outside his perception (the pull-back from its handover in 16.7 through step 1 of 16.8, and nowhere else);
  - `AUD:` audio;
  - `MUS:` band or music;
  - `UI:` HUD or prompt;
  - `SYS:` a system state.
- **Frames** are counted at the 30 fps cinematic timebase. If the timebase changes, keep the frame counts.
- **Flags** are listed in `17-tracked-state-registry.md`. Flags marked "(named here)" are new with this script and go into the registry.
- **The switch cue** (`SW_CUE`, bible §11.1) never fires in this mission. `SW:` none, throughout. Nothing in 16.5–16.8 may borrow any of its parts: no ambience narrowing over 8 frames, no projector-gate stutter, no depth-of-field pull, no `RMB_SWITCH` or `RMB_FAIL`. The pull-back is the camera leaving Ellis without a switch, and it must not read as one.
- **Clara** (CLA) is recorded and mixed like any person in the room. No processing. She's lit by the same light as everyone else (18 §2).

**Flags read here:**
- `clara_tests` (tests in I M1, II M10, III M3, IV M8, V M1; range 0–5): the notebook conditional, Node N16.9.
- the notebook's last entry (placement only, N16.9).

**Flags set here:**
- `midpoint_hold_seconds` (named here)
- `midpoint_complete` (named here)
- `notebook_prove_it_line` (named here)

---

## MISSION 16 · WHERE DID WE MEET? (Fri May 2, 1975, 9:00 p.m. – Sat May 3, 1:40 a.m.)

**Entry state (from M15 and the chapter's design summary)**
- Friday May 2, 1975. At 5:30 p.m. the four sat in the van in Marlon's lot with the doors shut against the rain and made the promise: no limousines; no treating each other like employees; no band decisions alone; nobody leaves somebody behind (Ellis's clause, the one he said to his sister in the other direction).
- Southern Star has offered a record. The contract draft was in the folder on Cal's lap. Nothing is signed. The town has decided "the Blakes got a record deal," and nobody corrects it.
- Riley told Dean and Cal about Grace in the van in March while Ellis slept. He knows she did.
- Clara has been possessive of his attention since the Exit ("Nobody understands." / "She just did."). In five chapters she has never cried.
- Bible §11.3 Rule 11 is in force for the last time. Clara has never shared a vehicle with a band member, and no third party's point of view has framed the place where she is (the V M7 fence, played from Riley's side, is the one sanctioned exception). She isn't in M15.
- Ellis has had one flash before this: twelve frames on the Laurel Gap in M5 (the green felt-tip hand on a dashboard).
- The help layer is active for Ellis. None is authored for M16, and none plays with Wayne in the room.
- `clara_tests` stands wherever the player left it.
- `UI:` HUD: FRIDAY.

### 16.1 · INT. MARLON'S TAVERN · FRIDAY · 9:00 P.M. · THE CELEBRATION
`SYS:` Ellis, free movement inside Marlon's. Clara isn't present (she first appears in 16.3). Observe behaves as normal; this script authors no targets. The chapter doesn't stage the Friday set, and this script doesn't add one: the mission opens on the party, with the band off the stage.
`CAM:` The Friday show has become a party. Blocking:
- the band's table beside the stage, so the room's center of gravity is the stage end;
- Marlon behind the bar, pouring the band's drinks free. Even Cal has one;
- Roy at a table with Evelyn, who has never been inside Marlon's in her life and is having a wonderful time;
- Mrs. Hensley at her corner, on a Friday, which she never does;
- Earl Pike at the pool table;
- Wesley Tate outside, at the window.

`AUD:` A full room: pool balls, ice, the door. Walla is indistinct: townspeople who once complained the band was too loud now telling Ellis they always knew. No intelligible words except the scripted lines.
`MUS:` The jukebox, from its existing Chapter V rotation. This script adds no selection.

The local man's exchange fires when Ellis is within 3 m of Riley at the band's table.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_LOC_001 | LOCAL MAN | Knew you boys had something. | Proud, a couple of beers in, meaning it. A neighbor, never a comic turn. |
| V16_RIL_001 | RILEY | Define "boys." | Argument form, for fun. |
| V16_LOC_002 | LOCAL MAN | You know what I mean. | Unbothered. |
| V16_RIL_002 | RILEY | Do I? | Dry. She lets him off by turning back to the table. |
| V16_ELL_001 | ELLIS | (laughs) | Easy. The night is going well. |

Dean's toast fires when Ellis is back at the band's table.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_DEA_001 | DEAN | To being disgustingly rich. | Glass up. Overstatement, picking up his own line from the van. |
| V16_CAL_001 | CAL | Not happening. | A correction, flat. |
| V16_DEA_002 | DEAN | To being moderately rich. | Negotiating down without losing any volume. |
| V16_RIL_003 | RILEY | Unlikely. | Crossword precision. |
| V16_DEA_003 | DEAN | To owning a van built after the moon landing. | His final offer, and he's delighted with it. |
| V16_CAL_002 | CAL | Which one? There were six. | A correction, played straight. It gets the laugh anyway. |

`AUD:` Laughter: the four, and the tables nearest them.

### 16.2 · INT. MARLON'S · WAYNE WALKS IN
**Trigger:** after Dean's toast, when Ellis is at the stage end of the room.
`SYS:` Movement locks as the door opens: Ellis waits for whatever this is. Look stays free. The help layer is off while Wayne is in the room. Clara isn't present (Rules 8 and 13; she doesn't appear before 16.3).
`AUD:` The front door. The room changes slightly before the player sees why: the walla thins from the door inward over about 2 s, as a wave and never as a cut to silence. The pool game stops (the last ball rolls out; Earl Pike sets his cue on the rail). Marlon's towel stops on the glass. The jukebox keeps playing, because nobody stops a jukebox.
`CAM (Ellis):` Free. If the player hasn't turned toward the door within 1.5 s, a soft look-assist brings it into frame: Wayne Blake, standing inside the door in his work jacket. Nobody in Hollow Ridge has seen him inside Marlon's since April 1973, and everyone in the room knows it. Heads turn one at a time.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_MAR_010 | MARLON | Wayne. | Flat and careful. The glass and the towel still in his hands. |
| V16_WAY_010 | WAYNE | Marlon. | Matched exactly. |

`CAM:` Wayne crosses the room to Ellis by the stage. People make way.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_WAY_011 | WAYNE | Heard about the record. | A report on a job. No congratulations in it, and no attack. |
| V16_ELL_010 | ELLIS | It's not— yet. Maybe. | Correcting the record for his father, which he wouldn't bother to do for anyone else in the room. Cornered, a little formal. |
| V16_WAY_012 | WAYNE | Heard about it. | He doesn't correct him back. He says it again. |

`CAM (Ellis):` Wayne looks around the room: his son's band; people he's known forty years slapping his son on the back. During the look, two or three townspeople clap Ellis on the shoulder on their way past. Hold about 45 s. For that minute Wayne sees his son the way the room does. Ellis waits for the other shoe. It doesn't come.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_WAY_013 | WAYNE | Your mother used to— | He stops himself. It's a subject he doesn't touch, and he has touched it. A choice; his throat is fine (compare X09_WAY_010). |
| V16_ELL_011 | ELLIS | What? | Quick. He wants the rest of it. |
| V16_WAY_014 | WAYNE | Be loud about it. | Plain, smaller, dry. The nearest thing to a joke he has. |
| V16_ELL_012 | ELLIS | (laughs) | Surprised out of him. |
| V16_WAY_015 | WAYNE | (almost laughs) | A breath through the nose, and it stops there. |
| V16_WAY_016 | WAYNE | Grace too. | Her name, said. He isn't using it as a weapon, and he isn't offering comfort. |

`CAM (Ellis):` Ellis's smile goes, then comes back, smaller.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_013 | ELLIS | Yeah. | Taking it the way it was meant. |
| V16_WAY_017 | WAYNE | Riley. | A nod with her name on it. Acknowledgement. |

`CAM:` Wayne nods to the others, nods to Marlon, and leaves. He doesn't stay for a drink.
`AUD:` The room exhales: the walla returns over about 3 s. Marlon picks the glass back up, and the towel starts again.
`SYS:` Door to door, target 2:45–3:00. He came to stand next to the son he blames, and he lasted three minutes. Movement returns when the door closes behind him.

### 16.3 · INT. MARLON'S · THE BAR · LATER · THE TOAST
`CAM:` Cut. Later: the four of them at the bar with Marlon's free round. The room is thinner but still going.
`SYS:` Ellis's movement locked at the bar; look free.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_DEA_020 | DEAN | To Southern Star. | Again. Still delighted with himself. |
| V16_CAL_020 | CAL | To reading it first. | Cal's toast is an instruction. |
| V16_RIL_020 | RILEY | To Carla Vickery. | The girl with the pink letter on the kick drum. Meant. |

**Node N16.3 · the toast** (fixed line, player-timed; sets nothing)
- `CAM:` Ellis raises his glass. He thinks.
- `UI:` One phrasing on screen, *To Grace.*, the same form as the fixed line in X M8. No timer on screen.
- The line plays on the player's input. With no input for 8 s, he says it anyway: he has already decided.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_020 | ELLIS | To Grace. | Plain. A toast, and he chose it. No confession in it. |

`AUD:` Silence among the four. The room around them keeps going at its level; this is private, and the town doesn't notice. Nobody at the bar looks surprised. Riley told them in March.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_RIL_021 | RILEY | To Grace. | First, and fast, so it doesn't sit there alone. |
| V16_CAL_021 | CAL | Grace. | Low. |
| V16_DEA_021 | DEAN | Grace. | No joke anywhere near it. |

`CAM:` They drink.
`CAM (Ellis):` A scripted look down the bar. Clara is standing at the far end by the cigarette machine, and she isn't smiling.
`SYS:` Rule 11 blocking: Riley, Cal and Dean face the bar or each other. None of their eyelines lands on the cigarette machine, and no shot is taken from their side of the bar toward it.

### 16.4 · INT. MARLON'S · A BOOTH · AFTER CLOSING · "WHAT'S WRONG?"
`CAM:` Cut. After closing. Everyone else has gone; Riley went home with Hannah. Marlon is mopping behind the bar and has turned the jukebox off. The sign outside is dark. Ellis sits in a booth with the last of a beer.
`CAM (Ellis):` Clara, sitting across from him.
`SYS:`
- Seated; movement locked; look limited to a soft ±10° that springs back.
- Observe is suppressed from here to the card.
- Marlon works behind the bar, mostly turned away. His eyeline never lands on the booth before V16_MAR_040 (Rule 11).
- `UI:` The HUD day rolls to SATURDAY at midnight, silently.

`AUD:` Room tone after hours: the mop and the wringer, the beer cooler's compressor, the ice machine cycling. `MUS:` none, from here to the card.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_030 | ELLIS | What's wrong? | Easy, a few free beers in. He's happy and wants her to be. |
| V16_CLA_030 | CLARA | Drink your beer. | An order, to change the subject. A big sister. |
| V16_ELL_031 | ELLIS | (laughs once) | At being bossed. She doesn't laugh. |
| V16_ELL_032 | ELLIS | We got a record. | Teasing her out of it. |
| V16_CLA_031 | CLARA | I heard. The whole county heard. Dean told the ice machine. | Dry, a real joke, still not smiling. |
| V16_ELL_033 | ELLIS | That's good. | Prompting her. |
| V16_CLA_032 | CLARA | Is it? | A real question. |
| V16_ELL_034 | ELLIS | Yeah. | Sure of it. |
| V16_CLA_033 | CLARA | Where do they make records? | Like asking directions she already knows. |
| V16_ELL_035 | ELLIS | Laurel City. Tannersville. | Answering it straight. |
| V16_CLA_034 | CLARA | Not here. | Flat. |
| V16_ELL_036 | ELLIS | That's sort of the idea. | Light. He hasn't heard what she heard. |

`CAM (Ellis):` She looks hurt.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_037 | ELLIS | You can come. | Quick, meant, the way he always says it. |
| V16_CLA_035 | CLARA | You always say that. | Tired of hearing it. |
| V16_ELL_038 | ELLIS | Because you can. | Simple. |
| V16_CLA_036 | CLARA | Until you don't want me to. | Plain. Played as a fact about him, never as wistful or knowing. |
| V16_ELL_039 | ELLIS | What are you talking about? | Honestly lost. |
| V16_CLA_037 | CLARA | Riley. | One word, like naming a culprit. |
| V16_ELL_040 | ELLIS | What about Riley? | A little defensive. |
| V16_CLA_038 | CLARA | She sings my part. | Jealous the way a kid sister is when her part gets taken. Petty, and she knows it's petty. |

`CAM (Ellis):` Ellis stares at her. Clara looks at the dark stage, at the house kit under its cover. The camera goes with her look to the stage, then back to her.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_039 | CLARA | I sang it first. | To the stage, a claim, the way somebody says they called the front seat. Nothing eerie in it. |

`CAM (Ellis):` He goes still.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_041 | ELLIS | What? | Quiet. He heard it. |

**The flicker.**
- `CAM (Ellis):` She looks back at him. A held shot on her across the booth, with no cut. For 8 frames the girl across the booth is fourteen: in the same jacket, too big for her, her hair in a ponytail, looking at him exactly the way Clara looks at him. Then Clara again.
- An in-place swap: same seat, same pose, same eyeline, same light. No dissolve, no frame blend, no glitch, no stutter, no camera move.
- `AUD:` Nothing marks it. No sound changes.
- Played by the Grace actor (18 §2), matched to Clara's pose and look.
- Duration: the chapter says "one instant"; the bible table says "for a frame." Eight frames is long enough for the ponytail and the too-big jacket to register and short enough to doubt.

`CAM (Ellis):` Ellis stands up so fast the booth table screeches on the floor. The stand begins 10–15 frames after Clara returns, so the screech lands as his reaction and never as punctuation on the picture.
`AUD:` The screech at its real level. Don't sweeten it; it must not work as a sting.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_MAR_040 | MARLON | (from behind the bar) You all right? | Across the room, plain. A bartender's check on a sound. He stays behind the bar. |

`CAM (Ellis):` Ellis looks at Marlon; the camera turns with his head, and the booth leaves frame. Then back at the booth. Empty. (Rule 13: she's gone when the camera comes back from looking somewhere else.)

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_042 | ELLIS | Yeah. | Too fast. |
| V16_MAR_041 | MARLON | You sure? | He's heard that "Yeah" before. |
| V16_ELL_043 | ELLIS | Yeah. | Worse. He isn't. |

`SYS:` Control returns: walk. The front door is the path out, lit, and the way Ellis's body turns. The chapter's header lists the alley, and the text sends him out the front door. If the build lets the player take the steel back door instead, the alley joins Depot Street along the side of the building and nothing happens in it. 16.5 fires on Depot Street either way.

### 16.5 · EXT. DEPOT STREET · LATE
`CAM:` Late, cold for May. The one streetlight (the Chapter I fixture). The rail line dark. The street is dry, or damp at most, with no standing water. No rain.
- **Geography, fixed by the pull-back's path:** the streetlight stands across Depot Street from Marlon's front.
- Ellis walks out of Marlon's and across toward the streetlight, and stops short of its pool, in the middle of Depot Street.

`SYS:` Walk control. He lights a cigarette on his first steps (automatic; the I M1 gesture, cupped backward in his palm). His hands are shaking.

The first call fires about 8 m out from the door. Its source sits behind him, toward Marlon's, about 5 m back.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_050 | CLARA | (o.s.) Ellis. | A normal call across a yard, at speaking volume. |

`SYS:` He keeps walking. Walk control continues. If the player turns the camera, the street behind him is empty, which is true.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_051 | CLARA | (o.s.) Ellis. | The same call again, a little more insistent, from the same place. |

`SYS:` Movement locks from here to the card. Look is limited to ±10° and springs back.
`CAM (Ellis):` He stops. Turns. Nobody: Depot Street back toward Marlon's, empty. Her voice has never come without her before.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_050 | ELLIS | Clara? | Toward the empty street. Asking. |

`AUD:` Nothing. About 2 s of the street. Then, behind him (the streetlight side):

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_052 | CLARA | What? | Ordinary, a little put out, as if he called her. |

`CAM (Ellis):` He turns. She's there, under the streetlight, completely normal, her hands in her jacket pockets. He's a few steps outside the pool of light. She's there when the turn arrives; she never pops in on screen. He stares at her.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_053 | CLARA | You're acting weird. | A sister's tease. |
| V16_ELL_051 | ELLIS | (almost laughs) | A breath of it. |
| V16_ELL_052 | ELLIS | *I'm* acting weird? | Mock-offended, cornered, funny. He's funniest when things are going badly. |
| V16_CLA_054 | CLARA | You're standing in the middle of Depot Street like a mailbox. | Comic, in her idiom. She's enjoying it. |
| V16_ELL_053 | ELLIS | Who are you? | Plain, level. No drama. |

`CAM (Ellis):` Silence. Her face goes frightened.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_055 | CLARA | What do you mean? | Frightened as a person is frightened. She doesn't understand the question. |
| V16_ELL_054 | ELLIS | Where did we meet? | Careful, like a test he doesn't want to give. |
| V16_CLA_056 | CLARA | Ellis— | Pleading him out of it. |
| V16_ELL_055 | ELLIS | Where? | Firm. |
| V16_CLA_057 | CLARA | Out back of Marlon's. | Relieved to have an answer. Quick. |
| V16_ELL_056 | ELLIS | When? | Quiet. |
| V16_CLA_058 | CLARA | (no line; opens her mouth, and nothing comes) | Hold about 3 s. She looks at him as if he's asked her what year it is and she has never once been told. A real blank; nothing withheld. |
| V16_CLA_059 | CLARA | Why are you doing this? | Hurt and confused. |
| V16_ELL_057 | ELLIS | Because I don't remember. | A confession, plain. |
| V16_CLA_060 | CLARA | Of course you do. | Reassuring, to both of them. |
| V16_ELL_058 | ELLIS | Then tell me when. | Level. |
| V16_CLA_061 | CLARA | El. | The way you'd say someone's name to settle them. It slips out; she doesn't hear herself say it. Never marked. |

`CAM (Ellis):` He freezes.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_059 | ELLIS | What did you call me? | Very quiet. |
| V16_CLA_062 | CLARA | Ellis. | Plain. She doesn't know what he means. |
| V16_ELL_060 | ELLIS | You called me— | He can't say it. |
| V16_CLA_063 | CLARA | You know. | The ordinary phrase people use to end a question. Nothing pointed in it. |

**The twelve frames.**

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_061 | ELLIS | (breathing changes) | Shorter, higher in the chest. No gasp. |

- `AUD:` The screen doesn't distort; the sound does, just slightly, like a room with the doors closing. Over 1.0 s the street's far layers drop away first, then its top end dulls a little. Ambience bus only; the dialogue bus is untouched. No tone, no ringing, no heartbeat, no sub-drop, no whoosh.
- `CAM:` Then twelve frames, cut in and out hard. Four images of 3 frames each (faster than the M5 flash, which put fewer images in its twelve):
  1. A windshield, broken into a web, rain coming through it.
  2. A car seat, before: the passenger seat, dry, in the dash light. The laugh (V16_GRA_001) starts here.
  3. A green felt-tip hand: a teenager's hand flat on a dashboard, green ink on the knuckles (the M5 image).
  4. Headlights.
- Gone. A hard cut back to Depot Street in the framing it left.
- No face in any frame. No flash-frame, no white-out, no transition, no shake, no color shift.
- `AUD:` The laugh is the only sound in the twelve frames, cut hard at the end of frame 12. The street's narrowing releases over 2.0 s from "Gone."

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_GRA_001 | GRACE (1973) | (a laugh, from a car seat, before) | Easy: a kid laughing at her brother. No word inside it. Not the X M8 laugh (`GRA_1973_LAUGH`). |

`CAM (Ellis):` Ellis bends over with his hands on his knees in the middle of Depot Street. Continuity: the cigarette drops from his fingers as he bends. Don't feature it.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_062 | ELLIS | (bent over; breath) | Getting it back. |

### 16.6 · DEPOT STREET · CLARA CHANGES TACTIC
`CAM (Ellis):` Continuous from 16.5. There are no cuts from V16_CLA_052 to the release in 16.8: she never gets closer between cuts (Rule 12).
She comes toward him. Gentle again. A few steps; she's at arm's length when he speaks.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_070 | CLARA | Hey. | Gentle. |
| V16_ELL_070 | ELLIS | Don't. | Low, from bent over. |
| V16_CLA_071 | CLARA | You're tired. | A sister's diagnosis. |
| V16_ELL_071 | ELLIS | Don't touch me. | Sharp, not loud. He doesn't shout. |

`CAM (Ellis):` She stops.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_072 | CLARA | Okay. | Stung. She keeps her hands to herself. |
| V16_ELL_072 | ELLIS | You're messing with me. | Wanting it to be true. |
| V16_CLA_073 | CLARA | No. | Simple. |
| V16_ELL_073 | ELLIS | Then tell me when. | The third time. Quieter than the first. |
| V16_CLA_074 | CLARA | (starts crying) | A person crying: fast, embarrassed by it, not pretty. Nothing eerie and nothing played. |

`CAM (Ellis):` This undoes him. In five chapters Clara has never cried.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_075 | CLARA | Why are you doing this to me? | Through the crying. Hurt, because he's scaring her. |

`CAM (Ellis):` And now he feels guilty. He softens immediately.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_074 | ELLIS | I'm sorry. | At once. |

`CAM (Ellis):` He steps toward her, into the pool of the streetlight.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_ELL_075 | ELLIS | I'm sorry. I'm sorry. | The way people say it who have been saying it for years: quick, low, automatic. It's the phrase Riley isn't allowed to say to him. |

`CAM (Ellis):` Clara puts her arms around him. From Ellis's side: real. Warm. A person. Her hair against his face, the jacket, the horse patch pressed against his shirt. They stand under the streetlight, side-on to the lens. Two shadows on the asphalt.

### 16.7 · THE EMBRACE AND THE PULL-BACK · 1:40 A.M.
**The one thing that must be true (18 §7):** the player holds the embrace while the camera leaves. Nothing tells them to let go. The embrace continues while the camera pulls back (18 §6).

`SYS:` The world clock holds at 1:40 a.m. from here to the card.
`UI:` As her arms close around him (about 1.0 s after contact), a prompt comes up, the same one the game uses for holding a long note: **Hold.** The HUD day clears as it appears, so the prompt is the only thing on screen.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| V16_CLA_080 | CLARA | (crying into his shoulder, tapering to breath) | Close. It runs down on its own, the way crying does, over about 6 s, then breathing. |
| V16_ELL_080 | ELLIS | (breath, in the embrace) | Steadying. He doesn't cry. |

**Node N16.7 · the hold** (sets `midpoint_hold_seconds`; the pull-back runs off it)

| Input state | What happens |
|---|---|
| Prompt up, nothing pressed | The embrace holds in Ellis's perception. Clara's crying tapers to breathing. The camera doesn't move. No timer, no reminder, no timeout. |
| Pressed, released before 2.0 s | Not a release. The embrace continues, the prompt stays, and the next press starts the count again. |
| Held to 2.0 s | The pull-back starts (Beat B). The prompt fades over 0.5 s and nothing replaces it. From here the move is committed. |
| Released during the move (Beats B–E) | The move doesn't stop, slow, speed up or reverse. Ellis keeps holding. His arms open at lock + 4.0 s (the floor, below). `midpoint_hold_seconds = 0`. |
| Held at lock (Beat F) | The objective frame holds for as long as the player holds. No timer, no end. |
| Released after lock | His arms open on the release frame, or at lock + 4.0 s if the release comes sooner. `midpoint_hold_seconds` = seconds from lock to release. |

**The floor (execution).** The chapter says the wide shot lasts exactly as long as the player keeps holding. That holds for every player still holding when the frame locks. A player who let go during the move gets 4.0 s of the locked frame with the embrace held, so everyone sees the frame the chapter describes at rest. The 4.0 s covers the horn's first long.

**Binding UX spec**
- The prompt is the Room's long-note **Hold.**: same glyph, type, size and position. Any fill, meter or duration element the Room's version carries is off here.
- It never pulses, blinks, grows or repeats. No idle reminder. No UI sound on appearance, press or release.
- No rumble from the prompt to the card. Rumble belongs to the switch.
- Nothing ever tells the player to let go: no release prompt, no timer, no fade that ends the hold for them, no camera drift that suggests an ending.
- **Accessibility.** The HOME toggle (`19-playtest-plan.md` §3): press once to hold, press again to release. Same meaning, and the same timings from the first press.
- **Pause.** The pause menu freezes the scene and the hold clock. On resume the embrace continues whether or not the button is down, and the next button-up ends it. No prompt comes back.
- `SYS:` `midpoint_hold_seconds` (named here): real seconds from the lock to the release, pause time excluded; 0 if the release came before the lock. No authored scene reads it. It's logged for Slice B (`19-playtest-plan.md` T1, T2) and is available to later scripts.

**THE PULL-BACK. Binding camera spec.** Seconds run from the press (T 0). Distances are from Ellis. Targets may move ±10% for level geometry; the order of the beats, the handover rule and the one-shot rule don't.

| Beat | T (s) | Move | In frame |
|---|---|---|---|
| A · Hold | 0.0–2.0 | Static. 1.2 m from the pair, side-on, lens at Ellis's eye height (about 1.55 m). The game's handheld noise eases to zero by 2.0 s. | `CAM (Ellis):` the embrace, close. His face against her hair. His near hand closes on the back of her jacket at about T 1.0. The patch is between them, out of sight. |
| B · Across Depot Street | 2.0–13.0 | Straight back, away from the pair. Eases in over 3.0 s to 1.1 m/s, slower than a walk, then steady. Height held. Ends at the far curb, about 11.5 m out. | Still his perception. Clara in frame, lit by the streetlight, her shadow beside his. Her crying and his breath fall away by distance only. |
| C · Past the front of Marlon's | 13.0–18.0 | Back at 1.1 m/s, with a lateral drift of about 2 m so the lens passes a near occluder on Marlon's side: the corner of its front wall, its dark sign or the sign's post (level art picks what the path allows). At about T 15.0 the occluder covers the pair completely for at least 12 frames. **The handover happens under it.** Ends about 17 m out. | Marlon's front, its sign dark. Past the occluder the frame is objective: Ellis alone, his arms around nothing. |
| D · Up, a little | 18.0–26.0 | Back at 1.1 m/s while rising from 1.55 m to about 6 m, the way a camera on a crane would move. Tilt down to keep Ellis at the same place in frame. | Ellis under the streetlight, smaller. |
| E · Past the depot. Farther. | 26.0–34.0 | The depot's roof edge passes through the bottom quarter of frame, never across Ellis. Ease out over the last 4.0 s. Rest about 33 m out, 6–6.5 m up. | The street opening out around him. |
| F · The objective frame | 34.0 → release | **Lock.** Locked off: no drift, no breathing, no handheld, no push-in, however long the player holds. | See below. |

**The handover** (Beat C, under the occluder)
- `SYS:` Ellis's perception → objective. Clara's body, shadow, cloth and audio sources are culled. Ellis's pose doesn't change.
- The only difference between the last perception frame and the first objective frame is Clara: her body, her shadow, her cloth, her sound. Light, grade, lens, focus, ambience and Ellis's pose are identical across it.
- It happens under full cover because she can't vanish on screen here (Rule 13) and can't appear in an objective shot (Rule 3). There's no cut: the camera makes one continuous move from the press to the lock.
- The handover distance (about 14 m) is chosen so her crying is already below the street bed there. If the mix can still hear her at the handover, move the handover farther out. Don't fade her.

**The objective frame (Beat F).** No character sees this. Only the player, who is still holding.
- Ellis is a small figure under the one streetlight on Depot Street, in Hollow Ridge, Georgia, at twenty to two in the morning: about 8% of frame height, in the lower middle of frame, off dead center.
- Alone. His arms wrapped around nothing. His head bowed onto nobody's shoulder. His hand holding the back of a jacket that isn't there.
- One shadow on the asphalt.
- Around him: the empty street; the pool of light and the dark past its edge; Marlon's dark sign and the depot low in the near frame; dark houses on the hill beyond.
- Nobody else anywhere in frame: no one in a window or a doorway, no parked or passing car, no animal. Marlon's front room is dark.
- He breathes, at a real rate. He doesn't cry. He doesn't move until the release.
- Level horizon. No Dutch angle, vignette, grade change, letterbox or slow motion. Real time.
- `AUD:` The town at the camera's position (see the audio spec). At lock + 2.0 s, the freight horn, once.

**Do not explain it (binding, from the chapter).** No text, no diagnosis, no flashback, no voice-over. No achievement, trophy, loading tip, chapter-select thumbnail or menu text that names or shows what the pull-back showed.

### 16.8 · THE RELEASE, THE CLOSE, THE FADE
1. `CAM (objective):` Far off under the streetlight, Ellis's arms open around nothing (1.2 s) and come down to his sides (0.8 s). The frame holds on him standing alone for 2.0 s more.
2. `CAM (Ellis):` A straight cut back to Ellis, close, in Beat A's framing. The camera doesn't travel back. Clara is there again, stepping back from him and wiping her face with her jacket cuff, because the camera is with Ellis again.
   - `SYS:` objective → perception on the cut. Clara re-enters already a step back, farther from him than at the handover, so Rule 12 holds.
3. Hold 4.0 s. She wipes once and lowers her hand. He looks at her. No lines.

   | ID | Speaker | Line | Delivery |
   |---|---|---|---|
   | V16_CLA_090 | CLARA | (a breath; the cuff across her face) | Unprocessed, close. Done crying and a little embarrassed about it. |

4. Fade to black over 2.0 s. The street holds 1.0 s into black, then silence.
5. `UI:` CHAPTER V COMPLETE · VELOCITY

- **Control.** After the press, control doesn't return in this mission. The release is the player's last input in Chapter V. The next input is Chapter VI's cold open; free control in Hollow Ridge returns in VI M1, Saturday, 9:30 a.m.
- `SYS:` At black: `midpoint_complete = true` (named here). N16.9 evaluates. Autosave after the card, never during the hold.
- `midpoint_complete` is read by:
  - the Clara rules layer. Rule 11 lifts: she may share a vehicle with a band member (VI M1, the back seat of Riley's Datsun), and a third party's point of view may frame her place (VI M9);
  - the test interactions, which retire (bible §11.8: tests exist before the midpoint).

### 16.9 · THE NOTEBOOK (CONDITIONAL)
**Node N16.9 · the line** (reads `clara_tests`; sets `notebook_prove_it_line` (named here))
`SYS:` Evaluated once, at black (16.8 step 4). `clara_tests` freezes there.

| `clara_tests` | Result |
|---|---|
| 3 or more | `notebook_prove_it_line = true`. One line is written under the last entry, in Ellis's hand, that no Observe cue produced: *I kept asking her to prove it and she kept not.* The player finds it the next time they open the notebook. |
| 0–2 | `notebook_prove_it_line = false`. Nothing is written. The page is as the player left it. |

- No cue marks it: no toast, badge, sound, new-entry marker, page highlight or achievement. Nothing ever refers to it.
- The same pen and hand as his entries from that spring. No place or date stamp, even if Observe lines carry one.
- Tag it as not an Observe line (it never joins `observe_lines`). It counts toward nothing, and no pool can select it: not the leaked pages (IX M11), and not Riley's reading or her book (Ep. M5), though the memo book it's in is copied and read.
- If the notebook is empty, it's the first line on the first page.

**Binding audio spec (16.5–16.8)**
- **Ambience only. No score, no sting.** `MUS:` none. No tonal bed, pad, drone, sub, riser, reversed sound or heartbeat dressed as ambience. Nothing sounds on the handover, the lock, the release or the cut back.
- **The street, in perception (16.5 to Beat B).** Depot Street at 1:40 a.m., cold for May:
  - a low, wide town bed;
  - Hollow Creek, faint (it runs past the one streetlight, I M1);
  - sparse insects, fewer than on a warm night;
  - the streetlight's ballast hum, audible only within a few meters of the pole.

  No wind gusts, no dog, no traffic.
- **Clara, while she's in frame from Ellis's perception:** unprocessed. No reverb, filter, pitch shift, breathiness or special panning.
  - Her off-screen calls sit at their blocking position like any off-screen voice.
  - Her crying in the embrace is close, on his shoulder.
  - As the camera leaves, she and Ellis fall away by distance only, on the same curve as every voice in the game.
  - The 16.5 narrowing is on the ambience bus and never touches her. None of her lines plays under it.
- **The objective frame.** The listener moves with the camera, so the player hears what's at the camera, about 33 m off and 6 m up: the town bed and the creek, and nothing of Ellis. His breath is too far away to hear, and Clara isn't there.
- **The freight horn** (`AUD_FREIGHT_HORN_FAR`, named here). At lock + 2.0 s, once. Very far down the valley: two longs, a short, a long (about 2.0 s, 2.0 s, 0.8 s and 3.0 s, with gaps of about 0.8 s, then the valley's own decay).
  - The same recording family as the horn in Chapter I's cold open and the I M1 alley. Recorded at real distance; no sweetening.
  - The release doesn't cut it. It plays out under the cut back and, if it has to, into the fade.
  - It doesn't repeat, however long the player holds. After it, only the town bed.
- **The close (16.8).** The street at close perspective; Clara's breath and the cuff, unprocessed; Ellis's breath.
- **Captions.** Dialogue subtitles have nothing to show after V16_ELL_075. Clara's lines, the off-screen calls included, are labeled CLARA like anyone's (`19-playtest-plan.md` §3). If sound captions are on, the horn gets one plain caption, *[Freight horn, far off]*, cleared when it ends. Nothing else in 16.7 is captioned.

**Binding camera and light spec (16.5–16.8)**
- **The streetlight.** The Chapter I Depot Street fixture (the Valiant parked under it in I M1): same pole, same lamp, same color, same pool. It isn't relit for the midpoint. No fill, rim or key is added for either of them. While she's in frame, Clara takes the same light as Ellis and casts a shadow the way he does.
- **No atmosphere.** No haze, fog, visible beam, lens flare or extra bloom. No rain and no wet sheen: nothing on the street or in Marlon's windows may reflect either figure (Rule 12). Marlon's front windows read dark and matte from the pull-back path.
- **No visible breath** on anyone, so the objective frame differs from perception in Clara alone.
- **The distance.** The frame rests at about 33 m out and 6–6.5 m up: far enough that he's small, near enough that the empty arms read.
- **One lens.** A fixed focal length (35 mm equivalent) from Beat A to the lock. No zoom, no dolly-zoom. Focus follows Ellis continuously, with no rack and no depth-of-field pull (that's switch grammar). The objective frame is deep focus.
- **No horror grammar** (Rule 12; bible §12.6; 18 §6).
  - No reveal in a mirror, a window or a reflection.
  - No stinger, glitch, chromatic aberration, distortion or whisper.
  - She never gets closer between cuts: V16_CLA_052 to the release is one shot.
  - The flicker in 16.4 and the twelve frames in 16.5 are clean swaps and cuts with no effect laid on them.
- **The move.** Slow and unshowy (18 §6): a smooth dolly and crane, no shake, never a speed-up.
- **Grade.** The game's standard night grade throughout. No shift at the handover or the lock.
- **Animation (for the objective frame).**
  - Author Ellis's embrace so his balance stays over his own feet. He holds her; he doesn't lean on her. In the objective frame he must be holding air, with nothing to fall toward.
  - His hand's grip on the back of her jacket is a closed-hand pose, not driven by cloth collision, so it keeps its shape when the cloth is gone.
  - His head bows forward and down to her shoulder height and stays there.
  - The perception beats use the paired capture pass, and the objective frame uses the solo pass (recording notes). The two are matched and blended under the occluder.

---

## Exit state into Chapter VI
- **Clock.** Saturday May 3, 1975. Chapter VI opens on its cold open (Dalton Sound, July), then THREE MONTHS EARLIER, then VI M1 at 9:30 a.m. `UI:` HUD: SATURDAY.
- **Ellis.** Wakes up in his clothes on top of the covers with his boots on. How he got home isn't shown, and mustn't be.
- **Clara.** On the floor under the window, knees up, exactly where she always sits. He looks at her differently; she knows it; neither says it. Her help continues ("Morning. It's half past nine.").
- **The player.** Knows she isn't there. From VI on, every Clara scene plays with dramatic irony: the camera stays in Ellis's perception, where she's fully there, lit and solid, and the player knows she isn't. She must still be warm, funny and lovable.
- **The mystery.** It has changed shape, from *Who is Clara?* to *What is Clara?* The game doesn't say who she is.
- **Flags.**
  - `midpoint_complete = true`: Rule 11 is lifted, and the test interactions are retired.
  - `clara_tests` is frozen.
  - `notebook_prove_it_line` is set as N16.9 decided.
  - `midpoint_hold_seconds` is logged.
- **World.** Southern Star has offered a one-album deal; nothing is signed. Wayne's truck is gone in the morning. Riley honks in the yard, twice, short: she's taking him to breakfast at the Starlite.
- **The next objective break** is VI M9, the Ellis → Riley switch at the farmhouse (bible §11.4, break #2).

---

## Performance and recording notes
- **The embrace.** Capture two passes.
  1. Ellis and Clara together, from V16_CLA_070 through the hold, so her crying and his apologies are recorded in the embrace.
  2. Ellis alone, holding the same shape with nobody in it, for the objective frame. Match it to pass 1 in duration and breathing. Direct it as the same embrace, never as a man miming one.
- **Ellis.** V16_ELL_075 is said the way people say it who have been saying it for years: quick, low, automatic. It's the phrase he can't hear without flinching, and here it comes out of him on its own. Don't ask the actor to imitate the X M8 apology; let it land near it. He doesn't cry (18 §2: no tear on camera before VIII) and he doesn't shout. "Who are you?" is plain. "*I'm* acting weird?" is a real almost-laugh.
- **Clara.** She's a person, not a mystery (18 §1).
  - The chapter's "changes tactic" is the writer's frame, never hers to play. She's hurt and frightened, and she's crying because he's scaring her.
  - She never knows she's a figment and never plays a line as if it means something twice.
  - "El." slips out, and she doesn't hear herself say it. Record several reads and use the least marked.
  - The silence after "When?" (V16_CLA_058) is a real blank.
  - The off-screen calls are projected, at speaking volume.
  - She has no lines in 16.7–16.8: crying that runs down to breath, then the cuff.
- **Grace (1973).** The X M8 actor.
  - The laugh (V16_GRA_001): recorded in the car shell, dry, with no rain machine, improvised with the Ellis-at-sixteen actor. Choose a take with no word shape in it.
  - The 8-frame flicker in 16.4: the same actor in Clara's adult-sized jacket (too big for her) and a ponytail, matched to Clara's seat, pose and look.
- **Wayne.** No performance in the voice. The stop in V16_WAY_013 is his choice. "Grace too." is said; it isn't a weapon and it isn't tender. He doesn't soften on camera. What he does is walk in. He doesn't raise his voice.
- **Marlon.** Wipes spots that are already clean. Record two reads of "You all right?" and use the plainer one.
- **The band.** Record the toasts together, live, at a bar set, so the two "Grace." lines fall naturally. Cal and Dean don't play surprise at "To Grace."
- **The local man.** A regional accent, and no caricature.
- **Walla.** A Hollow Ridge group record with local accents, kept indistinct. No scripted words beyond the local man's.
- **The freight horn.** Recorded at real distance in a valley, from the same source family as Chapter I's.
