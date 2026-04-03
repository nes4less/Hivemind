# Token Remote Express — API

## Identity

| Field | Value |
|---|---|
| **Repo** | `nes4less/TokenRemote-Express` |
| **Path** | `~/Developer/TokenRemote-Express` |
| **Stack** | Express/TypeScript, Supabase/PostgreSQL, Vercel serverless |
| **Live** | https://api.tokenremote.com |
| **GSD** | Yes (local `.gsd/`) |

## What It Is

REST API for Token Remote — 22 endpoints serving communications, content, auth, and base model CRUD. Deployed to Vercel as a serverless function.

## Key Capabilities

- Full auth: bcrypt, JWT access tokens (15min), revocable refresh tokens (30d), RBAC, login throttling, password reset via Resend
- 22 resource endpoints with standard CRUD (create, list, count, get, update, soft delete)
- Supabase-only (no MongoDB)

## Endpoints Summary

- **Public:** signup, login, token refresh/revoke, forgot/reset password
- **RBAC-gated:** organizations, publications, subscriptions
- **Authenticated:** comments, content, contexts, events, flags, handshakes, locatables, media, messages, modules, notifications, queries, ranges, relationships, scopes, styles, uploads, views

## Database

Supabase project `ximnhbkjjfsfalylluwf` — 24 tables, single migration.

## Environment Variables

`SUPABASE_URL`, `SUPABASE_SERVICE_KEY`, `JWT_SECRET`, `DB_PROVIDER` (supabase), `RESEND_API_KEY`

## Status

✅ Live at api.tokenremote.com.
