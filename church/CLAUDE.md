# Church

> Global conventions in the root CLAUDE.md apply. Below is what's
> specific to this folder.

## Role

Keeper of the church's facts. This folder is the single source of truth
for everything the website says about Double Branch Baptist Church; the
site in `docs/` is built *from* it. Goal: any fact on the site can be
traced to a line here, and every line here says how sure we are of it.

## Operating Principles

- **Facts first, then pages (hard rule).** A fact changes here before it
  changes on the site, in the same commit or earlier. Never edit a
  service time or address only in `docs/`.
- **Every fact carries a status:** `confirmed (source, date)`,
  `unconfirmed (source, date)`, or `unknown`. "Source" is a person's
  role ("Kevin", "per leadership via Kevin") or a sources-log.md entry.
  Only `confirmed` facts go on the public site; the rest render as
  `[TBD]`.
- **The church owns its doctrine.** beliefs.md text is the church's own
  words (expected source: the bylaws), approved by leadership. Don't paraphrase, summarize, or "improve" a
  statement of faith; if a plain-language intro is wanted, draft it
  separately and mark it for approval.
- **Public-safe only.** See the root Privacy rule. Contacts here are
  church contacts, not personal ones.
- **Watch for staleness.** events.md drifts fastest. Past events are
  removed (git keeps history); when a session finds an event date in
  the past, remove it and flag whether the site still shows it.
- Safety (repeated from root on purpose): never force-push; never
  rewrite past entries in sources-log.md.

## Files

- README.md — quick map of this folder (keep current).
- facts.md — STATE (budget 600 words). Name, address, service times,
  contact, affiliation, pastor/staff, online presence — each with
  status.
- beliefs.md — STATE (budget 1200 words). Statement of faith and
  identity, in the church's approved words.
- ministries.md — STATE (budget 800 words). Ministries and groups
  (Sunday school, youth, men's, women's, kids): what, when, who to ask.
- events.md — STATE (budget 600 words). Upcoming events and recurring
  calendar items only.
- media.md — STATE (budget 600 words). Sermons/livestream setup (where
  it streams, how, with what equipment) and the streaming-upgrade plan.
- audio-guide.md — REFERENCE. Weekly sermon-audio recording steps for
  the soundboard volunteer (human-facing). Update when the setup in
  media.md changes or a test Sunday shows a step is wrong.
- sources-log.md — APPEND-ONLY LOG. Manifest of source documents and
  information received: date, what, from whom, where the original is
  kept, which files it fed.

## Run Sequence

1. Orient: read facts.md in full, plus whichever other STATE file the
   task touches; tail sources-log.md.
2. Surface open items: `unknown`/`unconfirmed` facts that block the
   current phase, and any past-dated events.
3. Do the task — record new info with its status and source.
4. Journal:
   - Update the STATE file(s) touched.
   - Append sources-log.md for any document or batch of info received.
   - If a confirmed fact changed and the site already shows it, update
     `docs/` in the same commit (subject to the publish gate) or add a
     backlog item.
   - Project files per `project/CLAUDE.md`.
5. Commit with the prefixes below; end-of-task git per root CLAUDE.md.

## Commit Prefixes

- `facts:` — facts.md
- `beliefs:` — beliefs.md
- `ministry:` — ministries.md
- `events:` — events.md
- `media:` — media.md
- `source:` — appended to sources-log.md
- `context:` — structural changes to this folder
