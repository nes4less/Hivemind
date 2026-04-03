# Hivemind Protocol

> **Every GSD session must read this file before starting work.**

## The Rules

### 1. One File Per GSD, One File Per Project, One File Per Machine

- Each GSD instance writes **only its own file** in `gsds/`
- Each project has **one file** in `projects/` — any GSD that works on that project updates it
- Each machine has **one file** in `machines/` — only updated by sessions running on that machine
- **No merges. No shared write targets.** Conflicts are impossible because ownership is exclusive.

### 2. Read All, Write Yours

On startup, every GSD session:
1. Reads `PROTOCOL.md` (this file)
2. Reads `OBJECTIVES.md` (back-of-mind goals)
3. Reads **all files** in `gsds/`, `projects/`, and `machines/`
4. Reconciles its own GSD file with what it learned

On completion of meaningful work:
1. Updates its own `gsds/<name>.md` with current status, recent activity, and anything other GSDs should know
2. Updates the relevant `projects/<name>.md` if project state changed (milestone complete, new capability, status change, known issues)
3. Updates `machines/<name>.md` if machine state changed (new software, new project dir, service change)
4. Updates `knowledge/shared.md` if a cross-project lesson was learned
5. Updates `knowledge/effectiveness.md` if it observed something about its own performance or model limitations

### 3. How GSDs Communicate

GSDs don't talk to each other directly. They communicate through their files:
- **Status:** What am I doing right now?
- **Recent activity:** What did I just finish?
- **Blockers:** What's stuck and why?
- **Requests:** What do I need from another GSD or from the human?
- **Observations:** What did I notice that others should know?

### 4. Project File Updates

When a GSD completes work on a project, it updates that project's file with:
- New capabilities added
- Status changes
- Known issues discovered or resolved
- Next steps (if changed)

Multiple GSDs can work on different projects simultaneously. If two GSDs need to update the same project file, the second one should read-then-write (last writer wins is acceptable since updates are additive, not destructive).

### 5. Machine Files

Machines check each other's status via Token Remote. Machine files document:
- What's installed
- What services are running
- What projects are checked out
- Current activity (updated by the active GSD session on that machine)

### 6. Pulling Updates

Before starting work, pull Hivemind:
```bash
cd ~/Desktop/Hivemind && git pull --rebase
```

After updating files, commit and push:
```bash
cd ~/Desktop/Hivemind && git add -A && git commit -m "<gsd-name>: <what changed>" && git push
```
