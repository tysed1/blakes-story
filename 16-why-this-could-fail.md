# Why This Story Could Fail

*Deliverable 18. The honest list. Updated in V8: each risk now ends with the fix that was made and the playtest that checks it (`19-playtest-plan.md`). Each risk: what it is, how it fails in the player's hands, what the design already does about it, and what a production team must watch. Ranked by how badly each one would hurt the game.*

## 1. The player guesses Clara too early, and the midpoint is a shrug

**The risk.** A generation raised on *The Sixth Sense* and *Fight Club* looks for the imaginary friend. If they find her in Chapter II, the first half of the game becomes a waiting room.

**How it fails.** Someone says "Who're you talking to?" three times in one chapter. A third party's point of view frames the empty spot. A lyric says "Nobody here can see you." (All three were in the draft. All three were cut.)

**What the design does.** Clara rules 1–13. One "Who're you talking to?" before V, with a door hiding her. No third-party point of view on her place before V M16. No vehicles with band members before V M16. Social cover (Roy asks after "that Clara girl"; Ellis orders two coffees). The lyric became "Nobody here knows you." She's funny and warm for four chapters, so players *want* her to be real.

**Watch.** Casting and performance capture. If Clara's actor plays her as mysterious, the game is over. She has to be played as a bossy older sister at a county fair.

**Fixed in V8.** Clara is now the game's only help (bible §11.8). A player who guesses still depends on her, so the guess doesn't defuse anything. The likely guess ("his dead sister's ghost") is designed to be the tabloid version, which VIII and IX correct. Players who test her are acknowledged once, at V M16. Casting and delivery are fixed in `18-performance-and-direction.md` §2. **Test:** T1 and T2 in `19-playtest-plan.md`.

## 2. The finale reads as a drug death, or as the game killing him to make him meaningful

**The risk.** A beautiful young musician falls off a stage after a mystical experience. Players have seen that story, and the tone rule is "The death is not the meaning."

**How it fails.** He takes acid and remembers his sister. The music swells. The fall is framed as transcendence.

**What the design does.**
- He takes nothing; the tab goes back in the envelope (X M3), and Dean flushes it so the press never has it (Ep. M4).
- The truth arrives through a song and a phrase Roy has said every chapter, not through a drug.
- The death has four ordinary causes: a gap at a stage edge, a film crew needing light after sunset, a three-year-old trauma reflex, and no sleep.
- Nina's column says one true thing: "He was nineteen."
- The last things he does are laugh with his band, say "Sunday's fine" about biscuits, finish a song, and step toward Riley.

**Watch.** Music and lighting in the fall. If the score swells, or the light goes gold, or there's slow motion, it becomes the myth the game is arguing against. The fall has to be fast, ugly and specific.

**Fixed in V8.** A binding audio, light and camera spec for the fall is in X M8, and it's repeated in 18 §6: real time, no score, no gold, no wide shot. **Test:** T5.

## 3. The withheld *home* reads as "the game made me kill him"

**The risk.** The player presses the band's oldest signal and the character dies. Some players will feel tricked; some will refuse to press it and feel punished for that too. (The V5 draft had exactly this problem: the press was the frame he fell in.)

**What the design does.**
- No timer; the band varies the music so the screen never goes still.
- The player chooses *when*, not *whether*.
- **Pressing ends the song, and ends it right** (V7). The band lands the last chord together; there's a second of silence; he laughs and steps toward Riley. Only then does the crowd roar, the film crew step out for the bow, and the light come on.
- The gap and the light aren't pointed at beforehand. The flare in "Shape Note" reads as a technical problem.
- In the story the hold is capped at about three minutes, and the footage and Nina's 1996 line round it (under a minute, about two, close to three). Nobody is scored to the second.

**Watch.** Playtesting will show what happens when a player walks away from the controller for twenty minutes. The music has to still be alive when they come back. And the prompt must never pulse, blink, or nag.

**Fixed in V7 and V8.** The song ends first. A binding UX spec in X M8 says the prompt never pulses, there's no idle nag, and the vamp stays alive indefinitely. Clara gives no help at HOME. A toggle is available for accessibility. **Test:** T4.

## 4. Grief fatigue

**The risk.** VIII to the epilogue is six hours of loss. Players check out and the ending lands on numb people.

**What the design does.**
- VIII has an ordinary interlude with nothing at stake (Snow Day: a fish fry, bowling, a polka, the bus lost at gin), added in V7 because the chapter ran five hours without one.
- Every late chapter has a real comic set piece: Dean's coffee (VIII), Le Guin in one voice (IX), the Polaroid and the gorilla (X), the four dollars stolen by Tuesday (Ep.).
- Ordinary-first scenes sit between the heavy ones: the tailgate, the solder, fishing, Opening Day.
- The epilogue was cut to about 1.75 hours, with "Number One" folded into another mission.

**Watch.** Pacing in production. If any late chapter loses its funny scene to scope cuts, it will fail. Protect the jokes first.

**Fixed in V7 and V8.** Snow Day was added to VIII. The jokes that must survive scope cuts are listed in 18 §8. **Test:** T6.

## 5. Riley becomes the witness

**The risk.** The girlfriend who watches the genius suffer. It's the oldest trap in this genre.

**What the design does.**
- Her own spine: the song, her mother, the registration forms, her own record.
- She writes "Sunday Clothes" (V), loses it to his voice by her own consent (VIII), and hears her mother lead a hymn (IX).
- She stops using the thing she called a way of seeing.
- She leaves the house and keeps the band.
- She decides what the world gets to read of him.

**Watch.** The ratio. In VII–X she still has several scenes that are about Ellis (the extra chair, the payphone, the count). Every one of those must also be about her.

**Fixed in V8.** Every Riley segment in VII–X and the epilogue now carries a stake of her own: the bridge she can't finish in the hayfield, and Nina's request for an interview about her songs (X M2). In the epilogue she says "I'm carrying him" and writes "Maps." **Test:** T7.

## 6. The outing of Cal serves the straight lead's redemption

**The risk.** A gay character's worst moment exists to make the hero's apology meaningful.

**What the design does.**
- Cal provokes first and is right ("She isn't real, Ellis").
- He leaves on his own; Theo's hand is on his arm in public.
- He comes back on his own terms ("Theo's mine. That's real. You don't get to use it."), and refuses the apology in that room.
- Ellis's real apology comes a chapter later, in Cal's world, where Ellis is bad at something.
- The epilogue gives Cal and Theo twenty-one years, and the documentary doesn't make a point of it.

**Watch.** The voice direction on "At least mine isn't somebody I keep in a hotel room." It has to sound like Wayne, not like a villain.

**Fixed in V8.** Delivery is specified in 18 §2 (Ellis's line is his father's cruelty, flat and instant). **Test:** T9, a sensitivity read.

## 7. The medication thread says "pills kill art"

**The risk.** Everything good happens off the pills. A player who needs medication hears that they should stop.

**What the design does.**
- On the medication Ellis sleeps, swims, eats the pie with his father, and finishes his best song.
- Off it he gets Clara back, and also 3 a.m., a lost verse in front of 2,300 people, and Riley leaving.
- He stops out of grief, not for art.
- Dr. Lusk is the best adult in the chapter.
- The game says it doesn't pick.

**Watch.** Marketing. If a trailer cuts from the medicated porch to the Tabernacle, it will say the opposite of the game. Consider a content note on medication in the game's front matter.

**Fixed in V7 and V8.** Cal's "That's him too." The help layer makes the medicated quiet a playable cost with no moral attached. Marketing guardrails are in 18 §9, and a content note is in 18 §11. **Test:** T8, with sensitivity readers.

## 8. The myth critique becomes hypocritical

**The risk.** The game criticizes a country for turning a nineteen-year-old into a story, while turning him into a story.

**What the design does.**
- The hidden-poet system makes the player complicit: the lines the country calls genius are the ones the player collected.
- The game lets the player see what the footage can't: who was sitting on the edge of the stage.
- Riley's book gets to leave the train line out, and so does the game's marketing.
- The last scene is an ordinary Saturday.

**Watch.** The game's own merchandise. Replica ELLIS shirts in a real store would be exactly what the epilogue is sad about.

**Fixed in V8.** Marketing and merchandise guardrails are in 18 §9: no ELLIS shirts, no "genius" copy, never show the fall.

## 9. It's too long, and the middle sags

**The risk.** Fifty-seven and a half main-story hours. Chapters VII (about 7h) and VIII (7h, including the Snow Day interlude) are dense with set pieces, and the chapter text for VII runs about 31,000 words.

**What the design does.** The proportions are intentional: the ordinary life takes twenty hours so the player misses it.

**Watch.** VII in particular has nineteen missions. In production, protect Missions 6, 8, 14, 15, 17 and 19. Merge 4 into 2, and 11 into 10, if the game needs to lose an hour.

**Fixed in V8.** VII and VIII are cut by about 20% each, with their protected missions intact. **Test:** T10.

## 10. The switch grammar confuses more than it moves

**The risk.** A camera that changes who you are without a menu is disorienting. Failures of that grammar (VIII, IX, X) could read as bugs.

**What the design does.** Four chapters teach the grammar before it's ever violated. The first failure happens on a bus, in a quiet moment, at walking speed.

**Watch.** Playtest the first failed catch (VIII M4) with people who have played only I–VII. If more than a few think it's a glitch, add one frame of Clara in focus before the snap-back.

**Fixed in V8.** The failed catch in VIII M4 and M10 follows a fixed, identical grammar: the full cue, six frames of her in focus from Ellis's eyes, a stutter, and a snap-back with the same rumble. The audio rule is in 18 §5. **Test:** T3, which has fallbacks ready.

## 11. The period is set dressing

**The risk.** 1974–76 becomes flares and a WIN button.

**What the design does.** The period does work in the story:
- FM line of sight is why Wayne drives up a mountain.
- Milledgeville is why Ellis won't see a doctor.
- The royalty tricks are why Richard matters.
- Deinstitutionalization is why Dr. Lusk says "You can walk out."
- Game 6 is why father and son sit on one couch.
- Outpatient antipsychotics are why the medicated chapter looks the way it does.

**Watch.** The historical-authenticity checklist (§5 of deliverable 15).

**Held.** **Test:** T14.

## 12. The fictional cities read as Atlanta and Nashville with the serial numbers filed off

**The risk.** The user wanted loose resemblance. Real street names, a paper called the *Constitution* and a "Tennessee" in dialogue made it one-to-one; those were caught and cut.

**Watch.** Level design. Laurel City's skyline must not be Atlanta's. Tannersville's river bend must not be Nashville's. Nothing should be named after anything real there.

**Fixed in V8.** Level-design guardrails are in 18 §10. **Test:** T14.

## 13. The coda without Clara is misread

**The risk.** Players think she's been retconned, or that the game is saying she never mattered.

**What the design does.** It doesn't remark on it. It's an ordinary Saturday, and the player decides what her absence means.

**Watch.** If playtesters overwhelmingly read it as a bug, add nothing. Leave it. Some things in this game are supposed to be felt and not explained.

**Held by decision.** **Test:** T11, a do-not-fix test.

## 14. Wayne's redemption is too tidy

**The risk.** The hard father softens on schedule, one gesture per chapter, and becomes a cozy grief figure.

**What the design does.**
- He never says any of the things he'd never say unless the player makes him, in an ambulance, to a son who can't hear.
- He still closes the door on the documentary in 1996.
- He takes neither the yard job nor retirement well.
- He apologizes to a stranger before he apologizes to his son, and the apology fixes nothing.

**Watch.** The actor. Wayne must never cry on camera.

**Fixed in V7 and V8.** The "Hm." lexicon and "never cries on camera" are in 18 §2. **Test:** T12, which has a fallback ready.

## 15. The ending has too many endings

**The risk.** The gap, the ambulance, Route 17, the funeral, the list, the pocket, M., Tater, 1996, the coda, the credits, and the post-credits.

**What the design does.** The epilogue is short and playable, and each mission is one person keeping one thing. The 1996 frame was cut to four minutes and moved before the Tater mission (V7), so the documentary closes a door and the last mission goes behind it. The epilogue then ends on "Wayne goes on." The coda is open-ended and ends when the player drives home.

**Watch.** If the team has to cut more, cut the 1996 frame to Dean, Riley and the door, and keep everything else.

**Fixed in V7.** The 1996 frame was moved and cut to about four minutes.

## The one-sentence version

This story fails if it becomes the myth it's about: a beautiful doomed boy whose pain made him special and whose death made him matter. Everything in the design exists to stop that, and the most important protections are the jokes, the biscuits, and the tab put back in the envelope.
