# Current State

> Updated at the end of every work session. Read this first.

## Active Branch

`main`

## Plan

- [x] Make repo public + enable GitHub Pages (`main` / root)
- [x] Commit `CNAME` → `harnessdeck.finklea.dev`
- [ ] Human: add Cloudflare DNS CNAME `harnessdeck` → `taylorfinklea.github.io` (**DNS-only / grey cloud**)
- [ ] After DNS resolves: `gh api -X PUT repos/TaylorFinklea/harnessdeck-site/pages -f https_enforced=true`

## Build Status

- Pages: `status=built`; edge serves 200 (verified via `Host:` header against 185.199.108.153)
- `harnessdeck.finklea.dev`: does NOT resolve yet — DNS record missing

## Blockers

- Custom domain unreachable until the human adds the Cloudflare DNS record above.

## Open Questions

- Untracked screenshot litter in worktree (`hero.png`, `fullpage.png`, `.playwright-mcp/`) — delete or gitignore.
