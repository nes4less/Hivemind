# Token Remote — Web + Daemon

## Identity

| Field | Value |
|---|---|
| **Repo** | `nes4less/TokenRemote` |
| **Path** | `~/Developer/TokenRemote` |
| **Stack** | Next.js, Node.js, Supabase |
| **Live** | https://tokenremote.com |
| **GSD** | Yes (local `.gsd/`) |

## What It Is

Web app + daemon for managing GSD instances from anywhere. Phone-first chat UI for sending tasks, plus a Mac daemon (launchd) that polls Supabase for pending tasks and spawns GSD in the correct project directory.

## Architecture

```
Phone (Safari) → tokenremote.com (Next.js on Vercel)
                    ↕ Supabase task queue
Mac daemon (launchd) → polls queue → runs GSD → streams output back
```

## Key Capabilities

- Chat-style task UI with history
- Commands: free text tasks, /restart, /clear, /status
- Single-user auth (bcrypt hashed in Supabase)
- 2s polling for task output streaming
- PWA: add to home screen for full-screen
- Daemon: auto-starts on boot, auto-restarts on crash, auto-detects project directories
- One-line installer: `curl -fsSL https://tokenremote.com/install.sh | bash`

## GSD History

12 milestones complete — base model integration (4 phases), DataSource model, full auth layer, GSD project management interface, universal UI shell, auth hardening, multi-device fleet manager, unified communications platform, macOS status bar companion app.

## Status

✅ Complete — all milestones delivered. Live at tokenremote.com.
