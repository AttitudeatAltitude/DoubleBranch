# Website (docs/)

This folder is the church website. GitHub Pages publishes it (once
turned on, Phase 3). It's called `docs/` only because that's the folder
name GitHub Pages expects.

**Status:** draft. While `preview: true` is set in `_config.yml`, every
page shows a yellow "Draft preview" banner and asks search engines not
to list it. Change it to `preview: false` at launch. Anything in a
yellow dashed box marked `[TBD]` is a fact we're still gathering.

## How it works

The site uses **Jekyll**, which is built into GitHub Pages. There's
nothing to install. When a change is saved to GitHub, Pages assembles
the pages and publishes them within a minute or two. Shared pieces live
in one place, so you change them once:

| To change… | Edit this file |
|---|---|
| Service times (every page) | `_data/services.yml` |
| Church name, address, map link, exact map pin, email, YouTube | `_data/church.yml` |
| Upcoming events | The church Google Calendar (doublebranchbaptist@gmail.com), not a file here |
| Ministries list | `_data/ministries.yml` |
| Menu at the top | `_data/nav.yml` |
| Header, footer, preview banner | `_layouts/default.html` |
| Colors, fonts, layout | `assets/css/style.css` (colors are at the top) |
| Preview mode on/off | `_config.yml` |

## Pages

| File | Page | What it's for |
|---|---|---|
| `index.html` | Home | Service times and address first, then links to the main pages |
| `visit.html` | Plan a Visit | First-time visitors: when, where, directions, common questions |
| `about.html` | About | Who we are, statement of faith, and short blurbs on the pastor, deacons, and ministry leaders |
| `sermons.html` | Sermons | Newest sermon from the church YouTube channel (automatic), plus live and channel links |
| `events.html` | Events & Ministries | Weekly schedule, upcoming events (Google Calendar), ministries |
| `give.html` | Give | Ways to give |
| `contact.html` | Contact | Address, email |

## How to edit

- Edit any file right on GitHub: open it and click the pencil icon,
  make the change, then click "Commit changes".
- **The `_data` files are lists.** Each item starts with `- ` and each
  line is `label: value`. Keep the spacing exactly as in the lines
  around it: two spaces before each label under the `- `. Lines starting
  with `#` are notes and don't show on the site.
- **Adding an event:** add it to the church Google Calendar
  (doublebranchbaptist@gmail.com). The Events page shows it within
  minutes. Everything on that calendar is public; put "contact the
  church" instead of a home address.
- **On a page file**, the block between the two `---` lines at the top
  holds the page title, its search description, and the big heading.
  Below it is the page's own content. Change the words between the
  tags, e.g. in `<p>About an hour.</p>` change only `About an hour.`.
- To fill in a `[TBD]`, replace the whole `<span class="tbd">[TBD: …]</span>`
  with the real text. In a `_data` file, fill in the blank line.
- **If something goes wrong:** a typo in a `_data` file (usually
  spacing) stops the update. The last working site stays up and GitHub
  emails the repository owner. Undo the last change, or fix the
  spacing, and save again.
- Facts must match `../church/facts.md`. Change them there first.
