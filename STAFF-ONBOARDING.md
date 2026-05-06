# STAFF-ONBOARDING.md (Valor Church)

Welcome to the Valor staff workspace. This doc walks you through the one-time setup. Plan on 45 minutes for the technical setup, plus a 60-minute in-person training session with Justin.

If you get stuck, message Justin or Glenn. Don't hack around it. We want everyone on the same setup.

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

- **valor-core** (shared, read-only for you): the source of truth for who Valor is, our voice, brand, doctrine, stories, references. Justin maintains this. You pull updates.
- **valor-{your-name}** (your private workspace): your own files. Your CLAUDE.md, your department docs, your task list, your working files. You own this. Justin can see it on GitHub, but it's yours.

Two folders, two GitHub repos, one Claude account that reads both.

---

## The 6 phases

1. **Why** (5 min). You're reading this. Done.
2. **Accounts and tools** (15 min). Set up Claude Pro, Claude Desktop, Claude Code, Antigravity, GitHub.
3. **Setup** (15 min). Create your workspace folder, clone valor-core, create your private repo.
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

Claude Code is Anthropic's CLI. It runs in your terminal and reads the .md files in your workspace.

**On macOS:**

Open Terminal (Cmd+Space, type "Terminal", hit enter). Paste this:

```bash
xcode-select --install
```

If a dialog pops up, click Install. This gives you `git`, which you need.

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

Antigravity is Google's AI-native IDE. Same files as Claude Code, different surface. Useful for visual editing.

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
5. **Send your GitHub username to Justin in Slack.** He has to invite you to the valor-core repo before you can clone it.

You'll get an email invite from GitHub when Justin adds you. Click the link, accept, and you're in.

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

Justin will give you the exact URL when he invites you. Likely:

```bash
git clone https://github.com/justinmckay-bot/valor-core.git
```

You should now have a folder at `~/Applications/valor-core/`.

The first time, GitHub may ask you to sign in. Use your GitHub username and a **personal access token** as the password (GitHub doesn't accept passwords directly anymore). To get a token:

1. Go to https://github.com/settings/tokens. Click "Generate new token (classic)".
2. Name it `valor-laptop`. Expiration: 1 year. Scope: check `repo`.
3. Generate. Copy. Paste as password when prompted.
4. Save it in your password manager. You won't see it again.

### Create your own private workspace

Decide your workspace name. Use `valor-{firstname}` (lowercase). Examples: `valor-glenn`, `valor-nathan`, `valor-chris`.

```bash
cd ~/Applications
mkdir valor-{firstname}
cd valor-{firstname}
git init
```

This is your private folder. Nobody else sees what's in here unless you push it to GitHub.

### Push your workspace to GitHub (private)

1. Go to https://github.com/new.
2. Repository name: `valor-{firstname}`.
3. **Private.** (Important. This is your stuff.)
4. Do not initialize with README, gitignore, or license. Leave it empty.
5. Click Create repository.
6. GitHub will show you a "push existing repository" snippet. Run those commands in your terminal.

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

### What stays out of this workspace

- **Congregant PII** (full names, emails, phones, addresses) in committed files. Use Planning Center for that. If you must reference a person, use first name only or initials, and keep the full record in PCO.
- **Financial figures and partner giving amounts.** Those live in Justin's private workspace. If you need a number, ask him directly.
- **Secrets** (API keys, passwords, .env files). Add a `.gitignore` to your repo and never commit them.

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

4. **Commit and push when done:**

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

**Merge conflict**: Don't panic. Run `git status` to see which files. Open them in Antigravity, look for `<<<<<<<` and `>>>>>>>` markers, decide which version to keep, save, then `git add -A && git commit -m "resolve conflict" && git push`. If unsure, message Justin before saving.

**Claude says "I don't see CLAUDE.md"**: You're in the wrong folder. Run `cd ~/Applications/valor-{firstname}` and try again.
