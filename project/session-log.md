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
