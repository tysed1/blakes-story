# THE BLAKES — Playtest and Risk Plan

*Supplementary deliverable (V8). `16-why-this-could-fail.md` names the risks. This plan says how to find out, before ship, whether each one has happened, and what to do if it has. Every test names a metric, a pass line, and a fallback design that's already written, so a failed test becomes a known change rather than a debate.*

## 1. Slices and cohorts

| Slice | Content | Cohort |
|---|---|---|
| A | Chapters I–IV (about 20 h) | 30 players new to the game; half genre-savvy (have finished at least two narrative games with a twist) |
| B | V M10 – V M16, the midpoint | Cohort A, continued |
| C | VIII M1–M8 and Snow Day | 20 players who've completed I–VII |
| D | VIII M17 – IX M7 (the medicated stretch and Flush) | Cohort C, continued |
| E | X M5 – X M9 | 25 players who've completed I–IX |
| F | The epilogue and coda | Cohort E, continued |

Each session is recorded (screen, controller input, face camera with consent). The post-session interviews use open questions before prompted ones.

## 2. Tests

### T1. Is Clara guessed too early? (risk 1)
- **Measure.** After every chapter of Slice A, the unprompted question: "Is anything about any character unusual?" Then the prompted one: "Is there any character you think might not be what they seem?" Also log `clara_tests` (bible §11.8) and each player's use of Clara's help.
- **Pass.** Before V M16, fewer than 25% of all players and fewer than 40% of genre-savvy players name Clara as not real. Everyone who guesses early still rates the midpoint "affecting" or higher. That's the design aim of the help layer: guessing doesn't defuse it.
- **Fallback.**
  1. Pull clues in this order: Rule-11 near misses in III and IV, one "your daddy" line in II, the V M7 fence beat.
  2. Add one social-cover beat per chapter from the reserve list (Roy asking after "that Clara girl"; a waitress bringing two coffees because Ellis ordered two).
  3. Don't remove any help-layer moments. The help is the answer to early guessing, not the cause.

### T2. Does Clara's help land as help, and as the wound? (the help layer)
- **Measure.** How often players use or follow her help in I–IV. How much stuck time they have as Riley, Cal or Dean (no help), and in VIII M17 – IX M7 (no help). Post-midpoint interview: "What did you think of her help, looking back?" After IX M7: "How did it feel when she came back?"
- **Pass.** At least 70% follow her help at least five times per chapter in I–IV. Median stuck time with no help is under 3 minutes per mission. At least 50% describe relief when she returns in IX M7, and at least 50% of those describe unease at the relief.
- **Fallback.** If stuck time runs long without help, make the band's signals and the HUD objective clearer for Riley, Cal and Dean. Never add hint text. In the medicated stretch, strengthen environmental framing (lit doors, sound sources), not hints.

### T3. Does the failed switch read as a bug? (risk 10)
- **Measure.** In Slice C, the first failed catch (VIII M4) and the second (VIII M10). Unprompted: "Did anything seem wrong with the game?" Prompted: "What happened on the bus?"
- **Pass.** Fewer than 10% report a glitch, and at least 60% describe the camera "trying" to go to Clara.
- **Fallback.** The grammar is already fixed and identical every time (bible §11.1). If it still reads as a bug:
  1. Lengthen the focus-on-Clara window from 6 frames to 12.
  2. Let the HUD fade and return exactly as it does in a real switch.
  3. Last resort: hold the second stutter two frames longer before the snap-back.

  Don't add any text.

### T4. Does HOME feel like "the game made me kill him"? (risk 3)
- **Measure.** Hold-time distribution. Walkaways (no input for over 60 s). After Slice E: "Did the game make you responsible for his death?" (1–5), and "What did pressing HOME mean to you?" (open).
- **Pass.** The median agreement on responsibility is 2 or lower, and fewer than 15% answer 4–5. At least 50% of the open answers mention ending the song, letting go, or "go on."
- **Fallback.**
  1. Lengthen the "right silence" after the last chord to 1.5 s.
  2. Let Riley take one step toward him before the roar.
  3. Show the roar in the band's reaction, not the crowd's.

  Never add a timer. Never add a prompt pulse.

### T5. Does the fall read as beautiful? (risk 2)
- **Measure.** "Describe the moment he fell in three words" (open). Look for words like "beautiful," "epic," "meant to be."
- **Pass.** At most 10% use transcendence words. At least 60% use words about chance, speed or shock.
- **Fallback.** Enforce the X M8 spec. Cut any added music, slow motion or color grade that crept in.

### T6. Grief fatigue (risk 4)
- **Measure.** Session drop-off and self-reported energy (1–5) at the end of each mission in VIII–X, and which scenes players remember laughing at.
- **Pass.** Median energy at the end of VIII is at least 3. At least 70% recall at least two jokes from VIII–X unprompted.
- **Fallback.** Restore anything from the protect list (`18-performance-and-direction.md` §8) that scope has cut. After that, extend Snow Day. Don't cut grief scenes to fix this.

### T7. Riley as witness (risk 5)
- **Measure.** "What does Riley want?" asked after VIII, after X, and after the epilogue.
- **Pass.** At least 70% name something of her own (her songs, school, her mother, a record) before they name anything about Ellis.
- **Fallback.** Move one more beat from the V8 reserve (her Monday interview with Nina, the bridge she can't finish) into the chapter's main path instead of an optional beat.

### T8. Medication read as "pills kill art" (risk 7)
- **Measure.** Sensitivity readers with lived experience of psychosis and of antipsychotic treatment (at least three) read VIII M17 – IX M7 and play Slice D. Players are asked: "Does the game say he should have stopped his medication?"
- **Pass.** Fewer than 10% of players say yes, and no sensitivity reader flags the chapter as advocating stopping treatment.
- **Fallback.** Strengthen the medicated goods in IX (sleep, the pie, "New Skin") on the main path. Make Cal's "That's him too" unmissable. Review the content note.

### T9. The outing (risk 6)
- **Measure.** LGBTQ sensitivity readers (at least three) read VIII M7–M8 and IX M12.
- **Pass.** No reader identifies the scene as existing to serve Ellis's redemption.
- **Fallback.** Give Cal one more beat of his own in VIII M8 (Theo's fire escape, Sunday), and move Ellis's apology further from the outing.

### T10. Length and sag (risk 9)
- **Measure.** Time per chapter, quit points and replay intention.
- **Pass.** VII and VIII run 6.5 to 7 hours each, and fewer than 15% of players quit between VII M1 and VIII M8.
- **Fallback.** Use the cut lists in `16-why-this-could-fail.md` §9. Protected missions stay.

### T11. The coda without Clara (risk 13)
- **Measure.** "Who was missing from the last Saturday?" (open).
- **Pass (do not fix).** Any response. This is a "do not fix" test. If players call her absence a bug, the answer is not to add anything. Log the numbers for the post-mortem.

### T12. Wayne too tidy (risk 14)
- **Measure.** "Did Wayne change too easily?" (1–5).
- **Pass.** The median is 3 or lower.
- **Fallback.** Take one gesture off the epilogue's main path. First candidate: make Thanksgiving a real choice, where the player may start the truck and back out of the Rileys' drive, and the dish arrives on his porch either way.

### T13. Dialogue in performance
- **Measure.** Table reads with the cast for the scenes in `18-performance-and-direction.md` §7. Any line two or more actors paraphrase without being asked is flagged.
- **Pass.** Fewer than three flagged lines per scene.
- **Fallback.** A writer rewrites the flagged lines against the voice sheet, and they're read again.

### T14. Period and place
- **Measure.** A historian of the 1970s US South and a music-industry historian review the checklist in `13-historical-authenticity.md` §5, plus the level art for Laurel City and Tannersville against §10 of deliverable 18.
- **Pass.** No factual errors in dialogue or props. No landmark that reads as a real Atlanta or Nashville building.

## 3. Accessibility checks (run in every slice)

- **HOME.** A hold alternative: press once to toggle "holding," press again to release. The meaning is the same.
- **The switch stutter.** A reduced-motion option softens the stutter but keeps the sound and rumble cue.
- **Subtitles.** Clara's lines are labeled "CLARA" like anyone else's. There's no special color or italics that would mark her.
- **Colorblind-safe HUD.** The HUD is only the day, the objective and the prompts, so this check is short.
- **Content notes.** Shown before the title and available from pause (`18-performance-and-direction.md` §11).

## 4. Order

1. Slices A and B first. T1 and T2 are the riskiest assumptions: early guessing and the help layer.
2. Slice C (T3) as soon as VIII M4 is playable.
3. Slices E and F (T4, T5, T11), with the sensitivity reads (T8, T9) running in parallel from the first script draft.
4. T6, T7, T10 and T12 on the full-game beta.
