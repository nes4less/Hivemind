# Shared Knowledge

Cross-project lessons, patterns, and rules that apply across the entire fleet.

## Patterns

### Auth System
The Token Remote auth system (bcrypt, JWT access/refresh tokens, RBAC, throttling) was built in TokenRemote-Express M006 and is the canonical pattern. Cloned from Token Sports Express. Any new API service should follow the same shape.

### GSD Project Structure
Every project with active development should have a `.gsd/` directory (symlinked to `~/.gsd/projects/<hash>/`). The PROJECT.md inside is the source of truth for what the project is and where it stands. Hivemind project files mirror this but are readable by all GSD sessions.

### Supabase
Single Supabase instance (`ximnhbkjjfsfalylluwf`) serves the entire Token Remote ecosystem. All tables in one project — no multi-instance split.

### Vercel Deployment
- Web app: tokenremote.com (Next.js)
- API: api.tokenremote.com (Express serverless)
- Domain: tokenremote.com ($11.25/yr via Vercel)

## Rules

1. **One GSD per project repo at a time.** Don't run two GSD sessions in the same project directory — markdown artifact writes aren't transactional across sessions.
2. **Hivemind is read-by-all, write-by-active.** Any GSD session should read all project files on startup. Only update the file for the project you're actively working on.
3. **Machine files are self-reported.** Each machine updates its own file. Don't guess another machine's state.
4. **Every commit gets a tag and description.** Use a short tag prefix for the area of change (e.g. `fix:`, `feat:`, `refactor:`, `ui:`, `daemon:`, `auth:`, `ota:`, `model:`). Follow with a clear description of what changed and why. No bare "update" or "changes" commits. The commit message is the changelog — make it useful to a future agent landing cold.

## Lessons Learned

- Token Sports → Token Remote clone worked well. Removing sports-specific models was clean because the base model system was well-separated.
- WEBFu's SQLite + Next.js pattern is solid for local-only tools. No external dependencies, fast, simple.
- The daemon's auto-detect of `.gsd/` directories is the key to multi-project support — no manual config needed.
