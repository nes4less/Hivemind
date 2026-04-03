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

- **Render Protocol** — 7-step resolution chain (ViewGroup → View → Style → Platform Output)
- **Model-driven MessageCenter** — tabs, styles, interactions all defined as TokenBase model records
- **Thread model** — first-class threads table, app + daemon create/update Thread records, realtime
- **FunctionExecutor** — central gesture handler registry, eliminates copy-paste handlers
- **Generic renderers** — CardRenderer, RowRenderer, ThreadRow, TaskCard, ViewRenderer, ViewGroupRenderer
- **Full loop verified** — message → thread → task → daemon → reply → thread update → realtime
- **OTA live** — Build 22, latest OTA ab2f8559

## Known Issues

- iOS password autofill (Associated Domains not configured)
- Comments tab using notifications data (placeholder)
- SDK 54/Xcode 26 upgrade needed before April 28

## Next Steps

1. Extract ComposeModal as model-driven component (Prompt model)
2. ViewState persistence (scroll, expanded, filters → AsyncStorage)
3. Wire Comments tab to real data
4. SDK 54/Xcode 26 upgrade

## Status

🟢 Active development — all render protocol steps complete, model-driven UI working.
