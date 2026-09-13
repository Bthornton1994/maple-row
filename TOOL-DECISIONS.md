# Tool Decisions

*Decided 13 September 2026, the day before Week 1. These close the three open gaps in CONTEXT.md
and PRODUCTION-SOP.md. Each one names a primary, a fallback, and the cheap test that would prove it
wrong — run all three tests before Week 1 production starts.*

**Read the caveat at the bottom before spending money.** Pricing and licence terms here come from
secondary sources, not vendor pages.

---

## The stack, now that it's picked

| Step | Tool | Cost |
|---|---|---|
| Scripting, planning, visual-prompt writing, timeline generation | Claude Code | already have |
| Character frames, key shots, location plates, thumbnails | Google Gemini image models ("Nano Banana"), via AI Studio / API | ~$250–450 across all 40 episodes |
| Voice | ElevenLabs Creator, used as **speech-to-speech**, not text-to-speech | $22/mo |
| Edit + captions | Shotcut, version-frozen, timeline generated as `.mlt` | $0 |
| Upload / scheduling | YouTube Studio | $0 |

Four of the six tool slots used. Roughly **$25–35/month all-in** in year one, against a channel that
will earn $1–3 RPM for a long time.

---

## 1. Voice — ElevenLabs, as a voice changer, not a text-to-speech engine

**The decision that matters isn't the vendor, it's the method.** Do not type Maya's lines into a
TTS box. Perform every line of both characters into a microphone yourself, then convert Maya's
performance to a locked child voice. Gramps Lou ships as your own voice, or a clone of it.

**Why not TTS.** Two independent reasons, either one sufficient:

- The consistency setting and the expressiveness setting are the same dial, turned opposite ways.
  The preset that makes episode 12 sound like episode 1 is documented as "less responsive to
  directional prompts" — and this script is nothing but directional prompts. `voice-cast.md` asks
  for a real whisper at near-zero volume, a line delivered muffled from under a bench, a first
  smile audible in the voice, and one line that must deliberately **not** land. You cannot prompt a
  model to perform a line badly on purpose.
- Synthetic child voices are the weakest category in the field, and the best engine has removed the
  shopping aisle: ElevenLabs bans child and child-like voices from its Voice Library outright. What
  is left in the wider market is shared presets — which is the templated signal YouTube's
  inauthentic-content policy looks for.

**Why speech-to-speech fits this show specifically.** It carries timing, breath, volume and melody
straight from a real performance, which is where nearly all of `voice-cast.md`'s direction lives. It
turns "will the model give me the same performance in a year?" into "will I perform the same way in
a year?" — and the answer is already written: a 30-second calibration read A/B'd against the stored
EP01 reference take. It also makes the matched pairs in §4 trivially recordable back to back, since
you are voicing both sides. One slot covers all five recurring characters at no marginal cost.

**The source WAVs are the real master.** If ElevenLabs changes policy, deprecates the model, or
disappears, you re-convert elsewhere without re-performing a line. That is the main reason this is
a safe bet rather than a lock-in.

**Tier:** Creator, $22/mo. Not Starter — Starter is the commercial-rights floor but its credits
don't survive batching. The free tier grants no commercial rights and is unusable.

**Test before Week 1 (one evening, under $25).** Convert the three protected lines — the Scene 2
pause and "It just fell," the muffled "I see it! It's by the wheel!", and the skill line. If Maya
comes back uncanny, stop. Do not try to rescue it with settings.

**Fallback:** one adult voice actor who specialises in child roles, cast once for Maya and later
Nell, batch-recorded 4–8 episodes per session on a flat series rate with a written perpetual buyout.
Roughly $75–150/episode, so $2,400–6,000/year — likely more than year-one ad revenue. This is the
better-sounding product; it is simply the one that can't be paid for yet.

**Disclosure:** no YouTube synthetic-media label is required either way. Animation is exempt, and
cloning your own voice is explicitly listed as not requiring disclosure.

---

## 2. Editor — Shotcut, with the timeline generated rather than assembled

**The edit itself is trivial and the labour is somewhere else.** Twenty stills, three slow
push-ins, simple cuts. Every editor can do that. What none of them advertise is the actual weekly
job: `voice-cast.md` specifies 114 dialogue cues plus 7 named non-verbal assets as separate stems,
with 1:19 of the 6:38 runtime being deliberate silence the *edit* places. That is ~121 clips to
position precisely, every week, forty times — and it is exactly where episode 12 drifts from
episode 1, because a human placing 121 clips by ear makes slightly different choices each time.

**So the pick is the editor whose project file can be written by a program.** Shotcut's native
`.mlt` is plain, documented MLT XML. Claude Code — which you already own, and which already holds
the numbered cues, the shot list and the timing model — can emit the whole timeline: 20 image clips
at computed durations, ~121 audio clips at computed offsets, keyframed push-ins on exactly three
shots, and an SRT taken word-for-word from the script. Episode 12 is then assembled by the same
program that assembled episode 1, not by the same habit.

**This is the make-or-break, and it is the only reason to prefer Shotcut.** If you won't build the
generator, Shotcut loses to DaVinci Resolve free on polish and stability — take the fallback instead.

**Freeze the version.** Pick one build, validate it against ep01, and never update mid-season.
Shotcut is a portable download, so this is easy, but you have to decide to do it.

**Captions:** local Whisper, in-editor, no second tool and nothing uploaded. Treat its output as
*timing only* and overwrite every caption's text from `script.md` — the checklist requires
word-for-word, and that's faster than correcting by ear anyway.

**Test before Week 1 (one evening, $0).** Build the Shorts cut, not the episode — `shorts-cut.md`
already specifies it shot by shot, it contains the hardest element in the pipeline (the long
uncut pause that must hold in silence under a caption), and you need it anyway. Hand-build it in
the GUI first to get a known-good `.mlt` to read as a schema. Then regenerate the same 55 seconds
from the script. Then change one number in the source and regenerate. If the corrected file comes
back right without hand-fixing, the thesis holds.

**CapCut is rejected, overriding this repo's own earlier suggestion.** Its terms take an
irrevocable, perpetual, sublicensable, transferable licence over content uploaded to its servers —
reportedly including cloud-saved drafts, and reportedly surviving account deletion — while the free
tier restricts commercial use, so a monetised channel pays *and* grants the licence. Handing a
perpetual sublicensable licence over your locked original characters and your child-voice stems is
not a trade worth a Ken Burns effect.

**Fallback:** DaVinci Resolve free. Same $0, no watermark, more polished — but you hand-place all
121 cues weekly and build the SRT from the script, since transcription is Studio-only.

---

## 3. Image — Google's Gemini image models ("Nano Banana"), via AI Studio or the API

Use the Pro tier for master character sheets, the four location plates, final key frames and
thumbnails; the cheaper Flash tier for iteration before committing a frame. One tool covers frames,
plates and thumbnails, which is what PRODUCTION-SOP.md asks for.

**Why.** Look at what `visual-prompts.md` actually asks for and the choice makes itself. The worst
frame in the pilot needs four reference roles held at once — Maya's sheet, Gramps Lou's sheet, the
correct plate area, and the mug in a specific one of its four states — plus hard negatives, plus a
three-part continuity contract. That is an *editing* workload wearing a generation workload's
clothes. The Gemini line is documented for multiple reference images and multi-character
consistency in a single call, it reads long constraint-heavy prompts including negatives because it
is LLM-native, and it edits an already-approved frame instructionally, so "same frame, peach now
warm, stain on the overalls" is an edit rather than a re-roll.

**Midjourney makes the best-looking images and is the wrong tool here.** Its one-image Omni
Reference cannot carry four reference roles, its consistency feature and its current model version
are mutually exclusive, and it follows long negative-heavy prompts poorly. It would cost the most
human hours per usable frame, and hours are the scarcest input.

**The discipline that makes this work — write it on the wall.** Every frame branches from the
frozen master character sheets and plate files. **Never** from the previous frame's output.
Identity reportedly holds for roughly 8–10 sequential edits and then drifts; chain edit-on-edit
down a 20-frame episode and episode 12 will not match episode 1. Generate each master sheet
exactly once, ever, and re-anchor to it every time.

**Work in AI Studio or the API, never the phone app** — the consumer app stamps a visible watermark
on by default. Every image carries an invisible SynthID mark and content credentials regardless;
that's harmless for monetisation but permanent.

**Expect to reject frames for being too detailed, not too crude.** BIBLE.md asks for deliberately
minimal fine detail, which is the opposite of what these models are tuned to reward. The freckles,
the gap tooth and the untied shoe are exactly the features a model embellishes.

**Watch the retry rate, not the invoice.** The cost estimate assumes 3–4 tries per keeper. At ten
tries per keeper the money triples and, far worse, the schedule breaks — 10 × 21 frames × 40
episodes is where a 15 hr/week operation dies.

**Test before Week 1 (one day, under $20) — the "Episode 40" test.** Generate the two master
character sheets and the fix-it-stand plate in its three areas, and freeze them. From those
references only, generate pilot shots 1, 8, 14, 17 and 20. Then **close the session, open a fresh
one, and regenerate shot 1 from the saved files alone**, as if a year had passed. Put the two shot-1
images side by side and score five things: same two hair puffs; same yellow tee and teal overalls;
left shoe still untied in all six; freckles present and not migrated; and the wet peach stain
present in 8/14/17/20 and absent in both shot 1s. Then generate the thumbnail with three words on it.

Failed if the two shot-1 images read as a different girl to someone who hasn't been staring at
them, if the flat style hardens toward rendered across the five frames, or if holding the
continuity contract takes more than about five attempts per frame.

> **Check this on day one, before anything else: whether the tool will accept an uploaded
> stylised cartoon child as a character reference.** Both major vendors restrict imagery of minors,
> and refusals have been reported on uploaded references. Flat cutout styling should stay clear of
> the photorealism line those rules target, but that is not guaranteed and the policy can tighten
> mid-series. The entire workflow depends on it, so find out now rather than in episode 6.

**Fallback:** OpenAI's current image model, which takes many reference images and renders text well.
If *both* fail on identity rather than style, train private character models (e.g. Scenario) and
accept slower setup for a harder lock.

---

## 4. Location plates — build all four in Week 1, in this order

`ep02` is set in Theo's yard and `ep03` in Maya's house, so as originally scheduled weeks 2 and 3
each had to build a brand-new plate on top of a full episode, back to back.

Build all four in Week 1 instead — but **not** up front. The expensive part is locking the style,
not the plates; once the flat cutout look is right for one plate, the others are a handful of
generations each. So: build the fix-it stand, ship ep01 end-to-end with it, confirm the look
survives a real edit and export, **then** batch the remaining three in Week 1's tail. Building all
four before the style is proven in motion risks rebuilding all four.

The payoff is lopsided in your favour. Theo's yard serves ep02, 19, 20, 26, 30 and 39; Maya's house
serves ep03, 09, 16, 28, 35, 38 and 40; Ridgeline Elementary serves ep05, 11, 18, 24 and 29. One
week of work removes the cost for the life of the series — which is the whole point of the
four-plate rule in BIBLE.md.

---

## Before you spend anything — how solid these numbers are

Every price, tier and licence term in this file comes from **secondary 2026 sources found via
search, not from vendor pages**: the research session's network egress returned 403 for the vendor
sites directly. The figures were internally consistent across independent sources, but confirm
these three on the vendors' own pages before committing:

1. The per-image price of the Gemini image model you actually use, and whether a flat-rate
   subscription tier includes it.
2. ElevenLabs' current Creator price and credit allowance, and its voice-changer credit rate.
3. The output-ownership and commercial-use clause for whichever image vendor you land on.

Also genuinely unmeasured, and the largest assumption in the whole file: **nobody has tested
whether a flat minimal cutout style survives 800+ generations across a year.** The published
consistency claims are about character identity over tens of frames, not style over hundreds. That
is precisely what the Episode 40 test is for — run it, and re-run a cut-down version at episode 20.
