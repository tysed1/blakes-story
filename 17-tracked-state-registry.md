# THE BLAKES — Tracked-State Registry

*Deliverable 17 (V8 production supplement). Every piece of player-driven state the story keeps: where it's set, the values it can take, its default if the player never acts, and every place it's read. Programmers build the save from §2. Writers check a callback against §3. The lead's bug list is §4.*

**Sources.** The ten chapters, the epilogue and the coda (each design summary's "Tracked choices" list, plus every "if the player," "depending on," "the player chooses" and conditional line in the text); `01-story-bible.md` §11 (above all §11.5 Observe, §11.6 money, §11.8 Clara's help and `clara_tests`); the production scripts `scripts/V-M16-where-did-we-meet.md`, `scripts/VIII-M14-tolliver-road.md` and `scripts/X-M8-M9-the-last-light.md`; `10-setup-payoff-map.md`; `14-second-playthrough.md`. Where a chain the lead asked for is defined only in a side document, that document is cited by number: 11 = `11-open-world-evolution.md`, 12 = `12-side-content-framework.md`. Chapters IV–VI were read last, after the V8 IV–VI pass landed (commit 1787046). That pass contains the `clara_tests` prompts at IV M8 and V M1 and the conditional notebook line at V M16, and they're recorded here as written.

---

## 1. Conventions

**Names.** snake_case. Names already used in the sources are kept exactly: `clara_tests`, `riley_nina_interview`, and the flags in the VIII M14 and X M8–M9 scripts. Every other name was coined for this registry and is marked *(named here)* where it is defined. A † marks a choice that the chapter's own "Tracked choices" list names.

**Types.**
- **bool**: true or false.
- **enum**: one of a listed set of values, given in braces.
- **int**: a counter or an amount, with its range.
- **set**: unordered members, each at most once.
- **string list**: ordered IDs of text the player collected or selected.
- **float seconds**: real time measured on a held or waited input.
- A **derived** flag is computed from another flag and is never set directly.

**Scope.**
- **chapter-local**: read only inside the chapter that sets it. It can be dropped when the chapter completes.
- **global**: read in a later chapter, the epilogue, 1996 or the coda, so it persists in the save.
- **profile**: persists across playthroughs, for New Game Plus.

**Default.** The value the flag holds if the player never acts: no input, the prompt ignored, or the optional mission never found. Where the sources don't give one, the table says *unspecified* and the flag is listed in §4.5.

**Read where.** Every mission that consults the flag, with a few words on what changes. "Promised" means the text says a payoff happens but no mission scripts it (see §4.2).

**Flags are never shown to the player as numbers.** Nothing on screen names, counts or scores a flag. There's no meter, no percentage, no "this will be remembered" notice and no achievement pop-up. The Room has "no score, no meter" (bible §11.2), there's "no morality meter" (§11.6), and the tests are acknowledged by one notebook line and nothing else (§11.8). State reaches the player only as story: a line of dialogue, an object in a truck, a length of film, a paragraph in a magazine. The money screen shows dollars because Ellis counts dollars, and the HUD shows the day of the week because Ellis always knows it. Both are part of the fiction, and neither is a flag.

**What isn't registered.**
- Branches that resolve inside the scene they occur in, listed in §2.13 so nobody spends save space on them.
- Band responsiveness. Bible §11.2 grows it with shared hours, but the chapters fix it at story beats (slow in I, instant by VI, total in X), and no mission reads a player value for it.
- Fixed story state that no input can change: the four dollars, Wayne's twenty, the Engineers ticket book, the rent in the coffee can. These appear in §3 as fixed chains.

---

## 2. The registry

### 2.0 Systems that run across chapters

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `observe_lines` *(named here)* | string list of line IDs, ordered; each ID carries date, memo-book number and variant (normal, mushrooms, medicated). **Global + profile** | Every Observe cue Ellis takes (bible §11.5). Scripted cues: I M1 (the tutorial line: the dog Clara pointed at), I M2, I M9; II M6, II M7 (collected through Riley's camera); III M3, III M6 (mushroom variant); IV M3, IV M4, IV M8, IV M9; V M1, V M3, V M10; VI M4, VI M9, VI M13, VI M14; VII's eleven (memo books 61–66); VIII M4, VIII M14 (once, `obs_tolliver_oak`), VIII M18 (muted); IX M2 (muted), IX M7 (day two short, day four full), IX M13 (memo book 9, 1972); plus unscripted quiet-moment cues everywhere | Empty, except IV M4: if missed, "Ellis writes it anyway in the notebook between missions" | V M7 ("Still Here" offers collected lines; the ice-machine and Stony Knob images appear if collected); IX M11 (*Rave* prints the best lines in memo books 1–67, with an authored fallback set); X M8 (some open-verse phrasings are Observe lines; option C is a rain line); Ep. M5 (Riley reads every line that reached paper, dated, in order; it's the pool for her book); Ep. 1996 (one page of her book, made of these lines); New Game Plus (see `observe_lines_prev_run`) | Only lines on paper. X M5's arm lines are a separate flag (`arm_lines`). Monarch copied memo books 1–67 in January 1976; 68 was in his jacket; 69–73 come after *Rave*. Never in the pool: memo 68's train line (VIII M8, authored, and not selectable in Ep. M5) and the V M16 test line (§4.6). On medication (VIII M17 – IX M6) the cue is rare and the lines are short. |
| `observe_lines_riley` *(named here)* | set ⊆ {window_light, hymn_board, shoes_under_bench}. **Global (intended)** | V M1b, Riley's three Observe cues in Linwood Presbyterian ("Riley's notebook, not Ellis's") | empty | V M1b (the observed details come up as options while she writes the verse). VI M13: the second verse of "Sunday Clothes" is built from the margin; empty → the hymnals squared in their racks (resolved in V8, §4.2 item 2) | Keep it out of `observe_lines`: *Rave* and Riley's book print Ellis's lines. |
| `clara_tests` | int counter, 0–5. **Global (I–V)** | +1 for each optional prompt taken, each a one-time prompt: I M1 the Gulf station (*"You buying?"* / *"I'm company."*); II M10 bed (*"Get the lamp?"* / *"You've got hands."*); III M3 his room (*"Cut that off?"* / *"I'm not your mama."*); IV M8 the diner lot (*"Hand me that notebook."* / *"Do it yourself. You've got hands."*); V M1 midnight (*"Pull."* / *"I'm not your mama."*) | 0 | V M16, after the fade. If ≥ 3, the next time the notebook opens there's one line under the last entry, in Ellis's hand, that no Observe cue produced: *I kept asking her to prove it and she kept not.* Below 3 the page is unchanged. Nothing else reads it | Bible §11.8. No tests exist after the midpoint. `19-playtest-plan.md` logs the count as telemetry; the player never sees it. |
| `clara_details_seen` *(named here)* | set ⊆ {hair, eyes, gap_teeth, jacket, horse_patch}. **Global (I–VI)** | I–VI, whenever the camera lingers on a detail of Clara ("the camera has kept count") | empty | VI M14: Ellis's description of Clara to Wayne is built from these phrases, in whatever order the player picks. Details the player never looked at, he adds at the end on his own | A gaze metric, not a prompt. The description comes out close to the same sentence either way. |
| `ellis_cash` *(named here)* | int, cents. **Global (I–IV; the UI fades from VIII)** | Pay and purchases (bible §11.6): I M1 Marlon's $30; I M2 Roy's $76.40, strings $3.50, gas ~$7, cigarettes 50¢, the Starlite; II M3 $4 owed to Carson's; gig shares | authored sums (I M2: $106.40 after pay) | Money screen on the notebook's back page (I M2, II M3); IV M3 (his $50 van share is "everything he has," so no strings that week, shown and not changeable) | Rent isn't a choice: $20 goes on the kitchen table every Friday from Nov 1, 1974 (II M3), and every bill is in the coffee can (IX M13, $1,540; Ep. M6). The spending flags are in 2.1. |
| `peanut_rankings` *(named here)* | ordered list of stand IDs, each with a rank. **Global** | Every boiled-peanut stand Ellis stops at and rates: I M2 (the Tanner Valley corridor stand, the first); V M3 (the tour loop's "list that becomes an in-game collectible"); any chapter (12: "every stand on the map … Tracked") | empty | none. The callbacks (VII M7; IX M3; IX M5; X M4; Ep. 1996) quote the band's fixed ranking, which is Ellis's bit and not the player's list; 12 now says so | Resolved in V8 (§4.1 item 9): the player's list is a collectible and is in-scene |
| `dean_matchbooks` *(named here)* | set of venue IDs. **Global** | III M5 onward, one per venue (III M5: "keeps a matchbook from every venue in his trap case"); IV M4 (the Blind Tiger, headlining); per 12, "collect one of each from every venue, sign, diner and motel" | automatic: Dean's ritual (12 now agrees) | VII M10 (the cigar box he packs; if the player forgets it, Patty brings it: in-scene); Ep. M3, the van ceiling (Dean's two years, whole; fixed) | Resolved in V8 (§4.1 item 10): fixed, not a player collection. Cal keeps two single matchbooks, both fixed: IV M8 (Theo's number) and VII M6 (*11:47*). |
| `dean_sx70s` *(named here)* | set of subject IDs (signs, pools, a cow). **Global** | III M5 (the Blind Tiger's chalk sign, the first); IV M4; V M9 (the Exit's dumpster); X M2 (a famous band, from behind); per 12 as above | as `dean_matchbooks` | Ep. M3, the van ceiling ("SX-70 prints of club signs and motel pools and a cow looking in the windshield in a pasture outside Macon") | The Macon cow is authored: Ep. M5 ("Maps"), Ep. 1996 (Riley: "Dean took a picture of the cow"). |
| `dean_bets` *(named here)* | list. **In-scene** | 12: "small and stupid, settled on the spot … Not tracked." I M4 ("Take a stupid bet"); IV M4 (Dean owes Tully $5, fixed); VIII Snow Day (IOU ONE (1) BUS, fixed) | empty | none. VIII's Snow Day says "Nothing here is tracked" | Resolved in V8 (§4.2 item 11): not tracked |
| `ellis_maps` *(named here)* | list of napkin routes. **Global per 12** | 12: "the player can draw a route on a napkin; it's always wrong in a new way." III M4 (his napkin map to Laurel City, wrong) | empty | none. Ep. 1996 and Riley's "Maps" (Ep. M5) are about his maps whether or not the player drew one; 12 now says so | Resolved in V8 (§4.2 item 10): in-scene |
| `pinball_high_scores` *(named here)* | int. **Global per 12** | Marlon's *Fireball* (12: "high scores persist") | 0 | none. VII M1's Patty wins on the third ball, as scripted | By design: the scores persist on the machine, as the world's state. No scene reads them |
| `game_completed` *(named here)* | bool. **Profile** | finishing the game once (the coda and credits) | false | Replay timing only, no new information (14): I M9 (holding silence at Wayne's line lasts one beat longer); II (Clara's "your daddy" gets a half-second pause); VII M1 ("November's fine" a fraction slower); X M7 (Roy's "Go on" gets the second-step hold) | §4.6 on X M7. |
| `observe_lines_prev_run` *(named here)* | string list. **Profile** | copied from `observe_lines` when a run ends | empty | New Game Plus (optional): the first run's lines appear dimmed in the notebook's margins (14) | |

### 2.1 Chapter I

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `clara_tests` | +1 | I M1, the Gulf station | 0 | V M16 | 2.0 |
| `observe_lines` | + | I M1 (the tutorial: the porch light and the dog); I M2 (the river bridge); I M9 (Stony Knob) | | 2.0 | |
| `peanut_rankings` | + | I M2, the stand on the Tanner Valley corridor ("Ellis can stop; he rates them") | | 2.0 | the first stand |
| `tolliver_turnoff_tried` *(named here)* | bool. **Chapter-local** | I M1, reaching the Tolliver Road sawhorse (Clara: "Not that way," and he turns around) | false | Later in I: at the turnoff again, Ellis stops without being told ("Nah") and turns around | From II the sawhorse is gone and the refusal is systemic, not a flag ("Nah." / "Not tonight." / "Other way's quicker."). The first turn is VIII M14 (`tolliver_road_driven`); the coda refuses again. |
| `i_m2_strings_or_gas` *(named here)* | enum {strings, gas, none}. **Chapter-local** | I M2, payday: the money screen ("The live choice is strings or gas") | none | I M7: gas → Cal: "Your strings are dead." / "They're resting." / "Buy strings." I M9: strings → the needle's on the peg, and Ellis buys a dollar's worth at the Starlite's pumps first | Resolved in V8 (§4.2 item 1) |
| `i_ate_starlite` *(named here)* | bool. **Chapter-local** | I M9, the optional Starlite stop on the way home | false | I M9, the kitchen: true → Wayne's first line is "Starlite." (not a question), then "Another fortune?" | Resolved in V8 (§4.2 item 1) |

### 2.2 Chapter II

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `clara_tests` | +1 | II M10, bed: *"Get the lamp?"* / *"You've got hands."* | | V M16 | 2.0 |
| `observe_lines` | + | II M6 (the boy in the John Deere cap); II M7 (the lecture; "a rare case of an Observe line collected from outside Ellis's own control") | | 2.0 | |
| `ellis_cash` | − rent | II M3: Wayne sets rent at $20 a week, starting Friday | | IX M13; Ep. M6 | Fixed, not a choice. II M8's "That's rent. Put it back." is in-scene. |

The four dollars (II M9) and the Polaroid are fixed. See §3.15 and §3.16.

### 2.3 Chapter III

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `clara_tests` | +1 | III M3, his room: *"Cut that off?"* / *"I'm not your mama."* | | V M16 | 2.0 |
| `observe_lines` | + | III M3 (the guardrail); III M6 (the creek; the mushroom variant: "stranger and more specific") | | 2.0 | |
| `dean_matchbooks`, `dean_sx70s` | + | III M5, the Blind Tiger: the ritual is established | | Ep. M3 | 2.0 |

### 2.4 Chapter IV

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `clara_tests` | +1 | IV M8, the diner lot: *"Hand me that notebook."* / *"Do it yourself. You've got hands."* (optional) | | V M16 | 2.0 |
| `observe_lines` | + | IV M3 (Otis's porch); IV M4 (the ice machine: the forced fallback, and the first verse of "Ice Machine"); IV M8 (the Christmas window); IV M9 (the gutter) | | 2.0 | |
| `van_price` *(named here)* | int dollars, 400–475. **Global** | IV M3, haggling with Otis Crump as Ellis: pushing too hard raises it; "The best result is $400" | 475 (the haggle never closes: Otis takes $475) | IV M3 (the ledger: *D.H., the difference. Not a share.*; the shares don't move); IV M4 (Cal says the ledger's price, slower the higher it is). Ep. M3's ½, ¼, ⅛, ⅛ holds for every price | Resolved in V8 (§4.1 item 5) |
| `bedroom_wall_layout` *(named here)* | map of item → position; items {Lantern poster, the 45, Blind Tiger SX-70, Marlon's handbill, WTCR card, Eddie's typed six dates}. **Global** | IV M9, tacking them over the card-table desk ("The player chooses where each goes") | unspecified | Every later render of Ellis's room, "exactly as the player arranged it": VII M1, VII M18, IX M15, Ep. M3, Ep. M6 | The Starlite Polaroid can't go on the wall (Ellis puts it back in the mirror frame); Grace's crawdad snapshot goes back in the drawer face down. The coda (Nov 9, 1974) comes before the wall existed. |

IV M10 (Riley asks, or waits) is in-scene: asking shrinks the scene to "I was there," and VIII M15's "In December 1974 he told her *I was there*" holds either way.

### 2.5 Chapter V

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `clara_tests` | +1, then **read** | V M1, midnight: *"Pull."* / *"I'm not your mama."* (optional) | | **V M16**: the notebook line if ≥ 3 | 2.0 |
| `observe_lines` | + | V M1 (the Santa on the roof); V M3 (SEE ROCK CITY); V M10 (the scoreboard) | | 2.0 | |
| `observe_lines_riley` | set | V M1b | | 2.0 | |
| `peanut_rankings` | + | V M3, the tour loop's collectible list | | 2.0 | |
| `tour_rooming` *(named here)* | map of tour night → room pairs. **Chapter-local, in-scene** | V M3 onward, the tour loop's motels: "who rooms with whom (the player can influence it; it plays out that night and at breakfast)" | the default pairs: Ellis and Dean, Cal alone, Riley alone | that night and breakfast only | Resolved in V8 (§4.2 item 3): in-scene |
| `v_m12_sat_with_tully` *(named here)* | bool. **Chapter-local** | V M12, the Ogeechee Road motel (as Dean): follow Tully to the curb (input then locked to **Stay**) or go back to the room | unspecified | V M12, next morning: if false, "Tully at breakfast saying nothing" | |

The Engineers ticket book (V M1) is fixed. See §3.14.

**From the V M16 production script** (`scripts/V-M16-where-did-we-meet.md`):

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `midpoint_hold_seconds` *(named in the script)* | real seconds from the pull-back's lock to the release, pause excluded; 0 if released before the lock | V M16, node N16.7 (the hold) | 0 | no authored scene; logged for `19-playtest-plan.md` Slices A–B (T1, T2) | by design (§4.4) |
| `midpoint_complete` *(named in the script)* | bool | V M16, at black after the release | false | the Clara rules layer (Rule 11 lifts: VI M1's back seat, VI M9's third-party frame); the test interactions retire (§3.8) | |
| `notebook_prove_it_line` *(named in the script)* | bool | V M16, node N16.9, from `clara_tests` ≥ 3 | false | the memo book (the line is present or not). Tagged *not an Observe line*: no pool selects it (§4.6 item 3, resolved) | |

### 2.6 Chapter VI

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `observe_lines` | + | VI M4 (Roy in the bay door); VI M9 (the fireflies); VI M13 (the dark chapel); VI M14 (the lot) | | 2.0 | |
| `clara_details_seen` | **read** | | | VI M14, the description | 2.0 |
| `vi_m15_coupon_turned` *(named here)* | bool. **Global** | VI M15, the kitchen at 11:30 p.m.: turn Coupon 29 face down (Clara: "Turn that over. It's late.") or wait | false (waiting is the no-input path) | VI M15: false → Ellis sits down and writes "Borrowed Stone"; true → he goes to bed and is back at the table at 12:40 a.m., and writes it then. The song exists either way, so VI M17 and the track list hold | Resolved in V8 (§4.1 item 2) |
| `vi_m16_marlon_heard_all` *(named here)* | bool. **Global** | VI M16 (as Cal), timing only: speaking before Marlon finishes a thought skips the color (the wall at Roy's, the kitchen-light song, why Thursdays) | true (the scene waits; only early speech cuts it) | VII M7 (Cal "knows from Marlon where Grace was going"); VII M17 ("I know more than you—": "He promised Marlon"); IX M12 ("I promised somebody"); Ep. M3 ("I never told him it was you") | Resolved in V8: the facts and the promise play for everyone. Only the color is cut, and nothing later reads it (§4.1 item 1). |
| `vi_m18_riley_at_glass` *(named here)* | bool. **Global** | VI M18 (as Riley): walk to the glass and put her hand flat beside his, or leave | false | Ep. M2 (*Kneel*): true → "it's the same gesture, and the camera frames it the same way"; false → the kneel plays without the echo. 14 now says "if she walked to it" | Resolved in V8 (§4.1 item 11) |

The RENT — 10 WEEKS envelope (VI M3) is fixed. See the rent note in 2.0.

### 2.7 Chapter VII

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `observe_lines` | + | the eleven VII prompts (design summary; memo books 61–66) | | 2.0 | |
| `record_on_table` † *(named here)* | bool. **Global** | VII M1: take one copy of *Borrowed Stone* down the hall and leave it on the kitchen table, on the coupon book; it's gone by morning | false | VII M5 (backstory only: if false, Wayne bought the other Western Auto copy, and Mrs. Pardue knows; "Either way Wayne has one"; her lines don't change); IX M5 (if true, it's behind the F-100's seat, still in its shrink-wrap) | |
| `leipzig_record_bought` *(named here)* | bool. **Chapter-local** | VII M2 (as Riley): buy the Bach chorale-prelude record ($3.49) or put it back | false | VII M3: if true, Riley gives it to Joan on the way out ("Where did you get this?") | |
| `converter_dial` † *(named here)* | enum {moved_97_1, restored_88_9}. **Global** | VII M6, Wayne's F-100 at midnight: Ellis has already turned it to 97.1 for the second play; the prompt offers turning it back "to the exact line on the dial" | moved_97_1 (the dial is already there if the prompt is ignored) | VII M6 (moved: next morning Wayne knows someone was in his truck, face unseen; restored: nobody ever knows); VIII M17 (the drive to Dr. Lusk: set to 97.1 or 88.9, off, unmentioned); IX M5 (88.9: Wayne turns it on at the fire tower and listens to static for a mile; 97.1: he doesn't, and says "Somebody moved my radio last fall.") | §3.4 |
| `vii_m7_dex_answer` *(named here)* | enum {getting_strings, parking, hell_be_here}. **Chapter-local** | VII M7, Cal to Dex: "Where's the singer?" (every option is a lie) | forced (Dex waits) | VII M13, Cal's paragraph: *"Getting strings," Mercer told me. He was not getting strings.* / *He was not parking.* / *He was, eventually.* | Resolved in V8 (§4.2 item 4) |
| `vii_m7_grandstand_answer` *(named here)* | enum {drop_out_let_them, in_tune_for_once, monitors_up}. **Chapter-local** | VII M7, Engineers Park: "What if they sing it?" | unspecified | VII M8: if drop_out_let_them, the *space* prompt pulses before verse 2; otherwise it's there quietly | |
| `vii_m8_dean_sound` *(named here)* | enum {space_death, train_off_a_mountain, loud}. **Chapter-local** | VII M8 interviews: "What's the Blakes' sound?" | unspecified | VII M13: "Every Dean quote is in it, exactly as said" | VIII M11's letters headline, SPACE DEATH, INDEED, is fixed; the phrase is Dean's from V M8 either way. |
| `vii_m8_riley_interview` *(named here)* | enum {read_music, not_a_boy, arrangements, silence}. **Chapter-local** | VII M8: "What's it like to be the girl in the band?" | silence | VII M13: read_music → word for word, plus *Blake can't, which tells you something about what matters*; not_a_boy → *"One of us isn't a boy," she told me*; arrangements → *a college girl whose mother plays the organ in a Presbyterian church …* silence → *who, when I asked what it was like to be the girl in the band, looked at me until I asked about something else* | Resolved in V8 (§4.1 item 3) |
| `vii_m8_ellis_want` *(named here)* | enum {go_home, sleep, dont_know, silence}. **Chapter-local** | VII M8: "What do you want?" | silence | VII M13: four matching closing lines (silence: *He never did answer. I think that was the answer.*) | Cal's "whose band" answer is forced to "It's ours" on every path, so it isn't registered. |
| `chickweed_pulled` † *(named here)* | bool. **Global** | VII M9 (optional; open from Sun Nov 2 to the end of VII): pull the chickweed at the base of the stones | false (also false if the east slope is never found) | IX M5, past the state line: "You been up the hill." / "How do you know?" / "Somebody did the chickweed." | §3.4 |
| `film_canister_taken` † *(named here)* | bool. **Chapter-local** | VII M10, the bathroom cabinet in Belle Grove | false (Carol flushes it that night) | VII M10, the Starlite bathroom: the canister if taken, a folded packet from his wallet if not. The use happens either way ("Nothing else changes") | |
| `kevin_letter_answered` *(named here)* | bool. **Global** | 12 ("Kevin's Sound," VII, Ellis): from VII M7 to the end of VII, answer the letter at the kitchen table on Cold Branch Road | false | IX M9, the crowd: true → a boy at the front of the gallery, three seats down from Roy, with a Sears Silvertone case | Resolved in V8 (§4.1 item 8), §3.18 |
| `after_new_york_promise` † *(named here)* | bool, always true. **Global** | VII M14 ("Tracked"): every branch of Riley's reply in Tommy's room ends in Ellis's "After New York." | true | VIII M6 (Riley: "You said after New York"; Clara: "Don't you let some doctor poke at you."); VIII M16 ("Name one more thing it has to be after.") | Not a choice. It's registered because VII calls it tracked and VIII reads it unconditionally. |
| `riley_phone_answer` † *(named here)* | enum {love_you_too, goodnight, silence}. **Global** | VII M15, 11:52 p.m., Riley's end of the call | silence ("until he says goodnight") | Ep. M5, the M. poem dated August: love_you_too → *and said it back*; goodnight → *and said goodnight, which was the same thing*; silence → *and said nothing, and I heard it*. If Riley puts that poem in her book, the variant is what's published (Ep. M5, Ep. 1996) | "It isn't mentioned again until the epilogue." §3.5 |
| `lantern_ticket_left` *(named here)* | bool. **Chapter-local** | VII M16, Wednesday: leave one of Eddie's guest tickets on the coupon book (Coupon 33) | false | VII M16: true → gone by morning, and Wayne uses it; false → Roy buys two and hands one to Wayne at the depot. Wayne comes either way | |
| `borrowed_stone_for_wayne` † *(named here)* | enum {played, changed}. **Global per VII's list** | VII M16, the Lantern: with Wayne in the room, lift the headstock to Cal and call another song, or play "Borrowed Stone" | played | VII M16 only (played: Wayne looks at the floor through it and after; changed: Cal follows and doesn't know why) | §4.3 |
| `patty_letter_truth` † *(named here)* | enum {truth, deflect}. **Global per VII's list** | VII M18, writing back to Patty: tell her "No Name" is about his mother, or not | forced (he writes one or the other) | Ep. M4: the framed letter over Patty's desk reads *It's about my mother* or *I never finished figuring that out*, and under either, *The left flipper sticks.* VIII M9 quotes Patty's letter, not his | Read added in V8 (§4.3) |
| `white_crosses_taken` † *(named here)* | bool. **Chapter-local in effect** | VII M19, the Wytheville truck stop | false | VII M19, the drive only: taken → sharp, bright, too fast; left → the drowsiness system (lane lines swim). "Neither changes the story. Tracked." | §4.3 |
| `bowery_photo` † *(named here)* | enum {the_stare (the lens), the_look (across the street), riley (sideways at Riley), snow_picture (face up)}. **Global + profile** | VII M19 (played early and cut off as the cold open): the frame where the player held Ellis's gaze longest while Denny shoots the roll | unspecified | §3.2: VIII (the *Rave* cover and posters; the Kent State dorm; the Monarch lobby; the *Night Stage* scrim); IX M11; X M5; Ep. M1, M2, M4; Ep. 1996 | Dean smiles in every version, so VIII's cold-open line ("The one who isn't smiling") works for all four. New Game Plus can retake it, but the first run's frame stays the 1996 poster unless the player chooses otherwise (14). |

### 2.8 Chapter VIII

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `cal_rider_vote` † *(named here)* | enum {yes (4–0), no (3–1)}. **Global per VIII's list** | VIII M1, Monarch's conference room | unspecified | none: Cal signs either way and writes SIGNED UNDER PROTEST on page nine. The 1996 court note (VIII M1) is fixed | §4.3 |
| `sunday_clothes_harmony` † *(named here)* | enum {below, above, unison, silence}. **Global** | VIII M2, Studio B, the Room's harmony verb | silence (no input for three takes, and Lenny doubles Ellis) | VIII M11 (Nina's paragraph, four variants); the radio all spring (VIII–IX; 11: "Riley's harmony per the player's choice"); IX M8 (Dean's radio in the ditch: "Riley's or nobody's"); Ep. M3 (the radio plays "both versions") | "The one she picks is the one the country hears on the radio all spring." §3.3 |
| `observe_lines` | + | VIII M4 (Clara: "Look at the lines going under. Write that down."); VIII M14 (the oak, once: `obs_tolliver_oak`, below); VIII M18 (muted: *Porch. Dusk.*) | | 2.0 | |
| `asked_dex_about_page` † *(named here)* | bool. **Global per list** | VIII M4, morning: *Ask him.* | false (he keeps the notebook inside his jacket from then on) | VIII M4 only ("Out of your notebook? Man, I'd never."). X M4's "I owe you a page" is fixed | §4.3 |
| `night_stage_silence_seconds` † *(named here)* | float seconds, 40–90 (the **Continue** input comes up at 40 s). **Global** | VIII M10: the silence runs in real time until the player presses **Continue** | 90 (no input: Riley sings the line herself) | IX M3, Russ's card: < 50 s "For forty seconds"; 50–75 "For almost a minute"; 76–89 "For over a minute"; 90 "For a minute and a half." Gil's line no longer names a length | Resolved in V8 (§4.1 item 4) |
| `riley_sang_night_stage_line` † *(named here)* | bool, derived (true if no Continue by 90 s). **Global per list** | VIII M10 | true | none | §4.3 |
| `riley_rave_rack` † *(named here)* | enum {buy_both, metro_only, rave_back_to_wall, every_metro}. **Global per list** | VIII M11, the lobby newsstand on Central Park South | unspecified | none | §4.3. The scrapbook prompt after it is in-scene. |
| `tolliver_road_driven` | bool, world state. **Global** | VIII M14, script 14.1: set true on the turn onto Tolliver Road | false (it's always true once M14 is complete: the mission can't finish without the turn) | None specified. The script suspends the open-world turnoff rule (Ellis braking and turning around) for M14 only | §4.3, §4.6. The chapter-I refusal is `tolliver_turnoff_tried`. The coda must ignore this flag (Nov 1974: "Other way's quicker"). |
| `tolliver_passes` | int, 0 upward. **Global per script** | VIII M14, node N14.1a: +1 each time the player drives past the turnoff before taking it | 0 | none (the script reads no flags, and M14 plays the same way for every player) | §4.3. Clara says "Not that way" on the first approach only. |
| `tolliver_grace_reply` | enum {speed_limit, walk, silence}. **Global per script** | VIII M14, node N14.2a: Ellis's answer to "You drive like an old man." (*"Speed limit's forty-five."* / *"You want to walk?"* / silence) | silence (no input for 6 s) | none (GRA_011 and GRA_012 play whichever option was taken) | §4.3 |
| `tolliver_looks` | int, 0 upward. **Global per script** | VIII M14, node N14.3a: +1 for each look the player makes at the passenger, from the turn to the Bend | 0 | none | §4.3. Ellis's own fallback glances don't count. |
| `tolliver_ages_seen` | set ⊆ {14, 15, 16_17, 19, 21}. **Global per script** | VIII M14, node N14.3a: each age the player catches with their own look (age zones Z1–Z5) | empty (fallback glances add nothing, but they show every player all five ages) | none | §4.3 |
| `bend_stop` | enum {road, clay}. **Global per script** | VIII M14, node N14.4a: brake in the road or half onto the clay | road (no brake by the end of the stop zone, and Ellis stops in the road on his own) | none (the headlights stay on the oak either way) | §4.3 |
| `oak_touch` | enum {player, rising}. **Global** | VIII M14: node N14.4b *Touch* at the trunk (player); otherwise node N14.5b, getting up, when his hand lands on the scar (rising) | rising (it's always set by the end of M14) | VIII M15, the bench, if Riley asks about the road: "Did you touch it?" / "Yeah." / "What was it like?" / "Like a knuckle." The flag makes "Yeah." true on every playthrough | The script's exit state into M15 is binding. |
| `obs_tolliver_oak` | bool. **Global** | VIII M14, node N14.5a: the one Observe cue, 10 s after "Button your jacket." (*The bark grew back over it like a hand over a mouth.*) | false | Adds the line to `observe_lines` (2.0): Ep. M5 (Riley's reading, and the pool for her book) and Ep. 1996 | §4.6. The script says the line reaches IX M11's leaked pages, but *Rave* prints only from memo books 1–67, copied in January. |
| `riley_kitchen_chair` † *(named here)* | enum {newspaper_chair (Lorraine's; the cardigan), fourth_chair (Grace's), stand}. **Global per list** | VIII M16, breakfast | stand (no input: Wayne says "Sit down" and points at the newspaper chair) | VIII M16 only (Wayne sees the cardigan moved; or stops at the fourth chair; or says "Sit down" and points at the newspaper chair). Ep. M6, Thanksgiving: fourth_chair → Wayne pulls the seventh chair all the way out before he sits, and Riley sees him do it | Resolved in V8 (§4.2 item 6) |
| `april12_pie_cut` † *(named here)* | bool. **Global per list** | VIII M18, April 12: *Cut a piece.* | false (the pie goes to Tater; Wayne washes the dish) | VIII M18 only (true: father and son eat out of the dish). IX's design summary counts "the pie (VIII)" among what the medication gave | In-scene. The epilogue's April 12 was cut in V8 (Critic G: one ending too many), so nothing later reads it |

### 2.9 Chapter IX

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `observe_lines` | + | IX M2 (muted: *Lake. Still.*); IX M7 (day two: *Moon on the lake like a dropped plate*; day four, full: *Tannersville doing the blue ones twice …*); IX M13 (memo book 9, 1972: *Grace rides like she's mad at the horse …*) | | 2.0 | |
| `called_clara_at_lake` † *(named here)* | bool | IX M2, the dock at dusk: *Call.* | false | none | §4.3 |
| `report_answer` † *(named here)* | enum {let_me_think_i_killed_her, said_i_was_speeding, silence} | IX M4, across the report | silence | none (the next line is the same whatever is chosen) | §4.3 |
| `tailgate_answer` † *(named here)* | enum {okay, me_too, silence} | IX M5, the peanut stand south of Sylva, after Wayne's "I'm sorry" | silence | none. Of *Me too*: "He doesn't know what Ellis means, and he doesn't ask." | Resolved in V8 (§4.2 item 5): in-scene |
| `riley_dock_response` † *(named here)* | enum {what_did_she_say, argue, take_hand, silence} | IX M6, 3 a.m. | silence | none | §4.3 |
| `palm_it_wait_seconds` † *(named here)* | float seconds | IX M7, day one, from the prompt to *Palm it* | none (no timer; the scene waits) | none | §4.3 |
| `dean_poured_vial_self` † *(named here)* | bool | IX M8, the ditch: pressing *Pour it out* (true), or waiting until Dean pours it anyway (false) | false | none | §4.3 |
| `tabernacle_verse_carrier` † *(named here)* | enum {cal, riley}. **Global** | IX M9, "New Skin": Cal's *follow* turned around (up the neck, playing the lost verse's melody) | riley ("If the player doesn't, Riley sings the verse") | IX M10 (Ellis: "Cal got me." / "You got me."; Riley: "Cal got you." / "I got you."); Ep. 1996 (Cal's added line, two variants) | §3.6 |
| `riley_pillcount_argument` † *(named here)* | enum {turns_everything_up, name_one_person, different_bottle} | IX M10 | unspecified | none | §4.3 |
| `mrs_pardue_answer` † *(named here)* | enum {no_maam, some, silence} | IX M11, the Carnegie library: "Do you now?" | silence | none | §4.3 |
| `cal_bench_answer` † *(named here)* | enum {i_know, okay, silence} | IX M12, Walt's bench (as Cal) | silence (Cal moves Ellis's hand a quarter inch on the iron) | none | §4.3 |
| `grace_letter_signed` † *(named here)* | bool | IX M13, July 1972 supper: *Sign it* / *Don't* | false | none in play. IX's objects list: "*and Ellis* (if signed)" | §4.3 |
| `tried_on_jacket` † *(named here)* | bool | IX M13, Grace's closet: *Put it on.* | false | none | §4.3 |

### 2.10 Chapter X

Script node IDs are from `scripts/X-M8-M9-the-last-light.md`.

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `riley_kit_answer` † *(named here)* | enum {define_girl, read_music, lonely} | X M2, outside the film truck | unspecified | none | §4.3 |
| `riley_nina_interview` † | enum {monday, after_record, why_me}. **Global** | X M2, the press area at dusk | forced (Nina waits for an answer) | Ep. M5, the setup note: the first line of Nina's 1979 *Metro* piece: *She said Monday. It took three years of Mondays.* / *She told me after the record was done, and she meant it.* / *She asked me why her. This is why.* Nina writes MONDAY — RILEY whatever Riley says, because Nina decides that part | Resolved in V8 (§4.2 item 7), §3.20 |
| `talked_to_dex` † *(named here)* | bool | X M4, outside the press tent: let Dex ask "Not for print" | false (Ellis walks away; Dex says "Sure" to his back) | none (Dex "writes it down later, from memory"; no scene shows it) | §4.3 |
| `arm_lines` † | string list, ordered; its length is how far up the forearm it went | X M5, the infield: with no memo book, Observe writes on his left forearm in ballpoint | empty | none. The arm lines reach no one (X M5). Verse option C reads `observe_lines` instead (the most recent rain line in the memo books) | Resolved in V8 (§4.1 item 6); the extent is in-scene |
| `x_m6_vote` † *(named here)* | enum {yes_3_1, no_then_tiebreak_play, no_then_tiebreak_no}. **Global** | X M6, the trailer at 6:50 p.m.: Cal's vote, then his tie-break if he voted no (Riley yes, Ellis yes and Dean no are fixed) | forced (the scene waits for Cal's vote, then for the tie-break) | X M6. yes_3_1 → they play, and the 7:05 knock is "twenty-five minutes." no_then_tiebreak_no → "the no stands," Ellis says "Okay," fifteen minutes pass, then the 7:05 knock, "Then I'll play it by myself," everyone follows, and Eddie says "Scratch that." Ledger: *vote to play, 3–1 …* or *vote not to play, 2–2, C.M. breaking … Played.* Ep. M3 (Cal turns the ledger's pages; the *D.H.: "Stop." (On the record.)* line appears in both entries) | no_then_tiebreak_play → Cal says "Play," and writes it down before anybody can look at him; ledger: *vote 2–2, C.M. breaking: play. D.H. no: "Stop." (On the record.) C.M. no, then yes.* Resolved in V8 (§4.1 item 7). §3.19 |
| `lifted_hand` † | bool | X M8, "Still Here," node N8.3a: with *attention*, find Wayne at the foot of the mix tower; *lift hand* | false | X M8 only: true → Wayne sees it and puts his hand back in his pocket; false → his hand goes down on its own | §4.3 |
| `verse_line_1` † | enum {A "Rain on the roof like somebody counting", B "The engine ticking like it had somewhere to be", C a rain line from the player's notebooks} | X M8, N8.5a | A (the script's default; with no choice in 4 bars the band goes around again) | X M8 (sung to 150,000); X M9, Roll forty (the footage) | C is hidden unless a rain line exists. |
| `verse_line_2` † | enum {A "The oak in your window like a shut door", B "The dash light on your hands", C "The wipers still going, nobody to stop them"} | X M8, N8.5b | A | X M8; X M9 | The cutaway to the car plays on line 2 whatever the line is. |
| `verse_line_3` † | enum {A "You laughed, and the rain kept the word", B "You were fourteen and tired of me", C "I held your hand and it held back"} | X M8, N8.5c | A | X M8; X M9 | Line 4, *Go on.*, is fixed. It's the only part of the verse the Ep. M3 bootleg carries. |
| `home_hold_play_seconds` † | float seconds, from the HOME prompt to the press. **Global** | X M8, HOME (script 8.7; the accessibility toggle sets it the same way) | none: the vamp loops until pressed | X M8: the world clock advances min(seconds, 180); it feeds `home_hold_story_band` | Binding UX spec in X M8 and script 8.7 (never pulses, no idle reminder, fatigue plateaus at 180 s). §3.7 |
| `home_hold_story_band` † | enum {under_a_minute (< 60 s), about_two (60–150 s), almost_three (> 150 s)}, derived. **Global** | X M8 | — | X M9, Roll forty (the hold montage runs 40 s, 110 s or 170 s); Ep. 1996 (Nina: "under a minute / about two minutes / almost three minutes") | |
| `wayne_ambulance_meant` † | set ⊆ {not_your_fault ("It wasn't your—"), proud ("You done good up there."), scared ("Son."), son ("Son."), sing, silence} | X M9, node N9.9 (repeatable; each option once) | empty (he holds the hand) | none, by design: "he never repeats it" | §4.4, §3.9 |
| `wayne_sang` † | bool | X M9, N9.9 *Sing* (the bass line of "Wondrous Love," no words) | false | none, by design | §4.4 |
| `hand_held_seconds` † | float seconds | X M9 (script 9.9–9.11): *Hold his hand.* measures while held | 0 | X M9, 9.11: releasing the hand (or 180 s with no input after 9.10) starts the last failed switch. There's no prompt to let go | Nothing later. §4.4 |

### 2.11 Epilogue

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| `riley_book_title` † *(named here)* | enum {western_auto, memo, lines, allegedly}. **Global** | Ep. M5, "What she publishes" | unspecified | Ep. 1996 (the small gray book on Riley's office shelf, with the title the player chose) | Published 1978; sells a tenth of what Dex's sells. §3.12 |
| `riley_book_contents` † *(named here)* | string list: selected `observe_lines` that reached paper, plus any of the poems to M. **Global** | Ep. M5 | unspecified (may be empty: "or none of them") | Ep. 1996 (an insert shows one page, made of the Observe lines the player collected) | Not selectable: memo 68's train line (the cursor dims it) and the green notebook's first page (*M. —*). The August M. poem carries `riley_phone_answer`'s variant. |
| `stone_inscription` † *(named here)* | enum {name_and_dates ("No. That's him."), beloved_son, wondrous_love, later} | Ep. M6, Hollow Ridge Monument & Vault, Monday March 14, 1977 | unspecified | none | §4.4. Paid for outright from the coffee can. §3.10 |
| `portrait_1964_final` † *(named here)* | enum {face_up, face_down} | Ep. M6, Tuesday Nov 2, 1976 (as Wayne): turn it over, then set it face up or put it back face down | face_down | none | §4.4, §4.6. §3.11 |

In-scene in the epilogue, not registered: what Wayne orders in Ep. M1 (Biscuits is at the top of the list) and the radio; the girl on the curb, Dex and *Kneel* in Ep. M2; turning off the bootleg in Ep. M3; Dean's words at the grave in Ep. M4; MUS 350 in Ep. M5; opening Grace's door in Ep. M6.

### 2.12 Coda

| Flag | Type and values | Set where | Default | Read where | Notes |
|---|---|---|---|---|---|
| (none registered) | | | | The coda reads no flags | Saturday Nov 9, 1974. It renders its own day whatever the save holds: Coupon 20 of 48, Tater enormous, FRIDAY — THE BLAKES, the portrait face down, no IV M9 wall, no Clara and no help. Everything in it is in-scene: the coupon book (turn it face down or leave it), Roy's half day, Dean's lake, the phone call to Riley, the Georgia game in two rooms, and GO HOME at dusk. `game_completed` is set when the credits finish. |

### 2.13 Branches that don't persist

Resolved in the scene. None of these needs save state.

- **I:** the request in M1 (ignore it, answer it, or play at the pool table); standing up before playing; M3's seminar tone (three options, one outcome) and Riley's record; M4's party games and the chase; M8's *follow* window; M9's silence at "You got to keep yours"; staying on the hood ("Girl's flat on the second verse").
- **II:** the lug nuts in M3 ("Crisscross"); how long the M4 "Low Water" jam runs; M5's Thursday (drive away, or go in: Sit / Watch / Leave, and staying to the end); M7's silence at "What do you actually want?"; buying a round in M8 ("That's rent. Put it back.").
- **III:** flooring it as Dean (M3); M7's porch silence (it gives out after two seconds); Clara's one finger in M11.
- **IV:** fitting out the van (M3); asking or waiting (M10).
- **V:** getting the van back on the road (M5); who answers Paula (M8); how long the pull-back is held (M16: the wide shot lasts exactly as long as the hold).
- **VI:** the Edinburgh letter's tone (M5: every version declines); Riley's arguments (M13: the third wins); the order of the description (M14).
- **VII:** the speech (M1); the autograph words (M2); when Riley tells her parents, and the piano bench (M3); "Are you writing?" (M5); staying for Game 6 until 12:34 (M6); the *space* verb and the stage-door answers (M8: Ellis's is forced to "Old friend"); sitting and *Speak* on the east slope (M9); Dean's replies and his pay-phone call (M10); walking on in the hall (M12: every path turns him around); Riley's reply to "She sat in a chair" and crossing the hall (M14); what dries the distributor cap (M15: Joan's dish towel steams on the dashboard if used) and the phone lines before Riley's answer; "She still around?" (M16); "You could have waited" (M17); Riley's call to the Blake house (M18); the keys, "This one's for Clara" at the showcase, the new "Sunday Clothes" ending, and the Dayton letter (M19: open it, throw it away or pocket it, and it ends in the leather jacket's inside pocket every time).
- **VIII:** what Riley says and watches in Studio B (M2); the order of the fight's options (M7); Lynette's porch and the driveway (M9); which article Riley reads first, pasting the *Rave* page, the answer to Joan and telling Nina (M11); the form of her argument to Wayne (M12); driving past the turn first (M14); where Riley sits on the bench and what she says (M15); Ellis's "After—" attempts (M16); Dr. Lusk's topic order (M17).
- **IX:** the line order of "New Skin" (M2); going down from the fire tower or staying (M7); hanging up on Gil, and driving home or up the mountain (M11); stepping aside in the hall (M14).
- **X:** pushing Wayne on where he'll stand (M2); what Ellis puts on (M3: the ELLIS shirt either way); the press-tent answers (M4: the peanuts come anyway); looking for Wayne (M5); where he stops on the walk (M7).

---

## 3. Cross-chapter chains

Each chain lists its flag or flags, then every touchpoint in play order. *Fixed* means no input sets or changes it.

### 3.1 The Observe lines → *Rave* → Riley's book (Ep. M5, "M.") → 1996
Flags: `observe_lines`, `arm_lines`, `riley_book_contents`, `riley_book_title`, `observe_lines_prev_run`.
1. **I M1.** The first Observe cue: the porch light on the dog Clara pointed at. No text confirms it; the scratch of the pencil does.
2. **I–VII.** Cues in quiet moments; the scripted ones are listed in 2.0. IV M4's ice-machine line is written anyway if missed. The lines on mushrooms (III M6, VI M9) come out stranger. VII has eleven, in memo books 61–66.
3. **V M7.** Writing "Still Here," Ellis is offered collected lines (the ice machine, Stony Knob).
4. **VIII M4.** Dex tears the first half of "New Skin" out of memo 68. Fixed; it's a song, not an Observe line.
5. **VIII M8.** Memo 68: *If a train came through right now that'd be all right.* Authored. It's never in any pool.
6. **VIII M14.** At the oak, once: *The bark grew back over it like a hand over a mouth.* (`obs_tolliver_oak`). It's written in March 1976, after Monarch made its copies, so it can reach Riley (Ep. M5) but not *Rave* (§4.6).
7. **VIII M17 – IX M6.** On the medication the cue is rare and the lines are short and flat (*Dogwood. White.* / *Lake. Still.*). They still go in the notebook.
8. **IX M7.** The cue returns faint on day two, and at full strength on the fire tower on day four.
9. **IX M11.** *Rave*, September 1976, THE NOTEBOOKS OF ELLIS BLAKE. From Monarch's photocopies of memo books 1–67, "the game chooses the best of what the player gathered," with an authored fallback. The torn memo-68 page gets its own page, in the bus version. Mrs. Pardue: "They shouldn't have taken it. It's yours."
10. **IX M13.** Memo book 9, a fifteen-year-old's line in July 1972.
11. **X M5.** The infield: lines written on his forearm, washed off in the squall ("the only Observe lines in the game that never reach a notebook, a magazine, or anyone").
12. **X M8.** The open verse. Some phrasings are Observe lines; option C is "a rain line from the player's own notebooks." The script also accepts `arm_lines` here (§4.1).
13. **Ep. M3.** Memo books 1–70 in a Winston carton; 73 came back in the hospital sack; 71 is in Dean's bag.
14. **Ep. M5.** Riley reads "every one that reached paper, in the order they were written, with the dates," then chooses the book's title and its lines and poems. The train line and the *M. —* page can't be chosen. Published 1978.
15. **Ep. 1996.** The gray book with the player's title on Riley's shelf, and an insert page made of the player's lines.
16. **New Game Plus.** The first run's lines appear dimmed in the margins.

### 3.2 The photograph → the posters → 1996
Flag: `bowery_photo`.
1. **VII cold open.** The Bowery shoot is played early and frozen before the shutter. Clara stands across the street by the newsstand.
2. **VII M19.** The roll is shot. The frame is the one where the player held Ellis's gaze longest: *the stare*, *the look*, Riley, or *the snow picture*.
3. **VIII, world state.** *Rave*'s February cover; by March, a poster in college bookstores.
4. **VIII cold open.** A Kent State dorm wall. "Which one's Ellis?" / "The one who isn't smiling." (Dean smiles in every version.)
5. **VIII M1.** Framed, eight feet wide, in Monarch's lobby.
6. **VIII M10.** The *Night Stage* scrim: Ellis's face behind Ellis, three stories high.
7. **IX, world state.** "On dorm walls everywhere." **IX M11**: *Rave*'s September cover, a detail cropped to Ellis's face.
8. **X.** The festival program (promised in VII M19, but not scripted; §4.2). **X M5**: a girl holds it up on cardboard on a yardstick.
9. **Ep. M1.** The TV news still over the pie case at Wytheville.
10. **Ep. M2.** A girl on the curb with the poster in her lap. **Ep. M4**: a poster in a plastic sleeve, on a stick in the grave's clay.
11. **Ep. 1996.** The documentary's poster, "the player's version."
12. **New Game Plus.** It can be retaken; the first run stays canonical unless the player chooses otherwise.

### 3.3 The "Sunday Clothes" harmony → Nina's paragraph → the radio
Flag: `sunday_clothes_harmony`.
1. **V M1b.** Riley writes the first verse in the back pew and tells nobody. *Not yet.* (Fixed.)
2. **VI M13.** She arranges it on the drone; Cal writes TACET over the verses. (Fixed.)
3. **VII M4.** The *Herald* says "Ellis Blake imagines"; the correction says "written by Margaret Riley." (Fixed.)
4. **VIII M2.** Monarch recuts it with Ellis singing lead, and Riley's part is set: below, above, unison or silence. Label copy *(M. Riley)*. "The one she picks is the one the country hears on the radio all spring."
5. **VIII–IX.** The single on the ambient radio carries the chosen part (11). It peaks at #14 in April.
6. **VIII M11.** Nina's *Metro* paragraph:
   - below: *a theft committed by a friend, and the victim sings backup*;
   - above: *audible, just, on a high harmony somebody tried hard to bury*;
   - unison: *you'd need a lab to find her*;
   - silence: *"I didn't have anything to add." I don't believe her, and I don't blame her.*
7. **VIII M11.** Joan: "That boy sang your song … He sings it too fast." (Fixed.)
8. **IX M3.** The *Late Hour* caption: ELLIS BLAKE · "SUNDAY CLOTHES." (Fixed.)
9. **IX M8.** The Corvette in the ditch, WLRC faint: under Ellis's voice, "Riley's or nobody's."
10. **IX M9.** Riley sings it in the Tabernacle in her own key while Joan sings the harmony. **IX M12**: Charlene Hobbs's version with strings. (Both fixed.)
11. **X M5.** Overheard: "That's the girl's song." / "No, he sings it." / "It's her song, I read it." (Fixed.)
12. **X M8.** Riley sings it at Glen Arbor; Joan hears it on WLRC at 7:37. (Fixed.)
13. **Ep. M3.** The radio: "So is 'Sunday Clothes,' both versions." This is the only place the epilogue can surface the flag; the epilogue's design summary counts it (§4.2).

### 3.4 The converter dial and the chickweed → IX M5
Flags: `converter_dial`, `chickweed_pulled` (and `record_on_table`, which is read on the same drive).
1. **III M3.** Wayne's F-100 at the Stony Knob pull-off, engine off, dome light on, a radio on the dash. Then "Pruitt told me." (Fixed.)
2. **IV M1.** "Stony Knob": *my daddy parks his truck / and turns the dome light on*. (Fixed.)
3. **VII M1.** The record on the kitchen table: `record_on_table`.
4. **VII M6.** The converter under the dash has been on 88.9 since November 1974. Ellis turns it to 97.1; the prompt offers turning it back.
5. **VII M9.** The east slope, trimmed by hand, with a coffee can of zinnias. Pulling the chickweed sets the flag; Clara won't come up the hill.
6. **VIII M17.** The drive to Dr. Lusk. The dial is at 97.1 or 88.9, off, and unmentioned.
7. **IX M5.** The drive to Sylva:
   - the converter: at 88.9, Wayne turns it on at the fire tower and listens to static for a mile; at 97.1, he doesn't, and says "Somebody moved my radio last fall."
   - the glovebox of clippings (fixed);
   - *Borrowed Stone* behind the seat, if `record_on_table`;
   - past the state line, if `chickweed_pulled`: "You been up the hill." / "How do you know?" / "Somebody did the chickweed."

### 3.5 Riley's phone answer → the M. poem
Flag: `riley_phone_answer`.
1. **IV M4.** "Margaret." "Maggie." "Don't." He never calls her anything but Riley. (Fixed.)
2. **VII M1.** The green notebook: "It's too nice." It stays blank for nine months. (Fixed.)
3. **VII M15.** "I love you, hold it still." Then the 11:52 call, where Riley's answer is set.
4. **IX M7.** The first page, dated *7/4/76 — the fire tower*, says *M. —* and nothing else. The notebook fills (IX M15: "each one addressed to *M.*"). (Fixed.)
5. **X M3.** The Ithaca envelope goes inside its back cover. **Ep. M4**: Dean finds it, flushes the tab, and leaves the notebook in a sack marked RILEY. (Fixed.)
6. **Ep. M5.** The August poem ends *and said it back*, *and said goodnight, which was the same thing*, or *and said nothing, and I heard it*.
7. **Ep. M5 / Ep. 1996.** If Riley includes that poem in her book, the variant is what's published.

### 3.6 The Tabernacle verse carrier → "Cal got me" → 1996 Cal
Flag: `tabernacle_verse_carrier`.
1. **I M7–M8.** Cal's *follow*: catch a deviation and turn it into a change. (Fixed verb.)
2. **IV M8.** The Lantern: Ellis misses an entrance and the band covers him without a signal. (Fixed.)
3. **VIII M8.** Madison: Ellis loses a verse of "Low Water," and Riley sings it from her mic. (Fixed precedent.)
4. **IX M2.** "New Skin" is written on the medication, in daylight.
5. **IX M9.** At the Tabernacle, off the pills for seventeen days, he loses the second verse. As Cal, go up the neck and play its melody (cal), or don't, and Riley sings it (riley). The crowd thinks it's the arrangement.
6. **IX M10.** "Cal got me." / "You got me." — "Cal got you." / "I got you."
7. **X M8.** "New Skin" at Glen Arbor: he loses a line again, and "Cal is already up the neck." (Fixed.)
8. **Ep. 1996.** Cal:
   - if cal: *"He lost a verse. Twice. I played it for him up high, both times. He found it."*
   - if riley: *"He lost a verse at the end. I played it for him up high. He found it."*

### 3.7 How long HOME was held → the footage → Nina in 1996
Flags: `home_hold_play_seconds`, `home_hold_story_band`.
1. **II M4.** "Home" is defined: turn all the way around and face Dean. **II M8**: the first time in front of a crowd. It ends every song after. (Fixed.)
2. **III M11.** Clara's one finger: once more around before home. (In-scene.)
3. **IX M15.** "Stand by Dean." / "I always do." (Fixed.)
4. **X M8.** HOME, same size and type as every HOME before it, with no pulse and no reminder, and Clara gives no help. The band vamps and tires; the fatigue plateaus at 180 s. The seconds and the band are set, and the world clock advances min(s, 180).
5. **X M8.** The turn, the landed chord, the laugh, Riley's hand, the light.
6. **X M9.** Roll forty: the footage holds for 40 s, 110 s or 170 s, cut as the magazine allowed.
7. **Ep. M1.** Twenty seconds of the film on a truck-stop television. (Fixed.)
8. **Ep. 1996.** Nina: "you can see him stand at the edge of the stage for under a minute / about two minutes / almost three minutes before he turns around."

### 3.8 `clara_tests` → V M16
1. **I M1.** The Gulf station: *"You buying?"* / *"I'm company."*
2. **II M10.** Bed: *"Get the lamp?"* / *"You've got hands."*
3. **III M3.** His room: *"Cut that off?"* / *"I'm not your mama."*
4. **IV M8.** The diner lot: *"Hand me that notebook."* / *"Do it yourself. You've got hands."*
5. **V M1.** Midnight, the stuck boot: *"Pull."* / *"I'm not your mama."*
6. **V M16.** The pull-back. After the fade, if the count is 3 or more, the notebook shows *I kept asking her to prove it and she kept not.* "No cue marks it, and nothing ever refers to it." The V M16 script tags it *not an Observe line*, so no later pool can select it (§4.6 item 3).

### 3.9 Wayne's ambulance meaning (kept private, never repeated)
Flags: `wayne_ambulance_meant`, `wayne_sang`, `hand_held_seconds`.
1. **Bible §6.4.** Wayne would never say "It wasn't your fault," and he "could sing bass." (10, Spine 3.)
2. **VI M12.** Raymond sang "Wondrous Love" all the way to Milledgeville, and Wayne drove. (Fixed.)
3. **IX M5.** Wayne says "I'm sorry" twice, both times to the mountains. (Fixed.)
4. **IX M9.** Wayne stands at the gallery rail and sings the bass line. Clara is gone when the player looks back. (Fixed.)
5. **X M9.** The first playable Wayne. *Hold his hand*, and node N9.9: what he means, and whether he sings. The EMT looks out the window whenever he speaks.
6. **Never read.** Ep. M1 (he says nothing on the drive); Ep. M6 ("He could sing." — fixed); the 1996 door ("Hm."). 10 lists it among the deliberate open threads, and the epilogue's summary says "he keeps it."

### 3.10 The stone inscription
Flag: `stone_inscription`. Related: `vi_m15_coupon_turned`.
1. **I M2.** Hollow Ridge Monument & Vault, Coupon 19 of 48, $11.50. Ellis turns the book face down. (Fixed.)
2. **VI M15.** Coupon 29. Turn it over, or write "Borrowed Stone."
3. **VII M1.** The album cover is shot in the monument yard: *for G.* (Fixed.)
4. **VII M9.** The east slope: CLARA TATE BLAKE, GRACE CLARA BLAKE, and a space beside them, measured and reserved. (Optional.)
5. **VII M16.** Coupon 33. "Nineteen more and it's ours" is already out of date. **VIII M12**: Coupon 36. **IX M4**: Coupon 39. (Fixed.)
6. **IX M13.** The Maxwell House can: $1,540 of rent, unspent. (Fixed.)
7. **Ep. M2.** The burial in the space that was measured out for Wayne. **Ep. M4**: "No stone yet." (Fixed.)
8. **Ep. M6.** The last six coupons, $69, are paid from the can and stamped PAID IN FULL. The new stone matches Grace's. The inscription is set: his name and dates only, "Beloved son," "Wondrous love," or "Later." It's paid outright.
9. **After.** Nothing reads it; nothing after shows the grave.

### 3.11 Which way the 1964 portrait was left
Flag: `portrait_1964_final`.
1. **I M1.** The face-down Olan Mills portrait on the dresser. The player can turn it over; Ellis puts it face down again. (Fixed: Lorraine's gap teeth.)
2. **VI M14.** Wayne recognizes "the gap in the mother's teeth from the Chapter I portrait" in Ellis's description. (Design note.)
3. **VIII M13.** The two photographs: "The player has seen this face before, younger: at five in the 1964 portrait."
4. **Ep. M3.** Cal's inventory: "Cal doesn't turn it over. The player can." (§4.6.)
5. **Ep. M6.** Tuesday Nov 2, 1976, as Wayne: turn it over, then set it face up or put it back.
6. **Coda.** November 1974: "A photograph face down." (Fixed.)

### 3.12 Riley's book: title and contents
Flags: `riley_book_title`, `riley_book_contents`.
1. **I M3.** Riley's list of words on the inside cover of her notebook. It grows all game: *occasionally astonishing*, *whoever*, *hollow square*.
2. **VII M1.** The green notebook, a gift.
3. **IX M11.** *Rave* prints his lines without his consent.
4. **Ep. M5.** Wayne drives the memo books to Linwood ("He'd want you to have them." / "You don't know that." / "No. But I want you to."). Riley reads the train line and puts her hand over it. Title and contents are set, with two exclusions.
5. **Ep. M5.** Dex's *Who the Hell Was Ellis Blake?* (fixed) sells ten times what hers sells.
6. **Ep. 1996.** The gray book on her shelf, the player's title, and an insert page of the player's lines.

### 3.13 Wayne's twenty (fixed)
No flag. No input sets it or changes it.
1. **VII M16.** After Wayne fixes his collar, Ellis finds a twenty folded in quarters in his jacket pocket. "He puts it back. He doesn't spend it. (It's still on him in Chapter X.)" The design note: Wayne "does it with his hands, disguised as fixing a collar."
2. **VII M19.** He moves it from the corduroy to the leather jacket's inside pocket.
3. **X M3.** He checks the inside pocket: the Dayton envelope, "and behind it Wayne's twenty, folded in quarters."
4. **Ep. M1.** In the hospital sack of personal effects: "Wayne knows the fold."

### 3.14 The Engineers tickets (fixed)
No flag.
1. **III M1.** Mr. Vale: "Engineers lost again."
2. **V M1.** Christmas Eve: Ellis gives Wayne a book of four tickets (*GOOD FOR ANY APRIL HOME GAME*, $12). "We'll go."
3. **V M7.** The book is on the refrigerator. Wayne: "Saturday the twelfth. That's opening day." Clara: "Pick another Saturday." Ellis doesn't take her help.
4. **V M10.** April 12, 1975. Two tickets are used. "Your mother could sing that." Grace's three hot dogs. Forty miles an hour home.
5. **VII M7.** Cal finds Ellis in the Engineers Park grandstand ("Ellis told him on the Galveston run").
6. **VIII M18, Ep. M3.** The Engineers on Wayne's kitchen radio.
7. **Ep. M6.** April 14, 1977: the last two tickets, for Wayne and Roy. Three hot dogs, one eaten. "He could sing." / "He could."

Conflict: see §4.6 on VII M16's design note.

### 3.15 The four dollars (fixed; one optional line)
No flag.
1. **II M9.** At the Starlite, Dean is four short and Ellis puts down four ones. "That's a tomorrow problem." Cal writes it down.
2. **The ledger.** *D.H. owes E.B. $4.00 (Starlite)* — "since Chapter II, in Cal's hand" (X M6).
3. **IX M7.** Clara: "Dean still owes you four dollars." **IX M15**: the list reads *Dean owes me $4*.
4. **X M6.** Dean offers it; Ellis refuses. "I like having something on you."
5. **X M9.** Dean in the gap (script X09_DEA_001): "I owe you four dollars."
6. **Ep. M3.** Cal reads the list.
7. **Ep. M4.** Dean leaves four ones on the grave under a creek rock. If the player lets him talk: "Starlite. November second. Chess pie, two coffees and a patty melt. Paid in full." By Sept 14 the money is gone. "Of *course*." The ledger is never marked paid.

### 3.16 Dean's matchbooks and the van ceiling
Flags: `dean_matchbooks`, `dean_sx70s`.
1. **II M2.** Dean calls Marlon's from a matchbook: "he keeps every matchbook." **II M9**: the Starlite Polaroid (fixed).
2. **III M5.** The ritual is established: an SX-70 of every venue's sign and a matchbook from every venue.
3. **IV M3.** The van, owned in eighths. **IV M4**: the Blind Tiger, headlining (a Polaroid and a matchbook).
4. **IV M8.** The Lantern: posters stolen. Cal keeps one matchbook, Theo's.
5. **V M9.** An SX-70 of the Exit's dumpster.
6. **VII M6.** Cal writes *11:47* on a matchbook. (Fixed.)
7. **VII M10.** The cigar box of matchbooks "from every venue since the Blind Tiger." If the player forgets it, Patty brings it.
8. **X M2.** An SX-70 of a famous band, taken from behind.
9. **Ep. M4.** On the grave: "a matchbook from the Lantern" (fans).
10. **Ep. M3.** The van ceiling under the tarp: matchbooks, set lists in Cal's hand, SX-70s of club signs, motel pools and the Macon cow. 12 says it's the player's collection (§4.1).
11. **Ep. 1996.** Riley: "Dean took a picture of the cow."

### 3.17 The peanut rankings
Flag: `peanut_rankings`.
1. **I M2.** The stand on the Tanner Valley corridor: "Ellis can stop; he rates them."
2. **III M4.** Ellis gets in the van with a sack of boiled peanuts. (Fixed.)
3. **V M3.** The tour loop: "a list that becomes an in-game collectible."
4. **VII M7.** Cal's search list: "The boiled-peanut stand on the Spur, second in Ellis's rankings." (Kevin's letter comes from there; §3.18.)
5. **IX M3.** *Late Hour*: Mrs. Tharpe on US 19 is first ("a ham hock in the pot"); "Fourth place is a crime against God and peanuts."
6. **IX M5.** South of Sylva: "Second." / "Somebody has to."
7. **X M4.** The press tent: "For two years I had a stand on the Spur in second … You have to go back and check things." Dex's lead; "prophetic."
8. **Ep. 1996.** Dean: "He ranked boiled peanuts. He had a list. Fourth place was a crime against God and peanuts."

### 3.18 Kevin's letter
Flag: `kevin_letter_answered`.
1. **VII M7.** A boy of about fifteen at the Spur peanut stand, in a homemade shirt with both E's, gives Cal a letter: ELLIS BLAKE (SINGER). At a red light Cal hands it over: "Fan mail." Ellis pockets it unopened. From the inventory: Kevin wants "that sound" out of a Sears guitar, and his father left too.
2. **VII M8.** "Ellis has the Kevin letter in one pocket" through Dex's interview.
3. **VII, objects.** "Kevin's letter." (11: fan letters forwarded, "Kevin from the peanut stand.")
4. **12, "Kevin's Sound."** Answer it; "if answered, Kevin appears at the Tabernacle in IX."
5. **IX M9.** The Tabernacle crowd (the Mercers, the Holloways, Tom Riley, the Landrys, Wayne and Roy, a twelve-year-old bass singer from Alabama). No Kevin (§4.1).

### 3.19 The vote in X M6
Flag: `x_m6_vote`. Related: `cal_rider_vote`.
1. **II M4.** The band's rules. **V M15**: the van promise, including Cal's clause, "No band decisions alone."
2. **VII M4.** The vote on Theo: Cal abstains ("Scheduling"). (Fixed.)
3. **VII M17.** The first breach: Ellis said yes to Sawtooth alone, on a Tuesday.
4. **VIII M1.** The rider: `cal_rider_vote`.
5. **IX M15.** The festival vote is unanimous at the pine table: "the first band decision since Kenosha that everyone made together." (Fixed.)
6. **X M6.** "Stop." Ties go to the ledger, which means Cal. The vote is set, and so is the ledger entry (*vote to play, 3–1 …* or *vote not to play, 2–2, C.M. breaking … Played.*).
7. **X M7–M8.** They play either way. If the no stands, they follow him out of the trailer.
8. **Ep. M3.** Cal turns the ledger's pages: "the vote at Knob House, *D.H.: "Stop." (On the record.)*"

### 3.20 `riley_nina_interview`
1. **VII M19.** Nina Sorensen at the Bleecker Street showcase, watching Riley and nobody else. (Fixed.)
2. **VIII M11.** *Metro*'s cover says RILEY. At Greene Street: "When do you make yours?" The stairwell. (Fixed.)
3. **X M2.** "Monday, in the city. Not about him." Riley's answer is set, and Nina writes MONDAY — RILEY in every case.
4. **X M4.** Nina stands at the back of the press tent. **X M5**: "Nina Sorensen has readers." (Fixed.)
5. **Ep. M2.** Nina at the back of the church, because Riley asked. **Ep. M4**: her one sentence in *Metro* says he was clean. (Fixed.)
6. **Ep. M5.** The setup note: *Occasionally Astonishing*, 1979. It doesn't mention Nina or the interview (§4.2).
7. **Ep. 1996.** Nina's interview reads `home_hold_story_band`, not this flag.

---

## 4. Integrity checks

The lead's bug list. Every item gives the exact mission references. Every item is now marked with how V8 resolved it.

### 4.1 Read but never set, or read assuming a value that may not be set (bugs)
1. **`vi_m16_marlon_heard_all`.** VI M16 lets early speech cut "the last four lines," and those lines hold the promise ("Don't you tell him I told you." / "I won't."). VII M17 ("He promised Marlon"), IX M12 ("I promised somebody") and Ep. M3 ("I never told him it was you") all read the promise unconditionally. Either put the promise outside the lines that can be cut, or give those three scenes a variant for a Cal who never promised. **Resolved (V8):** early speech now cuts only the color; the facts and the promise play for everyone (VI M16).
2. **`vi_m15_coupon_turned`.** VI M15 lets the player turn the coupon face down, which skips writing the song. VI M17 still names the album after "the song he wrote at the kitchen table" (now "the week before"), and the track list and every chapter after it have "Borrowed Stone." It needs a fallback like IV M4's ("Ellis writes it anyway in the notebook between missions"). **Resolved (V8):** if he turns it over, he's back at the table at 12:40 a.m. and writes the song then (VI M15). "Her help buys an hour and no more."
3. **`vii_m8_riley_interview` = silence.** VII M8 offers silence; VII M13 has only three Riley variants. **Resolved (V8):** VII M13 has a silence variant.
4. **`night_stage_silence_seconds`.** VIII M10 lets the silence run to 90 s, and no input means 90. IX M3 hard-codes "the most talked-about forty seconds of television" and Russ's "For almost a minute." **Resolved (V8):** **Continue** comes up at 40 s (VIII M10); IX M3's Gil line names no length, and Russ reads the timed tape off his card in four variants.
5. **`van_price`.** IV M3 allows $400–$475, with the overage covered by Dean and the shares re-cut. IV M4 hard-codes Cal's "four hundred dollars," and Ep. M3 hard-codes ½, ¼, ⅛, ⅛. **Resolved (V8):** Dean's overage is entered as *the difference, not a share*, so the shares never move; Cal says the ledger's price in IV M4; a haggle that never closes defaults to $475.
6. **`arm_lines`.** The X M8 script (node N8.5a, option C) reads it as a source of rain lines. X M5 says the arm lines "never reach a notebook, a magazine, or anyone," none of X M5's arm lines mentions rain, and the chapter's own option C is "a rain line from the player's own notebooks." Decide what feeds option C. **Resolved (V8):** option C reads `observe_lines` (the most recent rain line in the memo books). The arm lines feed nothing, as X M5 says.
7. **`x_m6_vote` = no_then_tiebreak_play.** X M6 gives Cal a tie-break after a no, but scripts a ledger entry and a scene only for yes (3–1) and for a no that stands. **Resolved (V8):** X M6 has the scene line ("Play," written down before anybody can look at him) and the ledger entry.
8. **`kevin_letter_answered`.** 12 reads it at IX M9 (Kevin at the Tabernacle). No chapter sets it: VII has no scene or prompt for answering the letter. IX M9 doesn't read it. **Resolved (V8):** 12 sets it (the kitchen table, VII M7 to the end of VII); IX M9 reads it (Kevin in the gallery).
9. **`peanut_rankings`.** Every callback (VII M7, IX M3, IX M5, X M4, Ep. 1996) quotes an authored order: Mrs. Tharpe first, the Spur second, then Sylva second, an unnamed fourth. The player's list (I M2, V M3; 12, "Tracked") is never consulted, and a player who never stopped at Mrs. Tharpe's still hears her ranked first. Either lock those ranks as authored or read the list. **Resolved (V8):** the ranks are locked as authored. They're the band's ranking and Ellis's bit; the player's list is a collectible and in-scene (12).
10. **`dean_matchbooks`, `dean_sx70s`.** 12 says the Ep. M3 ceiling is "the player's collection." The chapters give the player no input to collect or skip anything (III M5 makes it Dean's automatic ritual), so no player value is ever set. **Resolved (V8):** Dean's ritual, fixed; 12 no longer calls it the player's collection.
11. **`vi_m18_riley_at_glass`** (low). Ep. M2's *Kneel* ("the way you'd put your hand on the glass at Dalton Sound, next to somebody else's") and 14 assume Riley walked to the glass. VI M18 lets her leave. **Resolved (V8):** the *Kneel* echo plays only if she walked to the glass; 14 says so.

### 4.2 Payoff promised in the text, never scripted
1. **`i_m2_strings_or_gas`, `i_ate_starlite`.** I M2 promises that Cal hears dead strings "at Marlon's next week," that the Valiant "runs on fumes," and that Wayne smells the Starlite on him. I M6–M9 script none of it. **Resolved (V8):** Cal hears dead strings in I M7; the needle's on the peg in I M9; Wayne smells the Starlite in I M9.
2. **`observe_lines_riley`.** V M1b: "goes in the margin beside it, for later." VI M13 doesn't use it. **Resolved (V8):** VI M13 builds the second verse from the margin.
3. **`tour_rooming`.** V M3: "it's remembered." Nothing reads it. **Resolved (V8):** in-scene ("it plays out that night and at breakfast").
4. **`vii_m7_dex_answer`.** VII M7: "Whichever Cal says ends up in the magazine." VII M13 has no Cal quote about soundcheck. **Resolved (V8):** VII M13 prints Cal's lie and Dex's correction.
5. **`tailgate_answer` = me_too.** IX M5: "He doesn't know what Ellis means, yet." No later scene resolves it. **Resolved (V8):** in-scene ("and he doesn't ask").
6. **`riley_kitchen_chair`.** 12 lists "whether Riley sat in Grace's chair" among the marks remembered later. Nothing after VIII M16 reads it. **Resolved (V8):** read at Ep. M6's Thanksgiving.
7. **`riley_nina_interview`.** X M2 calls it tracked, and 10 gives its payoff as "Ep. M5 (setup note)." That note doesn't mention Nina, and Nina writes MONDAY — RILEY whatever Riley says. **Resolved (V8):** Ep. M5's setup note gives the first line of Nina's 1979 piece, one per answer.
8. **`bowery_photo`.** VII M19 promises "the festival program in Chapter X." X has no program moment. **Resolved (V8):** X M4, the program on the press table (he turns it face down); X M5's cardboard poster.
9. **`sunday_clothes_harmony`.** The epilogue's design summary lists it as surfacing. Only Ep. M3's radio ("both versions") can carry it, and that isn't specified to use the flag. **Resolved (V8):** Ep. M3's radio names both versions and plays the single with the player's harmony.
10. **`ellis_maps`.** 12: "Riley's 1996 answer depends on it." Ep. 1996 is fixed. **Resolved (V8):** in-scene; 12 no longer promises a read.
11. **`dean_bets`.** 12 calls them tracked; VIII's Snow Day says "Nothing here is tracked." Nothing reads them. **Resolved (V8):** not tracked; 12 agrees with VIII.

### 4.3 Set, never read (the chapter calls it tracked; nothing downstream consults it)
For each one, the lead should either add a read or drop "tracked" and treat it as in-scene. **Resolved (V8):** a read added for `patty_letter_truth` (Ep. M4, the framed letter). (A read for `april12_pie_cut` was added and then cut with the epilogue's April 12 beat.) Every other flag below is now labeled **in-scene** in its chapter's design summary ("the choice pays off where it's made, and nothing later changes"). The VIII M14 script flags are in-scene by design: the mission is one continuous take with nothing to carry forward except the touch.
- **VII:** `borrowed_stone_for_wayne` (M16); `patty_letter_truth` (M18; Ep. M4 shows the framed letter without variant text); `white_crosses_taken` (M19; it affects that drive only).
- **VIII:** `cal_rider_vote` (M1); `asked_dex_about_page` (M4; X M4's "I owe you a page" is fixed); `riley_sang_night_stage_line` (M10); `riley_rave_rack` (M11); `april12_pie_cut` (M18).
- **VIII M14 script:** `tolliver_passes` (N14.1a), `tolliver_grace_reply` (N14.2a), `tolliver_looks` and `tolliver_ages_seen` (N14.3a), `bend_stop` (N14.4a). The script itself says "Flags read here: none," and no later mission reads them. `tolliver_road_driven` has no stated read either (§4.6). Of the script's flags, only `oak_touch` (VIII M15) and `obs_tolliver_oak` (the notebook) are read.
- **IX:** `called_clara_at_lake` (M2); `report_answer` (M4); `riley_dock_response` (M6); `palm_it_wait_seconds` (M7); `dean_poured_vial_self` (M8); `riley_pillcount_argument` (M10); `mrs_pardue_answer` (M11); `cal_bench_answer` (M12); `grace_letter_signed` (M13; only IX's objects list mentions it); `tried_on_jacket` (M13).
- **X:** `riley_kit_answer` (M2); `talked_to_dex` (M4); the extent of `arm_lines` (M5, "how far up it went"); `lifted_hand` (M8; only Wayne's response in the same scene).
- **Side content (12):** `pinball_high_scores`.

### 4.4 Set, never read, by design (confirmed, closed in V8)
- `wayne_ambulance_meant`, `wayne_sang` (X M9). "He never repeats it"; 10 lists it as a deliberate open thread.
- `hand_held_seconds` (X M9). It only ends the scene.
- `verse_line_1`–`verse_line_3` (X M8). Sung once, and seen once in X M9's footage. The Ep. M3 bootleg carries only *Go on*, and the 1996 track has no vocal.
- `stone_inscription`, `portrait_1964_final` (Ep. M6). Each is the last choice in its chain, and nothing after shows the grave or the room.

### 4.5 Defaults the sources don't give
`bowery_photo` (the frame if the player never moves the gaze); `van_price` (if the haggle fails, or never happens); `bedroom_wall_layout`; `tour_rooming`; `v_m12_sat_with_tully`; `vii_m7_dex_answer`; `vii_m7_grandstand_answer`; `vii_m8_dean_sound`; `patty_letter_truth`; `cal_rider_vote`; `riley_rave_rack`; `riley_kitchen_chair`; `riley_pillcount_argument`; `riley_kit_answer`; `riley_nina_interview`; `x_m6_vote`; `riley_book_title`; `riley_book_contents`; `stone_inscription`. Some of these may be forced choices (the scene can't go on without input), which is fine. The lead should mark which ones.

**Resolved (V8).** Forced (the scene waits for input): `vii_m7_dex_answer`, `vii_m7_grandstand_answer`, `x_m6_vote`, `riley_nina_interview`, `riley_book_title`, `riley_book_contents`, `stone_inscription`, `patty_letter_truth`, `cal_rider_vote`, `riley_kit_answer`, `riley_pillcount_argument`. Defaults on no input: `bowery_photo` = the_stare (the lens); `van_price` = 475; `bedroom_wall_layout` = as the art team dresses it for I M1; `tour_rooming` = Ellis with Dean, Cal alone, Riley alone; `v_m12_sat_with_tully` = false (he goes back to the room); `vii_m8_dean_sound` = the first option offered; `riley_rave_rack` = metro_only; `riley_kitchen_chair` = stand.

### 4.6 Other state conflicts found while registering
1. **The Engineers tickets.** VII M16's design note says "Wayne leaves money where it can be found: the heater, the half a tire, the Engineers tickets." V M1 and Ep. M6 have Ellis giving Wayne the ticket book on Christmas Eve 1974. **Resolved (V8):** VII M16's design note no longer lists the tickets.
2. **The 1964 portrait.** Ep. M3 lets the player, as Cal, turn it over. Ep. M6 finds it face down. Say whether Cal's turn is look-only, as it is in I M1. **Resolved (V8):** Cal's turn is look-only; he sets it back face down (Ep. M3).
3. **The V M16 test line.** It's written in a memo book in May 1975, inside the range Monarch copies for *Rave* (memo books 1–67, IX M11) and in the books Riley reads and selects from (Ep. M5). "Nothing ever refers to it" needs a rule: tag it as not an Observe line, so neither pool can select it. **Resolved (V8):** the V M16 script tags it not an Observe line (N16.9).
4. **The X M7 replay flag.** 14's replay flag gives Roy's "Go on" the second-step hold on replay. X M7 already holds on the second step on the first playthrough. **Resolved (V8):** on replay the hold runs one beat longer (14).
5. **`obs_tolliver_oak`.** The VIII M14 script (node N14.5a) says the oak line "joins the notebook pool that Chapter IX's leaked pages are built from." IX M11 prints only from memo books 1–67, which Monarch copied in January 1976; memo 68 was in his jacket, and the oak line is written on March 20. The line can reach Riley's reading and her book (Ep. M5), but not *Rave*. Fix the script note, or IX M11's rule. **Resolved (V8):** the script note now says it reaches Riley's reading and her book, not *Rave*.
6. **`tolliver_road_driven`.** It's set as world state, but no source says what it changes. The script suspends the open-world turnoff rule for M14 only, and nothing says whether Ellis may take Tolliver Road in free roam afterwards (VIII M18, IX). 12 forbids it only *before* VIII M14. Say what the turnoff does after M14, and make sure the coda ignores the flag (it refuses again: "Other way's quicker"). **Resolved (V8):** from VIII M18 the road is open in free roam and holds no content; Clara says nothing on it; the coda ignores the flag (the script, 12).
