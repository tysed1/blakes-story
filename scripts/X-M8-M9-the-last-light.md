# SCRIPT — Chapter X, Missions 8–9: The Last Light · The Gap

*Production script (V8). Source of truth for story: `chapters/chapter-10-the-last-light.md`. This script turns Missions 8 and 9 into the form the team builds from: numbered scenes, line IDs, delivery notes, branch nodes with the flags they read and set, camera and switch cues, audio cues and timing. Where this script and the chapter disagree on story, the chapter wins. Where they disagree on execution, this script wins. Binding specs from the chapter are restated here in full.*

**Conventions**
- **Line IDs:** `X08_<SPEAKER>_<nnn>`. Speakers: ELL, RIL, CAL, DEA, CLA, WAY, ROY, MC, JOE, KIT, TUL, EMT, TRP, GRA (Grace, 1973).
- **Cues:**
  - `SW:` switch;
  - `CAM:` camera;
  - `AUD:` audio;
  - `MUS:` band or music;
  - `UI:` HUD or prompt;
  - `SYS:` a system state.
- **Flags** are listed in `17-tracked-state-registry.md`.
- **The switch cue** (`SW_CUE`, bible §11.1) is identical every time it fires:
  - ambience narrows over 8 frames;
  - a one-frame projector-gate stutter;
  - a depth-of-field pull toward the target over 12 frames;
  - the soft double rumble `RMB_SWITCH`;
  - the HUD fades.

  A **failed** switch then holds six frames of the target in focus, gives a second stutter, and snaps back with one hard pulse (`RMB_FAIL`).
- **Clara** (CLA) is recorded and mixed like any person in the room. No processing.

**Flags read here:**
- `observe_lines` (all chapters): whether the notebooks hold a rain line for verse option C. The X M5 arm lines never feed it; they reach no one (X M5).

**Flags set here:**
- `lifted_hand`
- `verse_line_1`, `verse_line_2`, `verse_line_3`
- `home_hold_play_seconds`
- `home_hold_story_band` (derived)
- `wayne_ambulance_meant` (a set of up to 6)
- `wayne_sang`
- `hand_held_seconds`

---

## MISSION 8 — THE LAST LIGHT (7:26–8:22 p.m.)

### 8.1 · INT. STAGE-RIGHT WING — 7:26 P.M.
`CAM:` Wing, behind the black masking. The Vistalite on its rolling riser; through the clear shells, the stage beyond.
`SYS:` Clara present (Ellis's perception only). The help layer is active for Ellis.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_DEA_001 | DEAN | Kick drum. | Grinning. A ritual they mocked in II and did anyway. |

`SW:` Rapid, one per member, each on the kick-drum head. **Dean** gets both palms, "seven weeks today." **Cal:** one hand, two taps. **Riley:** palm, then forehead to the rim for a second. **Ellis** is last, his hand over the pink letter (Carla's, inside the shell).
`CAM (Ellis):` Clara beside him, looking at the pink through the acrylic. She touches nothing.
`CAM:` Across the wing, Joel checks focus behind the white tape. Kit clips the sun-gun cable to her belt and thumbs up to Tully; Tully thumbs up back. Roy stands at the back by the stairs, arms folded.

### 8.2 · EXT. STAGE — 7:30 P.M. — "OUT"
| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_MC_001 | MC | From Hollow Ridge, Georgia... | A Syracuse DJ. He doesn't get to finish. |

`AUD:` The crowd comes up from the whole bowl at once: layered, delayed by distance, rolling back from two miles. It's the largest crowd bed in the game.
`CAM:` The stage faces east. The sun is behind the band, low and gold. Four silhouettes. The valley goes from gold to amber through the set.

### 8.3 · THE SET — THE ROOM AT ITS LARGEST
`SYS:` The crowd model is at maximum size and warm everywhere. Band responsiveness is at maximum. The switching rides band signals: Cal's headstock, Dean's two clicks, Riley's nod, Ellis's turn.
Set list, taped to the deck: LOW WATER · STILL HERE · SUNDAY CLOTHES · TOMORROW PROBLEM · NEW SKIN · SHAPE NOTE · WHO ARE YOU?

**"Low Water" (Cal).** Verb: *lock*. `CAM (Cal):` the mix tower eighty yards out, and Theo at the board.

**"Still Here" (Ellis).** The valley sings verses 1 and 2. Verb: *space*, step back and let the valley sing. `CAM (Ellis):` Clara on the stage-left lip, boots over the edge, backlit.
- Node **N8.3a (optional):** with *attention*, the player finds Wayne at the foot of the mix tower. Wayne lifts one hand.
  - Input *lift hand* sets `lifted_hand = true`. Wayne sees it and puts his hand back in his pocket.
  - No input: `lifted_hand = false`. Wayne's hand goes down on its own.

**"Sunday Clothes" (Riley).** 7:37 p.m.: WLRC carries it live, and Joan hears it in Linwood (offscreen). The player sings Riley's lead. Ellis sings the low harmony.

**"Tomorrow Problem" (Dean).** The valley shouts the chorus. On the last chorus Dean throws one stick.

**"New Skin" (Ellis).** `SYS:` The one visible crack. At verse 2, line 2, the lyric input goes dead for 1.5 bars.
- `SW:` a soft pull to Cal, AI-driven. Cal plays the missing melody high on the bass.
- Ellis re-enters a beat late and laughs into the mic.

  | ID | Speaker | Line | Delivery |
  |---|---|---|---|
  | X08_ELL_010 | ELLIS | (sung) *You'd have hated every word of this.* | The last line of the song, plain. |
  | X08_CLA_010 | CLARA | (laughs, once) | Caught out, like a sister who's been teased back. |

- `CAM:` The sun goes behind the hills during this song. There's no separate beat for it.

**"Shape Note" (all), 8:04 p.m.** `CAM:` The four turn in and face each other across the front of the riser: a hollow square. Ellis's back is to the crowd, and he faces Dean. Riley is at the riser's stage-left corner, Cal at stage right. What's left of the light goes. Blue, then dark blue. The stage lights come up behind them. Lighters appear.
- `MUS:` Nine minutes of drone, with the Sacred Harp tune under it.
- `AUD:` The crowd falls to near-silence, the way a room does.
- `CAM:` In the stage-right wing, Joel taps Kit. She switches on the sun-gun (650 W).
- `CAM (Ellis):` The left side of frame goes white, low and sudden. His body jerks right in a small, hard flinch. His hand stops on the strings for half a beat.
- `MUS:` The band covers it. The crowd doesn't notice.
- `CAM (Riley):` if the player is Riley here, she sees his shoulders go.

  | ID | Speaker | Line | Delivery |
  |---|---|---|---|
  | X08_JOE_001 | JOEL | Kill it, it's flaring. | Technical, low, to Kit. |

- `CAM:` Kit kills the light.

### 8.4 · "WHO ARE YOU?" — VERSES 1–3 AND THE CHANT
`SYS:` The switching slows; the camera stays with Ellis longer each time.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_ELL_020 | ELLIS | (sung) *Who are you, in the jacket that was hers, / on the stairs at the top of the world? / I made a room in the house for you to stay in. / I never asked who'd be living there.* | The fire-tower verse. Plain, forward. |

Verses 2 and 3 are the Knob House lyrics (see the Music team's lyric sheet, "Who Are You?" v3).

`AUD:` The turnaround, then the chant, *EL-LIS, EL-LIS, EL-LIS*: enormous and loving.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_ELL_030 | ELLIS | (on mic, quiet) That's not— I'm not him. | Almost polite. No anguish. The chant rolls over it. |
| X08_ELL_031 | ELLIS | (off mic, to the band) Stay with me. | The band signal. Same read as the first night. |

### 8.5 · THE OPEN VERSE
`MUS:` The changes of LAST V. OPEN. Cal holds the root, Dean drops to a pulse, Riley's twelve-string rings.
`CAM (Ellis):` He drifts downstage to the stage-left lip, toward Clara, facing her and the valley. The yellow rope is at knee height, and the gap is beside the PA wing. The stage-right wing is behind him and far to his right. Joel shoots from there. Kit waits with the light off.
`AUD:` As the verse opens, rain comes up under the band. It's not in the PA; only the player hears it (`AUD_RAIN_MEMORY`, a bed that fades in over 4 s).
`SYS:` The songwriting system, live. Three choice nodes, then a fixed fourth line. No timer beyond the band's bar count; if the player doesn't choose within 4 bars, the band goes around again.

**Node N8.5a — the first line** (sets `verse_line_1`)
| Option | Sung |
|---|---|
| A (default) | *Rain on the roof like somebody counting.* |
| B | *The engine ticking like it had somewhere to be.* |
| C | the player's most recent Observe line with rain in it, from the memo books; hidden if there isn't one |

**Node N8.5b — the second line** (sets `verse_line_2`)
| Option | Sung |
|---|---|
| A (default) | *The oak in your window like a shut door.* |
| B | *The dash light on your hands.* |
| C | *The wipers still going, nobody to stop them.* |

`CAM:` **The cutaway (once).** On the downbeat of line 2, a hard cut to the 1973 car, after the white.
- The frame is dark, and the car is tilted.
- In the passenger window, filling it, the oak's bark. The dash light.
- Grace, pinned between the door and the tree, looking at him.
- `AUD:` Rain on the roof. Under it, Ellis at sixteen (ELL_1973), a run of apology mostly taken by rain. "Sorry" is audible once.

The picture **stays in the car** through line 3.

**Node N8.5c — the third line** (sets `verse_line_3`)
| Option | Sung |
|---|---|
| A (default) | *You laughed, and the rain kept the word.* |
| B | *You were fourteen and tired of me.* |
| C | *I held your hand and it held back.* |

`AUD` under line 3, in the car:
1. `GRA_1973_LAUGH`: a short laugh that hurts her. A word is inside it, masked by rain at -6 dB. It must never be intelligible.
2. `ELL_1973_STAY`: *Stay with me.* Clear. The only clean line.
3. `GRA_1973_OKAY_GOON`: *It's okay.* and *Go on.* recorded separately and overlapped by about 300 ms, low.

**Line 4 (fixed).** `UI:` one phrasing on screen, *Go on.* The player's input sings it. It's timed so the "Go" syllable lands on Grace's "Go" in the memory.
`CAM:` Hard cut back to the stage.
`CAM (Ellis):` Clara, at the lip, with her hand over her mouth.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_ELL_040 | ELLIS | (sung) *Go on.* | Plain. A little behind the beat. Not pretty. |

`AUD:` The rain memory bed fades over 2 s. The valley is quiet again.

### 8.6 · CLARA
`CAM (Ellis):` Clara on the lip, looking up at him. She says nothing. Behind him, the band goes around.
`SYS:` **The help layer is off.** No Clara line, no hint, no nudge of any kind until the end of the mission.

### 8.7 · HOME
`UI:` The HOME prompt, the same size and type as every HOME since II.

**Binding UX spec**
- The prompt never pulses, blinks, grows, rumbles or repeats. There is no idle reminder.
- `MUS:` The vamp loops indefinitely. There are at least 12 authored variations per player, band-driven: Cal moves the root, Dean shifts the pulse, Riley finds new voicings.
- Fatigue animations escalate to a plateau at play-time 180 s and hold. They include:
  - Cal's hand cramping on the root;
  - Dean mouthing *Blake*;
  - Riley's top note cracking on the 12th pass;
  - lighters, and stars over the hills.
- `CAM (Ellis):` Clara doesn't move and doesn't speak.
- **Accessibility.** A toggle mode: press once to "hold off," press again to press HOME.
- `SYS:` `home_hold_play_seconds` counts real time from the prompt's appearance to the press.
  - Derived value `home_hold_story_band`: `<60 s` → `under_a_minute`; `60–150 s` → `about_two`; `>150 s` → `almost_three`.
  - The world clock advances by `min(play_seconds, 180)`.

### 8.8 · THE TURN — THE SONG LANDS
On the press:

`CAM (Ellis):` He turns all the way around to face Dean.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_DEA_040 | DEAN | (no line; grins, both sticks up, two clicks) | *Hold.* |

- `MUS:` The last chord, all four together, and cut.
- `AUD:` 1.0 s of room silence ("the right kind"). No music, no crowd yet.
- `CAM (Ellis):` Riley is ahead of him and a little to his left, ten yards off. **Blocking:** she stands a step stage-right of the riser's stage-left corner. Glasses, hand out, open.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X08_ELL_050 | ELLIS | (laughs) | A real laugh. He got the verse. |

- `CAM (Ellis):` He steps toward her.
- `AUD:` The valley comes up. Full crowd bed, all at once.
- `CAM (objective, 18 frames, from the stage-right wing):` Joel steps out onto the upstage-right deck for the reverse on the bow. Kit steps out with him, raises the sun-gun, and switches it on.

**THE FALL. Binding audio, light and camera spec.**
- **Real time.** About 2.5 s from switch-on to black. No slow motion, no freeze.
- **No score.** The only sounds: the crowd, the last chord's ring-out, his boot on the deck, the rope, the Jazzmaster's feedback. Nobody screams.
- **Light.** The sun-gun's cold white. No gold, no bloom, no flattering flare.
- **Camera.** In his eyes at handheld height. Never cut to a wide shot or to the crowd.
- **Frames, and only these:**
  1. White on the left, with Riley's hand in it. The light comes about 15° left of his eyeline, past her shoulder.
  2. The swerve right.
  3. His right foot comes down on nothing past the deck edge.
  4. The yellow rope catches behind his knee.
  5. Stage lights slide up the frame.
  6. Scaffold pipe.
  7. Black.
- `AUD:` The Jazzmaster, still on its strap, passes the stage-left PA stack and feeds back through the whole system. At the mix tower, Theo pulls the guitar channel down at a real fader speed (about 1 s). Then silence.
- The crowd is still cheering at black.

---

## MISSION 9 — THE GAP (8:22–9:52 p.m.)

### 9.1 · BLACK — THE SWITCH FAILS
`SW:` `SW_CUE` toward Ellis → failed (six frames with no one in them, a second stutter, snap-back to black, `RMB_FAIL`). `SW:` `SW_CUE` toward the stage-left lip → failed. `SW:` lands on a machine.

### 9.2 · ROLL FORTY — JOEL'S VIEWFINDER
- `CAM:` 16mm, color, grain, the shoulder bob. Sync sound is thin: the PA through a small mic. No player control.
- The objective break (the third in the game).
- **Footage:**
  1. The young man in the leather jacket and the ELLIS shirt walks to the stage-left lip and sings to an empty corner.
  2. On line 2 of the verse, he lifts a hand toward nothing.
  3. The band follows. The girl with the twelve-string is at the riser corner with her hand coming out.
  4. **The hold.** Duration by `home_hold_story_band`: `under_a_minute` → 40 s; `about_two` → 110 s; `almost_three` → 170 s. The footage runs at that length as a montage of real-time fragments cut with jump cuts, as the film magazine allowed.
  5. He turns. The drummer's sticks go up. A clean stop. The boy laughs and steps toward the girl.
  6. The frame flares white (the sun-gun beside the lens), then recovers.
  7. The stage-left end is empty. The rope swings. The girl's hand is still out.
- The camera keeps rolling.

### 9.3 · RILEY — THE ROPE
`SW:` lands on Riley. `SYS:` Movement only. No help, no prompts except one line input.
- `CAM (Riley):` She runs ten yards to the edge and drops to her knees at the rope. Below: the gap, a yard wide and twelve feet deep, lit by stage spill. The Jazzmaster lies face down. Ellis is on his back half under a crossbar, one leg folded wrong, eyes closed.
- Tully is already at the bottom, hands either side of Ellis's head, holding it still.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X09_RIL_001 | RILEY | Ellis. | Her only line. The player triggers it. Not a scream: his name, to see if he answers. |

- `AUD:` The PA hums with the dead guitar. Then the crowd, thinking it's an encore break, starts *EL-LIS* again.

### 9.4 · CAL — THE LIST
`SW:` lands on Cal, standing over Riley. `SYS:` A practical task list; each task is one input, fast.
1. Take off the bass. It hums on the deck.
2. The stage manager.

   | ID | Speaker | Line | Delivery |
   |---|---|---|---|
   | X09_CAL_001 | CAL | Medical. Now. Stage left, under. | Low, exact. |

3. The MC.

   | ID | Speaker | Line | Delivery |
   |---|---|---|---|
   | X09_MC_001 | MC | Folks, we need everybody to stay where you are. Stay where you are, please. Stay calm. | Frightened professional. |

4. The path. Down the stage-right stairs past Roy, who says *what happened, what happened*, under the stage through the scaffold, to the stage-left end.
5. The flashlight. The EMT hands it to him; he holds it on Ellis's face. Input *Hold still*: the beam must stay on the face. Drift is allowed but corrected automatically. No fail state.

- `AUD:` The EMT, off: *Don't move him. Don't move him. Get me the collar.*
- `SYS:` The extraction takes forty minutes of story time. Play time is compressed to about 90 s across tasks.
- `CAM (Cal):` Riley at the rope above. Theo at the top of the mix tower, hands on his head.

### 9.5 · DEAN — THE HAND
`SW:` lands on Dean at Ellis's right hand. `UI:` *Hold.*

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X09_DEA_001 | DEAN | Hey. Hey, Blake. Blake. You're all right. You're okay. They've got you. Tully's got you. Hey. I owe you four dollars. You hear me? Starlite. November second. I owe you four dollars and you didn't let me pay it, so you can't— you don't get to— I owe you four dollars. Don't you dare. | Fast, looping, funny until it isn't. Record at least three full takes; the system can extend by looping phrases while the player holds. |

- `CAM:` Log-roll onto the backboard: the collar, the straps, six lifters. Dean walks beside the board holding the hand.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X09_EMT_001 | EMT (male) | You have to let go now, we have to go. | Kind, firm. |

- `SYS:` Dean's hand releases automatically on this line.
- `CAM (Dean):` He stands in the compound lights with his hand flat over his shirt pocket (the Polaroid).

### 9.6 · KIT — THE CASE
- `CAM (Dean):` Passing the film truck: Kit on an equipment case, the sun-gun in her lap and ticking as it cools, her hands shaking. Joel holds the camera, not rolling.
- Dean doesn't stop. The player may look.
- `CAM:` Later: Tully sits beside her and moves the sun-gun off her lap to his other side. No dialogue.

### 9.7 · THE GATE
- `CAM (Dean):` The ambulance at the compound gate, lights red on the mud. Wayne, muddy to the waist, pass in his fist, has been arguing with a trooper for half an hour.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X09_WAY_001 | WAYNE | That's my son. | Not loud. The tenth time he's said it. |
| X09_TRP_001 | TROOPER | Sir, I need you to— | |
| X09_ROY_001 | ROY | THAT'S HIS DADDY. LET HIM THROUGH. | The only time Roy raises his voice in the game. |
| X09_EMT_010 | EMT (Doreen) | Family? | |
| X09_WAY_002 | WAYNE | His daddy. | |
| X09_EMT_011 | EMT (Doreen) | Get in. | |

### 9.8 · THE SWITCH LANDS ON WAYNE
`SW:` `SW_CUE` from Dean to Wayne climbing in. **It lands.** This is the first time the player controls Wayne.
`SYS:` Wayne's locomotion: heavy, slow, two-stage rise, stiff knees. The camera moves as he moves.

### 9.9 · INT. AMBULANCE — ROUTE 14 SOUTH
- `CAM:` Two stretchers wide. Doreen on the jump seat with the bag. The siren. Lights turning on the ceiling. Ellis on the backboard: collar, mask fogging and clearing, the ELLIS shirt, blue ink on his wrist.
- `UI:` *Hold his hand.* Sets `hand_held_seconds` while held.
- `CAM:` Free look: his face, Doreen at the monitor, the rear windows, the yellow line going away.

**Node N9.9 — what Wayne means.** Repeatable. The player picks meanings, and each can be picked once. Sets `wayne_ambulance_meant` and `wayne_sang`.

| Option (the player sees) | What Wayne says | ID | Delivery |
|---|---|---|---|
| "It wasn't your fault." | It wasn't your— | X09_WAY_010 | Stops because his throat stops. He doesn't try again. |
| "I'm proud of you." | You done good up there. | X09_WAY_011 | Flat, like a report on a job. |
| "I'm scared." | Son. | X09_WAY_012 | Barely out. |
| "Son." | Son. | X09_WAY_013 | The only one he gets all the way through. |
| Sing | (hums the bass line of "Wondrous Love," no words) | X09_WAY_014 | Big rough voice, half a beat behind, sure of every note, almost under the siren. |
| Silence | (nothing) | — | He holds the hand. |

- `AUD:` No music under any of it. Doreen looks out the side window when he speaks.
- `CAM:` His thumb moves on the back of his son's hand.
- `SYS:` No cut. The ride runs as long as the player stays: 40 minutes of story time, with play time governed by input and a minimum of 3 minutes before 9.10 can trigger.

### 9.10 · 9:52
`UI:` SATURDAY · AUGUST 28 · 9:52 P.M. The date shows only on days somebody says it aloud.
- `CAM:` The mask stops fogging. Doreen leans in and works: hands and the bag, for about 60 s of play. She stops and sits back, and puts her hand on Wayne's arm.

| ID | Speaker | Line | Delivery |
|---|---|---|---|
| X09_EMT_020 | EMT (Doreen) | Sir. | That's all. |

- `AUD:` The driver switches off the siren. The lights keep turning. The ambulance slows to the limit and keeps going.
- `UI:` No prompt to let go.

### 9.11 · THE CAMERA
- **Trigger:** the player releases the hand, or 180 s pass with no input after 9.10.
- `SW:` `SW_CUE` leaves Wayne → reaches → fails. Again → fails. A third time: there's no target, the stutter doesn't resolve, and the picture goes to black mid-search.
- `UI:` CHAPTER X COMPLETE · THE LAST LIGHT

---

## Performance and recording notes
- **The open verse:** recorded live with the band vamping. Pick a take with a real crack in it (`18-performance-and-direction.md` §2, §4).
- **Grace (1973):** a 13–14-year-old actor, recorded in a car shell with a rain machine. Record the laugh, "Stay with me" (Ellis, 16) and "It's okay" / "Go on" as separate stems.
- **Wayne's ambulance lines:** record each at least five times and select the least performed. The actor must not cry.
- **Clara:** she has no lines in 8.6–8.8. Her silence is the performance: a hand over her mouth, then looking at him.
