# Cowork OS Starter

A starter template for [Cowork mode](https://www.anthropic.com/) — Anthropic's desktop tool that turns Claude into a workplace collaborator. Drop these files into a folder, point Cowork at it, and you have a working "operating system" with memory, voice, and modular workstations.

Inspired by [this video](https://www.youtube.com/watch?v=0_dSWLOHKng&t=465s).

## Using a different language

This starter is in English, but Cowork is multilingual. After setup, ask Cowork: *"Translate CLAUDE.md and MEMORY.md to [your language] and keep them in sync from now on."* Cowork will rewrite the files in place and preserve the section structure. You can do the same for any workstation you create later.

## What's in here

```
.
├── CLAUDE.md              # Root project instructions Cowork reads every session
├── MEMORY.md              # Long-term memory: active projects + facts about you
├── 00_Resources/
│   └── voice-principles.md  # Teaches Cowork to write in your voice
├── Vibe_Coding_HQ/        # Example workstation — rename, gut, or replace
│   ├── CLAUDE.md
│   ├── MEMORY.md
│   └── Resources/
└── _templates/
    └── workstation/       # Copy this folder when you create a new workstation
        ├── CLAUDE.md
        ├── MEMORY.md
        └── Resources/
```

`Vibe_Coding_HQ/` ships as a worked example so you can see the format before building your own. Read it for reference, then rename, gut, or delete the folder. The Routing Map row in the root `CLAUDE.md` points to it.

## How it works

**Two-tier memory.** `CLAUDE.md` holds rules that prescribe Cowork's behavior ("always do X"). `MEMORY.md` holds facts that change over time (active projects, contacts, decisions). When you say "remember this," Cowork picks the right file.

**Workstations.** As your work grows, you add focused subfolders — Email, Finances, a specific client — each with its own `CLAUDE.md`, `MEMORY.md`, and `Resources/`. The Routing Map in the root `CLAUDE.md` tells Cowork which workstation to load based on what you ask.

**Voice.** `00_Resources/voice-principles.md` is read whenever Cowork writes anything on your behalf, so emails and documents sound like you, not like an AI.

## Setup (5 minutes)

1. Download or clone this repo into a folder you'll keep — Obsidian vault, iCloud Drive, Dropbox, anywhere.
2. Open Cowork and point it at that folder (use the folder picker).
3. Open `MEMORY.md` and replace the placeholder entries with your real info — your tools, your manager, anything you want Cowork to remember.
4. Personalize `00_Resources/voice-principles.md` — either edit it directly or paste in 5 of your emails and ask Cowork to extract your voice patterns.
5. Start a session. Say "what can you do?" and Cowork will read these files and brief you.

## Creating a new workstation

When a new domain of work comes up — a project, a recurring report, a client — ask Cowork: *"Create a workstation for [name]."* It will copy `_templates/workstation/` into a new folder and add a row to the Routing Map so future sessions auto-route there.

You can also do it manually: copy `_templates/workstation/` to a new folder, fill in the Identity paragraph and Workflow steps in that workstation's `CLAUDE.md`, and add the routing row yourself.

## License

MIT. Fork it, remix it, share it.
