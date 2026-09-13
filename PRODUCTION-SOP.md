# Production SOP — One-Person Pipeline

story → script → locked character frames → key shots → voice → edit → captions → thumbnail → upload → Shorts cut

Built for: one person, not on camera, using AI assistance at each step, repeatable enough that episode 12 still looks like episode 1.

## Tool stack (max 6 — here's where it stands today)
| Step | Tool | Status |
|---|---|---|
| Scripting, planning, visual-prompt writing | Claude Code | **Have** |
| Character frames / key shots | An AI image tool (e.g. Midjourney, Nano Banana, or similar) | **Not yet picked** |
| Voice | An AI voice tool (e.g. ElevenLabs) or real voices | **Not yet picked — open gap** |
| Edit + captions | A video editor (e.g. CapCut) | **Not yet picked — open gap** |
| Thumbnails | Same image tool as character frames | Depends on above |
| Upload / scheduling | YouTube Studio directly | Available whenever |

**Before Week 1 production starts, close two gaps:** pick a voice tool and pick an editor. Script and visual-prompt writing can proceed without them (EPISODE-ENGINE.md doesn't need either), but nothing gets published until both are chosen. ElevenLabs and CapCut are the two most common defaults for a solo faceless-animation pipeline — reasonable starting points if nothing else is pulling you elsewhere — but the choice is yours to make, not assumed here.

## Constraints
- Not on camera, ever.
- Character sheets in `/characters/` must be locked before any episode is produced — episode 12 needs to look like it's from the same show as episode 1.
- Fewer shots, held longer, beats chaotic cutting. 12–20 key frames per episode (see EPISODE-ENGINE.md).
- If a week goes badly: the "tiny episode" path below, not a skipped week.

## The tiny-episode fallback
If 15+ hrs isn't available in a given week: cut to a 3-minute story, same formula (hook → problem → failed try → new try → skill named → practice), 6–8 key frames instead of 12–20, one location. Better to ship something small on schedule than to break the weekly habit — the habit is what the audience (and the algorithm) actually rewards.

## Character sheets
`/characters/hero.md`, `friend.md`, `sibling-or-cousin.md`, `adult.md` — each with name, age, a look that never changes (hair, colors, outfit), personality, a do/don't list, and one locked visual-prompt paragraph to copy into every image generation for that character.

## Production board
`/trackers/production-board.csv` tracks each episode through: script → voice → frames → edit → live, with an owner, a due date, and a blocker field. Filled with the first 30 days in 90-DAY-PLAN.md's schedule.
