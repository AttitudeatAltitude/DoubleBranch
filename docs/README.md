# Website (docs/)

This folder is the church website. GitHub Pages publishes it (once
turned on, Phase 3). It's called `docs/` only because that's the folder
name GitHub Pages expects.

**Status:** draft skeleton. Every page shows a yellow "Draft preview"
banner and has a "noindex" line so search engines skip it. Both get
removed at launch. Anything in a yellow dashed box marked `[TBD]` is a
fact we're still gathering.

## Pages

| File | Page | What it's for |
|---|---|---|
| `index.html` | Home | Service times and address first, then links to the main pages |
| `visit.html` | Plan a Visit | First-time visitors: when, where, common questions |
| `about.html` | About | Who we are, statement of faith, and short blurbs on the pastor, deacons, and ministry leaders |
| `sermons.html` | Sermons | Link to the Facebook livestream and past sermons |
| `events.html` | Events & Ministries | Weekly schedule, upcoming events, ministries |
| `give.html` | Give | Ways to give |
| `contact.html` | Contact | Address, email, Facebook |
| `assets/css/style.css` | (all pages) | Colors, fonts, and layout for the whole site |

## How to edit

- Each page is a plain text file. Open it in any text editor (or edit
  it right on GitHub with the pencil icon) and change the words between
  the tags. For example, in `<p>Sundays, 10:00 AM.</p>` you change only
  `Sundays, 10:00 AM.`.
- **The header, footer, and service times are copied on every page.**
  If a service time changes, search all the `.html` files for the old
  time and update each one.
- To fill in a `[TBD]`, replace the whole `<span class="tbd">[TBD: …]</span>`
  (or `<p class="tbd">…</p>`) with the real text. Don't leave the
  `class="tbd"` behind, or it will still show the yellow box.
- Colors are set at the top of `assets/css/style.css` (the `:root`
  section). Changing one line there changes that color everywhere.
- Facts must match `../church/facts.md`. Change them there first.
