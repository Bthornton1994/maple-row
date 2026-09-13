# 90-Day Studio Plan

Built around **15+ hrs/week**. Start date assumed: **Monday, Sept 14, 2026**. Adjust all dates below if the actual start slips.

## Days 1–7 (Sept 14–20) — Week 1
- Lock BIBLE.md and the 4 character sheets (already done in this build — review and confirm, don't re-litigate from scratch).
- ~~Write 3 scripts: at minimum `ep01` ("The Broken Cup"); stretch to `ep02` and `ep03` briefs if time allows.~~ **Done** — `ep01`'s full episode folder is at `/series/ep01-the-broken-cup/`, and the `ep02` and `ep03` briefs are written.
- Produce **ep01 end-to-end, even if ugly.** The goal this week is a complete pipeline pass — script → frames → voice → edit → upload — not a polished pilot. Fix quality in week 2+, once the pipeline itself is proven.
- ~~**Close the two open tool gaps first** (voice, editor — see PRODUCTION-SOP.md). Nothing downstream of scripting can happen without them.~~ **Tools are picked** — see TOOL-DECISIONS.md. What replaces this is three pre-flight tests, below.

### Day 0 — run three pre-flight tests before any production work

Each is cheap, falsifiable in an evening, and has a named fallback. Run all three *before* starting
ep01's frames, because each one can still change a tool choice. Full specs in TOOL-DECISIONS.md.

1. **Image — the "Episode 40" test** (~1 day, under $20). Generate the two master character sheets
   and the fix-it-stand plate, freeze them, generate five pilot frames from them, then open a
   *fresh session* and regenerate shot 1 from the saved files alone. If the two shot-1 images read
   as different girls, the pick is wrong. **Do the day-one sub-check first:** confirm the tool will
   even accept a stylised cartoon child as an uploaded reference. The whole workflow depends on it.
2. **Voice — the three protected lines** (one evening, under $25). Perform and convert the Scene 2
   pause and "It just fell," the muffled "I see it! It's by the wheel!", and the skill line. If
   Maya comes back uncanny, stop and move to the fallback. Do not try to rescue it with settings.
3. **Editor — the `.mlt` round-trip** (one evening, $0). Hand-build the Shorts cut in the GUI,
   regenerate the same 55 seconds as a generated project file, then change one number in the source
   and regenerate. If the corrected file comes back right without hand-fixing, the pipeline is real.

If a test fails, take that tool's fallback and keep going. Do not let a failed test stop Week 1 —
the fallbacks are all workable, just slower or costlier.

## Location plates — a cost weeks 2 and 3 didn't account for

Week 1 builds one plate: Gramps Lou's fix-it stand, which is the only plate Pilot 01 uses.
`ep02` is set in Theo's yard and `ep03` in Maya's house — so as originally scheduled, **weeks 2 and
3 each had to build a brand-new location plate from scratch on top of a full episode**, back to
back. That is real work the week-by-week plan below treated as free.

**Decided: build all four plates in week 1 — but not up front.** The expensive part is locking the
style, not the plates; once the flat cutout look is right for one, the others are a handful of
generations each. So build the fix-it stand, ship ep01 end-to-end with it, confirm the look
survives a real edit and export, *then* batch the remaining three in week 1's tail. Building all
four before the style is proven in motion risks rebuilding all four.

The reuse is lopsided in your favour: Theo's yard serves ep02, 19, 20, 26, 30 and 39; Maya's house
serves ep03, 09, 16, 28, 35, 38 and 40; Ridgeline Elementary serves ep05, 11, 18, 24 and 29. One
week removes this cost for the life of the series — the whole point of the four-plate rule in
BIBLE.md. See TOOL-DECISIONS.md §4.

## Weeks 2–4 (Sept 21 – Oct 11) — ep02, ep03, ep04
- 1 episode per week + 2 Shorts cut from each.
- Do not start a second series or side-project during this window — the habit matters more than breadth right now.
- Week 2: `ep02` "The Unfinished Tower"
- Week 3: `ep03` "The Candy on the Counter"
- Week 4: `ep04` "Too Heavy to Carry"

## Weeks 5–8 (Oct 12 – Nov 8) — ep05–ep08, batched
- Batch voice and frame generation across these 4 episodes rather than one-at-a-time — this is where the 15+ hr budget pays off most: batching is more efficient than serial production.
- These 4 (Sam's Crayon / Two Dollars / The Storm in My Chest / I Messed Up the Drawing) work as a loose mini-arc — money, feelings, and repair back-to-back. Consider releasing them as a named mini-arc in the Skills playlist.
- Week 5: `ep05` · Week 6: `ep06` · Week 7: `ep07` · Week 8: `ep08`
- **By end of week 8: 8 episodes live.** This is the full pilot season.

## Weeks 9–12 (Nov 9 – Dec 6) — consolidate, stretch if pace allows
- Baseline goal: catch up any slipped episodes, polish weak spots flagged in weekly reviews, build a script buffer for weeks 13+.
- Stretch goal (realistic only because of the 15+ hr budget): `ep09` and `ep10` ("The Missing Cookie," "Not My Drawing") to push total episodes toward the top of the "8–12 by week 12" range.
- Start the YPP checklist once subscriber + watch-hour numbers are close (see MONETIZATION.md) — don't wait for a round number, and don't celebrate hitting a milestone that isn't the actual threshold.
- Set up 1 autoplay-able playlist a parent can hand to a kid without supervision (the Stories playlist, in release order).

## After week 12
`episode-backlog.csv` has 40 total episodes mapped through week 40 at a steady ~1/week pace. Re-run EPISODE-ENGINE.md for each in priority order, interleaving skill pillars rather than producing them in the CSV's skill-grouped order (see the note in SKILL-MAP.md). Re-shuffle the week 13+ order for variety before locking it in.

## If a week runs short
Use the tiny-episode fallback in PRODUCTION-SOP.md (3-minute version, same formula, fewer shots) rather than skipping a week outright. The weekly habit is the actual growth lever here, more than any single episode's polish.
