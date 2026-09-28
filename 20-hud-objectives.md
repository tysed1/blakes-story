# THE BLAKES: HUD Objective List

*Deliverable 20 (V8 production supplement). Every objective string the HUD shows, mission by mission, from Chapter I's cold open to the coda, where each one appears and clears, and every stretch where the line stays empty and why. §1 is the UX spec for the line.*

**How it relates to the bible and the registry.** Bible §11.8 limits the HUD to three things: the day of the week, "a single plain objective when there is one," and input prompts. It makes Clara the only voice that tells the player where to go or what to look at. The objective line is the one part of that HUD that carries direction, so it's the easiest place to break the rule, and this file is its source of truth. The line reads no flag: `17-tracked-state-registry.md` §1 says nothing on screen names, counts or scores a flag, and no string here does. Where a mission branches, every branch gets the same string, so no string depends on registry state. Where a chapter implies guidance that isn't Clara, the objective or the band's signals, §6 quotes it and proposes a fix. This file changes no chapter.

---

## 1. The objective line (UX spec)

**Where it sits and how it looks.** The same all game.
- Top-left corner, inside title-safe, on the line directly under the day of the week (I CO: "in the top corner, small"). Left-aligned with the day.
- The day's typeface, size and color: a plain sans serif with no period dressing, regular weight, all capitals. Cap height about 2% of screen height (about 22 px at 1080p). Off-white at 85% opacity, with a soft 1 px shadow for bright scenes. No box, plate, icon, bullet, checkbox, number or color code.
- One line, one objective. Never two, never a list, never a count ("2 OF 4").
- The HUD text-size option scales the day and the objective together.
- Input prompts sit bottom center, in their own place and their own size (X M8's binding spec: HOME is "the same size and type as every HOME since Chapter II"). A prompt never sits on the objective line, and the objective line never shows a button. That keeps *home* (a prompt) and GO HOME (the objective) apart on screen.

**How it behaves.**
- It fades in over 0.8 s and out over 0.8 s. No sound, rumble, slide, pulse, blink, glow, color change or tick. Between two objectives: out, one second of nothing, in.
- A finished objective fades. Nothing says it was finished.
- No timer, distance, arrow, compass, minimap, pin or route line, and nothing in the world lights up to match it. A destination is findable because it's a named place on a map of named places, or because a character's life runs there.
- It never comes back as a reminder after idle time, never repeats, and has no log. The notebook isn't a quest log.
- In a switch the line fades with the HUD (bible §11.1) and returns with the new character's objective, or stays empty. In a failed switch (VIII M4, VIII M10, IX M1, X M9) it comes back at once with the HUD, because the chapter has the HUD come "back all at once."
- It hides while the Room is running (a set, a take, a jam, a rehearsal): the Room has "no score, no meter" (§11.2). A performance objective (PLAY THE SET) clears on the count-in. Any other objective still standing returns when the music stops.
- It hides wherever a chapter makes a prompt the only thing on screen (V M16 *Hold*; VIII M6 *Make her stop*; IX M6 *Look at her*), and during cutscenes and documentary footage.

**Markers.** The game has none. The chapters mention a marker only to rule one out: I M9 ("There's no urgency and no marker"), II M5 ("it has no objective marker"), VII M7 ("No destination is marked"; see §6), VII M9 ("It isn't marked"), VII M13 ("No waypoint, only Clara"), VIII M14 ("No destination marker"; the script: "No objective and no marker") and the coda ("There's no quest marker"). The map shows roads and places and nothing else.

**What a string can be.**
- Capitals, plain, one to five words: a destination (DRIVE TO VALE MUSIC) or a task (OPEN THE STORE). On the medication a landmark in parentheses may follow (§4).
- Never how to feel, how to play or what to notice. Never advice or a hint. Never Clara's words or a line anybody says in the scene. Never the name of Clara, the switch, the Room, Observe or any other system.
- No GO, HOME or "go home" anywhere but the coda at dusk. The verbs are GET TO, DRIVE TO, FIND, MEET, PLAY and plain task verbs.
- The Blake house is COLD BRANCH ROAD on the line, every time. The first objective in the game is DRIVE TO COLD BRANCH ROAD (I M1), and the last is GO HOME. The HUD doesn't call the house home until the coda.
- Nothing near Ellis in Chapter X may read as a send-off (Clara's Rule 10, and Roy's "Go on. Get up there." at the stairs). From X M3 to the coda's dusk the line stays empty. The last objective before GO HOME is X M2's FIND WAYNE AND ROY.
- Flat and period-neutral. Strings recur when the task recurs (FIND DEAN three times; GET TO LANDRY'S OFFICE five times).

**When there's an objective.** When the player has somewhere to be that the scene doesn't carry them to, or a job that frames the mission. It matters most where nothing else guides: as Riley, Cal or Dean, with Wayne in the room, in a car without Clara, and on the medication. The line stays empty in the Room, in conversations, in free roam, in memories with one input, wherever a chapter says there's no marker or objective, and wherever Clara is already giving the direction, because the line never repeats her.

---

## 2. How to read the table

- **Mission:** number and title. CO is the cold open.
- **Playable:** from the mission header.
- **Objective string(s):** exactly as on screen, in order, joined by →. Where the playable character changes, each character's strings follow their name, separated by ·. "none" means the line is empty for that stretch.
- **Appears and clears:** brief. For a mission with no objective, the reason.

---

## 3. The objectives

### Chapter I · Before the Noise

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO | nobody, then Ellis on the stool | none | Control arrives with "no tutorial card and no title"; the HUD fades up with THURSDAY only. |
| M1 The Gig | Ellis | DRIVE TO COLD BRANCH ROAD | Empty on the stool, through the three songs and in the alley. Appears when the Valiant starts on Depot Street; clears in the Blake yard. Wandering doesn't change it. The first objective in the game. |
| M2 What Things Cost | Ellis | GET TO ROY'S → DRIVE TO TANNERSVILLE COLLEGE | GET TO ROY'S when he takes his keys off the hook; clears at the bay. The garage loop and payday: none (Roy hands out the jobs; the money screen is the notebook's back page). DRIVE TO TANNERSVILLE COLLEGE when Roy throws him the truck keys; clears behind the science building. Campus: none. |
| M3 The Long Way Around | Riley | GET TO LANDRY'S SEMINAR | Appears after the argument under the oak, with campus left free; clears at the seminar table. Her room, the hall phone and the walk at dusk: none. |
| M4 Good Family | Dean | DRIVE TO BELLE GROVE → GET TO THE PARTY → GET TO THE CHEVELLE → LOSE THE CRUISER → DRIVE TO VALE MUSIC | BELLE GROVE from the faculty lot; clears in the Holloway drive. Dinner and the basement: none. THE PARTY out the back door; clears at the farmhouse. The party: none. THE CHEVELLE when the blue lights come up the drive; clears at the car in the tree line. THE CRUISER as he pulls out; clears when the cruiser passes the quarry turnoff. VALE MUSIC after the pay-phone call; clears at the steel door. |
| M5 Everything Has a Reason | Cal | FIX THE AMPLIFIER | At the bench; clears at the hum. Mr. Vale, Mercer Radio & TV, the Blue Moon set (the Room), the pay and Monday: none. |
| M6 Four Strangers | Cal → Riley → Dean | Cal: FIX THE HOUSE AMP · Riley: none · Dean: none | Cal's as the mission opens; clears when he finds the ground fault, or at the switch to Riley. Riley's stretch is free (pool, the jukebox, the Silvertone). Dean's is free until Marlon's phone call. |
| M7 Fifteen Minutes | Dean → Cal → Riley → Ellis | none | The back-room jam is the Room from the first count. |
| M8 One More Song | Ellis → Dean → Cal → Riley | none | The set starts as the mission opens; the alley pairings are free. |
| M9 Home | Ellis | none | The text: "There's no urgency and no marker." Wayne, the door, Stony Knob and the deputy come to him, and no string may name home. |

### Chapter II · Second Verse

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| M1 Circulation | Riley | RESHELVE THE CART | At the desk after Mrs. Voorhees's line; clears when Hannah comes in with the doughnuts. The phone and Dean on the bench: none (the bench prompt fades if the player waits). |
| M2 Four Calls | Dean | FIND THE BOOT → DRIVE TO VALE MUSIC → FIND ELLIS → CALL MARLON'S | The chapter calls this "Dean's objective" (Riley done, three to go). THE BOOT when he wakes on the bench; clears when it's on his foot. VALE MUSIC off the plinth; clears at the bell. FIND ELLIS out of Vale's; clears at Roy's bay. CALL MARLON'S once Ellis has heard; clears when Dean hangs up. |
| M3 Half a Tire | Ellis | DRIVE TO COLD BRANCH ROAD → CHANGE THE TIRE | The garage: none. COLD BRANCH ROAD when Dean has gone and Roy is back under the hood; clears in the yard. Wayne at the fence: none. CHANGE THE TIRE at dusk; clears when the bald tire goes in the trunk. |
| M4 Rules | Ellis → Cal → Riley → Dean | Ellis: GET TO MARLON'S · Cal: none · Riley: none · Dean: none | Ellis's as Sunday morning opens; clears at the front door at 10:02. The rehearsal, "Kick with me," the second verse and "Low Water" are the Room. The booth and the back steps: none. |
| M5 Thursday | Ellis | none | The text: "it has no objective marker." Driving away and going in are both complete. The prompts are Sit, Watch and Leave. |
| M6 Professional Musicians | Cal → Ellis → Riley → Dean | Cal: DRIVE TO TANNERSVILLE MOTOR SALES → PLAY THE SET · Ellis: none · Riley: none · Dean: none · Cal: FIND DEAN | MOTOR SALES at Vale's on Saturday morning; clears on the lot. PLAY THE SET on the flatbed; clears at the count-in, and the rotation is the Room. Ellis's break: none. FIND DEAN when Cal is sent after him; clears behind the service building. The money: none. |
| M7 The Long Way Home | Riley → Ellis | Riley: GET TO LANDRY'S LECTURE · Ellis: none | Riley's after "I've got Landry at eleven"; clears in the back row. The tour and the quad: none (the text: "No mission objective"). Ellis, after the camera stays: none. |
| M8 Second Friday | rotating | Ellis: PLAY THE SET | On the sidewalk under the sign; clears at the count-in. After the set: none. |
| M9 Four in the Morning | rotating (conversation) | none | The text: "Nothing to perform and nothing to win." |
| M10 The Hallway | Ellis | DRIVE TO COLD BRANCH ROAD | In the Starlite lot; clears in the yard. There's no Clara in the car, so the line carries the drive. The door, the frame and bed: none. |

### Chapter III · Signal

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO | nobody, then Cal | none | Radios and a tape; control arrives with M1. |
| M1 Tape | Cal | OPEN THE STORE | The chapter's own words: "Cal's first objective is mundane: open the store." Appears as control arrives; clears when the lights, cases, register and demonstration amp are done. The tape and Riley: none. |
| M2 Borrowed Time | Riley | GET TO LANDRY'S OFFICE → GET TO WTCR | OFFICE on Election Day; clears at his door. The hall phone: none. WTCR on Monday night; clears at the production room at 11:50. The session, including the stretches as Cal, Dean and Ellis: none (takes are the Room). |
| M3 Dead Air | Ellis → Riley → Dean → Cal → Ellis | Ellis: DRIVE TO COLD BRANCH ROAD → MEET ROY AT THE GARAGE → TUNE IN WTCR · Riley: none · Dean: none · Cal: none · Ellis: DRIVE TO COLD BRANCH ROAD | The garage afternoon: none. COLD BRANCH ROAD at six; clears at the kitchen table. MEET ROY after supper; clears when Roy's pickup pulls in at ten. TUNE IN WTCR as the truck climbs; clears when Martin's voice comes through. Each relay stop is one radio: none. COLD BRANCH ROAD again when Roy drops him at the garage; clears in the yard. |
| M4 Out of Town | Dean → Cal | Dean: DRIVE TO VALE MUSIC · Dean: none · Cal: DRIVE TO THE BLIND TIGER | Dean's on Friday with the contract form; clears at the bell. Saturday he rides in the passenger seat: none. Cal's at the city-limit sign when Ellis climbs in; clears on Tenth Street. |
| M5 Strangers | rotating | SOUNDCHECK → PLAY THE SET | SOUNDCHECK after the headliner's greeting; clears when the house engineer's check ends. PLAY THE SET then; clears at the count-in. After, the money and the invitation: none. |
| M6 The Farmhouse | Dean → Cal → Riley → Ellis | none | A party: "There is no menu. The game follows whoever matters." Ellis's walk is free; Cal's horn at the van is the only call. |
| M7 Night Road | Cal → Ellis | Cal: DRIVE TO COLD BRANCH ROAD · Ellis: none | Cal's as the van leaves the farm; clears at the switch to Ellis in the mirror. Ellis rides in the back; the drop-off and Wayne on the porch: none. |
| M8 Something Wrong | Cal | none | A duet in Vale's back room; the Room. |
| M9 Demand | Riley → Dean → Cal → Ellis | Riley: GET TO VALE MUSIC · Dean: GET TO VALE MUSIC · Cal: DRIVE TO MARLON'S · Ellis: none | Riley's when she reads the letter on the stairs. The line passes with the letter: Riley's clears when Dean takes it, Dean's when Cal reads it, Cal's when Ellis walks in for Friday's rehearsal. Ellis reads it: none. |
| M10 Thanksgiving | Ellis | none | Wayne drives; the diner and the ballgame are small things at a booth. |
| M11 Signal | rotating | PLAY THE SET | At the stage while Dean tapes the letter to the kick drum; clears at the count-in. After and the walk out: none. |

### Chapter IV · Momentum

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO | nobody | none | A tape machine and a title card. |
| M1 Eight Hours | Cal (switches to Ellis, Dean, Riley) | Cal: SET UP THE GEAR → RECORD THREE SONGS · Ellis: none · Dean: none · Riley: none | GEAR at 9:00; clears when the first run starts. THREE SONGS after the first playback; hides in every take; clears when Hoyt hands Cal the master. The Echoplex, the loud part, the overdub and the writing scene are the Room and the songwriting system: none. |
| M2 Five Hundred Copies | Riley | FIND $300 → GET TO TANNER CUSTOM RECORDS → STAMP THE SLEEVES | $300 after Cal's arithmetic ($112 of $412); clears when Marlon pushes the money across the bar. TANNER CUSTOM RECORDS leaving Marlon's; clears at the label form. STAMP THE SLEEVES when the rubber stamp comes back from River Street; clears at the last sleeve. |
| M3 Four Hundred Dollars and a Terrible Idea | Dean (Ellis for the haggle) | Dean: FIND A VAN · Ellis: BUY THE ECONOLINE → OUTFIT THE VAN · Dean: GET TO THE PURE OIL | FIND A VAN at Marlon's bar over the circled ads; holds across the four stops; clears at Otis Crump's. BUY THE ECONOLINE at the stutter to Ellis; clears when the price closes ($400 to $475), or at $475 if it never does. OUTFIT THE VAN in Marlon's lot; clears when the racks are in. Dean's stolen drive: none until the cow, then GET TO THE PURE OIL; clears at the pump where Cal is waiting. |
| M4 Three Towns | Cal → Riley → Ellis → rotating; Dean at the Starlite | Cal: LOAD THE VAN → DRIVE TO THE HOLLER HOUSE → PLAY THE SET → LOAD THE VAN → DRIVE TO TANNERSVILLE · Ellis: PATCH THE HOSE · Cal: FIND A MOTEL · Riley: none · Ellis: none · rotating: PLAY THE SET · PLAY THE SET · Dean: none | LOAD THE VAN at 6 p.m.; clears at the doors. HOLLER HOUSE clears in its lot; PLAY THE SET at the count-in. LOAD THE VAN again in the rain. TANNERSVILLE on the Tanner Valley road, until the van overheats. At the roadside Cal's stretch is empty; Ellis's PATCH THE HOSE clears when the tape is on. FIND A MOTEL after Mr. Gentry's hose; clears at the Tanner Valley Motor Court. Room 12 and the ice machine: none. Saturday's two shows (the ballroom; Tenth Street) each get PLAY THE SET, cleared at the count-in. The afterparty, the walkway and Dean at the Starlite: none. |
| M5 Monday | Riley → Dean → Cal → Ellis | Riley: GET TO THE FINAL · Dean: DRIVE TO BELLE GROVE · Cal: OPEN THE STORE · Ellis: DRIVE TO COLD BRANCH ROAD | Each appears at its switch. Riley's clears at the exam-room door, Dean's in the Holloway drive, Cal's when Vale's is open. Ellis's appears when he leaves Vale's with the strings and clears at the kitchen door at six. |
| M6 The Girl Nobody Knows | Cal → Ellis | none | A work session at a table, and the back step. |
| M7 Demand, Again | Dean → Cal | Dean: DRIVE TO TENTH STREET RECORDS · Cal: none | Dean's when he takes the ten copies; clears at Mitch's counter. Cal's walk down the Row and Wednesday's two calls: none. |
| M8 Thursday | rotating | Riley: GET TO LANDRY'S OFFICE · Dean: none · Cal: none · Ellis: PACK FOR LAUREL CITY · Cal: SOUNDCHECK · Ellis: PLAY THE SET | Riley's clears in the office. Dean in the front hall and Cal at Vale's: none. PACK at three in Ellis's room; clears when he takes Loretta and the bag. The drive (Cal at the wheel): none. SOUNDCHECK at the loading dock after Eddie; clears when Theo hands Cal the matchbook. PLAY THE SET in the backstage hallway; clears when Ellis walks into the light. The show, the city after midnight (free roam), the lot and the drive: none. |
| M9 The Wall | Ellis | CLEAN THE GUTTER | The wall has no right answer: none. The string appears when Wayne shuts the door; clears when Ellis comes down the ladder. |
| M10 Something Good | Riley; Ellis on the drive back | Riley: none · Ellis: DRIVE TO COLD BRANCH ROAD | Riley's night is the phone, the practice room and the wait ("the game doesn't say so"): none. The drive back at two-thirty is Ellis's, with "No Clara in the car"; it clears in the yard. |
| M11 Ledger | Cal → Ellis | Cal: BALANCE THE LEDGER · Ellis: none | Cal's at the counter; clears when the page totals. Ellis under the Chevrolet: none. |

### Chapter V · Velocity

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO | Ellis | none | The text: "The HUD, if the player looks: FRIDAY." It's M9's hallway, three months early. |
| M1 Christmas Eve | Dean → Ellis | Dean: none · Ellis: DRIVE TO COLD BRANCH ROAD | Dean works a party: none. Ellis's at the Valiant in the Holloway drive; clears in the yard. The kitchen (Wayne) and midnight: none. |
| M1b Saturday Bach | Riley | DRIVE TO LINWOOD PRESBYTERIAN | When she takes the Datsun keys off the hook; clears at the side door. Listening, the verse and the Datsun's options: none. |
| M2 Lettering | Riley | DRIVE TO MARLON'S → PAINT THE REAR DOORS | The gallery: none. MARLON'S after the vote; clears in Marlon's lot. REAR DOORS when she takes the brush from Dean; clears when the second door is lettered. |
| M3 Six Dates | Cal | DRIVE TO CHATTANOOGA → PLAY THE SET → FIND DEAN | CHATTANOOGA in the alley behind Vale's; holds through the band's detours; clears at the Hi-Fi. PLAY THE SET clears at the count-in. The autograph: none. FIND DEAN at load-out; clears in the headliner's dressing room. Outside and the Krystal: none. |
| M4 Dial | Dean → Ellis | Dean: DRIVE TO KNOXVILLE · Ellis: none → PLAY THE SET | Dean's when he takes the wheel; clears at the switch. Ellis on the wheel well: none. PLAY THE SET in the Knoxville bar; clears at the count-in. |
| M5 Two Cars | Ellis ‖ Riley | Ellis: DRIVE TO HOLLOW RIDGE · Riley: none · Riley: GET TO THE EXAM | Ellis's as the van leaves the Birmingham lot. Clara stays under the back-door light, so the line carries the night; it holds through the switches and clears when Dean takes the wheel at the pull-off. Riley rides in the Datsun: none. GET TO THE EXAM at 8:52 in the lot; clears at her desk. |
| M6 The Kitchen Table | Dean | none | The table is waiting when he comes in. Downstairs, "The player has no choice here." |
| M7 Still Here | Ellis → Riley | none | The room at 1 a.m., the kitchen (Wayne), the songwriting system, the rehearsal and the back step. |
| M8 Sold Out | rotating | PLAY THE SET | The interview: none. Appears after Denise's last question; clears at the count-in. |
| M9 The Exit | rotating | none | The cold open showed this hallway with FRIDAY alone on the HUD, so the line stays empty all night. |
| M10 Opening Day | Ellis | none | Wayne drives both ways; the ballgame is free. SATURDAY · APRIL 12 is the HUD's only text. |
| M11 Choosing | Riley | GET TO LANDRY'S OFFICE | Clears in his office. Hannah, the drawer and the van: none. |
| M12 Saigon | Cal → Dean | Cal: FIND DEAN · Dean: none | Cal's at four, when soundcheck starts without Dean; clears at the van in the loading lot. The fight and the show: none. Dean in the motel: *Stay* is the only input. |
| M13 Consequences | Riley → Dean → Cal → Ellis | Riley: GET TO LANDRY'S OFFICE · Dean: none · Cal: none · Ellis: none | Riley's clears in the office. The other three open where their scenes are. |
| M14 Southern Star | rotating | DRIVE TO LINDEN STREET | The card at Marlon's: none. Appears at the van on Thursday; clears on the Southern Star porch. The offer and the sidewalk: none. |
| M15 Four Hands | rotating (conversation) | none | Rain on the van roof, and a promise. |
| M16 Where Did We Meet? | Ellis | none | The script's UI is FRIDAY, then SATURDAY at midnight, and nothing else; the *Hold* prompt clears even the day. |

### Chapter VI · The Other Side of the Glass

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO | Ellis | none | A take at Dalton Sound; Clara's raised finger is the help. |
| M1 Don't Tell Them | Ellis | none | Riley's horn in the yard is the cue; the ride is a passenger's. |
| M2 Fine Print | Dean | none | The dining room; the lesson lets the player pick clauses. |
| M3 Sign Here | Cal | none | The parlor, the signing and the vignettes. |
| M4 Transmission | Ellis | none | A garage day that turns into Roy's closet and the glide. |
| M5 Two Worlds | Riley | GET TO LANDRY'S OFFICE → MAIL THE LETTER → GET TO THE WESTERN UNION | OFFICE on the last day; clears at his desk. The letter's drafts: none. MAIL THE LETTER when she signs; clears at the campus mailbox. WESTERN UNION at the slot; clears at the River Street counter. The hall phone: none. |
| M6 Dalton Sound | rotating | none | A first day: Frank's cards on the pews, takes, playback. |
| M7 2:13 A.M. | Dean | none | The take (the Room), the side porch, the Starlite. |
| M8 Sunday Morning | Cal → Riley | none | The text: in the apartment "nothing is urgent." The Blind Tiger and Tuesday: none. |
| M9 Pasture | Riley → Ellis → Riley → Ellis | none | A party. From Riley's side the text says "Nobody tells her where to look." |
| M10 The Field | Ellis ‖ Riley | none | A conversation in the grass. |
| M11 Afterimage | Ellis | none | A morning on a couch. |
| M12 Bloodline | Ellis | none | Wayne in the yard. |
| M13 Side B | Ellis → Riley → Cal | none | A studio sandbox, an arrangement argument, a playback. |
| M14 Visitor | Ellis | none | Wayne in the parlor; the lot. |
| M14b Pay Phone | Cal | none | Three minutes that open at the phone, with the call already written on a work order. |
| M15 Coupon 29 | Ellis | none | The coupon book and one prompt; the mission waits. |
| M16 Marlon's | Cal | none | Hold or speak, at the bar. |
| M17 Final Playback | rotating | none | Fragments, then the playback. |
| M18 The Glass | Ellis → Riley | none | The glass. Riley can leave or walk to it. |

### Chapter VII · Strangers Know Your Name

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO | Ellis | none | The only input is Ellis's gaze; the frame freezes before the shutter. |
| M1 Nineteen | Ellis | GET TO MARLON'S | Monday's box: none. Appears on Sunday after Dean's call about a rehearsal; clears at Marlon's back door at two. The party (a clock on the wall), the speech and the alley: none. |
| M2 Release Day | Dean → Riley → Cal → Ellis | none | Four shifts of waiting for a stranger to buy the record. |
| M3 Registration | Riley | GET TO THE GYM | When she signs the form in the car; clears at the P-through-S table. The line never names the form, so her decision stays hers. Landry, Sunday dinner and the piano: none. |
| M4 Occasionally Astonishing | Riley | none | A passenger with a folder of clippings; the vote by pay phone. |
| M5 Last Shift | Ellis | none | The last half-day of jobs; Floyd at the pumps (Clara's help); the shirt. |
| M6 11:47 P.M. | Cal → relay → Ellis | none | A song carries the camera; the phone, the truck and the couch are prompts. |
| M7 Where's Ellis? | Cal → Ellis → Cal | Cal: FIND ELLIS · Ellis: none · Cal: none | Walking the building: none. FIND ELLIS at "Keep him busy"; holds through the pawnshop, the peanut stand and the overpass; clears at the switch in the grandstand at Engineers Park. Ellis, with Clara two seats down: none. Cal's ride back: none. |
| M8 Sixteen Hundred | all four | PLAY THE SET | In the dressing room at 8:25; clears at the kick drum in the dark. The show, the stage door, the interviews and the money: none. |
| M9 East Slope *(optional)* | Ellis | none | The text: "It isn't marked." Clara turns back at the foot of the hill. |
| M10 Belle Grove | Dean | DRIVE TO BELLE GROVE | At noon in the Chevelle; clears in the drive. The study, upstairs, the pay phone, the Starlite and Cal's door: none. |
| M11 Ledger | Dean → Cal | Dean: FIND THE $270 · Cal: none | Dean's at the ledger under the lamp; clears when the Macon pair is circled. Cal's morning: none. |
| M12 Room 614 | Ellis | none | The hallway, the radiator, 614, breakfast. |
| M13 Who the Hell Is Ellis Blake? | Dean → Riley → Cal → Ellis | none | Each reads the article where they are. In Hollow Ridge the text says "No waypoint, only Clara." |
| M14 The Extra Chair | Riley | SET THE TABLE | In the dining room; clears when the seventh place is laid. Dinner, the hall, the piano and Tommy's room: none. |
| M15 Hold the Light | Ellis → Riley | Ellis: GET THE DATSUN RUNNING · Riley: DRIVE TO COLD BRANCH ROAD · Ellis: none · Riley: none | The ride: none. Ellis's when the engine dies on the shoulder; clears at the switch to Riley. Holding the light: none. Riley's when the engine catches; clears in the Blake yard. 11:52 (the hall; Cutler Street): none. |
| M16 Loud | Ellis | none | The ticket on the kitchen table is a prompt; the show opens mid-set; the loading dock. |
| M17 Twenty-One Dates | Cal | none | A meeting in Vale's back room. |
| M18 Four Rooms | relay | none | Four rooms joined by a whistle. |
| M19 North | all four | Cal: DRIVE TO NEW YORK · Ellis: DRIVE TO NEW YORK · all: none · Ellis: GET TO THE BOWERY | Cal's in the alley behind Vale's. At Wytheville the keys go to Ellis in both branches of Cal's choice, and the string stays; it clears in the Lincoln Tunnel. The city, lunch, the showcase, the Bowery bar, the jacket and the mail: none. After the letter, Clara is gone "until the Bowery" (the text), so GET TO THE BOWERY appears when the letter goes in the jacket and clears at the brick wall at 3:40. The photograph: none. |

### Chapter VIII · Feedback

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO The Poster | a stranger's view | none | "The camera belongs to nobody." |
| M1 Key Man | Cal | none | The conference room, the call, the vote, the signing. |
| M2 Single Version | Riley | none | The hotel room and Studio B; the harmony is a Room choice. |
| M3 The Opener | Dean | PLAY THE SET | In the empty arena at four; clears at the 8:05 count-in. The tunnel and the dock: none. |
| M4 The Bus | Ellis | none | The bus is a hub; the page; *Ask him* is a prompt. |
| M5 Cleveland | Dean → Cal | none | The show (the Room), the tunnel, and a waiting mission in the ER. |
| M6 Hotel Bar | Ellis | none | *Make her stop* is "the only thing on the screen" (text). |
| M7 Eleven Times | Cal | none | The table, the fight, Kenosha. |
| M8 No Floor | Ellis → Cal | none | Two shows without a floor, Walt's bench, the meeting in Bloomington. |
| Interlude Snow Day | Dean → Cal → Riley → Ellis → Dean | none | A day nobody planned; the text: "Nothing here is tracked." |
| M9 Five | Dean | DRIVE TO THE PINE KNOT | In the Corvette on the Laurel Gap road; clears at Lynette's trailer. The party and the porch: none. The drive east has "No prompts" (text), and the driveway is his: none. |
| M10 Night Stage | Ellis | none | Makeup, the floor, *Continue*. |
| M11 Rave | Riley | GET TO GREENE STREET | The rack and her mother's call: none. Appears when she reads Nina's message at the desk; clears at the freight elevator. The trip and the stairwell: none. |
| M12 Kitchen, Cold Branch Road | Riley | DRIVE TO COLD BRANCH ROAD | In Tannersville; clears in the yard when Tater barks. The kitchen: none. |
| M13 The Box | Ellis | none | The text gives the player Ellis's eyes "and nothing to do but move them." |
| M14 Tolliver Road | Ellis | none | The text: "No destination marker." The script: "No objective and no marker." |
| M15 Payphone | Riley | DRIVE TO PICKENS GROCERY → DRIVE TO COLD BRANCH ROAD | PICKENS when she hangs up and gets her keys; clears at the bench under the awning. COLD BRANCH ROAD when they get in the Datsun; clears in the yard at 11:40. |
| M16 Four Chairs | Riley → Ellis | none | Breakfast; the chair is the choice. |
| M17 Dr. Lusk | Ellis | GET TO THE CLINIC (3RD FLOOR) → FILL THE PRESCRIPTION (LOBBY PHARMACY) → FIND THE TRUCK (DECK, LEVEL 2) | The medicated form (§4). CLINIC when Wayne parks; clears at Dr. Lusk's door. PRESCRIPTION when he leaves her office; clears at the pharmacy counter. TRUCK with the white sack; clears at the F-100. The Starlite and the first tablet: none. |
| M18 Quiet | Ellis | none | The text: "The HUD shows the day of the week, and that's all the help there is." The money line is on the money screen (§4). |

### Chapter IX · Who Are You?

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO The Truck | nobody, then Cal | none | "The camera belongs to nobody"; the switch settles on Cal under the title. |
| M1 The Lodge | Cal | ASSIGN THE ROOMS | After the walk-through; clears when the last bag is up (Theo's, on Cal's bed). The pill, the empty chair and the switch to Ellis: none. |
| M2 Under Glass | Ellis | KNOB HOUSE → PARIETAL HOURS → THE BEND → NEW SKIN, one at a time | The chapter authors these: "The HUD carries the session list as its objective, one song at a time." The line shows the next unfinished title in this order, NEW SKIN last, because finishing it ends the mission (§6). Each clears when its take is kept. Fishing, the lake and *Call* keep the current title. |
| M3 Late Hour | Ellis → Riley | Ellis: GET TO THE SET (STUDIO 6B) · Riley: none | Ellis's when the stage manager calls him from the green room; clears at the black set. A wrong corridor gets a page, not a hint. The interview: none. Riley at Knob House: none. |
| M4 The Report | Ellis | DRIVE TO COLD BRANCH ROAD (PAST THE FALLS) | When Cal passes on Wayne's message; clears at the kitchen door. The report, *Open it* and Wayne: none. |
| M5 Sylva | Ellis | none | Wayne drives both ways; the porch is a conversation; the tailgate. |
| M6 The Argument | Ellis at sixteen → Ellis → Riley | none | The Impala is a memory with one input besides the wheel (*Look at her*). The kitchen and the dock: none. Riley follows the sound of the screen door. |
| M7 Flush | Ellis | none | Day one's only prompt is *Palm it*; day two walks a dark house; day three is a session; on day four he walks up the fire tower on his own, and the help returns there. The money line leaves the money screen on day four (§4). |
| M8 Bottom | Dean → Cal | Dean: none → GET TO KNOB HOUSE · Cal: none · Dean: none | The Starlite lot: none (both things there are optional). GET TO KNOB HOUSE when he leaves the Corvette in the ditch; clears at the kitchen door at 5:50. The bathroom and the knock: none. Cal's three nights and Dean at the step: none. |
| M9 The Tabernacle | all four | none | The class opens the night and the band walks on under the leader's hand; the Room. |
| M10 Count | Riley | LOAD THE DATSUN → DRIVE TO LINWOOD | The house, the count and the kitchen: none. LOAD THE DATSUN when she goes upstairs; clears on the last trip. LINWOOD as she gets in; clears in her parents' drive. |
| M11 Excerpts | Ellis | none | The library, the phone, Main Street. Clara steers, and the line doesn't repeat her. |
| M12 Bench | Ellis → Cal | Ellis: FIX THE CLOCK RADIO · Cal: none | Ellis's when Walt hands him the job ticket; clears at the switch to Cal. Cal's stretch: none. |
| M13 Grace's Room | Ellis; Ellis at fifteen | 1976: none · July 1972: HANG THE WASH → FIX THE FENCE → RIDE TO THE TOLLIVER FARM · 1976: none | The coffee can and the room: none (the text: "there's no help in Grace's room"). In the memory each chore appears when Grace starts it and clears when it's done; the ride clears at the Tolliver paddock. The ride back, supper and the porch: none (Grace leads the way back). The jacket: none. |
| M14 Hallway | Ellis | none | The text: "No help in the hallway, either." *Close the door* is the one prompt. |
| M15 Plans | Ellis → Riley → Ellis | none | The kitchen (Wayne), the dock, the list. |

### Chapter X · The Last Light

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| CO Roll One | a film camera | none | Footage. |
| M1 North | Cal | LOAD THE BUS | In Marlon's lot at 6:30, with Cal's clipboard; clears when everyone's aboard. The ride and Harrisburg: none. |
| M2 Glen Arbor | Dean → Riley | Dean: none · Riley: FIND WAYNE AND ROY | Dean's compound walk: none. Riley's at the switch in the hayfield; clears under the F-100's tarp. Nina and Kit: none. The last objective before GO HOME. |
| M3 Morning | Ellis | none | The text: "Nobody tells him what to look at, or what day it is, or what to do." *Put it back* is the one prompt. |
| M4 Press Tent | Ellis | none | The table and the questions; Dex in the mud. |
| M5 The Field | Ellis | none | "No clock" (text). In the squall Clara names the gate, and the line doesn't repeat her. |
| M6 Weather | Cal | none | Cal's tasks are prompts where they stand (§6); the trailer; the vote. |
| M7 The Walk | Ellis | none | The walk is the mission. Roy says "Go on. Get up there." at the stairs, and a stage objective would read as a send-off (Rule 10). |
| M8 The Last Light | all four, ending on Ellis | none | The line is empty for the whole set. *HOME* is an input prompt, "the same size and type as every HOME since Chapter II" (the chapter's binding spec). Nothing on the objective line mentions home or the song. |
| M9 The Gap | nobody → Riley → Cal → Dean → Wayne | none | Riley's movement, Cal's practical steps as prompts, *Hold*, *Hold his hand*. The HUD's only text is SATURDAY · AUGUST 28 · 9:52 P.M. (§6). |

### Epilogue and coda

| Mission | Playable | Objective string(s) | Appears and clears |
|---|---|---|---|
| M1 Route 17 | Wayne | none | *Drive* is the prompt and the road runs one way. The design summary makes GO HOME "the only instruction left," so the epilogue's line stays empty. |
| M2 Pettigrew | Riley | none | Main Street, the carrying, the square, *Kneel*. |
| M3 The List | Cal | none | A room's inventory, the ledger, the radio, Marlon's, the van. |
| M4 Pocket | Dean | none | *Flush it*, the grave, the step. |
| M5 M. | Riley | none | The bridge, the sack, the poems, the book; at registration *Hand it over* is the only input. |
| M6 Tater | Wayne | none | *Feed Tater*, twice a night by January; the stone; Opening Day. |
| M7 1996 | nobody (documentary) | none | Non-interactive. |
| Coda Saturday | Ellis | none → GO HOME | The text: "There is no objective. There's no quest marker." At dusk GO HOME appears wherever Ellis is, the only time in the game. No timer; it waits while he drives or sits at Stony Knob. It clears when he steps into the kitchen, where Wayne is at the stove. If he's already in the house at dusk, it appears anyway and clears at the same door. |

---

## 4. On the medication (VIII M17 – IX M7)

Bible §11.8: on the medication there's no Clara and no help, the Room has no hum and Observe is muted. IX M2 puts it plainly: "the day and the way come only from the HUD." For Ellis, in this stretch only:

- **The strings are a little more explicit.** Verb and destination as usual, then one landmark in parentheses: the floor, the room, the road. It's the kind of fact Clara used to give ("Left at the church"), put as a place. It's never advice and never a route.
  - VIII M17: GET TO THE CLINIC (3RD FLOOR); FILL THE PRESCRIPTION (LOBBY PHARMACY); FIND THE TRUCK (DECK, LEVEL 2).
  - IX M3: GET TO THE SET (STUDIO 6B).
  - IX M4: DRIVE TO COLD BRANCH ROAD (PAST THE FALLS).
- **Where the line stays empty anyway.** VIII M18's free roam ("that's all the help there is"), IX M5 (Wayne drives), IX M6 and IX M7. IX M2's session titles are the chapter's own strings and stay bare: the chapter has Ellis learn the lodge "by opening the wrong doors," and a room name in parentheses would do the pointing the quiet takes away.
- **Knob House.** It's reached by the Stony Knob road, above the overlook and past the fire tower (IX CO, IX M1), not the Tanner Valley road. No mission in this stretch has Ellis drive there. If one is added, the string is DRIVE TO KNOB HOUSE (STONY KNOB ROAD).
- **The money line.** Clara's money help was rent: "It's Thursday. Rent's Friday" (II M5), "That's rent. Put it back" (II M8). On the medication the money screen (the notebook's back page, which shows less from VIII on, bible §11.6) carries one line at the top, in the objective's type:

  > RENT $20 · FRIDAY

  Rent is fixed at $20 every Friday, and it's still going into the coffee can in August (IX M13). The line is there from VIII M17 through day three of IX M7. It goes on day four of Flush, when Clara is back and says the money herself ("Dean still owes you four dollars").
- **Scope.** Riley's, Cal's and Dean's stretches in these chapters never had help, and their strings keep the normal form.

---

## 5. Missions with no objective

86 of the 156 missions, cold opens, the interlude and the coda keep the line empty from start to finish. The other 70 have at least one objective. GO HOME appears once, in the coda, and no other string contains GO or HOME.

**Chapter I**
- **CO.** No tutorial card and no title; the HUD shows THURSDAY only.
- **M7 Fifteen Minutes.** The back-room jam is the Room.
- **M8 One More Song.** The set starts with the mission; the alley is free.
- **M9 Home.** "No urgency and no marker" (text); no string may name home.

**Chapter II**
- **M5 Thursday.** "No objective marker" (text).
- **M9 Four in the Morning.** A conversation; "nothing to perform and nothing to win."

**Chapter III**
- **CO.** Sound and a tape; control arrives with M1.
- **M6 The Farmhouse.** A party with "no menu"; Cal's horn is the call.
- **M8 Something Wrong.** A duet; the Room.
- **M10 Thanksgiving.** Wayne drives; a booth and a ballgame.

**Chapter IV**
- **CO.** A tape machine and a title card.
- **M6 The Girl Nobody Knows.** A work session and the back step.

**Chapter V**
- **CO.** "The HUD, if the player looks: FRIDAY" (text).
- **M6 The Kitchen Table.** The scene waits for him; "no choice here."
- **M7 Still Here.** Clara, Wayne, the songwriting system, a rehearsal, a back step.
- **M9 The Exit.** The cold open fixed this hallway's HUD at FRIDAY alone.
- **M10 Opening Day.** Wayne drives; SATURDAY · APRIL 12 is the only text.
- **M15 Four Hands.** A conversation.
- **M16 Where Did We Meet?** The script's UI: the day, then *Hold* alone.

**Chapter VI**
- **CO.** A take; Clara's finger is the help.
- **M1 Don't Tell Them.** Riley's horn is the cue.
- **M2 Fine Print.** A dining room and a lesson.
- **M3 Sign Here.** A parlor and a signing.
- **M4 Transmission.** A garage day, Roy's closet, the glide.
- **M6 Dalton Sound.** A first studio day.
- **M7 2:13 A.M.** A take, a porch, the Starlite.
- **M8 Sunday Morning.** "Nothing is urgent" (text).
- **M9 Pasture.** A party; "Nobody tells her where to look" (text).
- **M10 The Field.** A conversation.
- **M11 Afterimage.** A waking scene.
- **M12 Bloodline.** Wayne in the yard.
- **M13 Side B.** A sandbox and an argument.
- **M14 Visitor.** Wayne in the parlor.
- **M14b Pay Phone.** Opens at the phone with the call planned.
- **M15 Coupon 29.** One prompt; the mission waits.
- **M16 Marlon's.** Hold or speak.
- **M17 Final Playback.** Fragments and a playback.
- **M18 The Glass.** Riley can leave or walk to the glass.

**Chapter VII**
- **CO.** The only input is Ellis's gaze.
- **M2 Release Day.** Waiting for a sale.
- **M4 Occasionally Astonishing.** A passenger and a pay phone.
- **M5 Last Shift.** A day of jobs; Clara at the pumps.
- **M6 11:47 P.M.** A song carries the camera.
- **M9 East Slope.** "It isn't marked" (text); Clara won't climb the hill.
- **M12 Room 614.** A hallway and a breakfast.
- **M13 Who the Hell Is Ellis Blake?** Reading; "No waypoint, only Clara" (text).
- **M16 Loud.** A prompt, a set already running, a loading dock.
- **M17 Twenty-One Dates.** A meeting.
- **M18 Four Rooms.** Four rooms and a whistle.

**Chapter VIII**
- **CO The Poster.** The camera belongs to nobody.
- **M1 Key Man.** A conference room and a vote.
- **M2 Single Version.** A studio; the harmony is a Room choice.
- **M4 The Bus.** A hub.
- **M5 Cleveland.** A show and an ER wait.
- **M6 Hotel Bar.** *Make her stop* is the only thing on screen.
- **M7 Eleven Times.** A fight at a table.
- **M8 No Floor.** Two shows and a bench.
- **Interlude Snow Day.** "A day nobody planned."
- **M10 Night Stage.** *Continue*.
- **M13 The Box.** Looking is the mission.
- **M14 Tolliver Road.** "No destination marker"; the script: no objective.
- **M16 Four Chairs.** Breakfast and a chair.
- **M18 Quiet.** "That's all the help there is" (text).

**Chapter IX**
- **CO The Truck.** The camera belongs to nobody.
- **M5 Sylva.** Wayne drives; a porch and a tailgate.
- **M6 The Argument.** A memory with one input; the dock.
- **M7 Flush.** Prompts, a dark house, a session, the fire tower.
- **M9 The Tabernacle.** The class and the Room.
- **M11 Excerpts.** Clara steers on Main Street.
- **M14 Hallway.** "No help in the hallway, either" (text).
- **M15 Plans.** A kitchen, a dock, a list.

**Chapter X**
- **CO Roll One.** Footage.
- **M3 Morning.** "Nobody tells him … what to do" (text).
- **M4 Press Tent.** Questions at a table.
- **M5 The Field.** No clock; Clara names the gate.
- **M6 Weather.** Tasks are prompts where they stand.
- **M7 The Walk.** Roy's "Go on"; nothing may read as a send-off.
- **M8 The Last Light.** *HOME* is a prompt; the line is empty.
- **M9 The Gap.** Prompts only; the 9:52 time stamp.

**Epilogue**
- **M1 Route 17.** GO HOME is "the only instruction left."
- **M2 Pettigrew.** As M1.
- **M3 The List.** As M1.
- **M4 Pocket.** As M1.
- **M5 M.** As M1.
- **M6 Tater.** As M1.
- **M7 1996.** Non-interactive.

---

## 6. Conflicts found

Places where a chapter or script implies guidance that isn't Clara, the objective or the band's signals, or puts on the HUD something §11.8 doesn't list. Line numbers are as of this pass. None of these has been changed.

**Guidance outside the three**

1. **VII M7, a list on the map.** `chapters/chapter-07-strangers-know-your-name.md`, line 968: "Cal takes the van. No destination is marked; on the map there's a list in Cal's handwriting of the places Ellis would go, the kind only somebody who'd been paying attention for a year could make." A list of search places on the map screen is guidance from the UI, and it puts writing on a map that carries nothing else all game. **Fix:** put the list on a page of the clipboard Cal carries through this mission, read the way the notebook and the ledger are read, and keep the map bare. The objective is FIND ELLIS.
2. **VII M6, M8 and M12, prompts that pulse or glow.** Same file. Line 889: "The player can make him, but the prompt that pulses is the couch." Line 1159: "(If the player chose Cal's first answer in the grandstand, the prompt pulses. If not, it's there, quietly.)" Line 1603: "(the prompt to Riley's door is there, glowing)". A pulsing or glowing prompt tells the player which choice the game prefers. The V M16 script says a prompt "never pulses, blinks, grows or repeats," and X M8's spec says the same of HOME. M8's pulse also depends on a tracked answer, so hidden state changes what's on screen. **Fix:** every prompt looks the same everywhere. M6: plain prompts for the couch and the hall; Tater lying down at the couch end is the pull. M8: a plain *space* prompt in both branches; if the player gave Cal's first answer ("Then drop out on the second verse and let them"), Cal lifts his headstock toward Ellis before the second verse, which is the band's signal. M12: a plain prompt at 608; the light under the door is the pull.
3. **VII M11, a hint on a timer.** Same file, line 1473: "If the player hesitates, Dean says it out loud to nobody: / **DEAN:** Two-seventy. Divides by nine." A line that fires because the player is stuck is hint text in Dean's voice, where §11.8 says Dean has no help. **Fix:** make it unconditional. Dean says it the moment he reads $270, because it's his father's trick and he can't not see it. The player still finds the pair.
4. **X M6 and X M9, "a list."** `chapters/chapter-10-the-last-light.md`, line 575: "Cal's afternoon is a list, and the game makes it a playable list"; line 1243: "The game gives the player a list of practical things, and the player does them, fast:". Read literally, both put a checklist on screen, which one line can't hold and which Chapter X's empty line rules out. **Fix:** say that each task is a prompt where it stands (the Ampeg, the stage manager's arm, the MC, the flashlight) and that the objective line stays empty.
5. **I M2, "tutorial."** `chapters/chapter-01-before-the-noise.md`, line 492: "**Mrs. Pardue's goose** is the diagnostic tutorial." No text appears, but the word says the game has a tutorial, and §11.8 says it has none. **Fix:** "Mrs. Pardue's goose is the first diagnostic job."

**HUD text §11.8 doesn't list**

6. **II M4, a HUD clock.** `chapters/chapter-02-second-verse.md`, line 608: "Cal is already there. Obviously. The HUD clock reads 9:58." The HUD has no clock. **Fix:** "The clock over the bar reads 9:58." Cal looks at that clock two lines later.
7. **X M9, the time.** `chapters/chapter-10-the-last-light.md`, lines 1362–1364: "The HUD shows the date and the time. It has only ever shown the date on days somebody said it out loud. / SATURDAY · AUGUST 28 · 9:52 P.M."; `scripts/X-M8-M9-the-last-light.md`, line 342. It's authored and should stay, but neither §11.6 (the date, on days it's said aloud) nor §11.8 (day, objective, prompts) allows a time. **Fix:** write the exception into both bible sections: the HUD shows a time once in the game, at 9:52 p.m. on August 28, 1976.

**Wording and ambiguity**

8. **The epilogue's design summary.** `chapters/epilogue-what-remains.md`, line 956: "The last input in the game is *GO HOME*." GO HOME is the objective line, and *home* was a prompt; with the two kept apart on screen (§1), the sentence describes a different HUD. **Fix:** "The last objective in the game is GO HOME."
9. **IX M2, the session order.** `chapters/chapter-09-who-are-you.md`, line 166: "The HUD carries the session list as its objective, one song at a time: NEW SKIN, KNOB HOUSE, PARIETAL HOURS, THE BEND. Finishing 'New Skin' ends the mission." If NEW SKIN shows first, finishing it ends the mission before the other three can appear. **Fix:** list them in the order this file uses (KNOB HOUSE, PARIETAL HOURS, THE BEND, NEW SKIN), with "New Skin" writable at the kitchen table all along.
10. **IV M10's header.** `chapters/chapter-04-momentum.md`, line 2708: "He drives home at two-thirty. The player drives this one". The drive is Ellis's and playable, but the header and the chapter's at-a-glance table list Riley only. **Fix:** "Riley → Ellis."
