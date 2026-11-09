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

## 2026-10-19 — Pages verified
- Kevin made the repo public and enabled Pages. Verified: API shows
  `visibility: public`, `has_pages: true`; first "pages build and
  deployment" run (commit 8213b80) succeeded in build, report and
  deploy, with no Jekyll warnings.
- Session network can't reach github.io or the artifact store, so the
  live pages weren't fetched directly. Published bundle 7,335 B vs.
  local `/docs` build 7,171 B gzipped (zip wrapper accounts for the
  difference) → Pages built from `/docs`; notes and CLAUDE files not
  published.

## 2026-10-19 — Address correction
- Kevin: address didn't populate properly on the preview → street
  address now 18670 Old Highway 112 (city/ZIP unchanged). Updated
  facts.md first, then `_data/church.yml` (address + Maps link) and
  contact.html's description. Built and checked: new address on all 7
  pages, old one gone.
- Follow-up: the site was fine; Google drops the pin too far down the
  road. Added optional `map_pin` (lat,long) to `_data/church.yml`;
  `_includes/maps-url.html` uses it for every Directions link (Google
  directions to the exact point), else falls back to address search.
  Both modes tested. Waiting on Kevin's coordinates. Map-pin *Proposed*
  item replaced by a backlog task.
- Kevin may have given the wrong number: switched to 18650 Old Highway
  112 to test the pin; facts.md marks it unconfirmed until he checks.
- 18650 pinned the house next door. Kevin sent coordinates → `map_pin`
  set; Directions links now route to the exact point. Street number
  still unconfirmed (backlog).
- Closeout: all branches merged to main; backlog tidied (visitor copy
  done, editing guide done, missing facts listed). Street number left
  open at Kevin's request.

## 2026-10-19 — Tracker board
- Kevin asked for a dashboard to track status and give input outside
  Claude Code. Asked first: two-way, 50s atomic-age theme, Kevin only,
  all sections.
- Built https://claude.ai/artifact/Lp771qVc4DGzWEckWZH3gB: phase dial,
  next moves, quick links, key facts, then answer boxes (9 questions),
  to-dos (8), leadership decisions (6, with recommendations), notes to
  Claude, ideas (3, approve/not now), completed (9). Data in the
  artifact's db: `board/status`, `items/*`, `notes/*`; rules: owner-only
  read and write (checked: editor-level read sees nothing).
- Kevin's saves set `savedAt` + `synced:false`; Claude records them in
  the repo and sets `synced:true`. Repo stays the source of truth.
- Sync steps for project/CLAUDE.md held on `claude/tracker-sync` for
  review (root exception 2).

## 2026-10-21 — Tracker sync, deacon buy-in
- Kevin: talked to a deacon on 2026-10-20 — on board and gathering
  content. Informal; not a leadership approval (none recorded).
- Synced tracker saves: church email, D7 = YouTube, Facebook group is
  private, no translation needed, note: Nov 8 leadership meeting and
  New Year 2027 launch target. Recorded in church/ and project/.
- Site: Contact shows the church email (from `_data/church.yml`) and
  drops Facebook; Sermons and Home say services will stream on YouTube,
  with a [TBD] for the channel link/embed. Built with Jekyll 3.10.0:
  mailto renders; no "Facebook" left on any page.
- Suggestion: one-page handout for the Nov 8 meeting (backlog
  *Proposed*).

## 2026-10-22 — Nov 8 handout
- Kevin: church leaders hold the email login (Kevin doesn't yet); a
  deacon is gathering the bylaws, the mission statement and the street
  number; YouTube channel targeted before Nov 8. Recorded in facts.md,
  backlog.md, tracker.
- Built the handout draft: HTML → Chromium PDF, one letter page, QR
  (python `qrcode`, SVG) to the preview URL. Seven tick-box questions =
  the leadership list. No names besides "Questions: Kevin". Sent to
  Kevin; rebuild ~Nov 5.
- Suggestion: add the church email as a Google account's recovery
  contact for the YouTube channel, so the channel is owned by the
  church, not Kevin's personal account (see next-steps).

## 2026-11-06 — Status check, Kevin's facts
- Status for Kevin: no input since Oct 22; handout rebuild (due ~Nov 5)
  not done; site ~50% by TBD count (33). Tracker: no unsynced saves.
- Kevin, in chat: LeFlore Baptist Association; nursery rooms; Sunday
  school classes; bylaws still pending; names of pastor, deacons,
  youth leader, adult-class teachers. Recorded in church/ and on About,
  Visit, Events. Names withheld from repo and site — root Privacy rule
  needs public approval; asked Kevin. About now has 2 deacon cards and
  per-class teacher cards. Built with Jekyll 3.10.0.
- Suggestion: name-consent line on the Nov 8 handout (backlog).
- Later: Kevin answered nursery hours, Monday Bible studies, youth
  meetings; unsure about the children's class, so the site no longer
  claims one. Rebuilt the Nov 8 handout (one letter page, QR, done
  list, still-needed list, 7 decisions, name-consent table with blank
  names, no names printed). Kevin agreed to the consent table. PDF sent,
  not committed.

## 2026-11-08 — YouTube linked
- Kevin: channel live at @DoubleBranchBaptist, no videos. Sermons page
  links it (URL in _data/church.yml); embed waits for a video and the
  channel ID. Couldn't open youtube.com from the session (proxy).
- Suggestion: post a short welcome or test-recording video first so the
  channel isn't empty when leadership or visitors follow the link.
- Kevin: channel is under the church's Google account; uploading the
  Nov 8 sermon today. Embed waits on the channel ID.
- Kevin uploaded the Nov 8 sermon and sent the channel ID. Sermons now
  embeds the uploads playlist (UU + ID, youtube-nocookie) so new
  uploads show without edits; "Watch live" links to @…/live rather
  than a live embed, which shows an error when not streaming. Couldn't
  play it from the session (YouTube blocked) — Kevin to check.
- Kevin: sermon embed plays. Leaders' names allowed to be published;
  list given (no deacons). Names on About; children's church added to
  Visit and Events. Logged in approvals-log; asked about deacons and
  the rest of the meeting's answers.
- Deacons added to About; approval confirmed as from the Nov 8
  meeting (dated clarification in approvals-log); children's church
  "school age", during 11:00. Asking the handout decisions one by one.
- Recorded the Nov 8 meeting (asked Kevin one by one): go-ahead, D4,
  D6 = Kevin approves, D7, New Year 2027, blurbs all approved; D3 open
  (comparing, incl. Venmo). Phase 0 exit met except D3 — proposed
  closing it and carrying D3 to Phase 2. Root CLAUDE.md still calls D6
  open — needs an edit, held for review (standing-instruction file).
- Giving comparison: one-page PDF (Venmo charity, Tithe.ly, Givelify,
  Zeffy) from web search of vendor pages and 2026 reviews; not
  committed. Summary in decisions-needed D3.

## 2026-11-08 — Phase 0 retro (closed with Kevin's OK)
- Took 20 days (Oct 19 → Nov 8). Leadership said yes to everything
  asked except D3 giving, carried to Phase 2.
- What slowed us: a 15-day gap (Oct 22 → Nov 6) with no new facts and
  no session; the handout rebuild due ~Nov 5 slipped because work only
  happens when Kevin opens a session. The batched one-page handout
  worked: seven decisions answered in one meeting.
- Change proposed: a weekly scheduled check-in (backlog *Proposed*).
- Kevin approved the CLAUDE.md D6 wording; merged. Fixed docs/README
  (YouTube, no Facebook). Scheduled "Weekly website check-in" (Sun
  2:39 PM CT, fresh session; stores no repo/connectors — first run
  Nov 15 to confirm). Wrote the editing guide as a Claude Doc for a
  non-Claude editor.
- Tracker brought current (was Oct 22): phase 1, next moves, facts,
  links (Sermons, YouTube, editing guide); answered questions and
  decided items moved to Completed; new questions (Monday/youth times,
  children's ages) and to-dos (giving, check-in); D3 options updated.
  Kevin named as contact in the editing guide.

## 2026-11-08 (evening) — Google Calendar on Events
- Kevin asked how to show Google Calendar events; sent the church
  account's calendar. Events page embeds it (agenda, Central time)
  with subscribe buttons; events.yml removed; README, church/events.md,
  editing guide and tracker links updated. Couldn't verify it's public
  (Google blocked). Built with Jekyll 3.10.0; phone width checked.
- Suggestion: keep a separate "Double Branch Events" public calendar so
  personal or private items on the church account's main calendar never
  show on the site.
