# Backlog

STATE — budget 900 words. Status: todo / doing / blocked / done.
Blocked items name who and since when. Done items are cleared when
their phase closes.

## Phase 0 — Setup & decisions
- [done] Repo structure + CLAUDE.md files drafted — Claude, 2026-10-19
- [done] CLAUDE.md files approved — Kevin, 2026-10-19
- [done] Leadership-team approval wording merged — Kevin, 2026-10-19
- [todo] Tell the pastor/leadership team about the project; get an OK
  to proceed and agreement on how approvals will work (D6) — Kevin
- [todo] Decide D3, D4, D6, D7 (decisions-needed.md) — Kevin / leadership

## Phase 1 — Content gathering
- [doing] Fill facts.md — remaining: which Baptist body the church is
  affiliated with; Facebook page link (Sermons + Contact pages); year
  founded; mailing address if different — Kevin
- [todo] **Get a copy of the church bylaws** (photo or scan is fine)
  — Kevin. Feeds beliefs.md and possibly ministries/leadership
  structure. Original stays outside the repo; distil only.
- [todo] List ministries + recurring events with times and contact role
  — Kevin
- [todo] Pastor bio + photo, with permission to publish — Kevin → pastor
- [todo] Photo policy (no identifiable kids) approved by leadership — Kevin
- [todo] **Building photos** (agreed 2026-10-19): road sign, front of
  building, entrance, empty sanctuary. No people. Exterior in the first
  or last ~2 hours of sun, with the sun behind the photographer; bright
  overcast also works; avoid midday. Sanctuary mid-morning, lights on.
  Fall color now (late Oct–early Nov) is a good window — Kevin / a
  member
- [todo] Leader blurbs for About: pastor, each deacon, each ministry
  leader — name, role, 1–2 sentences, each person's OK — Kevin
- [done] Exact map pin set (35.073058, -94.588978); Directions links
  use it — Claude, 2026-10-19
- [todo] **Confirm the street number** (18650 or 18670 Old Highway 112)
  before launch, e.g. from the church's mail or a utility bill — Kevin
- [todo] Remaining visitor answers: nursery/children's class ages and
  when each meets — Kevin
- [done] "What to expect" copy on Plan a Visit from Kevin's answers —
  Claude, 2026-10-19

## Phase 2 — Build V1
- [done] Site skeleton (runs ahead of phase, Kevin asked) — 7 pages
  (D5), Jekyll (D2): shared layout; services, church, nav, events,
  ministries in `docs/_data/`; preview banner + noindex via
  `preview:` in `_config.yml` — Claude, 2026-10-19
- [todo] Fill page copy as church/ facts are confirmed — Claude
- [done] Preview link live: https://attitudeataltitude.github.io/DoubleBranch/
  — repo public + Pages from `main` `/docs` (Kevin), first deploy
  verified 2026-10-19

## Phase 3 — Review & launch
- [todo] Leadership full-site review → approvals-log.md — Kevin →
  leadership
- [todo] Launch: set `preview: false` in docs/_config.yml after
  leadership approval — Claude
- [todo] Link site from Facebook page — whoever runs it

## Phase 4 — Post-launch
- [doing] **Sermon audio** (runs ahead of Phase 4) — guide drafted
  (church/audio-guide.md). Next: confirm an SD card is in the L-20; one
  test recording; pick where audio lives (D7) — Kevin
- [todo] Video/camera upgrade recommendation — deferred until audio is
  running and a budget exists
- [todo] YouTube channel setup + migration plan from Facebook
- [todo] Name a second maintainer (editing guide already in
  `docs/README.md`)

## Proposed (not yet agreed)
- **Search-engine "church card" data** — add a hidden block to the
  layout that tells Google, in its own format (schema.org `Church`),
  the name, address, and service times, all read from `_data/`. About
  15 minutes. Helps Google show the address and times directly in
  search results. Pairs with the Google Business Profile item.
  (Claude, 2026-10-19)
- **Free church email (e.g. a Gmail account) for the Contact page** —
  the site currently has no way for a visitor to reach anyone. A free
  address owned by the church (not a person), with login shared between
  2 people on the leadership team, solves it in 15 minutes and survives
  volunteers changing. Optionally a free Google Voice number later.
  Needs leadership OK. (Claude, 2026-10-19)
- **Google Business Profile** — free; it's what shows when someone
  searches "Baptist church Poteau" or opens Maps. Arguably more visitors
  will find the church through it than through the site itself. Needs
  someone to verify the church address. (Claude, 2026-10-19)
- **Simple shared "events inbox"** — one person/channel (e.g. a church
  email or text thread) where ministry leaders send event updates, so
  events.md doesn't depend on Kevin hearing about things. (Claude,
  2026-10-19)
