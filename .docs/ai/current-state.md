# Current State

> Updated at the end of every work session. Read this first.

## Active Branch

`main`

## Plan

- [x] Make repo public + enable GitHub Pages (`main` / root)
- [x] Commit `CNAME` → `harnessdeck.finklea.dev`
- [x] Human added Cloudflare DNS record (came up **proxied** / orange cloud)
- [x] Decision: keep Cloudflare proxy on (see decisions.md 2026-07-15)
- [ ] Human: Cloudflare SSL/TLS → set mode **Full (strict)**
- [ ] Human: Cloudflare Edge Certificates → enable **Always Use HTTPS** (http:// not yet redirected)

## Build Status

- **LIVE**: https://harnessdeck.finklea.dev/ → 200, correct title, 36664 bytes (served via Cloudflare)
- GitHub Pages `status=built`; GitHub-native cert `null` / `https_enforced=false` (N/A while proxied)

## Blockers

- None. Site is live. Remaining items are Cloudflare-dashboard toggles only the human can do.

## Open Questions

- Untracked screenshot litter in worktree (`hero.png`, `fullpage.png`, `.playwright-mcp/`) — delete or gitignore.
