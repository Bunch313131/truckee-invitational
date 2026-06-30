# Golf Tournament Manager

A single-file, installable web app (PWA) for running a Ryder Cup–style golf event:
team match play, draft, live scoring, leaderboards, horse races, brackets, and a TV/broadcast mode — with **per-tournament branding** so the same app can be reused for any event.

It started as the Smashters app and was generalized into a reusable template.

## Set up a tournament

1. Open the deployed site. Go to **Settings** (admin code defaults to `0000`).
2. **Event Info** — set Event Name, Club Name, date, etc.
3. **Branding & Theme** — pick theme colors and upload a logo (auto-resized; one Main Logo covers the header, splash, watermarks, and favicon).
4. **Courses** — build a course library (par / stroke index / yards). Assign a course to each session.
5. **Sessions / Formats** — define rounds (Four Ball, Foursomes, Singles) and which course each uses.
6. **Access Codes** — change the admin and scorer codes from `0000` if you like.
7. **Players → Draft → Matches** — add players, draft teams, create pairings, then score on the **Scoring** tab.

Tap **Save Settings** (the sticky button) to apply changes.

## Multi-device sync

Live scoring and leaderboards sync across phones/laptops via Firebase. Each **deployment URL** is its own isolated event namespace, so separate tournaments never collide.

## Reuse for another tournament

- **Settings → Data & Backup → Export Template** saves your setup (courses, colors, logo, teams, sessions — no players/scores) to a JSON file.
- Copy this repo to a new repo, deploy, then **Import Template** (or reconfigure from scratch). A fresh deployment starts blank.

## Deploy

Pushing to `main` publishes the site via the included GitHub Actions workflow (`.github/workflows/deploy.yml`) to GitHub Pages.
