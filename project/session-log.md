# Session Log

APPEND-ONLY LOG. Dated: work done, suggestions made, phase retros.

## 2026-10-19 — Project setup
- Asked Kevin setup questions (role, hosting, V1 scope, PM style,
  visibility, existing presence, photos, git flow).
- Existing presence: sermons broadcast live on Facebook from a
  member's phone; intent to move to YouTube eventually; need proper
  streaming equipment. No website, no giving provider.
- Built repo structure from LifeOS conventions: root + project/,
  church/, docs/ domains. Church name/city taken from LifeOS
  Faith/practices.md (only public facts copied).
- Suggestions made: Google Business Profile; events inbox;
  audio-first sermon archive (all in backlog.md *Proposed*).

## 2026-10-19 — Setup follow-up
- Kevin approved CLAUDE.md files → merged to main.
- Recorded address + service times (confirmed), bylaws to-do,
  audio-only first with $0 budget, leadership-team approvals.
- Leadership change applied to non-instruction files directly; CLAUDE.md
  wording held on branch per root exception 2.
- Suggestion: verify the map pin for the county-road address (backlog
  *Proposed*).

## 2026-10-19 — Soundboard + contact gap
- Merged leadership-team CLAUDE.md wording (approved).
- L-20 records to SD card → $0 audio path; drafted church/audio-guide.md
  (new REFERENCE file; church/CLAUDE.md file list held for review).
- Found: no phone/email means the Contact page has nothing to show.
- Suggestion: free church-owned email account (backlog *Proposed*);
  D7 opened for sermon audio home.

## 2026-10-19 — Site skeleton (design pass)
- Kevin asked to start the site skeleton ahead of Phase 2, focused on
  design. Built docs/: 8 pages per the roadmap draft list (D5 still
  open) + one stylesheet. Plain HTML/CSS, no JS, system fonts, so it
  follows the standing D2 default (option A). D2 itself is still open.
- Design: pine green / cream / clay palette, serif headings, 18px body,
  hills SVG in the hero instead of photos, text wordmark + placeholder
  mark (not a logo). Facts used: name, address, service times only
  (confirmed in facts.md); everything else is a visible `[TBD]`.
- Preview safeguards: "Draft preview" banner and `noindex` on every
  page; remove both at launch.
- Verified with Playwright at 390px and 1280px: no overflow, internal
  links resolve, color pairs ≥ 5.4:1 contrast. Fixed stacked cards
  overlapping on phone.
- Suggestion: building photos to replace the illustrated header
  (backlog *Proposed*).

## 2026-10-19 — Visitor answers + About merge
- Kevin answered 5 of 6 Plan a Visit questions (dress + James 2:1–4,
  ~1 hr, hymns/piano + newer songs to tracks, parking obvious, no
  stairs) → facts.md, then visit.html. Kids/nursery still TBD.
- D5 decided: Pastor & Staff merged into About, which now has pastor,
  deacon, and ministry-leader cards (all TBD). Site is 7 pages.
- Explained Jekyll for D2 in chat; D2 still open.
- Building photos agreed → backlog with timing guidance. James verse
  shown as reference only. Quoting it needs the church's translation.

## 2026-10-19 — Jekyll conversion
- D2 decided: Jekyll (Kevin). Converted docs/: `_layouts/default.html`
  (header/nav/footer/banner), `_includes/` (service times, address,
  hills), `_data/` (church, services, nav, events, ministries).
  `_config.yml` `preview: true` drives banner + noindex; excludes
  README.md and CLAUDE.md from the published site.
- Built locally with Jekyll 3.10.0 (GitHub Pages' version). Verified 7
  pages at 390/1280px, links, launch mode (preview false → no
  banner/noindex), and a sample event rendering.
- Facts: nursery + children's class; directions by the bend (no
  landmark) → facts.md, visit.html.
- docs/CLAUDE.md "stack pending" wording update held on its own branch
  for review (root exception 2).
- Suggestion: Events first page on a data file. Done as part of the
  conversion, since Kevin had agreed to Jekyll.

## 2026-10-19 — Going public (draft preview)
- Merged docs/CLAUDE.md Jekyll wording (Kevin approved).
- D1 decided: public (Kevin). Scanned full history first: clean apart
  from Kevin's personal email as the initial commit's author.
- Can't change repo visibility or enable Pages from the session (no
  tool for repo settings) → Kevin does both; steps in chat + backlog.
- Found: root publish gate triggers on "GitHub Pages is live", which
  would put every draft edit behind leadership approval. Proposed
  re-keying it to launch (`preview: false`); held on
  `claude/publish-gate-preview` for review.
- Backlog *Proposed* unchanged at Kevin's request (schema.org data,
  Google Business Profile stay proposed).
