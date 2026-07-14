# Decisions

> Architecture decision records. Append-only — one entry per decision.

<!-- Template for each entry:

## [YYYY-MM-DD] Decision Title

**Context**: What prompted this decision?
**Decision**: What was chosen?
**Alternatives considered**: What else was evaluated?
**Rationale**: Why this over the alternatives?
-->

## [2026-07-13] Host on GitHub Pages; repo made public

**Context**: Site had never been deployed — private repo, one commit, no Pages, no
deployments. `index.html` already hardcoded `og:url`/`og:image` as
`https://harnessdeck.finklea.dev`, so a custom domain was assumed from the start.

**Decision**: Serve from GitHub Pages (`main`, root) at `harnessdeck.finklea.dev`.
Repo flipped **private → public**. `CNAME` file committed.

**Alternatives considered**: Cloudflare Pages (would serve publicly while keeping the
repo private); default `taylorfinklea.github.io/harnessdeck-site` URL (zero DNS, but
would have required rewriting the OG tags or breaking link previews).

**Rationale**: Free-plan Pages refuses private repos (`422: Your current plan does not
support GitHub Pages for this repository`), so public was the price of the simplest
host. Contents were reviewed first — static assets, LICENSE, repo AGENTS.md, blank
handoff templates; no secrets, single commit, so no history to leak. Custom domain was
chosen over the default URL because the OG tags already pointed at it.

**Caveat**: Cloudflare proxy (orange cloud) must stay OFF for the `harnessdeck` record
until GitHub issues the Let's Encrypt cert, or issuance fails / redirect-loops.
