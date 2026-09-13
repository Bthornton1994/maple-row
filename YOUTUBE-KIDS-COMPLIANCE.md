# YouTube Kids / COPPA Compliance

*Researched September 2026. Platform policy changes — recheck before major decisions (e.g. right before launch, and again before applying for YPP).*

## What "Made for Kids" actually turns off
Designating a video (or the whole channel) as Made for Kids, to comply with COPPA, disables:
- Personalized ads — only contextual ads (based on the video's topic, not viewer data) can run
- Comments
- The notification bell
- End screens and cards
- Super Chat, Super Stickers, Super Thanks, Channel Memberships
- Personalization/watch-history-based recommendations for that content

You can still join the YouTube Partner Program and run ads — the ads are just contextual instead of personalized, and they pay less (see MONETIZATION.md). This is a real trade-off, not a technicality: expect roughly **$1–3 RPM** on Made for Kids content vs. $5–15 on general-audience content, because targeting is off. That gap doesn't close as the channel grows — it's structural.

## COPPA, in plain terms
COPPA is the US federal law behind the designation. Core rule: no collecting personal information from viewers under 13 without verifiable parental consent. In practice, for this show:
- Never ask kids to comment their name, age, school, or location
- No external links in videos or descriptions that ask a kid to sign up, log in, or submit anything
- No embedded forms, quizzes, or "email us" asks aimed at the child viewer
- If parent-facing communication is ever needed (a mailing list, a site), it's addressed to parents explicitly, never framed as something the child viewer should do themselves — see the "no kid signup, ever" rule in MONETIZATION.md

State and regional layers exist on top of COPPA (e.g. California's Age-Appropriate Design Code, and children's-privacy provisions in Connecticut, Colorado, Virginia, Texas, Utah, and others) with their own penalty structures, but none of them change the practical rule for a single-channel content creator: don't collect data from child viewers, full stop.

## How parents actually find this content
Not through comments, not through a notification bell — those tools are off. In practice, parents find kids' content through:
- Search (which is why the title/skill formula below matters more here than in general content)
- Suggested-to-parents / autoplay from a similar channel
- Playlists a parent can hand to a kid and walk away from

Which means packaging has to be built for a parent scanning quickly, not a kid scrolling.

## Packaging
- **Title formula:** skill + story — e.g. *"Maya Broke the Vase | Telling the Truth."* The skill is the search term and the trust signal; the story is the hook.
- **Thumbnail:** one clear face + one object + 2–4 words max. No cluttered thumbnails — parents are scanning, not browsing for spectacle.
- **Description:** written for the parent, not the kid — see `/templates/parent-description.md`.

## Shorts strategy
One real moment pulled from the episode (see the `shorts_hook` field in `episode-backlog.csv`) — not a separate mini-universe, not a cliffhanger, not "you won't believe what happens next" framing. Shorts here are a discovery funnel into the full episodes and Skills playlists, not a second content stream to maintain.

## Metrics that matter for kids content vs. adult commentary content
- Watch time and session-starts-from-playlist matter more than raw CTR spikes — a kids channel's growth engine is "parent replays this weekly," not virality.
- Comments and community metrics are structurally unavailable — don't chase them or worry about their absence.
- Retention through the "skill named" beat (not just the cold open) is the signal that the format is working, not just the hook.

## Originality risk
Made for Kids content that leans too heavily on stock assets or an identical, generic AI look risks being treated as low-originality/reused content by YouTube's policies — which can affect monetization eligibility. The locked-character, four-location-plate approach in BIBLE.md and PRODUCTION-SOP.md is partly a cost-control measure and partly a hedge against this: consistent original characters read as a show, not a template.

## Sources
- YouTube Help, "How ads work on YouTube for supervised accounts and content set as made for kids" (support.google.com/youtube/answer/9713557)
- vidiq, "Made for Kids YouTube: How to Make Money in 2026" (April 2026)
- Gyre, "How to monetize a YouTube kids channel in 2026: rules and strategies"
- AuditSocials, "YouTube Made for Kids Ads 2026: COPPA + Limited Ads Update" (April 2026)
