# Channel Context

- Format: faceless animated kids series (no host on camera)
- Audience: kids ~5–10, parents watching with them
- Promise: short stories that teach useful life skills (not random "be nice" morals)
- Skill pillars: honesty, effort, money basics, emotions, friendship, problem-solving, responsibility, safety
- Style: simple characters, repeatable worlds, 6–10 min episodes + 30–60s Shorts
- Production: AI-assisted animation / storyboards / voice; no on-camera host
- Time per week: **15+ hrs/week** (near full-time push)
- Tools: **picked, 13 Sept 2026** — see TOOL-DECISIONS.md for the reasoning, costs, risks and the
  pre-flight test for each.
  - Scripting, planning, timeline generation: **Claude Code**
  - Images (frames, plates, thumbnails): **Google Gemini image models**, via AI Studio / API
  - Voice: **ElevenLabs**, used as speech-to-speech — every line performed into a mic and converted,
    never typed into a text-to-speech box
  - Edit + captions: **Shotcut**, version-frozen, timeline generated as `.mlt` by Claude Code
  - Upload: **YouTube Studio**
- Three cheap pre-flight tests must pass before Week 1 production starts. They are specified in
  TOOL-DECISIONS.md and each one is falsifiable in an evening. The image test includes a day-one
  check that the tool will even accept a stylised cartoon child as a reference image.
- Starting from: brand new channel
- Goal: consistent library + path toward YPP monetization
- Hard rules:
  - No horror, no cringe slang, no political content
  - No "this video is educational so ignore COPPA"
  - No medical, legal, or "do this instead of a parent" advice
  - Every episode has one skill, one problem, one practice

## Notes on the 15+ hrs/week budget

That's a serious, near-full-time commitment for a solo operation. It buys room to do the pipeline properly (locked character frames, a real edit pass, actual Shorts cuts) rather than rushing — it does **not** mean episodes should ship faster than the pipeline can actually support. 90-DAY-PLAN.md uses this budget to hold a steady ~1 finished 6–10 min episode/week once the pipeline is proven, which is already a full production cycle for one person even with AI assistance. If weeks are going faster than planned, that time is better spent building a buffer (batching voice/frames, pre-writing scripts) than compressing the schedule further.
