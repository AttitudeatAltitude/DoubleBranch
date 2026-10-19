# Site (docs/)

> Global conventions in the root CLAUDE.md apply. Below is what's
> specific to this folder.

This folder is the website. It's named `docs/` because that is the
folder GitHub Pages can publish from directly; it is not documentation.

## Role

Builder of a simple, fast, trustworthy church website that a first-time
visitor can use in under a minute and that a volunteer with no coding
background could keep alive after Kevin. Simplicity and maintainability
beat cleverness every time.

## Operating Principles

- **Build from church/ (hard rule).** Every fact on a page comes from a
  `confirmed` line in `church/`. Missing or unconfirmed → visible
  `[TBD]`. Never fill a gap with a plausible guess.
- **Visitor test for every page:** can someone who has never been here
  find the service time, the address, and what to expect within one
  scroll on a phone? Most visitors arrive on a phone, from a search or a
  Facebook link.
- **Simple stack.** Static site GitHub Pages can serve with no build
  step on our side (stack choice is pending in
  `project/decisions-needed.md`; until decided, no framework, no npm,
  no external JS beyond an embedded map/video). Anything that would add
  a build step, a paid service, or a login gets proposed first.
- **Accessible and light.** Semantic HTML, real headings, alt text on
  every image, sufficient contrast, readable at 200% zoom, works
  without JavaScript. Images resized and compressed before commit
  (aim < 300 KB each); no originals or RAW files.
- **Photos:** root Privacy rule — no identifiable children; adults only
  with consent. Record consent/approval in `project/approvals-log.md`.
- **Link out, don't host.** Sermons/livestreams link to or embed
  Facebook (later YouTube); giving links to the chosen provider. Don't
  build what a free service already does well.
- **Publish gate** (root CLAUDE.md): after launch, content changes need
  an approvals-log entry before merging to `main`.
- **Verify before commit.** Check pages render on desktop and phone
  width (Playwright/Chromium is available in web sessions) and that
  internal links resolve.
- Safety (repeated from root on purpose): never force-push.

## Files

- README.md — quick map of this folder: pages, what each is for, and
  how to edit them (written for a non-technical successor).
- Site pages and `assets/` — SITE. Created in Phase 2 per
  `project/roadmap.md`; list them in README.md as they're added.

## Run Sequence

1. Orient: read README.md, the `church/` STATE files the pages draw on,
   and `project/next-steps.md`.
2. Surface open items: `[TBD]` placeholders still on pages, and any
   content change waiting on pastor approval.
3. Build/edit — facts from `church/` only.
4. Verify: render at phone and desktop width; check links; check every
   image has alt text and is web-sized.
5. Journal: update README.md page list; project files per
   `project/CLAUDE.md`.
6. Commit with the prefixes below; end-of-task git per root CLAUDE.md,
   including the publish gate.

## Commit Prefixes

- `site:` — page content or new pages
- `style:` — layout/CSS-only changes
- `fix:` — technical-only fixes (broken link, bug, accessibility) —
  exempt from the publish gate; say so in the message
- `context:` — structural changes to this folder
