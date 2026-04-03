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

## Known Issues

- `useAuth` hook still expects `data.token` — needs update for `{ accessToken, refreshToken }` response
- Xcode bundle ID still has `com.anonymous.TokenSports-Utility` — needs prebuild to sync

## Next Steps

1. Update useAuth for new token pair response
2. Build GSD dashboard — visual list of GSD instances with status
3. Set up EAS for TestFlight builds
4. Add human users

## Status

🟡 Functional but needs auth hook update and TestFlight build.
