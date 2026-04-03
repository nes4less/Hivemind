# Hivemind

Central coordination point for all GSD-managed projects and machines. No application code — just the shared brain.

**Read `PROTOCOL.md` first.** Every GSD session must.

## Structure

```
Hivemind/
  PROTOCOL.md            ← Coordination rules (read first)
  OBJECTIVES.md          ← Back-of-mind goals for all GSDs
  gsds/                  ← One file per GSD instance — read all, write yours
  projects/              ← One file per project — updated by any GSD that works on it
  machines/              ← One file per machine — self-reported by sessions on that machine
  knowledge/
    shared.md            ← Cross-project patterns, rules, lessons
    effectiveness.md     ← Self-improvement observations (model limitations, process friction)
```

## The Protocol (summary)

1. **Read all, write yours.** Every GSD reads everything on startup. Each GSD writes only its own file in `gsds/`.
2. **No merges.** One file per entity. Ownership is exclusive. Conflicts are impossible.
3. **GSDs communicate through files.** Status, activity, blockers, requests, observations.
4. **Project files are shared-write.** Any GSD that works on a project updates its file. Last writer wins (updates are additive).
5. **Self-improvement is mandatory.** Track what works, what doesn't, and where models fall short.

## GitHub

`nes4less/Hivemind`
