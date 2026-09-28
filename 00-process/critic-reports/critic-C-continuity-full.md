# Critic C — Full-Draft Continuity Audit (Chapters VII–X, Epilogue/Coda)

*Scope: `chapters/chapter-07…` through `chapters/epilogue-what-remains.md`, read in full against `01-story-bible.md` (§4, §5, §6, §11.3, §13), `00-process/WORKLOG.md`, `00-process/V4-red-team.md` Part 2 and `02-macrostructure.md`. Chapters I–VI were checked only where a later chapter cites them. Audited at HEAD `188e702`. Two fixes landed while this audit ran (VIII "Dolly stood for twenty years"; the epilogue's Hannah and Landry beats) and are not reported.*

**Method notes.** A script checked every explicit weekday-plus-date in VII–Epilogue: **190 of 190 are correct.** The calendar problems below are relative ("Friday morning", "three weeks ago") or schedule arithmetic. Sunset at Watkins Glen on 28 Aug 1976 comes out at 7:46–7:47 p.m. EDT, which matches the text's 7:46. Game 6 of the 1975 World Series (Doyle out at the plate in the 9th, Evans's catch in the 11th, Fisk at 12:34 a.m.), *Born to Run* ("three weeks ago" on 15 Sept), "Don't Go Breaking My Heart" (#1 Aug–Sept 1976), *Horses*, *Cuckoo's Nest*, "Convoy", the Staten Island Ferry quarter and the Carter nomination all check out.

Severity: **P1** breaks canon, a rule, or the finale; **P2** is a visible contradiction or a false cross-reference; **P3** is polish or a nit.

---

## 1. P1 — must fix

### P1-1. Clara says "go, go, go" (Rule 10), and the note claims she "wouldn't know" it (Rule 6)
- **PROBLEM.** `chapter-10`, M5 *The Field*, the squall: "Clara is running beside him in it… yelling *go, go, go*". The note under it says: "(She never says *go on*… *Go, go, go* is what Grace said, getting into the Impala… Clara wouldn't know.)" The clue ledger repeats it ("*Go, go, go* in the rain | … Clara doesn't know"), and "Go, go, go." is listed under Language.
- **WHY.**
  - Bible §6.3 and Rule 10: she never says "go on," **or "go,"** or anything that sends him away from her.
  - Rule 6: after IX M6, Ellis has consciously relived the Impala scene, and that scene opens with Grace's line "Go, go, go, you're late." Whatever Ellis knows, Clara knows, so "Clara wouldn't know" is false.
  - The planned handling was: Grace's "Go, go, go" stays inside the IX memory, and Clara says only "Come on" (X M7).
- **REPAIR.**
  - Replace the phrase with "…jumping puddles, yelling *come on, come on*, and he's laughing too…".
  - Replace the parenthetical with: "(She never says *go*. She never has. *Come on* is toward her.)"
  - In the ledger row, change the moment to "*Come on, come on* in the rain" and the meaning to "Toward her, never away."
  - In the Language list, change "Go, go, go." to "Come on, come on."

### P1-2. Tolliver Bend is on the wrong side of the farm for the crash to happen on the way to town
- **PROBLEM.** The chapters consistently place the Bend *beyond* the farm, away from the South Fork road and town:
  - VIII M14: "Two miles past the farm the road starts to curve right."
  - IX M4 report: "0.3 MI S OF HENSLEY RES," with the Hensley house "past the farm." "VEH 2… NORTHBOUND" means the Impala was southbound.
  - IX M6: "the same road… in the same direction."
  - On 12 April 1973, though, Ellis left the farm at 7:32 to take Grace home (Cold Branch Road, north of town) and then play Marlon's (in town). Heading south past the farm takes him away from both.
  - IX M13 is also inconsistent inside itself: the bikes ride round the Bend ("Two miles past the Tolliver farm…") and only then reach "**The farm.**"
- **WHY.** It is the central event. The player drives this road (VIII) and then reads a document (IX) that puts the car heading the wrong way. The same error is in bible §3.2.
- **REPAIR.** Keep every existing beat and make Tolliver Road a through road:
  - **Bible §3.2**, append: "Past the Bend, Tolliver Road climbs back to the Tanner Valley road east of Roy's: the back way into town, which Wayne told the children to use whenever it rained, because the low-water bridge on the South Fork road floods."
  - **VIII M14**, after "Tolliver Road.", add: "It runs on past the farm and the Bend and comes out on the Tanner Valley road: the back way home. The way you go when it's raining and the low-water bridge is under."
  - **IX M6**, after the dashboard clock line, add: "Rain. The low-water bridge will be under. He turns right out of the farm lane, the back way, the way Daddy always said."
  - **IX M13**: move the "Two miles past the Tolliver farm…" paragraph so it comes after **The farm.** and begins "Going home the back way,".
  - This also rhymes the crash with "Low Water".

### P1-3. Wayne's twenty has four contradictory states
- **PROBLEM.**
  - VII M16: "He doesn't spend it. (It's still there in Chapter X.)" The player is given no choice.
  - VII M19: "He pays with the twenty Wayne put in his jacket, if the player kept it… If the player spent it, he pays with something else." But there is no way to have spent it.
  - Bible §13: "otherwise still in the corduroy jacket, which is in the van in X." In X the van stays home ("The van is staying home"), and the epilogue puts the corduroy in the festival duffel (Ep M4).
  - Ep M1 puts it in his **wallet**, "if the player kept Wayne's twenty… and didn't spend it on the jacket."
  - X never mentions it.
- **WHY.** V4 Part 4 says "the ELLIS shirt and Wayne's twenty (both carried to X)". As written, the tracked object teleports.
- **REPAIR.** Make it one path: never spent, and carried in the leather jacket.
  - **VII M19**: replace the two sentences with: "He pays out of his Civic money. Before the corduroy goes into a paper sack he goes through its pockets: Winstons, a carpenter's pencil, and Wayne's twenty, still folded in quarters. He moves it to the inside pocket of the leather."
  - **VII M16**: change "(It's still there in Chapter X.)" to "(It's still on him in Chapter X.)"
  - **Ep M1**: drop the parenthetical from the wallet list. Before the envelope, add: "In the inside pocket, a twenty-dollar bill folded in quarters. Wayne knows the fold. Behind it, a white envelope…"
  - **Bible §13**: "Wayne's twenty… never spent; moved to the leather jacket's inside pocket in New York; returned to Wayne with the personal effects (Ep M1)."

### P1-4. Two lines in the finale contradict the final stage geometry (bible §13 FINAL)
- **PROBLEM (a).** `chapter-10`, M8 *Home*, withheld-home bullets: "The **sun-gun** stays on him from the stage-right wing, white on the left side of his vision."
- **WHY (a).** At that moment Ellis is at the stage-left lip facing downstage toward Clara, so he faces east. The stage-right wing is south of him, which is on his **right**. The light is only on his left once he turns to face upstage, which is the whole point of the turn.
- **REPAIR (a).** "…white at the right edge of his vision."
- **PROBLEM (b).** M8 *The turn*: "Three yards to his right, at the riser's stage-left corner… Riley."
- **WHY (b).** Ellis is about a yard from the stage-left edge. The riser is upstage centre, and M9 has Riley take "six steps to the edge". Facing upstage, that puts Riley ahead of him and to his **left**. Only the edge and the gap are on his right. The bible's "toward Riley's side" is also loose.
- **REPAIR (b).** "Ahead of him and a little to his left, at the riser's stage-left corner… Riley, her hand out toward him, open. He was turning toward her. The swerve takes him the other way." In the bible, change "toward Riley's side" to "away from Riley, toward the edge."
- **Also (P3).** M8 *"Shape Note"*: "the stage goes white on the left side of his vision." Add "(he's turned in to the square, facing the riser)" so the planted flinch comes from the correct side.

---

## 2. P2 — visible contradictions and false references

### Calendar and durations
- **P2-1. VIII M7 *Eleven Times*.** "Earlier, at the hotel desk on **Friday morning**, Dex found Cal… and the player… had the whole day and the second Amphitheatre show to carry that." The mission takes place at 12:50 a.m. on Friday, *after* the second show (Thu 29 Jan), and M6 says Dex "is supposed to leave for Detroit tomorrow." **REPAIR:** "Thursday morning."
- **P2-2. VIII M8 *Walt's bench*.** "Monday evening… Cal got off the Greyhound **at noon** after nineteen hours." He boarded at Kenosha at 3:40 a.m. on Friday, so nineteen hours puts him in about 11 p.m. Friday. **REPAIR:** "Cal got off the Greyhound late Friday night after nineteen hours. It's been three days."
- **P2-3. IX M7 *Day four*.** Clara: "Five weeks." Ellis: "Nine." The actual gap is the first pill (8 Apr) to 4 Jul: **12 weeks 3 days**. Ellis always knows the day, so his figure must be right.
  - The IX clue ledger's "Absent for nine weeks" and the macro's "Gone for five weeks" carry the same error.
  - Day two's "after two months" is short too.
  - **REPAIR:** Clara: "Two months." Ellis: "Twelve weeks. Since the eighth of April." Ledger: "twelve weeks". Day two: "after nearly three months." Macro IX: "Gone for twelve weeks."
- **P2-4. IX M10 *Count*.** "Qty: 60. Filled 6/24… Fifty-two." Then six more in the Sucrets tin. 52 + 6 = 58 means two pills taken since 24 June. But he took them twice a day from 24–30 June (14 pills) and "hasn't taken one since July first." This is a count the player performs.
  - **REPAIR:** change "Fifty-two." to "Forty." in both places (40 in the bottle + 6 palmed in the tin + 14 taken = 60).
  - Design summary: "Riley counted to forty"; objects: "the Sucrets tin (40 and 6)".
- **P2-5. IX M15 vs X M6.** IX has Eddie offer "A sunset slot, 7:30, before the headliners." X has the storm cause "The Blakes' **four-thirty** slot becomes seven-thirty." **REPAIR** in IX: "A late-afternoon slot, 4:30, before the headliners."
- **P2-6. IX M9 *Wondrous Love*.** Wayne sings "a line his mother taught him **fifty** years ago." He is 47. **REPAIR:** "forty years ago."
- **P2-7. The van promise was made on Fri 2 May 1975 (V M15 *Four Hands*, Fri 2 May, the van in Marlon's lot), not in April.**
  - VII M17: "in the van, in April"; VII M17 note: "In April the four of them made four promises in the van."
  - VIII world state: "a promise made in a van in April"; VIII M1: "It was Dean's clause, in the van, in April."
  - **REPAIR:** change "April" to "May" in all four places.
- **P2-8. Ep M6 *The balance*.** "Six left, Wayne. Sixty-nine dollars." The schedule is coupon 19 = Oct 1974, one a month, so coupon 48 falls due in **March 1977**. Only one should be left unless Wayne stopped paying.
  - **REPAIR:** "Six left, Wayne. Sixty-nine dollars. You quit paying in October." / **WAYNE:** "Hm."
  - This also sharpens the scene.

### Objects
- **P2-9. The Polaroid's owner flips.** In II M10 and IV it lives in the frame of Ellis's mirror; it is his. In X M1, "Dean… has a Polaroid in his shirt pocket he keeps touching", and in M6 Dean takes it out of *his own* pocket. Then Ellis puts it in Dean's pocket: "Keep it." / "I'll lose it."
  - **REPAIR** X M1: cut the Polaroid from Dean's pocket and make it "a sobriety chip in his shirt pocket he keeps touching."
  - **REPAIR** X M6: "Ellis takes something out of the inside pocket of the leather jacket (he took it out of the mirror frame on Sunday night) and puts it face up on the fruit tray."
- **P2-10. Memo-book counts in Ep M3.**
  - "A box of memo books… **1 through 72**, in order." But 71 is in the duffel (Ep M4, M5) and 72 is open on the dresser. **REPAIR:** "1 through 70."
  - "the last entry, in pencil, from the bus on August 26" comes after the 28 Aug entry "D.H.: 'Stop.'" in the same sentence. **REPAIR:** "the last money entry."
- **P2-11. Ep M3 *Marlon's*.** Cal brings "the Friday money from the fall of 1974… settled." But VI M16 *Marlon's* already had Cal pay "the last of Marlon's loan… plus interest", and Marlon pushed the interest back.
  - **REPAIR:** "an envelope: the interest Marlon pushed back across the bar last summer, which Cal has kept in the back of the ledger ever since." Keep "the way he did in Chapter VI."
- **P2-12. Ep M6 *Opening Day*.** "It had four tickets in it when **Wayne bought it** on Christmas Eve 1974 and left it where Ellis would find it."
  - In V M1, Ellis gives Wayne the envelope ("Ellis takes an envelope out of his coat and puts it on the table next to Wayne's cup").
  - V's book reads "OPENING HOMESTAND — GOOD FOR ANY APRIL HOME GAME." The epilogue says "good for any home game, no expiration."
  - "Roy always gets three hot dogs, the story from Chapter V" is wrong too: in V it is *Grace* who "Ate three hot dogs," in Wayne's story.
  - **REPAIR:**
    - "…when Ellis gave it to him on Christmas Eve 1974, in an envelope next to his coffee cup."
    - "OPENING HOMESTAND — GOOD FOR ANY APRIL HOME GAME, 1975. The boy at the gate looks at the year, looks at Wayne, and tears them anyway."
    - "Wayne buys three hot dogs and eats one. Roy looks at the other two. 'Grace ate three once,' Wayne says: the story from Chapter V, told to somebody else for the first time."
- **P2-13. VII M16 design note.** "He has done it all game: the heater, the half a tire, **the Maxwell House can**." The can is not Wayne leaving money; it is Ellis's rent that Wayne *saved* (IX M13), and naming it here spoils IX. **REPAIR:** replace "the Maxwell House can" with "the Engineers tickets he never used without Ellis."

### False cross-references
- **P2-14. The locations of "Liar" are wrong twice.**
  - VIII M4: "the way she said it in October 1974, sitting on his bed, and in December on the stairs."
  - X M8: "In Chapter I on his bed. In Chapter V on the stairs."
  - In I M9 she is "sitting on the floor under the window"; in V M1 she is "sitting on the sill."
  - **REPAIR:** "in October 1974 on the floor under his window, and at Christmas on his windowsill." In X: "In Chapter I on the floor under his window. In Chapter V on the sill."
- **P2-15. VII M19 *The mail*.** "A looping, careful hand the player has seen before, once, in Chapter I, on the back of a birthday card in a cigar box in a room with the door closed." The player never enters Grace's room in I, and the cigar box first appears in IX M13.
  - **REPAIR:** "A looping, careful hand the player hasn't seen before. (They will, in Chapter IX, on two birthday cards in a cigar box.)"
- **P2-16. X M4 *Press Tent*.** "…second best in the South. **I'd have told you it was fourth.** I was wrong." In IX M5 he ranks Sylva "Second" on the first taste. Fourth place is the "crime against God and peanuts" stand, and VII M7 puts the Spur stand at #2.
  - **REPAIR:** "For two years I had a stand on the Spur in second. I was wrong. You have to go back and check things."
- **P2-17. Ep M5 poem.** "An hour later you called from **your mother's kitchen** / and said it back." In VII M15, Riley calls from Cutler Street ("Cutler Street, the kitchen, the wall phone"). **REPAIR:** "called from your kitchen on Cutler Street." Apply the same change in all three variants.
- **P2-18. Five promised payoffs never arrive.**
  1. VII M6 replay: if Ellis left the converter on 97.1, Wayne says in IX "Somebody moved my radio last fall"; otherwise the converter is still on 88.9. Absent from IX.
  2. VII M9 tracked: the chickweed line ("Somebody did the chickweed") in IX. Absent.
  3. VII M1: "The player won't find out where it [the record] went until Chapter IX." Absent.
  4. VII M13 downstream: IX shows the F-100 glovebox of clippings with *Rave* folded open to Grace. Absent. The bible lists this as something Wayne hides.
  5. VIII M17: "Dr. Lusk writes to Wayne… The letter is in the epilogue." Absent.
  - **REPAIR (one insert fixes 1–4).** In IX M5 *North*, add to the passenger options:
    > "open the glovebox for a map: no map. Every clipping about the band, folded flat, and on top the *Rave* article, open to the paragraph about Grace. Behind the seat, a copy of *Borrowed Stone* still in its shrink-wrap. (If the converter was moved in VII: 'Somebody moved my radio last fall.' If not: it's on 88.9.) (If Ellis pulled the chickweed: 'You been up the hill.' / 'How do you know?' / 'Somebody did the chickweed.')"
  - **REPAIR (item 5).** In Ep M6 *Thin*, add:
    > "On the kitchen table, a letter on university letterhead, opened and read and folded back: *Dear Mr. Blake, I only met your son three times…* — H. Lusk. Wayne keeps it in the coupon book."
- **P2-19. X M4.** "*'Loud.'* (…some of the writers laugh, and **Dex, who knows the story**, doesn't.)" The story is Wayne at the Lantern loading dock (VII M16), and Dex wasn't there.
  - **REPAIR:** "(…some of the writers laugh. Ellis doesn't. It's his father's word.)"

### Plan compliance and documents
- **P2-20. The macro is out of sync with the final canon.**
  - `02-macrostructure.md` X, **Riley**: "At the riser's **stage-right** corner." It should be stage-left, per bible §13 FINAL.
  - Macro IX: "Gone for five weeks." See P2-3.
  - Macro VIII M8: "Sun Feb 1 – Tue Feb 3." The chapter runs to Wed Feb 4.
  - **REPAIR:** update the macro.

### Geography
- **P2-21. The route home in Ep M1 is backwards.** "Route 17 **west** along the Southern Tier… then south on I-81." From Montour Falls or Elmira, Route 17 **east** leads to I-81 at Binghamton; west leads away from it.
  - X M9 has the ambulance going "Route 14 along the lake, toward the hospital in Montour Falls, forty minutes." Montour Falls is about 10 minutes from the Glen, and the route to it is not along the lake.
  - **REPAIR:**
    - X M9: "Route 14 south, toward the hospital in Elmira, forty minutes."
    - Ep M1 (header and body): "Elmira, New York… Route 17 east along the Southern Tier to Binghamton, then south on I-81."
    - Ep M1 also has Pettigrew driving 900 miles between an 11 p.m. call and noon, which is not possible. **REPAIR:** "He called from a truck stop in Virginia at seven this morning; he'll be here by dark."
- **P2-22. X M2.** Dean: "More people than live in *Georgia*." / "(It isn't. It's close to the population of Laurel City…)" Laurel City is half a million (bible §3.3); the crowd is 150,000.
  - **REPAIR:** "(It isn't. It's seventy Hollow Ridges, and Dean will spend the evening telling everyone that.)"

### Clara rules (VII)
- **P2-23. VII M12 *The radiator*.** Clara: "**Go ahead.** Tell her about the car." This is imperative "go," sending him toward Riley, so it breaks Rule 10. **REPAIR:** "Tell her about the car, then."

### Names
- **P2-24. Two men called Russ in Chapter IX**, plus a Rusty in VIII: Russ Pickett, Frank's assistant (IX M1); Russ Mandel, the *Late Hour* host (IX M3); Rusty Kowalczyk (VIII M3). **REPAIR:** rename the assistant "Lamar Pickett".

---

## 3. P3 — polish

### Calendar and arithmetic
- **X, world state and M1.** "Dean seven weeks sober" on Thu 26 Aug. The sober count (six days on 16 Jul, eight weeks on 5 Sept) makes 11 Jul day one, so 26 Aug is 6 weeks 4 days. **REPAIR:** "nearly seven weeks sober." M3/M6/M8's "Seven weeks tomorrow" is correct.
- **VIII M9.** "You were in the hospital **three weeks** ago." It was 27 days: "a month ago."
- **VIII M10.** "since the tour ended. **Three weeks.**" It was 26 days: "Almost a month."
- **VIII M7.** "Eleven times **this week**." Cal's column runs 19–30 Jan: "in two weeks."
- **VIII M4.** "In **seventy-odd** notebooks since he was fourteen." This is number 68: "In sixty-eight notebooks."
- **VIII M5.** "an open line, **four hundred** miles long" (Akron to north Georgia): "six hundred."
- **VII M16.** "He's made **$378 a night** since November." One Civic night paid that: "He made $378 in one night in November."
- **VII M8.** Ledger: "Band 1/3 after hall & promoter — $2,400.00." One third of $7,110 is $2,370. **REPAIR:** "Band guarantee — $2,400.00."
- **IX M13.** "every Friday starting **October 25**, 1974." II first shows the RENT envelope on Fri 1 Nov, and on Sat 26 Oct says "rent… is due Friday." **REPAIR:** "November 1"; also the epilogue's "Every Friday from October 1974."
- **IX M15.** "*Dad — Sunday?*… dinner, the Sunday after New York, **August 29**, at the kitchen table on Cold Branch Road." Both men will be 900 miles away. **REPAIR:** "the first Sunday he's home after New York." Ep M1's truck-stop biscuit still works.
- **Ep M7.** "twenty years after a label released it… as *Last Light*" (1977 to 1996 is 19): "nineteen years."

### Clara rules and tone
- **VII M13.** Clara: "Let's go." It isn't a send-away, but it breaks the letter of Rule 10. **REPAIR:** "Drive."
- **Rule 13** (she vanishes only for Wayne or Lorraine's handwriting). "Clara's gone" at VII M12 (after Cal), VII M18 and VII M9 ("gone by the gate") are unexplained vanishings. **REPAIR:** show her leaving. For example, VII M12: "Clara slides off the radiator and goes round the corner by the stairwell while Cal and Ellis look at each other."
- **"She never touches anything"** (VIII M14, IX M14, X M5, X M8) is contradicted by VII M13 "puts one finger on the page" and IX M11 "puts her finger on the page." **REPAIR:** "points at her name, a finger's width above the paper."
- **IX M9.** "Clara is at his shoulder, **suddenly**." This is a stinger (tone rule 6). Cut "suddenly."
- **IX M5.** Hollis names "Opal Hensley's porch light… Opal had her hand," and the note steers the player toward her at the bar. V4 said "The player may put it together; the game doesn't point." **REPAIR:** Hollis: "The Hensley place. The lady there let me use the phone… she had her hand." Cut the design-note sentence.

### Unplanted "since Chapter N" claims (true to the plan, never shown)
- VIII M5: Cal's "roll of dimes… since Chapter IV." Not in IV.
- IX M2: the Philco "in the background of every Mercer shop scene since Chapter I." Not in the text of I–VI.
- IX M15 and X M8: Riley "on every song's ending since Chapter II" at the riser's stage-left corner. It never appears in I–VI. **REPAIR:** plant one line in VII M8's last chorus: "Riley drifts back to the stage-left corner of the riser, where she always ends up."
- X M6: "In the ledger, since Chapter II: *D.H. owes E.B. $4.00*." II has no ledger line. Add it in II M9 after "You owe me four dollars": "Cal writes it down."
- X M8: Carla's letter "where Dean moved it when he bought the kit in Chapter VI." Not shown in VI. Acceptable, or say "when the Vistalite came."
- VII M7: the peanut list "from Chapter IV." It is a V collectible (V M3 *Six Dates*): change to "Chapter V."
- Ep M3: van ceiling "a cow in a field in Chapter IV." In IV the cow is in the road, with no SX-70: "a cow in the road."
- Ep M5: the notebook "blank on his nightstand in Chapter VIII." VIII shows only the porch; VII shows the dresser. **REPAIR:** "on his dresser in Chapter VII, on the porch at the end of Chapter VIII."
- VIII M14: "In Chapter I… a county sawhorse… with a **DETOUR** sign… The sawhorse is gone." I M1 (free-roam note) says "ROAD WORK — LOCAL TRAFFIC" and that it is gone from II onward. **REPAIR:** use I's sign text and "gone since the fall of 1974; the refusal was always his."
- **Coda.** "The sawhorse is across it, where it was in Chapter I." On 9 Nov 1974 it is already gone (I design note). **REPAIR:** "No sawhorse. Ellis brakes at the turnoff and turns around: 'Other way's quicker.'"
- VIII M13: "at **six** in the 1964 portrait." The bible and Ep M6 say five: "at five."
- Ep M6: Joan's voice, "heard once before, at a graveside." Wayne also heard her call "Holy Manna" at the Tabernacle: "heard twice."
- Ep M6 recap: "Coupon 33 at the Lantern" should be "in the kitchen before the Lantern"; "Coupon 36 in Riley's hands" should be "under Riley's coffee cup."
- X M9: "the only name-only line the game has saved for her." Riley says "Ellis." alone in VII M14. **REPAIR:** "the last line the game gives her tonight."
- X M9 design note: Kit's "name appears in one line of a court document and nowhere else." Ep M7 has Joel discuss her and a title card. **REPAIR:** "In the epilogue her name appears once, on a title card."
- Ep design summary: "a still of him **falling** on the cover." The footage flares and he's gone (X M9), and X M3 describes the cover as him at the edge. **REPAIR:** "a still of him at the edge of the stage."
- IX M9: "everybody knows the first verse, because *Rave* is about to print it." They can't know it yet. **REPAIR:** "the first verse comes; it's the part he wrote before the pills."
- IX M2: first week of June, "number 70, **and the green notebook**." Ep M5 dates its first page 7/4/76. **REPAIR:** "and the green notebook, still blank, under his elbow."
- IX M11: Monarch copied memo books "1 through 67" from a tour bus. Ellis carrying 67 notebooks on tour is implausible; the macro says "from the van." **REPAIR:** "from the van, where he kept the carton."
- Ep M3: "The Jazzmaster **isn't here**. It's in a case in the corner." **REPAIR:** "The Jazzmaster is in its case in the corner…"
- Ep M5: Hannah in Sept 1976 has "Her class." Riley's roommate would be a senior. **REPAIR:** "the class she's student-teaching."
- Ep M1: truck stop "in the Shenandoah Valley… where the band's van stopped in December." VII M19 put that stop near Wytheville: "off I-81 near Wytheville."
- Ep header ends "Saturday, April 16, 1977." The last dated scene is Thu 14 Apr: "Thursday, April 14, 1977."
- Ep M6 "Where" includes Linwood; the at-a-glance row omits it.
- Ep M6: "a sack of peaches… from a can." **REPAIR:** "a jar of peaches Evelyn put up."
- VIII M12: Riley drives "an hour and a quarter" from Tannersville; VII M15 says "It's an hour." Pick one.
- IX M5: "Balsam Gap." From north Georgia to Sylva the road crosses Cowee Gap (US 441); Balsam Gap is on the far side of Sylva. **REPAIR:** "Cowee Gap."
- VII M19 knowledge note: Lorraine "learned from a magazine… that her daughter died in a car he was driving." She was at the funeral. **REPAIR:** "read in a magazine what she'd heard at the back of a church."

### At-a-glance tables that disagree with mission headers
- IX, M6: glance "Ellis → Riley"; body "Ellis (at sixteen) → Ellis → Riley."
- IX, M15: glance "Ellis → Riley"; body "Ellis → Riley → Ellis."
- X, M5: glance "12:30 – 2:45"; body "12:30 – 2:50."
- X, M6: glance "2:45 – 7:10"; body "2:50 – 7:10."
- X, M8: glance "7:30"; body "7:26."
- X, M9: body "(no one) → Riley → Cal → Dean → Wayne"; glance omits "(no one)."
- VII, M16: glance "Fri Dec 5"; body "Wed Dec 3 (kitchen); Fri Dec 5."
- VII, M12: glance "Sat Nov 15"; the scene is 1:40 a.m. Sunday. Say "Sat Nov 15 (night)."

### Period and technology
- **VIII world state.** "Carter has won Iowa." The caucus was 19 Jan and the chapter opens 12 Jan: "Carter is campaigning in Iowa."
- **VIII.** "*Frampton Comes Alive!* is in every dorm" in January. It was released 6 Jan and was everywhere by spring. Move to the March beats.
- **VIII M3.** Sawtooth has "two platinum records." RIAA platinum was first awarded 24 Feb 1976. **REPAIR:** "two gold records."
- **X world state.** "Hurricane Belle… left the Finger Lakes soaked." Belle came ashore on Long Island and tracked through New England, and it is doubtful for the Finger Lakes. **REPAIR:** "a wet August and a week of rain."
- **X M2.** The sun-gun is "Twelve volts and a thousand watts" on a battery belt. Period units were about 30 V and 250–650 W. **REPAIR:** "Thirty volts and six hundred and fifty watts." Change "a thousand watts" elsewhere in X to "six hundred and fifty watts."
- **VIII M4.** The bus is "somewhere south of Toledo" on the way to Cleveland. I-75 south of Toledo heads to Dayton. **REPAIR:** "east of Toledo on the Turnpike."

### Names
- Darla Kay Hinson (IX M12) is close to Donna Kay (Sisk) Carson and to the Hensleys. **REPAIR:** "Charlene Hobbs."
- Nadine **Crowe** (VIII M9), Lynette's mother: if Crowe is Lynette's married name, her mother wouldn't share it. **REPAIR:** "Nadine Pike," or state that Lynette took back her maiden name.
- "Mr. Ridge" of the Ridge Pharmacy (VII M13, Ep M2) is named after the town. **REPAIR:** "Mr. Cantrell."
- Gene Poteet (VII M13) adds to the Pettit/Pettigrew cluster. Optional rename.

### Bible sync (no chapter change needed)
- §4: "1970 — Grace (11) gets a cassette recorder." She turned 12 on 2 Nov 1970; IX is correct.
- §8 Wesley: "fourteen in the epilogue." The epilogue has him 13 (1976) and 33 on Marlon's stage (1996).
- §10.3 "Borrowed Stone": listed as Chapter V with "a book in the truck." VI and VII say VI and "a book on the table."
- §8 Patty: "In the epilogue she… has the letter framed." Not paid off. Either add one line to Ep M4 ("Patty's violet envelope reply, framed, on her dorm wall") or drop it from the bible.
- §13, Wayne's twenty: see P1-3.

---

## 4. Required counts (whole game, grep-verified)

**Clara's "Liar" — exactly 3.**
- I M9 (`chapter-01`, l.2026)
- V M1 (`chapter-05`, l.271)
- VIII M4 (`chapter-08`, l.429)
- Grace's "Liar" in X is the payoff, not a Clara line. ✔

**"El" — once, spoken.**
- IV snapshot, in Grace's writing ("*El caught it, I held it. G.*")
- V M16 *Where Did We Meet?* — Clara's only use. ✔

**Clara's "Daddy" — once.**
- VIII M14, "GRACE/CLARA: Daddy'll kill us both." Everywhere else she says "your daddy." ✔

**Clara saying "go".**
- X M5, "go, go, go": **violation**, P1-1.
- VII M12, "Go ahead": **violation**, P2-23.
- VII M13, "Let's go": borderline, P3.
- X M7, "Come on. They're waiting on you.": correct.
- IX M6, Grace's "Go, go, go, you're late": Grace, not Clara, so correct in itself; but see P1-1.

**Rules 3, 4, 5, 7, 8, 9 and 11 hold in VII–X.**
- Riley's point-of-view shots at the seventh chair and the finale riser are permitted echoes.
- The camera catches on Clara in VIII (bus, *Night Stage*) and on the empty chair in IX, and fails each time.
- She enters Grace's room once, in IX M14.
- She is absent from the cemetery (VII M9, Ep M2) and from the coda, and no character remarks on it. ✔

---

## 5. Knowledge-state check (VII–Epilogue)

Apart from the errors already listed (P1-1; P2-19; the Ep M6 phone call), who-knows-what holds:
- **Clara's name.** Wayne from Aug '75 (VI M14) → Riley (VIII M12) → Ellis told by Riley (VIII M15).
- **The crash facts.**
  - The country learns he was driving from *Rave* (VII).
  - Wayne knew about the truck the next day and admits it (IX M4).
  - Hollis couldn't make out Grace's last words (IX M4 statement and M5).
  - Only X gives the last three lines.
- **Cal and Theo.** Riley (VI) → Ellis (VII M12) → everyone, from Cal (VIII M8).
- **Marlon's secret.** Cal tells Ellis without the name (IX M12) and tells Marlon he kept it (Ep M3).
- **The argument.** Ellis and Riley (IX M6).
- **The tab.** Ellis (X M3), then Dean alone (Ep M4).
- **Lorraine's letter.** Ellis (unopened), then Wayne, who hands it back (Ep M2).
- **The M. poems.** Riley; Dean sees only the "M."
- **The train line.** Riley alone.

One soft spot: in IX M6, Riley's option "a truck came over the line" assumes Ellis told her about the report off-screen. Acceptable.

---

## 6. Plan compliance (V4 Part 2)

**Compliant:**
- No LSD taken; the tab is put back and later flushed by Dean.
- Roy's "Go on. Get up there."
- Withheld home with no timer: the band tires, Cal's hand cramps, Riley's voice cracks.
- Hollis can't make out the words.
- Ellis is fifteen in the 1972 afternoon, which has chores and jokes.
- *Late Hour* is fluent, with no second silence.
- The outing: Cal provokes first; Tully's "That's enough" and the crew truck; "Theo's mine. That's real."; Dean's coffee the day after.
- The medication thread: "New Skin" finished while medicated, sleep, Tater on his boot, Riley's laugh, the Tabernacle crack carried by Cal, no verdict.
- Kit Adair gets two humane beats (the tape line; Tully on the case).
- The press tent gives the peanut ranking.
- Mrs. Pardue's line; Carla's letter on the kick drum; Cal's "since August"; the Engineers tickets.
- The epilogue runs about 110 minutes plus the coda, which is on target. "Number One" is folded into "The List." Clara is absent from the coda and no one remarks on it.
- The 1996 epigrams, Riley's maps, Dex's "I sold a lot of magazines" and Wayne's closed door.

**Deviations:**
- P1-4: two geometry lines.
- P2-20: macro still says stage-right.
- P3 (IX M5): Opal is pointed at.

---

## 7. Real-city leakage

A grep across **all** chapters for Atlanta, Nashville, Tennessee, Peachtree, Braves, Falcons, Opry, Ryman, Music Row, Vanderbilt, Emory, Buckhead, Juniper, Midtown and I-75/85/40/24/59 found:
- No Atlanta or Nashville terms.
- "Midtown" only for New York (VII, three times; IX, once), which is allowed.
- "I-75" only in Ohio (VIII M4), which is fine.
- "University of Tennessee" once (V M4), for Knoxville, which is an off-map real town. Acceptable; optionally make it "a college bar by the campus."

"The Row" and the Tabernacle's history (Jubilee 1943 – March 1974) are analogs by design, not leaks.

---

## 8. The 25 most important fixes, ranked

1. **P1-1.** Clara's "go, go, go" in the X squall: change to "come on, come on", fix the Rule 6 note, the ledger row and the Language list.
2. **P1-2.** Tolliver Road as the back way past the Bend: bible §3.2, VIII M14, IX M6, and reorder the IX M13 bike ride.
3. **P1-3.** One path for Wayne's twenty: VII M16/M19, Ep M1, bible §13.
4. **P1-4a.** X M8 withheld home: the sun-gun is at the *right* edge of his vision while he faces downstage.
5. **P1-4b.** X M8 *The turn*: Riley is ahead and to his *left*, not "three yards to his right"; fix the bible's "toward Riley's side."
6. **P2-18.** Five missing payoffs: one insert in IX M5 (glovebox, record, converter, chickweed) and one in Ep M6 (Lusk's letter).
7. **P2-12.** The Engineers ticket book: Ellis gave it; valid for "April home games, 1975"; the three hot dogs are Grace's story.
8. **P2-9.** Polaroid provenance in X M1/M6: Ellis has it, then gives it.
9. **P2-4.** IX M10 pill count: 52 becomes 40 (and in the summary).
10. **P2-3.** Clara's weeks away in IX M7: "Twelve weeks", plus the ledger, Day two and the macro.
11. **P2-5.** IX M15's slot: 4:30, delayed to 7:30 in X.
12. **P2-14.** "Liar" locations in VIII M4 and X M8: floor under the window, windowsill.
13. **P2-15.** VII M19: remove the false "seen in Chapter I" claim about Lorraine's hand.
14. **P2-16.** X M4 peanut line: "had a stand on the Spur in second."
15. **P2-2.** VIII M8: Cal's Greyhound arrives Friday night.
16. **P2-1.** VIII M7: Dex at checkout on *Thursday* morning.
17. **P2-7.** The van promise was made in *May* (four places).
18. **P2-8.** Ep M6: "Six left… You quit paying in October."
19. **P2-17.** Ep M5 poem: "your kitchen on Cutler Street."
20. **P2-11.** Ep M3: Marlon's envelope is last summer's refused interest.
21. **P2-10.** Ep M3: memo books "1 through 70"; "last money entry."
22. **P2-21.** Ep M1/X M9 route: Elmira, then Route 17 *east*; Pettigrew arrives by dark.
23. **P2-23.** VII M12: "Tell her about the car, then."
24. **P2-13.** VII M16 note: drop "the Maxwell House can."
25. **P2-20 and P2-24.** Sync the macro's stage-left corner and five weeks; rename Russ Pickett.
