# Token Remote App — Mobile

## Identity

| Field | Value |
|---|---|
| **Repo** | `nes4less/TokenRemote-App` |
| **Path** | `~/Developer/TokenRemote-App` |
| **Stack** | React Native / Expo 53, Redux Toolkit, React Navigation |
| **Live** | Not yet (pending TestFlight) |
| **GSD** | Yes (local `.gsd/`) |

## What It Is

Mobile app for Token Remote. Communications hub for managing GSD agents — messaging, alerts, board (documents/links), comments, and activity feed.

## Key Capabilities

- Role-based navigation (home, admin, operator)
- MessageCenter — threads, replies, tabs
- Generic entity list/detail views with Context/Style/Query support
- CommentSection — threaded comments on any entity
- HandshakeAlerts — approval gate UI
- AI provider auth integrations (Claude, Gemini, ChatGPT)
- Profile editor, View-driven dashboard sections

## Recent Progress

- **Render Protocol implemented** — 7-step resolution chain (ViewGroup → View → Style → Platform Output)
- **Model-driven MessageCenter** — tabs, styles, interactions defined as TokenBase model records
- **Generic renderers** — CardRenderer, RowRenderer, ViewRenderer, ViewGroupRenderer
- **OTA live** — Build 22 on TestFlight, OTA b1b86359

## Known Issues

- iOS password autofill (Associated Domains not configured)
- Comments tab using notifications data (placeholder)
- SDK 54/Xcode 26 upgrade needed before April 28
- Thread replies not appearing live (needs Thread model)

## Next Steps

1. Extract Thread as first-class entity (fix reply chain)
2. Test full app → daemon → reply loop with Thread model
3. Wire Interaction model to gesture handlers (eliminate copy-paste)
4. Build GSD dashboard — visual list of GSD instances with status

## Status

🟢 Active development — Render Protocol landed, model-driven tabs working.
