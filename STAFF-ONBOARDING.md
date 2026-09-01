# STAFF-ONBOARDING.md (Valor Church)

Welcome to the Valor staff workspace. This doc walks you through the one-time setup. Plan on 45 minutes for the technical setup, plus a 60-minute in-person training session with Justin.

**Before you start, read `GLOSSARY.md` in this same folder.** It defines every technical word used below in plain English. You do not need a tech background to do any of this, but you do need the vocabulary, and nobody was born knowing it. Terms are also defined in-line the first time they show up here.

If you get stuck, message Justin or Glenn. Don't hack around it. We want everyone on the same setup. If the technology fights you or something breaks in a way you can't fix in a couple of minutes, that is exactly when to reach out. Getting help fast is the standard here, not a last resort.

## Who has a workspace right now

This first round is for **Glenn, Nathan, Lacy, Abigail, and Dylan.** Elizabeth will be brought on later. If you are not on that list yet, hold tight; Justin will bring you in when it is your turn.

---

## Why this matters

You are a pastor, a minister, an associate, a partner. You did not get into ministry to be an admin or a content factory. You got into it for people.

This system exists to give you that time back. Your AI workspace handles the recurring work the way you would handle it: the bulletin draft, the follow-up email, the talk outline pulling from our doctrine, the social caption matching our voice. Done in your style, by your standards, before you even sit down to it.

Three reasons this is worth your 45 minutes today:

1. **More time with people.** Every hour spent on admin is an hour not spent shepherding. This system claws those hours back.
2. **One Valor voice.** When the youth minister writes a talk, the marketing associate drafts a caption, and the operations minister sends a partner update, all three should sound like Valor. Not like three different churches stitched together. The shared canon makes that possible.
3. **Who, not how.** Justin's signature framework lives here too. The agent is the *who* for the recurring stuff. Which means you become the *who* for the work only you can do.

This is technical. It is also pastoral. The same way a sermon manuscript or counseling notes are tools that serve the soul of the work. Treat it that way.

---

## What you're setting up

You're building **your own private workspace** that reads from a shared canon.

First, three words you will see constantly:

- **Repo** (short for repository): a folder of files that keeps a history of every change ever made to it. A filing cabinet with a built-in memory. You can always see what a file looked like last week and go back to it.
- **GitHub**: the website that stores a backup copy of a repo online. Git is the program on your computer that tracks the changes. GitHub is the place on the internet that holds the copy. Same idea as a document on your laptop versus that document in Dropbox.
- **Canon**: the shared "this is who we are" files. Mission, voice, brand, convictions, stories. Justin maintains them. Everyone reads them.

- **valor-core** (shared, read-only for you): the source of truth for who Valor is, our voice, brand, doctrine, stories, references. Justin maintains this. You pull updates.
- **valor-{your-name}** (your private workspace): your own files. Your CLAUDE.md, your department docs, your task list, your working files. You own this. Justin can see it on GitHub, but it's yours. Private means only invited people can see it.

Two folders, two GitHub repos, one Claude account that reads both.

---

## The 6 phases

1. **Why** (5 min). You're reading this. Done.
2. **Accounts and tools** (15 min). Set up Claude Pro, Claude Desktop, Claude Code, Antigravity, GitHub.
3. **Setup** (15 min). Create your workspace folder, clone valor-core (clone = download your own copy of it, one time), create your private repo.
4. **Compose** (60 min). Draft your CLAUDE.md and starter files from templates.
5. **Justin approval** (15 min). Justin reviews your CLAUDE.md and key files. Edits or green-lights.
6. **In-person training** (60 min). Pair session with Justin. First real task, daily rhythm drill, Q&A.

---

## Phase 2: Accounts and tools

You need five things:

### 1. Claude Pro account

Valor pays for this. Confirm with Justin before paying. Either he sends you an invite to a Pro seat, or you sign up at https://claude.ai and forward the receipt to Glenn for reimbursement.

### 2. Claude Desktop

Download from https://claude.ai/download. Install. Sign in with your Claude account.

### 3. Claude Code (the terminal version)

Claude Code is Claude running in your **terminal**: a plain window where you type commands instead of clicking buttons. It looks intimidating and it is not. You will use about eight commands total, all listed at the bottom of this doc. On Windows the same window is called Git Bash.

Why bother, when Claude Desktop has a nice chat box? Because Claude Code can actually read and write the files in your folder. It sees your notes, your doctrine, your voice, your task list. That is the difference between a chatbot and an assistant who knows your job.

(You may also see it called a **CLI**, which stands for command line interface. That is just another name for the same terminal window.)

The `.md` files it reads are **markdown**: plain text with a few simple formatting marks. `#` makes a heading, `**bold**` makes bold. That is most of it. Everything in this workspace is markdown because both people and AI read it easily.

**On macOS:**

Open Terminal (Cmd+Space, type "Terminal", hit enter). Paste this:

```bash
xcode-select --install
```

If a dialog pops up, click Install. This gives you **git**: the free program that gives a folder its memory of changes. It runs quietly in the background and you will only ever type a handful of its commands.

Then:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Close Terminal. Reopen it. Test:

```bash
claude --version
```

**On Windows:**

1. Install Git from https://git-scm.com/download/win.
2. Open Git Bash (not regular Command Prompt).
3. Run the same `curl` command above. If it fails, install Node.js from https://nodejs.org and run:

```bash
npm install -g @anthropic-ai/claude-code
```

### 4. Antigravity IDE

Antigravity is Google's AI-native **IDE**. IDE stands for integrated development environment, which is a heavy name for one window where you can see all your files, edit them, and run commands, instead of hunting through Finder. Same files as Claude Code, different surface. Useful when you want to see and edit your files visually.

1. Go to https://antigravity.google.com (verify with Justin if the link has moved).
2. Download the installer for Mac or Windows.
3. Install, open, sign in with your Google account.

You can run Claude Code *inside* Antigravity's terminal. Open the integrated terminal (View → Terminal), type `claude`, and it works the same way.

### 5. GitHub account

If you already have a GitHub account, skip ahead.

1. Go to https://github.com/signup.
2. Use your @valor.church email if you have one. Otherwise a personal email you'll keep.
3. Pick a username. Lowercase first-last (e.g. `nathan-ewing`) is the cleanest. This is public, so don't pick anything embarrassing.
4. Verify your email.
5. **Send your GitHub username to Justin in Slack.** He has to invite you to the valor-core repo before you can download a copy of it.

You will be added as a **read-only collaborator** on valor-core. That means you can pull updates but cannot change the shared canon. If you spot an error in it, flag it to Justin so he fixes it once for everybody instead of five people fixing it five different ways.

You'll get an email invite from GitHub when Justin adds you. Click the link, accept, and you're in.

### 6. Notion (the people layer)

The core files teach you the *system*. The actual people, groups, and pipeline live in **Notion**, in the shared Valor **People + Groups** space. That is where you find the current body, who is in which group and Bible study, each group's leader, and where every person sits in the assimilation pipeline (Guest, Connected, Discover Valor, Next Steps, All In, Member) and across the Four Chambers.

A **connector** is a link that lets your agent read a live system instead of a static file. The Notion connector means it reads the real, current people data rather than a copy that goes stale the day it is made.

1. Make sure you have a Notion account and are signed in.
2. Ask Justin for access to the shared Valor People + Groups space if you don't already have it (the team space is being finalized; he'll add you).
3. In your Claude workspace, connect the Notion connector so your agent can read that space. Then it can answer "who haven't we followed up with?" or "who leads the West Arvada group?" straight from the live data.

**Never** copy congregant names, phones, emails, or giving details out of Notion into a committed file. Read from Notion; keep the record in Notion.

---

## Phase 3: Setup

### Create your workspace folder

In Terminal (Mac) or Git Bash (Windows):

```bash
cd ~
mkdir -p Applications
cd Applications
```

### Clone valor-core into your Applications folder

**Clone** means download your own working copy of a repo from GitHub. You do this once. After that you **pull** to get updates.

Justin will give you the exact URL when he invites you. Likely:

```bash
git clone https://github.com/justinmckay-bot/valor-core.git
```

You should now have a folder at `~/Applications/valor-core/`.

The first time, GitHub may ask you to sign in. Use your GitHub username and a **personal access token** as the password. A personal access token is a long password GitHub gives you to use instead of your real password when your computer talks to GitHub. You generate it once and save it in your password manager. (GitHub stopped accepting regular passwords here years ago, so this step is normal, not a sign something is wrong.) To get one:

1. Go to https://github.com/settings/tokens. Click "Generate new token (classic)".
2. Name it `valor-laptop`. Expiration: 1 year. Scope: check `repo`.
3. Generate. Copy. Paste as password when prompted.
4. Save it in your password manager. You won't see it again.

### Create your own private workspace

Decide your workspace name. Use `valor-{firstname}` (lowercase). Examples: `valor-glenn`, `valor-nathan`, `valor-lacy`, `valor-abigail`.

```bash
cd ~/Applications
mkdir valor-{firstname}
cd valor-{firstname}
git init
```

`git init` turns that plain folder into a repo, meaning it starts keeping a history of every change you make in it.

This is your private folder. Nobody else sees what's in here unless you push it to GitHub.

### Push your workspace to GitHub (private)

1. Go to https://github.com/new.
2. Repository name: `valor-{firstname}`.
3. **Private.** (Important. This is your stuff. Private means only you and the people you invite can see it.)
4. Do not initialize with README, gitignore, or license. Leave it completely empty. Those options add starter files, and your folder already has yours.
5. Click Create repository.
6. GitHub will show you a "push existing repository" snippet. Copy those commands and paste them in your terminal. **Push** means send your work up to GitHub so it is backed up online.

You're now set up. Two folders side by side at `~/Applications/`:

- `valor-core/` (shared, read-only for you)
- `valor-{firstname}/` (private, yours)

---

## Phase 4: Compose

In your private workspace, you'll create five starter files. Templates live in `valor-core/templates/`. Copy them in:

```bash
cd ~/Applications/valor-{firstname}
cp ../valor-core/templates/CLAUDE-template.md CLAUDE.md
cp ../valor-core/templates/staff-workspace-starter.md ./
```

Open `staff-workspace-starter.md`. It contains four templates concatenated together. Follow the instructions inside it to split them out into `department.md`, `workflows.md`, `references.md`, and `tasks.md`. Then delete the starter file.

### What each file does

| File | What goes in it |
|---|---|
| **CLAUDE.md** | Your role, scope, voice, who you collaborate with, how your agent should behave. The most important file. |
| **department.md** | Your ministry area: scope, KPIs, owned assets, what success looks like for your lane. |
| **workflows.md** | Recurring tasks and weekly rhythms. The sequences your agent should learn. |
| **references.md** | Your *personal* references. Vendor contacts, books you read, tools you use. Layered on top of `valor-core/references.md`. |
| **tasks.md** | Your live to-do. Time-sensitive items only. Prune weekly. |

### Build your own voice profile

`valor-core/voice.md` is the Valor house floor: the shared rules that keep the whole team sounding like one church. It is not meant to make you sound like Justin. In your own workspace, build a short **voice profile** so your agent writes like *you*, inside Valor's rules. Capture how you actually talk: your go-to phrases, your rhythm, what you'd never say, a few real examples of your own writing. Put it in your CLAUDE.md or a `voice-me.md`. The house floor is the same for everyone; your profile is your fingerprint. Justin can point you to the voice-profile builder if you want help.

### What stays out of this workspace

- **Congregant PII** (personally identifiable information: full names, emails, phones, addresses) in committed files. Use Planning Center for that. If you must reference a person, use first name only or initials, and keep the full record in PCO.
- **Financial figures and partner giving amounts.** Those live in Justin's private workspace. If you need a number, ask him directly.
- **Secrets** (API keys, passwords, .env files). An **API key** is a secret password that lets one piece of software use another. Treat one like a credit card number. A **`.gitignore`** is a short list of files you are telling git to ignore and never back up. Add one to your repo and never commit a secret.
- **Counseling and pastoral confidences. Never, anywhere, in any AI tool.** Do not paste, type, summarize, or store counseling sessions, care conversations, confessions, or disciplinary matters into Claude, a workspace file, or any AI chat. These stay off the system entirely. If you want to think through a care situation in general terms, do it with no names and no identifying detail.

---

## Phase 5: Justin approval

Send Justin a Slack DM in `#justin-claude` with:

- A link to your GitHub repo
- One question: anything you're unsure about

Justin will read, edit if needed, and green-light. Usually under 24 hours.

Once approved, you're cleared for Phase 6.

---

## Phase 6: In-person training (60 min)

Schedule 60 minutes with Justin. Format:

1. **The Why, in his words** (10 min).
2. **Tour your setup together** (15 min).
3. **First real task** (20 min). Bring a real piece of work from your plate. Run it through Claude Code together. Refine.
4. **Daily rhythm drill** (10 min). Pull, work, push. Do it once with him watching.
5. **Q&A and homework** (5 min). Leave with one solo task to run before next week.

After this session, you're live.

---

## The Valor week

The shared staff rhythm your agent should assume:

- **Monday, 8:30-10:00 AM: Executive Team meeting.** Some in person, some on Zoom. This walks the eight checkpoints in `scoreboard.md`. Come with your numbers and your section ready.
- **Tuesday through Friday:** office or work-from-home, on your own ministry work.
- **Wednesday nights:** youth night.
- **Sunday:** Sunday. Services, guests, load-in and teardown (mobile church).

Justin's own rhythm to respect when you need him: Wednesday is his day off, and Thursday/Friday are sermon-writing days. Don't stack heavy asks against those unless it's urgent.

## Daily rhythm

Every time you sit down to work in your workspace:

1. **Pull from valor-core** (so you have the latest canon):

   ```bash
   cd ~/Applications/valor-core
   git pull
   ```

2. **Pull from your own repo** (in case you worked on another machine):

   ```bash
   cd ~/Applications/valor-{firstname}
   git pull
   ```

3. **Work.** Open your workspace in Antigravity, run `claude` in the integrated terminal, edit files, do your thing.

4. **Commit and push when done.** A **commit** is a saved snapshot of your changes with a short note about what changed. Saving a file saves it on your computer; committing marks that version in the history so you can find it or undo it later. **Push** sends those commits up to GitHub so they are backed up. `git add -A` in the first line just means "include all my changed files in this snapshot."


   ```bash
   git add -A
   git commit -m "short description of what changed"
   git push
   ```

   Examples:

   - `update workflows for new content rhythm`
   - `add June bulletin draft`
   - `notes from Tuesday staff meeting`

If `git push` says "rejected" because you pushed from another machine first, run `git pull`, then `git push` again.

---

## Hard rules

- **Never commit secrets.** API keys, passwords, .env files. Use a `.gitignore`. If you accidentally commit one, tell Justin immediately. Do not try to clean it up yourself.
- **Your repo is private.** Don't fork it, share screenshots, or paste contents into public tools (ChatGPT, public Slack, public Notion). Claude Code and Antigravity are fine. They are under our agreements.
- **CLAUDE.md is the law.** Your CLAUDE.md AND `valor-core/CLAUDE.md`. Voice, brand, doctrine rules apply to anything produced for Valor.
- **No em dashes in public copy.** This is the most-violated rule. Use periods or commas. Internal working files in your workspace can use them. Anything destined for an audience outside the staff cannot.
- **When in doubt, pull then ask.** A 30-second message in Slack saves an hour of untangling a problem.

---

## Quick-reference commands

| What | Command |
|---|---|
| Update valor-core (the shared canon) | `cd ~/Applications/valor-core && git pull` |
| Update your own repo | `cd ~/Applications/valor-{firstname} && git pull` |
| See what you've changed | `git status` |
| Stage everything | `git add -A` |
| Commit | `git commit -m "message"` |
| Push to GitHub | `git push` |
| Start Claude in this folder | `claude` |
| Quit Claude | `/exit` |

---

## Troubleshooting

**"command not found: git"**: Phase 2 didn't finish. Re-run it.

**"command not found: claude"**: Close and reopen the terminal. If still missing, re-run the Claude Code install.

**"Permission denied (publickey)" when pushing**: You probably set up SSH instead of HTTPS. Easiest fix: re-clone with the HTTPS URL and use a personal access token.

**Merge conflict**: This is what happens when the same line of the same file got changed in two places and git cannot tell which version wins. Nothing is broken and nothing is lost. It just needs a human to pick. Don't panic. Run `git status` to see which files. Open them in Antigravity, look for `<<<<<<<` and `>>>>>>>` markers, decide which version to keep, save, then `git add -A && git commit -m "resolve conflict" && git push`. If unsure, message Justin before saving.

**Claude says "I don't see CLAUDE.md"**: You're in the wrong folder. Run `cd ~/Applications/valor-{firstname}` and try again.
