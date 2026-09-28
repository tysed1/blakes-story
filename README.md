# THE BLAKES

A narrative open-world game in ten chapters, an epilogue and a coda. Georgia's north mountains, October 1974 to August 1976. Four people who didn't mean to become a band become one. The one who's easiest to love is talking to someone who isn't there.

This repository is the complete story design: the story bible, the macrostructure, all ten chapters and the epilogue written mission by mission at production detail, and the supporting documents a development team would need to build it. It began as a rebuild of an earlier draft. The process folder shows how it got here.

## Where to start

**Read the story, in order:**

1. `01-story-bible.md`: the world, the map, the timeline, the crash, the characters, the rules (Clara's thirteen rules are §11.3).
2. `02-macrostructure.md`: the ten-chapter shape on one page, then each chapter's thesis and turn.
3. `chapters/`, I through X, then the epilogue and coda:

| # | File | Dates | Runtime |
|---|---|---|---|
| I | `chapter-01-before-the-noise.md` | Oct 10–19, 1974 | 4.5 h |
| II | `chapter-02-second-verse.md` | Oct 19 – Nov 2, 1974 | 5 h |
| III | `chapter-03-signal.md` | Nov 4–29, 1974 | 5 h |
| IV | `chapter-04-momentum.md` | Dec 7–23, 1974 | 5.5 h |
| V | `chapter-05-velocity.md` | Dec 24, 1974 – May 2, 1975 | 6.5 h |
| VI | `chapter-06-the-other-side-of-the-glass.md` | May 3 – Aug 16, 1975 | 6.5 h |
| VII | `chapter-07-strangers-know-your-name.md` | Sept 8 – Dec 13, 1975 | 7 h |
| VIII | `chapter-08-feedback.md` | Jan 12 – Apr 30, 1976 | 7 h |
| IX | `chapter-09-who-are-you.md` | May 10 – Aug 22, 1976 | 6 h |
| X | `chapter-10-the-last-light.md` | Aug 26–28, 1976 | 4 h |
| Ep. | `epilogue-what-remains.md` | Aug 29, 1976 – Apr 1977; 1996; Nov 9, 1974 | 1.75 h |

Main story: about 57.5 hours. With side content: 80–110.

**If you only have an hour:** the bible's first three sections, then Chapter I's Mission 9, Chapter V's Mission 16, Chapter VIII's Mission 14 (Tolliver Road), Chapter X's Mission 8, and the epilogue's coda.

## Reading paths by role

- **Writers:** the bible (§1, §2, §6, §11.3, §11.8, §12), `00-process/V3-character-audit.md` (the voice sheet), then the chapters in order.
- **Designers:** the bible §11 (every system, including §11.8 Clara's help), `02-macrostructure.md`, `17-tracked-state-registry.md`, `12-side-content-framework.md`, `11-open-world-evolution.md`, and the scripts in `scripts/`.
- **Producers:** `02-macrostructure.md` (runtimes), `16-why-this-could-fail.md`, `19-playtest-plan.md`, and the protect list in `18-performance-and-direction.md` §8.
- **Actors and directors:** `18-performance-and-direction.md`, `03-character-arcs.md`, `04-relationship-matrix.md`, and the scripts.
- **Marketing:** `18-performance-and-direction.md` §9 (guardrails) and §11 (content notes). Read nothing past Chapter IV until you've read the guardrails.

## The eighteen deliverables

| # | Deliverable | File |
|---|---|---|
| 1 | Story bible | `01-story-bible.md` |
| 2 | Macrostructure | `02-macrostructure.md` |
| 3 | Chapters I–X | `chapters/chapter-01` … `chapter-10` |
| 4 | Epilogue (and coda) | `chapters/epilogue-what-remains.md` |
| 5 | Character arc maps | `03-character-arcs.md` |
| 6 | Relationship matrix | `04-relationship-matrix.md` |
| 7 | Clara/Grace clue timeline | `05-clara-grace-clue-timeline.md` |
| 8 | Ellis's psychological timeline | `06-ellis-psychological-timeline.md` |
| 9 | Band and music evolution | `07-band-music-evolution.md` |
| 10 | Drug-use progression | `08-drug-use-progression.md` |
| 11 | Motif and object map | `09-motifs-and-objects.md` |
| 12 | Setup/payoff map | `10-setup-payoff-map.md` |
| 13 | Open-world evolution | `11-open-world-evolution.md` |
| 14 | Side-content framework | `12-side-content-framework.md` |
| 15 | Historical-authenticity notes | `13-historical-authenticity.md` |
| 16 | Second-playthrough notes | `14-second-playthrough.md` |
| 17 | Continuity audit | `15-continuity-audit.md` |
| 18 | Why this story could fail | `16-why-this-could-fail.md` |

## Production supplements (V8)

| File | What it's for |
|---|---|
| `17-tracked-state-registry.md` | every tracked flag: where it's set, its values, where it's read, its default |
| `18-performance-and-direction.md` | casting, delivery, audio, camera, music, marketing and level-design guardrails; content notes |
| `19-playtest-plan.md` | a test, metric, pass line and ready fallback for every risk |
| `scripts/` | production scripts with dialogue trees for V M16 (the midpoint), VIII M14 (Tolliver Road) and X M8–M9 (the last song, the fall, the ambulance) |

## Process (`00-process/`)

How the story was rebuilt, in the order it happened:

- `V1-ingest-and-autopsy.md`: what the original draft had, what worked, and what had to go.
- `research-notes.md`: verified period facts for 1974–76, with sources.
- `critic-reports/`: independent critiques. A (character and dialogue) and B (continuity and systems) on Chapters I–VI; C (full-draft continuity) and D (emotional arc, replay, anti-AI prose) on the complete draft; E (verification of the rebuilt finale and epilogue); F (a table read of the 25 key scenes); G (a three-reader cold read of the whole game after V8: I–IV, V–VIII, IX to the coda).
- `V3-character-audit.md`: decisions after the character critique.
- `V4-red-team.md`: the two red teams' findings and the decisions taken, with work orders R1 and R2.
- `repair-log-R1.md`, `repair-log-R2.md`: what changed in Chapters I–VI.
- `V6-V7-audits.md`: the decisions on Critics C, D and E, the work orders, and the phase 16 quality gate.
- `V8-plan.md`: the V8 pass that brought every rating to 8 or better (Clara's help, the cuts, the Riley pass, the production supplements), and the cold read.
- `WORKLOG.md`: the running canon log.

## Version history

| Version | Stage | Commit |
|---|---|---|
| V1 | Ingest and autopsy of the original draft | `edab132` |
| V2 | Story bible; rebuilt macrostructure; relationship matrix; research | `1c89e3b`, `2c4cf53` |
| — | Chapters I–VI drafted; critics A and B | `eda8a11` … `fcd60b3`, `d1bec6f` |
| V3 | Character audit | `e1559e0` |
| V4 | Red-team decisions; bible and macro to V4 canon; Chapters I–VI repaired | `e1559e0`, `db75ff5`, `55afc57`, `9ed13bb` |
| V5 | Complete draft: Chapters VII–X, epilogue and coda | `d1bec6f`, `0853c99`, `b1b87df`, `5d62593`, `bf4fc7a` |
| V6 | Critics C (continuity) and D (emotion, replay, prose) on the full draft; decisions; continuity repaired across I–X and the epilogue | `f625f14`, `c541f21`, `95fc084`, `129734d`, `2431ed7` |
| V7 | Finale and epilogue rebuilt and verified (Critic E); prose and voice passes; timelines reconciled; quality gate | `bac4b1b`, `6c7965f`, `a94ae9c` |

## The fiction line

Hollow Ridge (the small hometown, center of the map), Laurel City (west; loosely like Atlanta) and Tannersville (east; loosely like Nashville) are fictional. So are the labels, magazines, TV shows, festival and people. The national history is real: the pardon, the WIN button, Saigon, Game 6 of the 1975 World Series, the Bicentennial, Hurricane Belle, Milledgeville. `13-historical-authenticity.md` draws the line in detail.
