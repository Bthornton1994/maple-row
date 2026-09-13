# Kids Studio — Repo Guide

A faceless, animated kids life-skills channel, built as a studio system rather than a single-video project.

## Start here, in this order
1. **CONTEXT.md** — the constraints everything else is built from. Already filled in.
2. **BIBLE.md** + **SERIES.md** — the show itself: premise, cast, world, naming.
3. **SKILL-MAP.md** + `/trackers/skill-curriculum.csv` + `/trackers/episode-backlog.csv` — the 12-skill curriculum and the 40-episode backlog.
4. **PRODUCTION-SOP.md** + `/characters/*.md` + `/templates/*.md` — the one-person pipeline and the locked character sheets.
5. **YOUTUBE-KIDS-COMPLIANCE.md** + **MONETIZATION.md** — Made for Kids / COPPA rules and a realistic money plan.
6. **90-DAY-PLAN.md** — the schedule that ties it all together, built around 15+ hrs/week.
7. **EPISODE-ENGINE.md** — the repeatable process for turning one backlog row into a produced episode. Already run once, for Pilot 01 — see `/series/ep01-the-broken-cup/`. Run it again per episode, in priority order.
8. **/templates/weekly-review.md** + `/trackers/kpi-dashboard.csv` — the recurring weekly check-in once episodes are live.

## What's been built
- **Pilot 01, "The Broken Cup"** — the complete ten-file episode folder at `/series/ep01-the-broken-cup/`: brief, script, storyboard, shot list, character sheet, visual prompts, voice cast, parent description, Shorts cut, publish checklist. 586 spoken words, ~6:38 with a trim list to 6:17, one location plate, 20 key frames, a cast of two.
- **ep02 and ep03 briefs** — `/series/ep02-the-unfinished-tower/` and `/series/ep03-the-candy-on-the-counter/`. Briefs only: the 90-day plan's Week 1 stretch goal, not the start of production.
- **Channel and series name: Maple Row** — recorded in SERIES.md.

## What's still open

**Blocks production — three tool decisions nobody has made yet**
- **Voice tool** (or a real-voice path). `voice-cast.md` is written tool-agnostic and has a "when a tool is picked" checklist waiting to be filled in.
- **Editor + captions.** Gates the edit, the captions, the Shorts cut, and every box in the Publish section of the checklist.
- **Image tool** for character frames, key shots and thumbnails. PRODUCTION-SOP.md lists this as unpicked too, though CONTEXT.md names only the first two — it blocks frame generation just as hard.

Everything upstream of these is done for Pilot 01. Nothing downstream can start until they're chosen.

**Noted, not blocking**
- **Ms. Rivera has no locked sheet in `/characters/`.** She's recurring in BIBLE.md but has no age, look, or locked visual-prompt paragraph, so the first episode that uses her would lock her by accident. Blocks her first school-set episode, not Pilot 01.
- **`episode-backlog.csv` has no `produced` column** — add one at publish time rather than overloading `flag`.
- **Compliance recheck.** YOUTUBE-KIDS-COMPLIANCE.md and MONETIZATION.md were researched Sept 2026 and say to recheck before launch. Pilot 01 *is* the launch, so that recheck is live now.

## Folder map
```
/kids-studio
  CONTEXT.md            constraints
  BIBLE.md               show, cast, world, voice rules
  SERIES.md               naming, positioning, playlists
  SKILL-MAP.md             the 12-skill curriculum, explained
  EPISODE-ENGINE.md         how to turn a backlog row into a produced episode
  PRODUCTION-SOP.md          the one-person pipeline + tool stack
  YOUTUBE-KIDS-COMPLIANCE.md  Made for Kids / COPPA, dated
  MONETIZATION.md              staged money plan, dated
  90-DAY-PLAN.md                 the schedule
  /series/ep01-the-broken-cup/      Pilot 01 — the full ten-file episode folder
  /series/ep02-.../ ep03-.../        briefs only, so far
  /characters/                       locked character sheets
  /templates/                         reusable fill-in templates
  /trackers/                           the CSVs — curriculum, backlog, board, KPIs
```
