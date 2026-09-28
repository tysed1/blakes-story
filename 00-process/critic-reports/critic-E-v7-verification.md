# Critic E: V7 Verification of Chapter X and the Epilogue

*X and the epilogue read line by line; IX M8 and M13–M15, bible §5, §6.3, §11.3, §12 and §13, the V3 sheet, Critics C and D, and V6–V7 read against them. X and the epilogue diffed against `f625f14`, the last commit before the rebuild. VII not audited.*

---

## 1. Did the findings land?

| # | Verdict | Evidence / what's left |
|---|---|---|
| **E-1** | **Landed, one regression** | "The band lands it… A second of silence, the right kind." The light comes after the roar; the telegraphs and "the loudest sound" are gone; the hold is capped and the figure rounded. **New telegraph** in "Shape Note": "She'll need it at the end, when he wants the bow." Cut it. "The world clock stops" can read as the world freezing: write "counts no further than about three minutes." |
| **E-2** | **Partly** | The verse is now fragments and the "the player hears…" lines are gone. But it still runs line/cut ×3, in near-canonical order, one option leaks what the rain took, and the default third line is transcript. See §6. |
| **E-3** | **Landed** | "Late, is what. Push your hair out of your eyes…" / "Come on. They're waiting on you." One gloss to cut: "She means it." |
| **E-4** | **Landed** | "It wasn't your—" / "You done good up there." / "Son." is the only line said whole. The EMT's "*son*, you have to let go now" to Dean, eight minutes earlier, dilutes it. Cut the word. |
| **E-5** | **Partly** | Six of the seven cuts are confirmed by the diff. M8's narration still cites earlier scenes nine times ("the way she perched on a crate in Chapter I," "through Marlon's window," "went dead at the Lantern in Chapter V," "the way he did in July," "to three strangers on a plywood stage"…). Three lifted hands remain in M8. New callbacks: Dean's hand flat on his pocket twice, and the "New Skin" rescue repeated. Roy still says "Go on" twice in the coda, after "Wayne goes on." |
| **E-7** | **Landed; no branch broken** | "Then I'll play it by myself." "Stop" stays on the record in both ledger entries. The no branch breaks on the clock (§4.1). |
| **E-8** | **Landed** | §2. |
| **E-9** | **Landed; one number** | The order is 1996 → Tater → "Wayne goes on." → coda → post-credits. But the documentary is billed "~4 min" and ends on a track "for three minutes and forty seconds." Have the documentary fade the track out at about 30 seconds, before Dean's clicks: the film can't hold the open verse. |
| **T-3** | **Partly** | Ep M4: "It came back in the bag untouched. It's still here. He didn't take it." Then the coroner, then "He's not tempted; he's shaking because…". Add X M3's note and the X summary's "(he didn't)": five clearances. |
| **T-4** | **Landed** | "I'm carrying him." / "She carries."; M5 opens on "Maps"; the X M1 call to Joan. |
| **T-6** | **Partly** | He leaves before the coffee and the dish comes back washed, which is good. But the stone note brings the gloss back ("which the player hated Wayne for charging… He knows now") and contradicts the line before it: "He doesn't know yet what it's for." Cut the note. |
| **"El"** | **Landed** | "Hi, El. It's me." / "Don't get weird." on the unlabeled tape from IX M13. |

## 2. Geometry

**No hard contradiction** in X M8–M9 or bible §13. Left, right, upstage and the wings all agree. Facing Dean from a yard off the stage-left edge, the gap is behind him and to his right, so "the yellow rope catching behind his knee" is physically correct. Three soft points:

- **G-1, scale.** "A few yards off at the corner of the riser" and "She runs, the few yards to the edge," on a stage with a 40-foot truss and PA towers "like two office buildings." The real distance is 25–35 feet. Write "ten yards off" and "She runs the width of the deck."
- **G-2, facing.** If he literally faces Dean, the sightline passes almost exactly through the riser's stage-left corner, so Riley is dead ahead. The sun-gun comes in about 15° left, which is right for oncoming headlights. Add a blocking note: Riley stands a step stage-right of the corner, so "a little to his left" reads on screen.
- **G-3.** Bible §13 has the crew step out "as he turns home"; in the chapter it's the bow, after the song lands. Write "to catch his face on the bow." In "Roll forty," add "then on the deck" after "in the stage-right wing."

## 3. Clock

The anchors are right: sunset is 7:46 EDT at Watkins Glen on August 28, 1976, civil twilight ends about 8:15, and 8:04 "blue, then dark blue" fits. The order doesn't fit the times.

- **Sunset.** "Sunday Clothes" at 7:41 is the third song, which puts "New Skin" at about 7:48. The hills across the lake hide the sun before the flat-horizon 7:46, so "went down during 'New Skin'" is 3–6 minutes late. **Repair:** Joan hears Riley at **7:37**.
- **The fall (P1).** "Shape Note" ends about 8:10. Then three verses (5 min), the chant (1), the verse (2) and the capped hold (3): the last chord lands about **8:20**, not 8:41. The cap made this hole. More songs can't close it, because "Shape Note" must stay at twilight. **Repair:** move the fall to **8:22** everywhere. Keep 9:52, and add to M9 *Cal*: "It takes them forty minutes to get him up out of the gap." He then dies a few minutes short of Elmira, which fits "there's still a hospital."
- **The helipad.** M2's "helicopter pad marked with lime" invites the question why he went by road. Cut it, or add "The helicopter belongs to the headliner and doesn't fly after dark."

## 4. New contradictions, ranked

1. **The no branch of the vote (X M6).** "Stop" is at 6:10. On a no, "Eddie picks up the phone to call production." At 6:40 Roy says "We came to say good luck," and nobody mentions the cancellation. At 7:05 production says "Blakes, twenty-five minutes." Eddie's "Scratch that" comes 55 minutes after he picked up the phone. **Repair:** put *Wayne* before *Stop*. "Stop" at **6:50**, "for fifteen minutes," with Eddie on hold. Dean's "Stop" then follows the biscuits, which is stronger.
2. **The 8:41 fall.** See §3.
3. **Branch: the "New Skin" rescue.** 1996 Cal: "He lost a verse once. In the Tabernacle." He has now lost it twice, the second time on film. **Repair:** "He lost a verse. Twice. I played it for him up high." *(X M8's "the way he did in July" was cut in `6c7965f` while this audit ran; that part is resolved.)*
4. **Dean's count.** *Resolved in `6c7965f`:* "Seven weeks today," which matches IX's July 10.
5. **Memo books.** Ep M5: "(71 was already in Dean's sack.)" But in Ep M4 only the green notebook goes in the sack. M5 also claims "every" Observe line, but 73 went to Wayne with the effects. **Repair:** in M4, "the green notebook and memo book 71"; in M5, "and 73, from the hospital sack, under it."
6. **Wayne's twenty.** X M3 has "the envelope… and behind it Wayne's twenty," matching bible §13. Ep M1 reverses the order. Put the envelope first.
7. **Route.** Leaving Elmira at noon and reaching Wytheville at 10:20 p.m. puts Maryland at about 6 p.m., before dusk. **Repair:** "Maryland by suppertime, the Shenandoah at dusk." Not new: X M1's "I-83 into Pennsylvania" should be I-81.
8. **Small.** Ep M2, "where Tully parked the van": the van is under a tarp "since August" (Ep M3), so write "the crew truck." Ep M3, "last summer": write "the summer before last." Summary, "his last ninety seconds": a stopwatch figure, so write "his last minutes." Summary, "She was never in anyone's room but his": false (the VII Thanksgiving chair, the X trailer), so cut it.

**Clean:** the Polaroid path (IX M8 night two → "found it on his nightstand" → "Keep it." → M9 pocket); the letter; the coupons (six left at $11.50 is $69, exactly October–March); the ticket book (matches V: "Your mother could sing that," three hot dogs); Route 14 south, Route 17 east, Binghamton, Wytheville, Pettigrew; all weekdays and ages. **Clara rules:** all 13 hold. One risk to Rule 10's spirit: in M8 she "looks past him… upstage… at Riley… her hand coming out," which is a send-off without words and a hint to press HOME. **Owned phrases:** "Hm." in X is Wayne's alone; in the epilogue Wayne says it six times and Ellis once, which V3 allows. "Exactly." "Allegedly." and "Be specific." are all correctly owned. But "held the light so still" belongs to Riley, from VII's Observe line and the M. poem, and the verse option "somebody held the light so still" hands it to Hollis. Cut that option.

## 5. Anti-AI tells remaining

Superlatives are essentially clean, and there are **no em dashes in narration**.

| # | Where | Quote | Repair |
|---|---|---|---|
| 1 | X M1, M6 | "The game doesn't let them; it keeps the camera with Cal." / "The game lets him." | "Cal watches them from the walkway, too far to hear." Cut the second. |
| 2 | X M6 | "The player can see him take it: Ellis knows exactly where he is and when." Note: "…what his sister said after the white." | "Cal looks at his wrist. He nods, and gets up." Cut the note's last two sentences. |
| 3 | X M2 note | "It doesn't matter. Tomorrow night the last song goes somewhere nobody planned…" | Cut from "It doesn't matter." |
| 4 | X open, M8 | "Nobody in this chapter is a villain." / "He's a good cameraman. It's the right shot." | Three clearances of the crew; keep M2's. Cut these. |
| 5 | X M8 | "The last song on the list. The last song he wrote. The first time they've played it for anyone." / "It's the last light." | "The last song on Cal's list." Cut the title drop. |
| 6 | X M8 | "Holding off is *stay*, which is what Ellis has been doing for three years and four months." | "Holding off is *stay*." |
| 7 | X M8 | "…the way a man on the other side of the glass couldn't make them out." / "The player chose when the song ended. Nobody chose the light." | Cut both. Cut M8's "go on" note to "No drug is involved." (M7 already explains it.) |
| 8 | X M9 | "The player knows the grammar in their hands by now." / "Twice in Chapter VIII…" / "The third and last time the game breaks its rule…" / "For the first time in the game, the player is Wayne Blake." | This is a lecture at the moment of loss. Cut the first three. "The player is Wayne Blake." |
| 9 | X M9 | "because there's still a hospital, because there are forms, because you don't stop…" / "Seventeen days before his twentieth birthday." | "…and keeps driving. There's still a hospital." Cut the caption: Ep M4's September 14 pays it off. |
| 10 | X M2, M9 | "That's all, and it's enough." / "That's all she says." | Cut ", and it's enough." Cut the second. |
| 11 | X M2 | "(It isn't. It's seventy Hollow Ridges…)" | "(By supper Dean has worked out it's seventy Hollow Ridges, and tells everyone.)" |
| 12 | Ep M4 | "He's not tempted; he's shaking because it's the last thing Ellis decided, and it was *no*." | End at "He's shaking a little." |
| 13 | Ep M7 | The stone note; "Wayne understands it in the vet's office. His face doesn't move."; the Tater note | Cut all three. The vet's line and "Hm." carry it. |
| 14 | Ep M2, M3 | "…and none of them know why." / "That's the end of that." / "Nobody ever finds out." / "The history of the band nobody else kept." | Cut. |
| 15 | Ep M5, M7 | "the last real authorship choice in the game" / "It's his last choice in the game." | Cut. "Last" is the new "first time." |
| 16 | Ep M6 | Nina: "Everybody else was writing about genius. I just wanted somebody to write down how old he was." | This is Dean's "Nobody writes that" move again. Cut both sentences. |
| 17 | Coda | "There's nothing to do but eat a sandwich… with your father on a Saturday night in 1974." | Cut. |

## 6. The open verse

**One line is good.** "Rain on the roof like somebody counting" is the best line Ellis sings: concrete, heard, and it rhymes with the count-ins without saying so. The rest:

- **"You laughed at me in the dashboard light."** Players will hear Meat Loaf and smirk at the worst possible moment. "Laughed at me" is also a report, not an image.
- **"I kept saying stay, and you kept saying / go on."** The transcript returns as reported speech with a neat antithesis, and it makes the last line a quotation of Grace rather than plain. It also misstates canon: she said it once.
- **Structure.** Strict alternation. The text says "Not in order," but only "Stay with me" moves.
- **The options leak.** "You said I was lying and I was" names the word the cutaway says the rain takes. "A man with a flashlight couldn't make it out" is Hollis's testimony.

**Would it land?** The overlapped audio will. The lyric that 150,000 people hear, and that the bootleg carries, is the weakest writing in the finale.

**Proposed default:**

> *Rain on the roof like somebody counting.*
> *The oak in your window like a shut door.*
> *You laughed, and the rain kept the word.*
> *Go on.*

Line 2 is the bark filling the passenger window. It rhymes, unspoken, with the door he shut on Clara in IX M14 and with Grace "between the door and the tree." Line 3 admits the loss (Bartlett) without naming "Liar," and answers the squall, which took his lines and here keeps hers. The syllables run 10–9–8–2, like a voice giving out. The last line has no speaker.

**Structure.** One cutaway instead of three. Rain under the whole verse; the picture cuts once, on line 2; the laugh, then "Stay with me" with "It's okay. Go on." under it, play beneath line 3. He sings "Go on" as the memory's last words arrive, so the two land on the same syllable.

## 7. Quality gate

**Yes, at the floor, not yet above it.** The architecture clears RDR2. HOME finishes the song, and the death comes after it from ordinary causes. The switch fails on Ellis and lands on a machine, and the footage shows a boy singing to nobody. Then it lands on Wayne for the first time, with "Son." whole, the siren switched off, and "Sir." The epilogue now has a shape: biscuits at Wytheville, "She carries.", four dollars gone in six days, and "Then somebody used to be giving him more." The documentary can't get past the door, and the game goes in. It ends on "Wayne goes on.", a spatula, and "Hi, El." Nearly all of it is played, not narrated, and the order is right.

What holds it at the floor: the verse is the weakest writing at the point of greatest weight; the narration of M8–M9 still explains its own grammar; and a player on a second run will find the clock and branch holes in §4.

1. **The verse.** Use the default above, a single cutaway, and cut the three options that leak or borrow.
2. **The narration in M8–M9.** Cut the nine chapter citations and Theo's raised hand (keep Wayne's), the "bow" telegraph, "It's the last light," and the four M9 lines on the switch. In the coda, change Roy's "Go on, get out of here" to "Get out of here, it's Saturday."
3. **Clock and branches.** The fall at 8:22, with forty minutes in the gap. "Stop" at 6:50, after Wayne leaves. Fix 1996 Cal's "once."
