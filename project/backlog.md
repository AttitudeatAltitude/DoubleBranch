# Backlog

STATE — budget 900 words. Status: todo / doing / blocked / done.
Blocked items name who and since when. Done items are cleared when
their phase closes.

## Phase 1 — Content gathering
- [doing] Fill facts.md — remaining: year founded; mailing address if
  different (affiliation done 2026-11-06) — Kevin (a deacon is also
  gathering info)
- [done] Church email doublebranchbaptist@gmail.com on Contact page —
  Kevin set up, 2026-10-21
- [doing] **Get a copy of the church bylaws and the church's mission
  statement** (photo or scan is fine) — a deacon is gathering both
  (2026-10-22); Kevin as backup. Feeds beliefs.md and possibly ministries/leadership
  structure. Original stays outside the repo; distil only.
- [doing] List ministries + recurring events with times and contact role
  — Sunday school classes recorded 2026-11-06. Remaining: times for
  Monday and youth meetings; events — Kevin
- [todo] Pastor bio + photo, with permission to publish — Kevin → pastor
- [todo] **Building photos** (agreed 2026-10-19): road sign, front of
  building, entrance, empty sanctuary. No people. Exterior in the first
  or last ~2 hours of sun, with the sun behind the photographer; bright
  overcast also works; avoid midday. Sanctuary mid-morning, lights on.
  Fall color now (late Oct–early Nov) is a good window — Kevin / a
  member
- [done] Leader names on About, incl. deacons — leadership approved
  Nov 8 (per Kevin)
- [todo] Leader blurbs for About (leadership OK'd asking, Nov 8):
  pastor, each deacon, each ministry leader — 1–2 sentences, each
  person's OK; photos optional, under the photo policy — Kevin
- [done] Exact map pin set (35.073058, -94.588978); Directions links
  use it — Claude, 2026-10-19
- [todo] **Confirm the street number** (18650 or 18670 Old Highway 112)
  before launch, e.g. from the church's mail or a utility bill — Kevin,
  or the deacon if Kevin doesn't get to it first
- [doing] Remaining visitor answers: nursery done (2026-11-06).
  Children's church: "school age" for now; exact ages later — Kevin
- [done] "What to expect" copy on Plan a Visit from Kevin's answers —
  Claude, 2026-10-19

## Phase 2 — Build V1
- [blocked] D3 online giving — leadership comparing (incl. Venmo),
  since 2026-11-08. One-page comparison sent to Kevin 2026-11-08
  (not committed); summary in decisions-needed.md
- [done] Site skeleton (runs ahead of phase, Kevin asked) — 7 pages
  (D5), Jekyll (D2): shared layout; services, church, nav, events,
  ministries in `docs/_data/`; preview banner + noindex via
  `preview:` in `_config.yml` — Claude, 2026-10-19
- [todo] Fill page copy as church/ facts are confirmed — Claude
- [todo] **~80% of V1 ready for leadership's Nov 8 meeting** — Claude
  (copy) / Kevin (facts, photos)
- [done] Tracker board for Kevin (private artifact, two-way: answers,
  ticks, decisions, notes) — Claude, 2026-10-19. Sync steps in
  project/CLAUDE.md (approved)
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
- [done] Weekly check-in: scheduled task "Weekly website check-in",
  Sundays 2:39 PM Central, fresh session, push note to Kevin (Kevin
  agreed 2026-11-08). Runs ahead of phase. First run Nov 15 — check it
  reached the repo (no repo or connectors stored on the task)
- [done] Editing guide for a non-Claude editor: Claude Doc "How to
  Edit the Double Branch Website" (Kevin's, private;
  https://claude.ai/artifact/WMHvV1eTwSC9MViTDbUe9p), 2026-11-08.
  docs/README.md is the in-repo version; keep both in step
- [doing] **Sermon audio** (runs ahead of Phase 4) — guide drafted
  (church/audio-guide.md). Next: confirm an SD card is in the L-20; one
  test recording; pick where audio lives (D7) — Kevin
- [todo] Video/camera upgrade recommendation — deferred until audio is
  running and a budget exists
- [done] YouTube channel @DoubleBranchBaptist live; linked from
  Sermons — Kevin / Claude, 2026-11-08
- [done] Sermons embeds the channel's uploads (newest first); "Watch
  live" links to /live — Claude, 2026-11-08. Kevin to check it plays
- [todo] Name a second maintainer (editing guide already in
  `docs/README.md`)

## Proposed (not yet agreed)
- **Search-engine "church card" data** — add a hidden block to the
  layout that tells Google, in its own format (schema.org `Church`),
  the name, address, and service times, all read from `_data/`. About
  15 minutes. Helps Google show the address and times directly in
  search results. Pairs with the Google Business Profile item.
  (Claude, 2026-10-19)
- **Google Business Profile** — free; it's what shows when someone
  searches "Baptist church Poteau" or opens Maps. Arguably more visitors
  will find the church through it than through the site itself. Needs
  someone to verify the church address. (Claude, 2026-10-19)
- **Simple shared "events inbox"** — one person/channel (e.g. a church
  email or text thread) where ministry leaders send event updates, so
  events.md doesn't depend on Kevin hearing about things. (Claude,
  2026-10-19)
