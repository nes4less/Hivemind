# WEBFu — Web Inventory Management

## Identity

| Field | Value |
|---|---|
| **Repo** | `infinitetoken/Webfu` |
| **Path** | `~/Desktop/WEBFu` |
| **Stack** | Next.js (App Router), TypeScript, SQLite, MUI v7 |
| **Live** | Local only — http://localhost:3000 |
| **GSD** | Yes (`~/.gsd/projects/09144e9623bf`) |

## What It Is

Web port of the CashierFu Utility mobile app. Self-contained local inventory management — catalogs, products, units, containers — with auth, search, unitize wizard, transfer, label printing, and image management.

## Key Capabilities

- Full CRUD for Catalogs, Products, Containers, Units
- Library (catalog-first) and Inventory (container-first) browsing
- Cross-entity search across all 4 entity types
- Unitize wizard (5-step flow)
- Transfer units between containers
- Image upload, label printing (CSS @media print)
- Barcode keyboard wedge detection
- Light/dark theme with persistence
- Auth: `admin@webfu.local / password`

## Stats

65 source files, 17 API routes, 28 pages, 4 reusable components, 1 custom hook.

## GSD History

3 milestones complete — Foundation, Utilities & Search, Polish & Desktop Integration.

## Status

✅ Complete — all milestones delivered. Runs locally.
