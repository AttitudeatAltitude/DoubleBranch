# Decisions Log

APPEND-ONLY LOG. Never rewrite past entries; corrections get an
explicit dated note.

## 2026-10-19
- **Project shape** — Kevin. Kevin (member, volunteer) drives; pastor
  approves content before it's public. Why: Kevin's role in the church.
  Reopen if: a staff member or team takes ownership.
- **Hosting: GitHub Pages, no custom domain for now** — Kevin. Why:
  free, served from this repo. Reopen: custom domain in Phase 4.
- **V1 scope: visitor essentials, sermons, events & calendar, online
  giving** — Kevin.
- **PM style: phased roadmap + backlog** — Kevin.
- **Repo visibility: decide later** — Kevin. Consequence: root Privacy
  rule treats repo as public from day one. Open as D1.
- **Photos: no identifiable children** — Kevin; pending pastor (D4).
- **Git: LifeOS rules + publish gate** — Kevin. After launch, public
  content changes need logged pastor approval before merging to main.

- **CLAUDE.md files approved** — Kevin. Merged to main.
- **Approvals come from the leadership team, not the pastor alone** —
  Kevin. Mechanics open as D6. CLAUDE.md wording change held for review.
- **Sermons: audio-only first; no media budget** — Kevin. Why: no
  budget; audio is cheaper and an improvement over phone video. Reopen
  when a budget exists.
- **Bylaws exist; copy to be obtained** — Kevin.
- **Leadership approval wording in CLAUDE.md files approved** — Kevin.
  Leadership team = pastor and deacons.
- **D5 page list: Pastor & Staff merged into About** — Kevin. Why: the
  church has no staff in the usual sense; About carries blurbs for the
  pastor, deacons, and ministry leaders instead. V1 is now 7 pages:
  Home, Plan a Visit, About, Sermons, Events & Ministries, Give,
  Contact. Reopen if: the leaders section outgrows the About page.
- **D2 site stack: Jekyll (GitHub Pages' built-in)** — Kevin. Why:
  service times appeared in 10 places in plain HTML; Jekyll keeps
  shared pieces (header, footer, times) and changing lists (events,
  ministries) in one file each, with no tooling on our side. Cost: a
  data-file typo fails the Pages build (last good site stays up; GitHub
  emails the error). Reopen if: a successor finds it harder than plain
  HTML in practice.
- **D1 repo visibility: public** — Kevin. Why: free GitHub Pages, and
  a shareable draft preview now. History scanned first: no private
  content; the initial commit's author email is Kevin's personal Gmail
  and becomes public (Kevin told). Leadership hasn't been told yet;
  the preview carries a draft banner and noindex. Reopen if:
  leadership objects, or private content ever needs to live here.
- **docs/CLAUDE.md Jekyll stack wording approved** — Kevin. Merged.
- **Publish gate starts at launch (`preview: false`), not when Pages
  turns on** — Kevin approved; root CLAUDE.md merged. Why: lets the
  draft preview stay online while content is still changing. Reopen
  if: the draft is mistaken for the real site.
- **Tracker sync steps in project/CLAUDE.md** — Kevin approved; merged.
  Sessions read the tracker at start and refresh it at journal time;
  repo wins on conflict.

## 2026-10-21 — Tracker sync
- **Church email: doublebranchbaptist@gmail.com** — Kevin set it up
  (backlog *Proposed* item, chosen on the tracker). On the Contact
  page. Who holds the login is open; recommendation stays 2 leaders.
  Leadership not yet asked.
- **D7: YouTube** (option A) — Kevin's choice; leadership to confirm
  Nov 8. Why: the Facebook group is private, so it can't serve
  visitors; Kevin wants the Sermons page to embed the latest/live
  service. Reopen if: leadership prefers another home.
- **No Facebook link on the site** — Kevin: the group is private.
- **Targets: ~80% V1 at leadership's Nov 8 meeting; launch around New
  Year 2027** — Kevin. Leadership hasn't agreed the date.

## 2026-10-22
- **Nov 8 handout: build it** — Kevin approved the *Proposed* item.
  Format: one-page letter PDF in the site's colors, QR to the preview;
  not committed (printed material, not site content). Leadership
  questions on it match decisions-needed.md.
- **YouTube channel target: before Nov 8** — Kevin. Why: a working
  Sermons page makes the ~80% draft more convincing at the meeting.

## 2026-11-08 — Leadership meeting (handout answers, per Kevin)
- **OK to proceed with the website** — per Kevin, leadership approved.
- **D6 approvals: one designated approver — Kevin** — per Kevin,
  leadership approved. Kevin signs off on site content for the team
  after the team has had the preview link a week (the handout wording).
  Why: keeps approvals from waiting on a full meeting. Note: Kevin both
  builds and approves; approvals-log entries should still say what was
  shown to the team. Reopen if: leadership wants to see changes first.
- **D4 photo policy adopted as written** — per Kevin, leadership
  approved: no identifiable children, ever; adults only with their OK;
  building, grounds and groups from behind are fine. Who can say yes
  to a photo: the person in it.
- **D7 sermons on the church's YouTube channel** — per Kevin, leadership
  confirmed. Channel already live and embedded.
- **Launch target: New Year 2027** — per Kevin, leadership agreed.
- **OK to ask leaders for About-page blurbs** — per Kevin, leadership
  approved.
- **Leaders' names may be published** — per Kevin, leadership approved
  (approvals-log.md).
- **D3 online giving: still open** — leadership is comparing options,
  including Venmo.

## 2026-11-08 (evening)
- **Upcoming events come from the church Google Calendar** — Kevin
  (sent the calendar link, doublebranchbaptist@gmail.com, main
  calendar). Embedded on Events in agenda view, plus Google/iCal
  subscribe links; `_data/events.yml` removed. Why: one place to add
  events, no site edit, past events drop off automatically. Cost:
  Google's look, and everything on that calendar is public. Reopen if:
  the look matters more than simplicity (API-key version), or private
  events need to live on the same calendar (use a separate public one).
- **Correction/update (2026-11-08):** the Events page uses a separate
  public events calendar on the church account, not the main calendar
  — Kevin created it. Removes the "private items leak" risk above.
- **Color-coded ministry calendars** — Kevin. One public calendar per
  ministry (Church-wide, Men's, Women's, Youth, Golden Days), shown in
  one embed with Google palette colors (Men's = Basil green, Kevin's
  choice; others Claude's: Blueberry, Grape, Tangerine, Peacock), a
  text key, and per-calendar subscribe links. Why: Google doesn't show
  per-event colors publicly. Reopen if: colors should change (edit
  `calendars` in _data/church.yml).
- **Calendar colors changed (2026-11-08)** — Kevin: Church-wide deep
  red (Tomato #D50000), Men's strong blue (Blueberry #3F51B5), Women's
  strong pink (Cherry Blossom #D81B60, extended palette — check it
  renders in the embed), Youth orange (Tangerine #F4511E), Golden Days
  gold (Banana #F6BF26). Nearest Google colors to Kevin's words.
