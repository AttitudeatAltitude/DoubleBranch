# Media & Streaming

STATE — budget 600 words.

## Current setup (Kevin, 2026-10-19)
- Sermons broadcast live to the church Facebook group, which is
  private (Kevin, 2026-10-20) — visitors can't see it.
- Captured on a member's personal phone. Audio source (phone mic vs.
  soundboard feed), mounting, and who runs it: unknown.
- Archive: whatever Facebook retains; no separate archive.

## Direction
- YouTube channel @DoubleBranchBaptist created, no videos yet (Kevin,
  2026-11-08).
- **Audio-only first** — agreed (Kevin, 2026-10-19) and done: sermon
  audio on a still image uploaded to YouTube two weeks in a row as of
  2026-11-15 (Kevin). Live video is the next step.
- Budget: Kevin expects leadership to approve up to $1,000 for all
  live-stream equipment, hoping ≤$500 for the camera — unconfirmed
  (Kevin, 2026-11-15; was "none", 2026-10-19). Still lead with a $0
  option.
- Soundboard: **Zoom LiveTrak L-20** (Kevin, 2026-10-19). Records to SD card
  (20 channels + stereo mix, WAV 44.1/48/96 kHz, 16/24-bit) and works as
  a USB audio interface (retailer spec listings, 2026-10-19). SD-card
  recording means no computer needed — $0 path, plus ~$10 SD card if
  none. Steps in audio-guide.md.
- Computer at the board: Windows 11 PC by the soundboard (Kevin,
  2026-11-15; replaces "no computer", 2026-10-19).
- Internet at the church: ~99 Mbps upload, 3 runs, board PC on cable
  (Kevin via app, Sun 2026-11-15 ~5:27 PM, before the 6 PM service —
  not under service load; margin makes 1080p safe).
- Board PC: Intel i5-8265U (2018 laptop CPU), 8 GB RAM, UHD 620 (has
  QuickSync); wired port, free USB (Kevin via app, 2026-11-15).
- Publish to YouTube: live services and past sermons; the Sermons page
  embeds the latest/live one (Kevin chose D7 A, 2026-10-21; leadership
  to confirm).
- Board and live stream run weekly by the sound booth operator
  (Kevin, 2026-11-15).
- Still needed later for video: room size, lighting, upload speed.

## Live-stream plan (Kevin, 2026-11-15)
- Goal: stream services live to YouTube instead of uploading
  afterward; follows the audio-only stage (now running).
- Recommended free setup: OBS Studio on the board PC, L-20 over USB
  for sound (stereo mix into OBS).
- Camera bought: iuZee 4K AI NDI PTZ Camera, model IUZ-UHD20U-4KN
  (Kevin, box-label photo, 2026-11-25). Price, seller, return date:
  unknown. Per retailer listings (unverified for this exact model): 20x
  optical, 4K30, USB 3.0/HDMI/LAN, presenter tracking + auto-framing,
  255 presets (10 on remote), box has 12V adapter, USB 3.0 cable, wall
  mount, remote. PoE and NDI HX version unconfirmed — app Task 6 Part 0
  bench test checks both before mounting. NDI into OBS via NDI runtime
  + DistroAV (installed, Task 2).
- Equipment list (Claude Doc "Live Stream Equipment List", Kevin's,
  private; https://claude.ai/artifact/Pwp2D6oNEGmeiUh8icfRke; 2026-11-15): must-haves about $500–$725
  — camera $360–$450, PoE+ switch, Cat6, mount, headphones. Prices
  from search listings, unverified. L-20: install Zoom driver, route
  master to USB 1–2 (OBS reads ch 1–2). Music: CCLI Streaming ~$65–$75/yr
  if copyrighted songs (unverified).
- Setup procedure: same doc, "Setup Procedure" tab (2026-11-15) — 9
  task cards in maintenance-manual style (pre-purchase checks →
  install → tests → Sunday checklist) + troubleshooting. Operator-
  facing; menu paths from general knowledge, unverified on this PC.
- Checklist app (artifact "Live Stream Setup", Kevin's, private;
  https://claude.ai/artifact/2LrLKkw1ehJ694hSdhWr7m; 2026-11-15): same
  task cards as tickable tabs; db: `progress/<t1..t8>`,
  `sundays/<YYYY-MM-DD>`, `shopping/list`. Claude reads it with
  ArtifactData. The doc tab and the app must be kept in step.
- App progress (2026-11-25): Task 1 Pass; Task 2 done except L-20
  connection checks (B2; L-20 port is USB-B); Task 3 live streaming
  enabled 2026-11-25, Part B after 24 h.
- Open: D8 status (camera already bought — approval not recorded);
  PoE yes/no; who runs it besides the operator.
