# Kids Studio — Repo Guide

A faceless, animated kids life-skills channel, built as a studio system rather than a single-video project.

## Start here, in this order
1. **CONTEXT.md** — the constraints everything else is built from. Already filled in.
2. **BIBLE.md** + **SERIES.md** — the show itself: premise, cast, world, naming.
3. **SKILL-MAP.md** + `/trackers/skill-curriculum.csv` + `/trackers/episode-backlog.csv` — the 12-skill curriculum and the 40-episode backlog.
4. **PRODUCTION-SOP.md** + `/characters/*.md` + `/templates/*.md` — the one-person pipeline and the locked character sheets.
5. **YOUTUBE-KIDS-COMPLIANCE.md** + **MONETIZATION.md** — Made for Kids / COPPA rules and a realistic money plan.
6. **TOOL-DECISIONS.md** — which tools were picked, why, what they cost, and the cheap test that would prove each one wrong.
7. **90-DAY-PLAN.md** — the schedule that ties it all together, built around 15+ hrs/week.
8. **EPISODE-ENGINE.md** — the repeatable process for turning one backlog row into a produced episode. Already run once, for Pilot 01 — see `/series/ep01-the-broken-cup/`. Run it again per episode, in priority order.
9. **/templates/weekly-review.md** + `/trackers/kpi-dashboard.csv` — the recurring weekly check-in once episodes are live.

## What's been built
- **Pilot 01, "The Broken Cup"** — the complete ten-file episode folder at `/series/ep01-the-broken-cup/`: brief, script, storyboard, shot list, character sheet, visual prompts, voice cast, parent description, Shorts cut, publish checklist. 586 spoken words, ~6:38 with a trim list to 6:17, one location plate, 20 key frames, a cast of two.
- **ep02 and ep03 briefs** — `/series/ep02-the-unfinished-tower/` and `/series/ep03-the-candy-on-the-counter/`. Briefs only: the 90-day plan's Week 1 stretch goal, not the start of production.
- **Channel and series name: Maple Row** — recorded in SERIES.md.
- **The tool stack** — images, voice, editor and the location-plate build order, all decided in TOOL-DECISIONS.md.
- **Ms. Rivera's locked character sheet** — `/characters/teacher.md`, closing the last gap in the recurring cast.

## What's still open

**Next action: three pre-flight tests, before any production work**

All three tool gaps are closed — see **TOOL-DECISIONS.md** for the reasoning, costs, risks and
fallbacks. But each pick is provisional until its cheap test passes, and each test can still change
the tool. They're specified in TOOL-DECISIONS.md and scheduled as Day 0 in 90-DAY-PLAN.md:

1. **Image — the "Episode 40" test** (~1 day, under $20). Generate the master character sheets and
   a plate, freeze them, generate five frames, then reopen fresh and regenerate shot 1 from the
   saved files alone. Do the day-one sub-check first: confirm the tool will even accept a stylised
   cartoon child as an uploaded reference.
2. **Voice — the three protected lines** (one evening, under $25). Note the method is
   speech-to-speech: performed into a mic and converted, never typed into a text-to-speech box.
3. **Editor — the `.mlt` round-trip** (one evening, $0). Proves the timeline can be generated
   rather than hand-assembled, which is the whole reason for the editor pick.

A failed test means take that tool's fallback, not stop.

**Noted, not blocking**
- **`episode-backlog.csv` has no `produced` column** — add one at publish time rather than overloading `flag`.
- **Compliance recheck.** YOUTUBE-KIDS-COMPLIANCE.md and MONETIZATION.md were researched Sept 2026 and say to recheck before launch. Pilot 01 *is* the launch, so that recheck is live now.
- **Pricing in TOOL-DECISIONS.md is from secondary sources**, not vendor pages — confirm the three numbers you'll actually spend against before committing.

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
  TOOL-DECISIONS.md            the tool stack, why, and the test that falsifies each pick
  MONETIZATION.md              staged money plan, dated
  90-DAY-PLAN.md                 the schedule
  /series/ep01-the-broken-cup/      Pilot 01 — the full ten-file episode folder
  /series/ep02-.../ ep03-.../        briefs only, so far
  /characters/                       locked character sheets
  /templates/                         reusable fill-in templates
  /trackers/                           the CSVs — curriculum, backlog, board, KPIs
```
