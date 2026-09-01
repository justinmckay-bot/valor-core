# GLOSSARY.md (plain English)

Every technical word used in this workspace, explained the way you would explain it to someone who has never written a line of code. Nothing here assumes a tech background. If you hit a word in any Valor file that is not on this list, tell Justin and it gets added.

Read this once before setup. Come back to it any time a term stops making sense.

---

## The big picture, in one paragraph

You are going to keep a folder of plain text files on your computer. Those files tell your AI assistant who Valor is and how you work. A free service called GitHub keeps a backup copy of that folder online, so nothing is ever lost and Justin can share updates with the whole team. The words below are just names for the parts of that arrangement.

---

## The core words

**Repository (or "repo")**
A folder of files that keeps a history of every change ever made to it. Think of it as a filing cabinet with a built-in memory. You can always see what a file looked like last week and go back to it. `valor-core` is a repo. Your own `valor-{yourname}` folder is a repo.

**Git**
The free program that gives a folder that memory. It runs quietly in the background. You will only ever use four or five of its commands.

**GitHub**
A website that stores repos online. It is the backup copy and the sharing point. Git is the program on your computer. GitHub is the place on the internet. Same idea as a Word document on your laptop versus that document in Dropbox.

**Clone**
Downloading a copy of a repo from GitHub onto your computer for the first time. You clone `valor-core` once, at setup.

**Pull**
Downloading the latest changes from GitHub into your folder. Do this when you sit down to work, so you have the newest version of the canon. Same instinct as refreshing your email.

**Commit**
Saving a snapshot of your changes, with a short note about what you changed. Saving a file saves it on your computer. Committing marks that version in the history so you can find it later.

**Push**
Sending your commits up to GitHub so they are backed up and visible. Do this when you finish working.

**Stage (or `git add`)**
Telling git which changed files you want in the next commit. `git add -A` means "all of them," which is what you will use nearly every time.

**Private repo**
A repo only invited people can see. Yours is private. Nobody but you and Justin can read it.

**Fork**
Making your own separate copy of somebody else's repo. You will not need to do this. It is listed here only because the button is on the GitHub page and you should leave it alone.

**Merge conflict**
What happens when the same line of the same file got changed in two places and git cannot tell which version wins. It is not damage and nothing is lost. It just needs a human to pick. Message Justin the first time you see one.

---

## Your tools

**Terminal (Mac) or Git Bash (Windows)**
A plain window where you type commands instead of clicking buttons. It looks intimidating and is not. You will use maybe eight commands total, and they are all in the quick-reference table in `STAFF-ONBOARDING.md`.

**Command line / CLI**
Two other names for the same thing as the terminal. CLI stands for command line interface. If a doc says "run this in the CLI," it means type it in that window.

**Claude Code**
Claude that runs inside the terminal and can read and write the files in your folder. This is what makes your workspace more than a chat window. It actually sees your notes, your doctrine, your voice, and your task list.

**Claude Desktop**
The regular Claude app with the chat box. Good for quick conversation. It does not read your workspace files the way Claude Code does.

**Antigravity (IDE)**
An editor for working with folders of files. IDE stands for integrated development environment, which is a heavy name for "one window where you can see your files, edit them, and run commands." You can run Claude Code inside it.

**Markdown (`.md`)**
Plain text with a few simple formatting marks. `#` makes a heading. `**bold**` makes bold. That is most of it. Every file in this workspace is markdown because both people and AI read it easily.

**Path (like `~/Applications/valor-core`)**
The address of a folder on your computer. The `~` is shorthand for your home folder. So that address means: home folder, then Applications, then valor-core.

---

## Words about the system

**Workspace**
Your folder plus the files in it plus the AI reading them. When someone says "open your workspace," they mean point Claude at your folder.

**Agent**
Your AI assistant once it has been given instructions and files to work from. A chatbot answers questions. An agent works from your standards, in your voice, on your recurring tasks.

**Canon**
The shared "this is who we are" files in `valor-core`. Mission, voice, brand, convictions, stories, references. Justin maintains them. Everyone reads them. That is how the whole staff sounds like one church.

**CLAUDE.md**
The instruction file your agent reads first, every session. It tells the AI who you are, what you do, and how to behave. It is the single most important file you will write.

**Connector**
A link that lets your agent read a live system instead of a file. The Notion connector lets it see the real people and groups data. The calendar connector lets it see your actual schedule.

**Personal access token**
A long password GitHub gives you instead of your real password, for use when your computer talks to GitHub. Generate it once, save it in your password manager, and you are done.

**API key**
A secret password that lets one piece of software use another. Treat one like a credit card number. Never put one in a file you commit.

**`.gitignore`**
A short list of files you want git to ignore and never back up. This is where secrets and private scratch files go.

**PII**
Personally identifiable information. Full names, emails, phone numbers, addresses, giving records. It stays in Planning Center and Notion. It never goes in a file you commit.

**Repo owner vs collaborator**
The owner controls a repo. A collaborator has been invited to it. You own your own workspace repo. You are a read-only collaborator on `valor-core`, which means you can pull updates but cannot change the shared canon. If you spot an error there, flag it to Justin and he corrects it once for everybody.
