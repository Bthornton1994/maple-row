# Episode Engine

The repeatable process for turning one row of `/trackers/episode-backlog.csv` into a produced episode. Run this once per episode.

## Input
- The next unproduced row from `episode-backlog.csv`, in priority order (or a specific `ep_id` if you're pulling out of order).
- `BIBLE.md` and `/characters/*.md` for voice, world, and locked visual descriptions.

## Output
For each episode, create `/series/EPXX-slug/` containing:
```
brief.md              one paragraph: who wants what, what goes wrong, what changes
script.md               full script from /templates/script.md
storyboard.md            beat-by-beat visual plan from /templates/storyboard.md
shot-list.md               12-20 key frames from /templates/shot-list.md
character-sheet.md          which locked characters appear, any one-off side character for this episode only
visual-prompts.md            image/video generation prompts, characters locked to /characters/ descriptions
voice-cast.md                 which voice reads which line
parent-description.md          from /templates/parent-description.md
shorts-cut.md                   the 30-60s cut, from /templates/shorts-cut.md
publish-checklist.md              from /templates/publish-checklist.md
```

## Script rules
- 6–8 minutes spoken (`runtime_min` in the backlog is the target, +/- 1 min).
- Scene headings + character lines + [VISUAL] notes for anything the animator/AI-image step needs to see, not just hear.
- The first thing on screen shows the problem — no slow open.
- No host, no narrator breaking the fourth wall.
- Ends with the 20-second "your turn" practice from the backlog row's `practice_for_viewer` field.
- Reading level: grade 2–3. If you wouldn't say it to a 7-year-old at the dinner table, rewrite it.

## Visual-prompts rules
- Every character prompt starts from the locked description in `/characters/`. Never regenerate a character's look from scratch — copy the paragraph, change only the pose/action.
- 12–20 key frames maximum per episode. This is what keeps a one-person AI pipeline affordable — resist the urge to storyboard every line.
- Reuse the four location plates from BIBLE.md rather than generating new backgrounds per episode.

## If a backlog row is flagged
Rows with a `flag` in the backlog note a reason the concept leans too abstract or socially complex for the 5–7 end of the audience. Before scripting a flagged episode: re-read the flag note, simplify the conflict until a 6-year-old could summarize it in one sentence, and only then start the brief.

## Order of operations for this project, right now
1. Confirm which pilot episode to write first — default is `ep01`, "The Broken Cup" (highest priority, simplest complexity).
2. Write `brief.md` and `script.md` for that one episode.
3. Finish that entire episode's folder — every file above — before starting `ep02`.
4. Only then move to the next row.

This mirrors the source plan's own instruction: one episode fully finished before the next one starts.
