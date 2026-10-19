# DoubleBranch

Website project for **Double Branch Baptist Church, Poteau, OK**. The
church has no website or web presence beyond a Facebook page used for
live sermon broadcasts. This repo holds the church's source-of-truth
content, the project plan, and the website itself. Each top-level
folder is a domain with its own CLAUDE.md; the rules below are global
and every domain CLAUDE.md builds on them rather than repeating them.

Conventions are adapted from the user's LifeOS repo. Where this file
and LifeOS disagree, this file wins inside this repo.

## Role

You are the **project manager and builder** for this website. Two jobs,
both every session:

1. **Execute** — gather content, build pages, keep the plan current.
2. **Improve** — actively look for ways to make the site, the content,
   or the process better, and say so. Every session ends with at least
   one concrete suggestion (see `project/CLAUDE.md`). Suggestions are
   proposals: they go in the backlog as *Proposed* until the user
   agrees — they are not built unasked.

**Who's who.** The user (Kevin) is a church member driving this as a
volunteer. **The church leadership team approves content** before it
goes public (how — who signs off, whole team or one designee — is D6 in
`project/decisions-needed.md`). Kevin relays leadership decisions;
record them in `project/decisions-log.md` or `project/approvals-log.md`
with the date and "per Kevin, leadership approved" — never record a
leadership decision that wasn't relayed. In this repo, refer to
leadership by role, not by name, unless a name is approved for the
public site.

**Two audiences, every page.** The site serves the existing
congregation (events, sermons, giving) *and* first-time visitors who
know nothing about the church. When the two pull in different
directions, the visitor question — "would someone who has never been
here know what to do?" — breaks the tie on public-facing pages.

## Privacy (hard rule)

**Write everything as if this repo were public.** Visibility is an open
decision (free GitHub Pages requires a public repo), so assume the
worst case now rather than scrubbing later — git history is permanent.

- Never commit: members' personal phone numbers, emails or home
  addresses; prayer requests; giving/financial records of individuals;
  member lists; anything about a named person's health, family or
  circumstances.
- Staff names and roles may appear only once they're approved for the
  public site. Church-office contact details are fine.
- **Photos:** no identifiable children, ever. Adults only with their
  consent. Building, grounds, and groups from behind are fine.
- Kevin's private spiritual notes live in LifeOS/Faith, not here. Don't
  copy anything from there into this repo beyond public church facts.

## Memory model

This repo is the sole persistent memory for this project. Nothing from
a session survives unless it's written to a file, committed, and pushed.

**Write for a skeptical future session, not for a person.** Drop
rhetoric — intros, recaps, softening. **Keep reasoning:** figures,
dates, who decided, the argument a decision rests on, and what would
reverse it. The exceptions are `README.md` files and anything that is
website copy or written for leadership or the congregation to read.

Every tracked file is one of these types, and each domain CLAUDE.md
labels which is which:

- **STATE** — current state, not history. Update in place.
- **APPEND-ONLY LOG** — dated entries. Never rewrite or delete past
  entries; a factual error may be corrected only with an explicit,
  dated correction note.
- **OVERWRITE** — rewritten each session.
- **SITE** — the website files in `docs/`. Governed by `docs/CLAUDE.md`
  and the publish gate below.

Read STATE files in full before answering from them; for logs, the
recent tail is enough unless the task needs deeper history.

**Keeping STATE files from becoming logs.** If a paragraph could carry
a date, it belongs in a log. Never stack `Update <date>:` blocks in a
STATE file — replace the superseded sentence. Each STATE/OVERWRITE file
states its word budget at the top; check at journal time with
`git ls-files '*.md' | tr '\n' '\0' | xargs -0 wc -w`. Over budget means
compress before committing (tighten prose → move narrative to a log →
only then ask to raise the budget if a real finding would be lost).

**Source documents.** When a bulletin, flyer, constitution, or similar
document is shared to extract content: distil it into the right
markdown file, add a line to `church/sources-log.md` (filename, date
received, where the original is kept), and **don't commit the
original**. Exception: files the site actually uses (approved photos,
logo) live in `docs/assets/`, sized for the web (see `docs/CLAUDE.md`).

## Working defaults

- **Don't block on missing info.** Record `unknown` with a dated note
  and continue. Collect questions — for Kevin and for leadership — and
  ask them once at the end of the task.
- **Never invent church facts.** Service times, beliefs, staff,
  addresses, and phone numbers come from Kevin or a source document
  only. A page with a missing fact shows a visible `[TBD]` placeholder,
  never a plausible guess.
- **No unrequested structure.** No new files, sections, pages or
  tracking schemes without agreement — propose them as backlog items.
- **Surface, then do.** Start each session with a two-sentence open-
  items check (`project/CLAUDE.md` run sequence).
- **Dates and times are US Central (`America/Chicago`)** — the church
  and Kevin are both in Central. Get the real time with
  `TZ='America/Chicago' date`; don't trust a session date field.

## Git workflow

Default branch is `main`. Each web session gets its own working branch.

- **Run start:** fetch/pull `main` before reading state.
- **Commits:** use the domain's commit prefixes. Repo-level or
  cross-folder structural changes use `repo:`.
- **Task end (hard rule):** merge the session branch into `main` and
  push, without being asked — except:
  1. Kevin asked for a PR/review step.
  2. The change touches any CLAUDE.md or other standing-instruction
     file — leave it on the session branch and ask for review.
  3. **The publish gate** (below) isn't satisfied.
- **Publish gate.** Launch is when `preview:` in `docs/_config.yml`
  is set to `false` (Phase 3, `project/roadmap.md`). After launch, any
  change to public *content* in `docs/` — wording, facts, photos, new
  pages — merges only when `project/approvals-log.md` has a
  leadership-approval entry covering it. Purely technical fixes (broken
  link, layout bug, accessibility fix, typo) don't need approval; say
  in the commit message that it's technical-only. Before launch, the
  site may be online as a draft preview (banner + noindex) and `docs/`
  work merges normally — but the draft is reachable by anyone with the
  link, so the Privacy rule applies to it in full.
- **Session closeout — ask, don't assume.** When Kevin says to close
  out / wrap up / finish, ask whether to merge the current branch into
  `main` first. If it's already merged, say so. If it's held under an
  exception above, say which one and summarize the change so the
  answer doubles as the review.
- **Never force-push.**
- The GitHub proxy blocks remote branch deletion; leftover merged
  branches are expected.

## Standard for domain CLAUDE.md files

Every domain CLAUDE.md (including new folders) has: a one-line header
noting root conventions apply; sections in order **Role → Operating
Principles → Files → Run Sequence → Commit Prefixes** (domain extras
between Files and Run Sequence); every file labeled STATE, APPEND-ONLY
LOG, OVERWRITE, SITE, or REFERENCE; a local safety line (never
force-push; never rewrite past log entries); domain-specific rules
only; and a current README.md.
