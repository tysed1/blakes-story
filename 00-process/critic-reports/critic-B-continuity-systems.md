# Critic B: Continuity, Period and Systems Red Team (Chapters I–VI)

**Scope.** I read `01-story-bible.md`, `00-process/WORKLOG.md`, `02-macrostructure.md`, `00-process/research-notes.md` and Chapters I–VI in full, and cross-checked `04-relationship-matrix.md`. I report errors and suggest fixes but do not rewrite anything.

**Format.** Each finding has an ID, a priority (P1 breaks the game's logic or a canon rule outright, P2 is visible to attentive players or undermines a system, P3 is polish or bookkeeping), the location and a short quote, why it matters, and a repair. Mission numbers refer to the chapter files, not the macro.

**Headline result.** I computed the weekday for every explicit weekday-and-date pair in Chapters I–VI with a script: all 60 or so are correct, including Thu Oct 10 1974, Thu Nov 28 1974, Tue Jan 28 1975, Sat Apr 12 1975, Tue Apr 29 1975, Fri May 2 1975 and Sat Aug 16 1975. The calendar problems are elsewhere:
- relative-day references ("yesterday", "last week", "Friday") that point at the wrong day;
- one show that is booked *after* it happens;
- one paid gig that disappears;
- one chapter that runs outside its date range in the macro.

---

## 1. Calendar and sequencing

**CAL-1 · P1 · I M8 → II M6/M8.** On Fri Oct 18, Marlon says *"Next Friday… Fifty each"* and writes FRIDAY — THE BLAKES. Dean, Riley and Clara all repeat "Friday." Chapter II then plays no show on Oct 25 (*"Friday's second rehearsal (offscreen)"*) and treats Nov 1 as the second show: *"More people than last Friday"* but *"better than two weeks ago."* **Why:** a booked, paid gig vanishes, the ledger has a hole, and the text contradicts itself. **Fix:** I M8, change Marlon's line to `MARLON: Friday after next. County Line Boys owe me next Friday, if they make bail. Fifty each.` In II M8, change `More people than last Friday` to `More people than two weeks ago`.

**CAL-2 · P1 · IV M7/M8.** M7 runs "Wednesday Dec 18 → Friday Dec 20": *"Two days later the phone rings"* (Mitch), then *"That same Friday afternoon… EDDIE: I've got a cancellation Thursday."* The Lantern show is Thu Dec 19, so Eddie books it the day *after* it happens. In M8, Mitch says at 1 a.m. Friday *"I'm not calling you again"* before his first call. **Fix:** shift the pressing and pickup three days earlier:
- M2: `ready in ten days` becomes `ready in a week`.
- M4 (Carla): `Ten days.` becomes `Next week.`
- M7 header becomes `Monday Dec 16 → Wednesday Dec 18`; `### Friday` becomes `### Wednesday`; `That same Friday afternoon` becomes `That same Wednesday afternoon`.
- Update the at-a-glance row the same way.

On Monday Ellis is already at Vale's ("Roy sent him east with parts"), so mailing Carla's copy that day works.

**CAL-3 · P2 · IV header vs bible §4 / macro.** The chapter runs *"Saturday, December 7 – Monday, December 23"*; the canon range is Dec 2–21. M11 falls on Dec 22–23. **Fix:** update the bible and macro to Dec 7–23 (nothing collides with V, which starts Dec 24). The macro also lists "Something Good" and "The Wall" in the opposite order to the chapter; sync that too.

**CAL-4 · P2 · V M11 vs VI M5.** In V (Apr 17–24): *"The Galveston dates run through the last two weeks of the semester."* In VI (May 28–Jun 1): *"Spring semester is ending… finals in the morning."* **Fix:** in V, change the line to `The Galveston dates run through the last two weeks of April, three weeks before finals.`

**CAL-5 · P2 · III M10, Thanksgiving, "12:30 – 4:30 p.m."** The 1974 Washington–Dallas game was the late game, after Detroit's 12:30 ET game. Longley's winning touchdown came around 7 p.m. Eastern. **Fix (verify the kickoff time first):** change the time to `4:00 – 7:45 p.m.` and make the plate their supper.

**CAL-6 · P3 · I M5.** The header says *"Friday Oct 11, 12:10 a.m."*; that is Saturday. **Fix:** `Saturday Oct 12, 12:10 a.m. → Monday Oct 14`.

**CAL-7 · P3 · II M2.** Security: *"the same one Dean almost ran over yesterday"*, but that happened on Oct 11. **Fix:** change `yesterday` to `last Friday`.

**CAL-8 · P3 · II M4.** Cal: *"You rewrote the second verse last night."* The rewrite was early Saturday morning, and this is Sunday. **Fix:** `Friday night.` In the same mission, *"Methodist bell is ringing for eleven o'clock service"* rings at 9:58. **Fix:** `ringing for Sunday school`.

**CAL-9 · P3 · II M9/M10.** The at-a-glance says 3:30 a.m. but the mission runs 1:30–4:00. They leave at 3:45, the Starlite is about 15 minutes from Cold Branch Road, and yet it is *"a quarter to five"* at Grace's door. **Fix:** `a quarter past four`.

**CAL-10 · P3 · III M3.** Martin, Nov 13: *"recorded right here at WTCR last week"*. The session was Monday Nov 11. **Fix:** `Monday night`.

**CAL-11 · P3 · III M6/M7.** At 3:30 Cal says *"We're leaving"*, but M7 starts at 5:15. **Fix:** start M7 at `3:50`. Separately, M9 is dated Wed Nov 20 but ends at *"Friday's rehearsal"*; **fix:** `Wed Nov 20 – Fri Nov 22`.

**CAL-12 · P3 · IV M5/M8.** Landry says *"Thursday. Nine a.m."*, while M8 says *"due at nine Friday morning."* **Fix:** Landry's line becomes `Friday. Nine a.m.`

**CAL-13 · P3 · IV M4.** *"Dead Week Dance… the last day of finals week"*, yet Riley's final is Mon Dec 16, and "dead week" means the week *before* finals. **Fix:** world state becomes `The week before finals`; M4 becomes `the Dead Week dance, the Saturday before finals`.

**CAL-14 · P3 · IV M5.** *"the Sunday Banner… weekend listings"* shows Saturday's dance, which is already past. **Fix:** `Friday's Banner`. In IV M6, the text says *"Two in the afternoon"*, but Riley arrived "around three" and Ellis then left for food. **Fix:** `Half past three`.

**CAL-15 · P3 · V.** The cold-open card says *"FOUR MONTHS EARLIER"*, but Dec 24 to Apr 4 is 3.3 months. **Fix:** `THREE MONTHS EARLIER`. In V M4, *"Cal fell asleep… after the Krystal and hasn't fully woken up since"* spans Feb 8 to Feb 13. **Fix:** `Cal fell asleep before they cleared Chattanooga`.

**CAL-16 · P3 · V M8 vs IV M8.** Eddie's six dates included the Exit (and he said *"February, March"*), yet Mar 20 is *"The last of Eddie's six dates"* and the Exit follows on Apr 4. **Fix:** `The fifth of Eddie's six dates`, and have Eddie say `February into April`.

**CAL-17 · P3 · I M9.** *"Ellis comes home near six. The sky is going gray."* In 1974 Georgia was on emergency year-round DST (Jan 6 – Oct 27), so sunrise on Oct 19 was about 7:50 EDT and 6:00 is full dark. **Fix:** `near seven-thirty` and end the mission at `7:50 a.m.` Alternatively, keep six and make it `still black; the ridge won't gray for an hour and a half`, which also works as a period detail.

---

## 2. Ages and durations

All stated ages are correct:
- Ellis is 18 throughout I–VI, and Grace would turn 16 on Nov 2, 1974.
- The snapshot and portrait ages are right, and Wayne is 19 in Nov 1948.
- The supporting cast's ages match the bible.
- The "eighteen months" in I (measured from the crash) and the "six months" of Thursdays in II are right.

**AGE-1 · P3 · V M1.** *"There hasn't been [a tree] since 1973… up every Christmas Eve for three years."* Grace's last Christmas was 1972, and only 1973 and 1974 have passed without her. **Fix:** `There hasn't been one since Grace.` and `two years running`.

**AGE-2 · P3 · Bible premise.** *"talking to… Clara for eighteen months"*. Clara began in late April 1974, so it is about 5.5 months at the start and 28 at the end. The 18 months belong to the crash. **Fix:** `…a young woman named Clara since the spring, and who has never once asked himself…`

**AGE-3 · P3 · WORKLOG.** *"license six months"* conflicts with bible §5, *"seven months"* (Sept 14 to Apr 12 is seven). **Fix:** WORKLOG → `seven`. Bible §6.1 also says Ellis *"Would never say… 'Grace' (for months)"*, but he says it on Oct 29 (II M7, approved in the macro). **Fix:** change the bible to `rarely says "Grace"`.

---

## 3. Money

**Reconstructed ledger (key entries):**

| Date | Entry | Status |
|---|---|---|
| Oct 10 | Thursday set $26, plus $4 slid back = $30 | ✓ |
| Oct 11 | Roy: 44 h × $2.00 = $88, $76.40 net. Text says "$106.40", ignoring the "dollar and change" | P3 |
| Oct 18 | Marlon counts "$120… Forty, like we said", then pays $160 | ✗ $-1 |
| Oct 19 | $8 tire: Wayne pays $4, Ellis owes Carson $4. Rent $20/wk from Oct 25 | ✓ |
| Oct 26 | Pool $80 + $35 + $20 + $60 = $195, minus $20 = $175 down on the $325 PA; balance $150 unrecorded | P3 |
| Nov 2 | Dean owes Ellis $4 | ✓ |
| Nov 4 | Still "owes Vale forty" on the PA | see $-3 |
| Nov 16 | Blind Tiger $150: fund $30, shares $30 × 4; "PA balance paid"; Ellis's $20 paid | ✗ $40 > $30 |
| Dec 7 | Fund "about $190" + Dean LOAN $40 = $230; session costs $300 | ✗ $-2 |
| Dec 9 | "$110 left" + Marlon's $300 = $410 against the $412 pressing | ✗ $2 short |
| Dec 11 | Van $400: D.H. $200, C.M. $100, R. $50, E.B. $50 = ½, ¼, ⅛, ⅛ | ✓ |
| Dec 19–20 | Lantern $100 (fund $20, shares $20 × 4); Marlon's loan balance $250 | ✓ |
| Jan 28 | Echoplex EP-3 $150 from the fund | ✓ |
| May 20 | Advance $7,500 − 15% = $6,375; fund 20% = $1,275; shares $1,275 each ("about $1,300") | ✓ |
| May | Ellis "RENT — 10 WEEKS" = $200 | ✓ |
| Aug 15 1975 | Coupon **29** of 48, 19 remaining | ✓ (Oct 74 = 19; May 26, Jun 27, Jul 28, Aug 29; #48 due Mar 1977, after the epilogue payoff) |

**$-1 · P3 · I M8.** *"He counts out a hundred and twenty dollars… 'Forty, like we said.'"* **Fix:** `He counts out forty dollars on a keg.`

**$-2 · P2 · IV world state / M1 / M2.** The fund of $190 plus the $40 loan cannot cover the $300 session and still leave $110, and $110 + $300 is $2 short of $412. Riley's *"three Fridays of their share"* also doesn't work: at $50 each, one Friday is $160 in shares, so $300 is under two Fridays. **Fix:** world state `About $370 in the band fund`; M2 `They have $112 left` (with the loan, $112 + $300 = $412 exactly: "to the dollar"). Riley's line becomes `Two. Two and a half.`

**$-3 · P3 · III world state.** *"owes Vale forty"* can't be cleared from a $30 fund share. **Fix:** `owes Vale thirty`.

**$-4 · P2 · VI world state.** *"sold four hundred and eighty copies. Twenty are in a box"* adds up to exactly 500 with nothing given away. But at least 34 went free: 30 college stations, WLSU, Carla, Marlon, and Vale's store copy. **Fix:** `Their 45 has sold a little over four hundred copies; about sixty went free to radio stations and friends; twenty are in a box under Dean's bench.`

**$-5 · P3 · IV M3.** *"Every price between $400 and $475 is achievable"*, but the pool is exactly $400 and the eighths assume $400. **Fix:** add `(Dean covers any overage; the ledger re-cuts the shares)`, or cap the price at $400.

**$-6 · P3 · II M3.** *"It's a four-dollar tire, Ellis."* It is an $8 tire, and the wheel arrives "mounted" while Roy offers to "mount it". **Fix:** `It's four dollars, Ellis.` and `I'll put it on for nothing`.

**$-7 · P3 · V M1.** *"Twelve dollars. More than a week's groceries."* A week of food for two men in 1974 was roughly $25–30. **Fix:** `About half a week's groceries.`

**$-8 · P3 · VI M16.** Cal ("hates debt") holds Marlon's balance from the May advance until August. **Fix:** add `He tried in May. Marlon said "against the Fridays" and meant it.`

---

## 4. Knowledge state

**K-1 · P2 · Crash canon split.** Bible §5 has Ellis taking Grace *home* and refusing to bring her to Marlon's. Several texts instead say she was headed to the show:
- I design summary: *"His sister was on her way to his first show."*
- V M16: *"the bar his daughter was riding to on the night she died."*
- VI M16 knowledge note: *"crash on the way to Ellis's first show."*
- The macro's crash ladder for VI says the same.

**Why:** Chapter IX's argument ("You're not coming") depends on her *not* going. **Fix:**
- I: `His sister was in the car the night of his first show.`
- V: `the bar his son was driving to the night his daughter died.`
- VI: `Grace died in the car the night Ellis was driving to his first show.`
- Macro: `she died the night of Ellis's first gig.`

**K-2 · P3 · V M16.** *"The others know who she is now."* Only Riley has ever been told (II, IV), so Cal and Dean learn off-screen. **Fix:** `Riley told them, in the van in March, while Ellis slept. He knows she did.` This also seeds her Chapter VII disclosure.

**K-3 · P3 · VI M5.** Joan's *"Well… It's your life, Margaret"* shows she knows about the decline on the day Riley mails it. **Fix:** add `Riley called home before she walked to the mailbox.` Mailing to Scotland on the June 1 deadline is also late; `She sends a cable from the Western Union on River Street too.`

**K-4 · P3 · V M5 note vs bible Ch V table.** The bible says she *"Cannot say where they met"*, but she answers *"Tolliver Road."* The answer is better. **Fix:** change the bible to `cannot say when`.

**K-5 · P3 · V M7.** *"That's Riley's first anomaly."* She already saw him "talking to yourself" (III M6) and smiling at nobody (III M11). **Fix:** `It's the first one Riley counts.`

**K-6 · P3 · V world state vs V M3.** The world state says Martin *"has quietly mailed"* copies (Dec 24); Cal later says *"After Christmas."* **Fix:** `is about to mail`.

**K-7 · P3 · V M13.** *"Roy has hired Dale Kimsey"*, but Dale already covered for Ellis in IV M5 (*"I switched with Dale"*). **Fix:** `Roy has put Dale Kimsey on full time`.

The rest of the knowledge chains are consistent: Cal's trail from "Who's Clara?" to Marlon's story, Wayne's trail from "Pruitt told me" to the description, Edinburgh from application to decline, Richard's "Are you high?" to "I know," and Riley's two sightings of Cal with Theo.

---

## 5. Clara

### 5.1 Every appearance, I–VI

**Flagged appearances** (all others pass):

| # | Ch · date · place | Problem |
|---|---|---|
| 4 | I · Oct 19, ~1:10a · Ellis's room | Wayne awake (bible I–II table) |
| 7 | II · Oct 20, ~11a · Marlon's booth, sober, band present | table says "night, alone"; pre-empts IV |
| 10 | II · Nov 2, ~4:50a · mirror/bed | Wayne awake |
| 13 | III · Nov 17 · farmhouse field, *"grass, flattened a little"* | R1: physical trace |
| 17 | III · Nov 30, 1:30a · lot; camera "stays behind at the steel door" | R3 |
| 20 | IV · Dec 19 · Lantern EXIT sign, *"Go."* | R10 spirit |
| 28 | V · ~Mar 10 · pulls records from the crates | R1 unverified; show the record out the next morning |
| 33–34 | V · May 1 · behind Vance, "Don't" ×2; boarding-house porch | duplicates VI M3; POV unstated |
| 43 | VI · Aug 16 · chapel beyond the glass; Riley switch | repeats break 2 (SYS-6) |

**Passing appearances:**
- **I:** the alley (Oct 10); the Valiant and "Not that way" at Tolliver; looks away from the church (R7); stays in the car (R4, R8, objective shot); Stony Knob with Pruitt's blocking (R2).
- **II:** the porch, gone when Wayne flips the light; the quad after weed; the bar with Junior's "What?".
- **III:** the WTCR glass; the clock radio; the van wheel well; the shoulder framing (R3); the cigarette machine.
- **IV:** the ice machine; behind Marlon's with the fry (R1 unverified) and Marlon's question; the mezzanine; the van amp case ("I would've"); the room when Wayne enters.
- **V:** the Exit cold open; "He hang it?" (R6); the Birmingham back lot; the engine cover; Riley's POV (withheld); the wings flicker; the window flicker at 14; "Nobody understands"; the booth flicker at 14; Depot Street, **"El,"** tears and the pull-back (break 1).
- **VI:** the cold open; "Don't tell them" (Wayne out); the Datsun; behind Vance; Tenth St Records; the screen-door slap (subjective) with the switch (break 2) and the age-17 flicker; the tree line; the chair arm.

**Rules that pass everywhere:** Tater never reacts (R4). She never enters Grace's room (R5). She never knows more than Ellis (R6). She never goes to the cemetery (R7). The switch never catches on her (R9). She never says "go on" (R10). Only Ellis speaks with her (R2).

**Counts:** **"El" = 1 (V) ✓. "Liar" = 0.** The bible requires one each in I and V.

### 5.2 Findings

**CL-1 · P2 · "Liar" missing in I and V.** The relationship matrix lists "Liar" as her running joke; Chapter X's payoff depends on players having heard her tease him with it.
- **Fix, I M9:** replace `CLARA: Ellis. / ELLIS: I said nothing.` with `CLARA: Ellis. / ELLIS: I'm fine. / CLARA (lightly): Liar.`
- **Fix, V M1, midnight:** after `CLARA: Good.` insert `CLARA: You okay? / ELLIS: Fine. / CLARA: Liar.`
- Keep it out of the rain drive (V M5): "Liar" in a car in rain would spend Chapter X early.

**CL-2 · P2 · Rows 4 and 10.** Clara is in the house while Wayne is awake (I M9 right after *"Don't"* in the hall, with Wayne *"in bed, eyes open"*; II M10 just after Wayne closes Grace's door). The I design summary claims she *"never enters the house while Wayne is awake."* **Fix:**
- I M9: before `ELLIS: Asshole.`, insert `Down the hall Wayne's door shuts. After a while, through the wall, the slow saw of his snoring.` Change the late-drive beat to `The Valiant's starter wakes Wayne`.
- II M10: after `Click.`, insert `Wayne's footsteps; his own door. Ellis waits in the hall until the snoring starts.`

**CL-3 · P2 · Row 17, III M11.** A detached camera shows Clara walking beside Ellis and then *"alone in the frame."* That breaks R3 and spends an objective shot. **Fix:** `He jogs toward them. At the cars he looks back over his shoulder. From his eyes: Clara alone in the middle of the gravel lot. Then a car's headlights…`

**CL-4 · P2 · Row 13, III M6.** *"empty grass, flattened a little, the way grass gets"* is a physical trace (R1) and hints at a ghost (tone rule 7). **Fix:** `empty grass, the frost on it unbroken.`

**CL-5 · P2 · Row 20, IV M8.** *"CLARA: Go."* sends him away from her. Clara is "Stay with me" given a body, and "Go (on)" belongs to Grace. **Fix:** `CLARA: They're waiting on you.`

**CL-6 · P2 · Row 7, II M4.** A sober, daylight booth appearance with the band present contradicts the bible's I–II row and flattens IV M6's escalation (*"Broad daylight… No drugs"*). **Fix (minimal):** amend the bible table to `Mostly at night and alone; one daytime slip (II, the booth), unremarked`, and reword the IV M6 note to `the first time anyone catches him at it in daylight.`

**CL-7 · P3 · Rows 33–34.** "Clara behind Vance: Don't" appears in V M14 and again in VI M3. **Fix:** cut it from V (keep the porch). For row 34 add `Ellis glances across the street:`.

**CL-8 · P3 · I M9 note.** *"(She slips once, in Chapter VIII)"*, saying "Daddy", is a second slip that isn't recorded in the bible. **Fix:** add it to bible §6.3 next to "El."

---

## 6. Objects

| Object | Track | Issue |
|---|---|---|
| Polaroid | Nov 2 mirror frame → Dec 9 *"Ellis has it in his jacket"* → Dec 21 *"stays… in the mirror frame"* | **OBJ-1 P3** |
| Coupon book | 19 (Oct 15 1974) → 29 (Aug 15 1975) ✓ | **OBJ-2 P3**: #19 on Oct 15 puts #1 due Apr 15 1973, three days after the death |
| Chalkboard | I "FRIDAY — THE BLAKES"; II and WORKLOG "THE BLAKES — FRIDAY" | **OBJ-3 P3** |
| 45s | 500 pressed ✓; see $-4 | |
| Carla's dollar | "kept in the back of notebook 44" (IV M4 and summary) vs *"her dollar folded back into the sleeve"* (IV M7) | **OBJ-4 P3** |
| Echoplex | Hoyt's (Dec 7); band's EP-3 (Jan 28) "from now on… live"; *"live for the first time"* (Mar 20) | **OBJ-5 P3** |
| Van | '66 Econoline, $400, eighths, possum, lettering, passenger-side heater ✓; seller "Otis Crump… off the Laurel Gap road" vs bible "a man in the South Fork" | **OBJ-6 P3** |
| Jazzmaster | 1962 sunburst, alder, Mercury transmission, 1971 ✓ | — |
| Loretta | green felt-tip inside the lid ✓; retired to the wall (VI) ✓ | — |
| Notebooks | #44 (Oct–Dec), #46 (Feb) ✓ | — |
| Jacket and patch | Clara's is adult-sized; the 14-year-old flicker is "too big for her" ✓ | — |
| Ledger | Western Auto green book, Oct 26; *Clara?* crossed out Dec 22 ✓ | — |
| Evelyn's radio | borrowed Nov 13; returned; Roy buys his own ✓ | — |
| Tater | 11, fat, fed twice, eats the pie ✓ | — |
| 1-inch reel | *"the reel of one-inch tape… the master"* goes to the plant | **OBJ-7 P3** |

Fixes:
- **OBJ-1:** IV M2 `Ellis has it in his jacket.` becomes `It's in the frame of Ellis's mirror; he answers without needing to look at it.`
- **OBJ-2:** accept it (a first coupon paid at signing) or change I to `Coupon 18 of 48` and VI to `Coupon 28… Twenty more`. I recommend accepting and adding `(first payment at signing)` to bible §4.
- **OBJ-3:** standardize on `FRIDAY — THE BLAKES`.
- **OBJ-4:** IV M7, `with her dollar folded back into the sleeve and a note` becomes `and a note… You were first. Paid in full. —E.B.` He keeps the dollar.
- **OBJ-5:** `With the Echoplex in a room this size for the first time`.
- **OBJ-6:** bible §9 becomes `from a man in a hollow off the Laurel Gap road`.
- **OBJ-7:** `Hoyt hands Cal the one-inch multitrack in its box and the quarter-inch mono mixdown, the master, plus a reference copy.`

---

## 7. Period accuracy

**PER-1 · P2 · III M6.** Psilocybin tea made from mushrooms *"picked that morning"* on Nov 16, in *"frosted grass"* after *"the first hard frost."* Research §18 says they fruit May–September. **Fix:** `a tea made from mushrooms somebody picked out of the cow pasture across the road in September and dried in a coffee can.`

**PER-2 · P2 · VI M3.** Cal buys *"a James Jamerson session compilation."* No such LP existed in 1975; Jamerson went uncredited until 1971. **Fix:** `a fresh copy of What's Going On, the first Motown sleeve that printed James Jamerson's name, to replace the one he wore out.`

**PER-3 · P2 · I M2.** *"a Ford Falcon that needs a water pump and a timing belt."* Falcon sixes and V8s used chains or gears, not belts, and Ellis's competence is the point of the scene. **Fix:** `a water pump and a fan belt`.

**PER-4 · P3 · IV M3.** *"a gorgeous 1970 Dodge Tradesman"*: the Tradesman B-series began with the 1971 model year. **Fix:** `1971 Dodge Tradesman`.

**PER-5 · P3 · V M16.** *"To owning a van built after Kennedy."* A 1966 van *was* built after Kennedy. **Fix:** `after the moon landing`.

**PER-6 · P3 · V M12.** The late-news film on Tue Apr 29 shows the ship pushing a helicopter over the side and the rooftop ladder; those images mostly aired Apr 30 – May 1. **Fix (verify):** keep the date but show `a correspondent by phone from the fleet, a map, the words FINAL EVACUATION`, or move the lobby TV to the next night. The bible says Apr 30, so sync the bible.

**PER-7 · P3 · II M8.** *"a boy of about sixteen… at the bar"*, while Wesley is *"too young to come in."* **Fix:** `a boy of about eighteen`.

**PER-8 · P3 · VI M2.** *"Your mother plays it in the car."* There were no car turntables in 1975. **Fix:** `in the kitchen, on Patty's portable—never mind.`

**PER-9 · P3 · VI M6 vs VI line 1440.** *"Clara came before any drug."* By bible §6.1 weed and beer predate her. **Fix:** `Clara came before the mushrooms.`

**PER-10 · P3 · V M2.** The Georgia Senate ERA vote is dated Jan 28, 1975 (33–22 per the research notes). Verify the exact date against the GSU source.

Everything else checks out against the research notes: the songs and chart dates; the politics; gas at 53.9¢ and the $2.00 minimum wage; the gear (SX-70, Vocal Master, Scully, EP-3, MCI, Vistalite, 360/12); the TV schedule; the drinking age; the royalty terms.

---

## 8. Map, geography and real-city leakage

Grep results: no Atlanta, Nashville, Braves, Falcons, Peachtree, Opry, Ryman, Music Row, Vanderbilt, Georgia Tech, Emory, Buckhead, I-85, I-40 or I-24 anywhere in I–VI. Found instead:

**MAP-1 · P2 · VI M6.** *"the calmest man in Tennessee or Georgia or wherever the Row is."* This names Tennessee as the Row's possible state, so it points at Nashville and breaks the fiction. **Fix:** `the calmest man on the Row.`

**MAP-2 · P2 · IV M3.** *"the Laurel City Constitution"* echoes the Atlanta Constitution. **Fix:** `Laurel City Courier`.

**MAP-3 · P2 · IV M8.** *"The Terminal… chili dogs, onion rings, frosted orange"* is The Varsity's signature menu. **Fix:** `(chili dogs, onion rings, cherry Cokes)`.

**MAP-4 · P3 · V M14 / VI.** *"1142 Juniper Street"* plus *"Midtown"* plus Tenth Street matches real Midtown Atlanta street for street. **Fix:** `Linden Street`, and drop "Midtown" from VI M8's header (`off Tenth`). Upstream, bible §3.3 has "SR 400" and "Emory-style medical district". Rename them before Chapter VIII uses them.

**MAP-5 · P3 · V M11.** *"south of Macon on I-75"* is harmless, but it implies I-75 runs through Laurel City. **Fix:** `south of Macon on the interstate`.

**MAP-6 · P2 · III M4.** Riley at Vale's in Tannersville says *"It's forty miles."* Hollow Ridge to Laurel City is 38 miles (I M1), and the cities are about 90 minutes apart. **Fix:** `It's eighty miles.`

**MAP-7 · P3 · V M5.** *"Birmingham → US 78 → the map edge → the Laurel Gap corridor"* skips Laurel City; the map is continuous from west to east. **Fix:** `…the map edge → Laurel City's half-built expressway → the Laurel Gap corridor`. In V M2, *"rode a bus for three hours"* (Tannersville to Laurel City) should be `an hour and a half`. Riley *"drives back… in her Datsun"* after coming on the bus: `Riley, who followed the bus in her Datsun so she could make rehearsal, drives back up the Gap.`

**MAP-8 · P3 · II M2.** Dean at Roy's (the east edge of town): *"It's across the street"*, meaning Marlon's at the foot of Main. **Fix:** `It's in town.`

**MAP-9 · P3 · III M3 vs IV M1 lyric.** Wayne listens *"a mile below the summit"*, yet WTCR is *"dead air until… the top"*, and the lyric says *"a pull-off at the top."* **Fix:** `Just below the summit, at the fire-tower spur, where the valley is still in view.`

**MAP-10 · P3 · IV M4.** A Blind Tiger crowd follows the van roughly 55 miles to the Tanner Valley Motor Court at 1 a.m. **Fix:** `a few carloads who were headed east anyway`.

**MAP-11 · P3 · VI world state.** *"a regional draw in four states"*: they have played Georgia, Tennessee, Alabama, Florida and South Carolina. **Fix:** `five states`.

---

## 9. Game systems

**SYS-1 · P2 · I M2 money screen vs II M3.** The player can buy the $8 tire on Oct 11, but II has Wayne buying half of it on Oct 18, and Wayne and Pruitt both remark on the bald tire. **Fix:** the tire row reads `Carson's: on order, in Friday (unavailable)`. Scarcity still bites through strings versus gas.

**SYS-2 · P2 · Observe starves.** Observe prompts by chapter: I 3, II 2, III 2, IV 1, V 0, VI 0. The bible (§11.5) says Observe is the hidden-poet system that feeds the leaked poems in IX. **Fix:** at least three prompts per chapter from V on. In VI: Roy's service bay with the Jazzmaster; the pasture fireflies; the dark chapel; the Dalton lot after Wayne drives off. Sample: `Aug 6. The truck went down the Row and the gravel kept the shape of it.`

**SYS-3 · P3 · No-proximity switches before VII.** Bible §11.1 makes VII's Four Rooms the first switch *without proximity*, but IV M5 (Belle Grove to Vale), V M13 (relay) and VI M8 (*"Stutter, across a cut"*) already do it. **Fix:** codify in the bible: `Relays (III–VI) switch on a carrier: a sound, an object, or a vehicle crossing frame. VII is the first switch with none.` Give VI M8 a carrier: `WLRC on Theo's radio carries across a cut into the Blind Tiger jukebox.`

**SYS-4 · P3 · Room verbs promised for VI but not taught.** Bible §11.2 promises "controlled feedback" (Ellis) and "twelve-string drone" (Riley) from VI; only the glide is introduced. **Fix:** add both as labeled first uses in VI M6/M13.

**SYS-5 · P3 · Missions with no player verb.** IV M11 (Cal "writes"; Ellis is only boots) and VI M16 (Marlon's confession). **Fix:** IV M11, the player enters the ledger lines and the *Clara?* appears when they idle, while Ellis's garage loop continues under the radio. VI M16, give Cal the timing/silence dialogue input from bible §11.7.

**SYS-6 · P3 · Objective-camera count.** VI M18's Riley switch at the glass repeats break 2; V M7 (Riley's POV) is a preview; III M11 was an accidental break (CL-3). **Fix:** rename bible §11.4 to `three authored reveals`, and allow Riley-POV confirmations (V M7, VI M18) as echoes.

**SYS-7 · P3 · HUD.** V M10 shows *"SATURDAY · APRIL 12"*; the rule is weekday only. It is useful, because IX needs players to remember the date. **Fix:** codify in bible §11.6: `The HUD shows the date only on days a character says aloud.`

**SYS-8 · P3 · Chapter at a glance vs mission text.** Several headers disagree with their mission bodies (II M9; III M9; IV M7; VI M5 vs Mission 5). Regenerate the tables after the fixes.

---

## 10. Names

**NAME-1 · P2.** *"The Blue Lantern Supper Club"* (I M5, Tannersville) will be confused with **the Lantern** (the band's key Laurel City room). **Fix:** `the Blue Moon Supper Club`.

**NAME-2 · P3.** **Ferrell** (car-lot manager, II) against **Farris** (Eddie), the exact clash the WORKLOG removed. **Fix:** `Stroud`.

**NAME-3 · P3.** Too many Har-/Hol- names: Harlan Vale, Harold Vance, *"Harold"* (the I M1 bar patron), great-aunt **Harriet** (III) against Dr. Harriet Lusk, HARMON & SONS (VI), Hollis, Holloway, Holler House, Hensley, Hoyt, Hannah. **Fix:** the bar patron becomes `Virgil`, the great-aunt `Louise`, and the funeral home `PEARCE & SONS`.

**NAME-4 · P3.** Other collisions:
- *"Tommy opened for Skynyrd"* (V) vs Riley's brother Tommy → `Gary`.
- *"Bobby Ray… & the Starlighters"* vs Bobby (Lynette's son) and the Starlite → `Jimmy Ray… & the Nightcaps`.
- Big Ronnie (IV) vs Lonnie (III) → `Big Wendell`.
- Flag only: Pettit / Pettigrew (bible) and Dalton / Dale.

**NAME-5 · P3.** The bible calls Vance the man who "runs Southern Star"; V's card says *"Harold Vance, A&R."* **Fix:** `Harold Vance, President`. Spellings are consistent across I–VI (Tolliver, Hensley, Econoline, Pettit, Pruitt).

---

## (a) Corrected master timeline, Chapters I–VI

Entries marked ★ are corrected or proposed.

| Date | Day | Ch | Mission | Event |
|---|---|---|---|---|
| 1974-10-08 | Tue | bg | — | Ford's WIN speech |
| 10-10 | Thu | I | CO/M1 | Thursday set, $30; Clara in the alley; Wayne awake at 12:40 |
| 10-11 | Fri | I | M2–M4 | coupon 19 (due Oct 15); pay $76.40; campus; the raid; Tully |
| ★10-12 → 10-14 | Sat–Mon | I | M5 | amp at 12:10a; Mercer shop; Gaslight Alley; Marlon calls Vale |
| 10-17 | Thu | — | offscreen | Ellis's last Thursday set |
| 10-18 | Fri | I | M6–M8 | four strangers; the turn; $40 each; ★next show booked for Nov 1 |
| 10-19 | Sat | I/II | I M9; II M1–M3 | "keep yours"; Stony Knob; ★home ~7:30; library; four calls; half a tire; rent from 10/25 |
| 10-20 | Sun | II | M4 | first rehearsal; rules; home; "Low Water" |
| 10-24 | Thu | II | M5 | *The Waltons* |
| 10-25 | Fri | — | offscreen | second rehearsal; first $20 rent |
| 10-26 | Sat | II | M6 | car lot, $80; PA $325; ledger begins |
| 10-27 | Sun | bg | — | DST ends |
| 10-29 | Tue | II | M7 | memory lecture; "Grace"; Clara in the grass |
| 10-30 | Wed | bg | — | Ali–Foreman |
| 11-01 | Fri | II | M8 | second show; Martin's card |
| 11-02 | Sat | II | M9–M10 | Polaroid; $4 debt; Grace would be 16; hallway |
| 11-04 | Mon | III | M1 | tape |
| 11-05 | Tue | III | M2 | Election Day; Riley tells Joan |
| 11-11/12 | Mon–Tue | III | M2 | WTCR session, midnight to 3 a.m. |
| 11-13 | Wed | III | M3 | broadcast; Wayne's dome light; "Pruitt told me" |
| 11-15 | Fri | III | M4 | Blind Tiger booking |
| 11-16 | Sat | III | M4–M5 | Blind Tiger, $150 |
| 11-17 | Sun | III | M6–M7 | farmhouse; ★dried mushrooms; "I already buried one child" |
| 11-19 | Tue | III | M8 | "Who's Clara?" |
| ★11-20 → 11-22 | Wed–Fri | III | M9 | Carla's letter relay |
| 11-28 | Thu | III | M10 | Thanksgiving; ★~4–7:45 p.m. game |
| 11-29 | Fri | III | M11 | letter on the kick drum; "Don't forget me" |
| 12-07 | Sat | IV | M1 | Mockingbird, $300 (★fund $372) |
| 12-09 | Mon | IV | M2 | Marlon's $300; ★$412 pressing, ready in a week |
| 12-11 | Wed | IV | M3 | van, $400, owned in eighths |
| 12-12 | Thu | bg | — | Carter announces |
| 12-13 → 12-15 | Fri–Sun | IV | M4 | Holler House; Room 12; ★Dead Week dance; Blind Tiger headline; the kiss |
| 12-16 | Mon | IV | M5, ★M7 | final; "Are you high?"; ★records picked up; Carla's copy mailed |
| 12-17 | Tue | IV | M6 | "Who're you talking to?" |
| ★12-18 | Wed | IV | M7 | Mitch's call; Eddie books Thursday |
| 12-19 | Thu | IV | M8 | the Lantern; Theo; six dates; "She know?" |
| 12-20 | Fri | IV | M8/M11 | home at 5 a.m.; Marlon's Friday; loan balance $250 |
| 12-21 | Sat | IV | M9–M10 | the Wall; "Take me with you"; "I was there" |
| ★12-22/23 | Sun–Mon | IV | M11 | *Clara?*; WLSU plays the 45 |
| 12-24 | Tue | V | M1 | Christmas Eve; ★"Liar"; tickets; the star |
| 1975-01-28 | Tue | V | M2 | ERA vote (verify); lettering; Echoplex |
| 02-07 | Fri | V | M3 | Chattanooga |
| 02-13/14 | Thu–Fri | V | M4 | Knoxville; phantom harmony; Cal's call |
| 02-26/27 | Wed–Thu | V | M5 | Birmingham; the rain flash; B− |
| 03-04 | Tue | V | M6 | probation; Dean uses alone |
| 03-10 → 03-14 | Mon–Fri | V | M7 | "Still Here"; Thu 3/13 "Saturday the twelfth" |
| 03-20 | Thu | V | M8 | Lantern sold out (★5th of 6) |
| 04-04 | Fri | V | CO/M9 | the Exit (6th of 6); Galveston offer |
| 04-12 | Sat | V | M10 | second anniversary; pie; Engineers; drive home at 40 |
| 04-17 → 04-24 | Thu–Thu | V | M11 | Edinburgh acceptance; Jacksonville; exam missed |
| 04-29 | Tue | V | M12 | Savannah; the punch; Saigon on TV |
| 04-30 / 05-01 | Wed/Thu | V | M13–M14 | "Own the cost"; Eddie's card (Wed); Vance (Thu) |
| 05-02 → 05-03 01:40 | Fri–Sat | V | M15–M16 | the promise; Wayne at Marlon's; "El"; pull-back |
| 05-03 | Sat | VI | M1 | "Don't tell them" |
| 05-11 | Sun | VI | M2 | Richard's markup; Stony Knob Music |
| 05-20 | Tue | VI | M3 | signing; $7,500 advance, $12,000 recording fund |
| 05-24 | Sat | VI | M4 | Jazzmaster; the glide |
| 05-28 → 06-01 | Wed–Sun | VI | M5 | semester ends; Edinburgh declined |
| 06-02 | Mon | VI | M6 | Dalton Sound |
| 06-18/19 | Wed–Thu | VI | M7 | 2:13 a.m. |
| 06-29 | Sun | VI | M8 | Theo's; Riley sees |
| 07-19/20 | Sat–Sun | VI | M9–M11 | the Pasture switch; the field; afterimage |
| 07-24 | Thu | VI | M12 | Raymond |
| 07-31 | Thu | VI | M13 | "Shape Note" in the dark |
| 08-06 | Wed | VI | M14–M15 | Wayne at the studio; coupon 29 |
| 08-09 01:45 | Sat | VI | M16 | Marlon tells Cal |
| 08-11 → 08-16 | Mon–Sat | VI | M17–M18 | "Borrowed Stone" cut (Mon); final playback; the glass |
| 08-15 | Fri | — | — | coupon 29 due |

---

## (b) Twenty most important fixes, ranked

1. **CAL-2 (P1).** Eddie books the Lantern the day after the show. Retime IV M7 to Mon Dec 16 – Wed Dec 18.
2. **CAL-1 (P1).** The Oct 25 gig vanishes. Marlon: "Friday after next."
3. **CL-1.** Add Clara's "Liar" in I M9 and V M1; the count is currently zero.
4. **CL-3.** III M11: a detached camera shows Clara. Make it Ellis's look-back POV.
5. **CL-2.** Clara in the house while Wayne is awake (I M9, II M10). Add sleep beats.
6. **K-1.** Grace "on her way to the show" contradicts the bible's crash account. Standardize "in the car the night of his first show."
7. **CL-4.** Flattened grass is a physical trace. Change to "frost unbroken."
8. **MAP-1.** "Tennessee or Georgia or wherever the Row is." Cut it.
9. **$-2.** The Chapter IV fund, studio and pressing arithmetic ($190, $300, $110, $412). Use $372 and $112.
10. **CL-5.** Clara says "Go." Change to "They're waiting on you."
11. **$-4.** 480 + 20 = 500 leaves no free copies. Revise the VI world state.
12. **SYS-1.** The Chapter I tire purchase breaks Chapter II. Put the tire "on order."
13. **SYS-2.** Observe is absent from V–VI. Add at least three prompts per chapter.
14. **CAL-4.** Semester end conflicts between V and VI. Fix the V line.
15. **MAP-2 / MAP-3 / MAP-4.** The *Constitution*, frosted orange, Juniper and Midtown point at Atlanta. Rename them.
16. **PER-1.** Fresh mushrooms in November frost. Make them dried.
17. **CAL-5.** Thanksgiving game timing. Retime to about 4–7:45 p.m. after verifying kickoff.
18. **CL-6.** The Chapter II daylight booth vs the bible table and Chapter IV's escalation. Amend the bible and the Chapter IV note.
19. **CAL-3.** Chapter IV runs outside its canon range. Update the bible and macro to Dec 7–23.
20. **PER-2 / PER-3 / NAME-1.** The nonexistent Jamerson LP, the Falcon's timing belt, and the "Blue Lantern" collision.
