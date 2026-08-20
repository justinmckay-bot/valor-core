# YouTube Playbook

Strategy and growth plan for Valor's YouTube presence. Production pipelines (sermon upload, Reel extraction, posting cadence) live in [WORKFLOWS.md](WORKFLOWS.md). This file is the "where we're going and how we know we're winning" layer.

**Owner:** Justin (directs YouTube strategy). Chris Jones executes the weekly sermon upload only.
**Reviewed by:** Justin McKay
**Last updated:** 2026-05-07

---

## The premise

Chris gets obsessed when the loop closes fast: ship → see result → see win logged. The scoreboard has to reward what he *controls* (output, creative quality) more than what *trails* (subscribers, views), or he'll lose steam when growth lags effort. Output wins fuel reach wins. We log both, but we celebrate the controllable ones loudly so he stays in the seat.

The goal isn't a viral channel. The goal is a YouTube presence that gives people a reason to come back during the week, find Valor when they're searching, and walk into a Sunday already half-known.

---

## Three phases over six months

### Phase 1 — Lock the machine (Months 1–2)

**Goal:** the sermon → Reels → IG/YT/TikTok pipeline runs without Justin checking on it.

**Chris owns:**
- Clip selection from Sermon Clips output
- Captions, titles, thumbnails
- Posting cadence and timing
- Which Reel wins for IG that week

**Constraints:**
- Stays inside the pipeline documented in [WORKFLOWS.md](WORKFLOWS.md)
- No new tools beyond Notion, Drive, Sheets, YouTube Studio
- Brand rules in [CLAUDE.md](CLAUDE.md) apply to every caption, title, description

**Graduation criteria:**
- 8 straight weeks of clean weekly output (sermon up, Reels banked, IG posted, filler running)
- Reel bank holds 16+ unused, tagged clips
- Chris can find any past Reel by topic in under 30 seconds

---

### Phase 2 — Add a second format (Months 3–4)

**Goal:** one new Short-form format that isn't a sermon clip, shipped on a sustainable cadence.

**Format options for Chris to pick from:**
- Testimony Shorts (story-first, peer-to-peer tone)
- "Behind the sermon" cuts (Justin's prep, quick context, what didn't make it in)
- Pastor Q&A ("Ask Justin," 60–90 second answers)
- Prayer-room moments
- Family-life beats (carefully, with consent)

**Chris owns:**
- Format selection from the list above
- Ideation, scripting, production cadence
- Visual style and recurring look

**Constraints:**
- Shorts and Reels only — no long-form non-sermon content yet
- Justin reviews the first 3 before they ship publicly
- Stays inside brand rules and consent rules ([STORIES.md](../STORIES.md) consent line applies)

**Graduation criteria:**
- 8 non-sermon Shorts shipped
- At least one Short cracks 1,000 views
- Chris has a written one-pager on which format is working and why

---

### Phase 3 — Build a draw (Months 5–6)

**Goal:** a recurring series or hook that gives people a reason to *subscribe*, not just visit.

**Chris owns:**
- Concept, naming, hook, schedule
- Whether it's hosted by Justin, Chris, or another staff member
- How it's promoted across platforms

**Constraints:**
- Must be sustainable at Chris's current bandwidth (no format that requires more than 4 hours/week of new production)
- 2 weeks of pre-production and at least 3 episodes shot before public launch
- Justin signs off on the concept before shooting begins

**Graduation criteria:**
- First identifiable subscriber bump tied to a non-Sunday traffic source
- Series has its own URL/playlist with consistent visual identity
- Chris can name the audience the series is for, in one sentence

---

## The scoreboard

Tracked weekly. Posted somewhere Chris (and the team) sees it without asking. Output layer is the win Chris controls; reach and engagement are the trailing reward.

### Output layer *(his control, immediate wins)*

| Metric | Target | Cadence |
|---|---|---|
| Sermon uploaded to YouTube + podcasts | ✅ | Weekly |
| Reels banked from new sermon | 3+ | Weekly |
| Filler Reels posted to YT Shorts + TikTok | 3+ | Weekly |
| IG Reel from new sermon posted | ✅ | Weekly |
| Phase 2 format Short shipped | 1+ | Weekly (once Phase 2 starts) |

### Reach layer *(trailing, monthly review)*

| Metric | Cadence | Notes |
|---|---|---|
| YouTube subscribers (delta vs last month) | Monthly | Baseline TBD — pull from YouTube Studio |
| Total watch time | Monthly | Trend matters more than absolute |
| Top-performing Reel of the week | Weekly | Called out by name in the scoreboard, not just listed |
| Traffic source breakdown | Monthly | Are we getting found, or just re-served? |

### Engagement layer *(quality signal)*

| Metric | Cadence | Notes |
|---|---|---|
| Comments per post | Weekly | Replies count too |
| Shares and saves | Weekly | Saves are the strongest pre-subscribe signal |
| First-time Sunday visitors who say "I found you on YouTube" | Monthly | Pulled from guest follow-up forms |

---

## The freedom corridor

The boundary is now simple: Chris's lane is the **weekly sermon upload** (title, description, correct publish). Anything beyond that (strategy, thumbnails as creative direction, series planning, cross-posting, ads) runs under Justin. When in doubt, upload the sermon and flag the rest to Justin.

**Chris owns, no permission needed:**
- Clip selection, captions, titles, thumbnails
- Posting times and cadence within targets
- Format experiments inside current platforms (YT, IG, TikTok)
- Visual style choices inside brand rules

**Chris flags first:**
- Any new tool beyond Claude Code, GitHub, Drive, Sheets, YouTube Studio, Sermon Clips
- Any decision that takes more than half a day to reverse
- Long-form content (anything past Phase 1–2 scope)
- Anything that names or shows a congregant without consent
- Series concepts or recurring formats before they go public
- Any git operation that rewrites history or touches `main` directly (force push, reset --hard, branch delete). When in doubt, open a PR and ask.

**Chris does not own:**
- Brand rules ([CLAUDE.md](CLAUDE.md))
- Theology, doctrine, scripture framing in captions or titles
- Decisions about which sermons get posted (assume all unless told otherwise)

---

## Review cadence

- **Weekly:** Chris updates the output layer of the scoreboard. Justin or Glenn glances at it, no meeting needed.
- **Monthly:** 30-minute review with Justin. Reach + engagement layers, what's working, what's next.
- **End of each phase:** Graduation check. Did we hit the criteria? If yes, advance. If no, name what's blocking and adjust before moving on.

The phase boundary is a checkpoint, not a permission gate. Chris keeps shipping during the review.

---

## First concrete action

Chris pulls baseline numbers from YouTube Studio:
- Current subscribers
- Watch time last 90 days
- Top-performing video last 90 days
- Top traffic source last 90 days

**Time estimate:** 30 minutes.
**Owner:** Chris.
**Why first:** without baseline, Phase 1 graduation is unverifiable and Chris can't see the wins compound.

---

## Working tools and where things live

Chris operates this playbook from his own Claude Code workspace, with files committed to the [valor-church](.) GitHub repo. This is the same .md-as-source-of-truth pattern the rest of the staff is moving onto.

**Chris's workspace lives at `marketing/chris/`** with three starter files:

- `SCOREBOARD.md` — weekly entries for output, reach, and engagement layers
- `REEL_BANK.md` — index of clips with sermon date, topic, strength tier, and link to the video file in Drive (videos themselves stay in Drive, not the repo)
- `IDEAS.md` — format experiments, sermon-by-sermon notes, concepts in flight

Structure inside each file is Chris's call within reason. The questions each file must answer are fixed; the schema is not.

**Git workflow:**

- Chris works on his own long-lived branch (e.g., `chris/youtube`)
- He opens PRs to merge into `main`
- `main` is branch-protected: no direct pushes, no force pushes
- Justin (or Glenn) reviews and merges PRs, which doubles as a lightweight weekly review

**Why this stack vs Notion or Sheets:**

- Aligned with the staff AI workspace rollout already in motion
- Claude Code becomes Chris's thinking partner, not just a tracker (weekly summaries, trend surfacing, caption drafting all live in the same workspace)
- Source of truth is versioned, auditable, and survives tool churn
- Justin and the team read Chris's files the same way they read everything else in the repo

---

## Open questions to resolve before Phase 1 starts

- Does Chris have a Claude Code seat yet? If not, who provisions it?
- Does Chris have read/write access to the valor-church GitHub repo?
- Is `main` branch-protected? (If not, set this before Chris commits anything — non-negotiable given his working profile.)
- Who reviews and merges Chris's PRs? Default Justin; Glenn as backup when Justin is in sermon prep.
- Is there a budget for thumbnail tools, stock footage, or creator licenses Chris should know about up front?
- Does Chris have admin access to YouTube Studio yet, or is that still routed through Justin?
