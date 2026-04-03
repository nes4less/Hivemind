# Hivemind

Central coordination point for all GSD-managed projects. This repo doesn't contain application code — it holds the shared brain: project registry, machine fleet, cross-project knowledge, and learning material.

## Structure

```
Hivemind/
  projects/           One file per project — read by all GSD sessions
    token-remote.md
    token-remote-express.md
    token-remote-app.md
    token-remote-kit.md
    token-remote-desktop.md
    token-base.md
    webfu.md
    cashierfu-utility.md
  machines/           One file per machine — self-reported status
    macbook-pro.md
    imac.md
  knowledge/          Shared patterns, rules, lessons
    shared.md
```

## How It Works

- **Every GSD session reads `projects/` and `machines/`** to understand what exists and what's happening across the fleet
- **Each GSD updates only its own project file** when meaningful state changes (milestone complete, new capability, status change)
- **Each machine updates its own machine file** when a GSD session starts on it
- **Machines check each other's status** via Token Remote — the machine files tell you what's installed where and what each machine is responsible for
- **`knowledge/`** captures cross-project patterns and lessons that any GSD session should know

## What Doesn't Live Here

- Per-project milestone trees, plans, task artifacts (those stay in each repo's `.gsd/`)
- Per-project databases
- Application source code

## GitHub

`nes4less/Hivemind`
