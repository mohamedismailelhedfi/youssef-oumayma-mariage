# Youssef & Oumayma — Wedding Invitation

A single-page, luxury wedding invitation site with a live countdown, event
details, an embedded map, and an RSVP link. Built as plain HTML/CSS/JS —
no build step, no dependencies — so it deploys straight to GitHub Pages.

## 1. What to edit before publishing

Open `index.html` and search for the comment `EDIT ME` — every one marks a
value you need to fill in:

| What | Where |
|---|---|
| Wedding date shown in the hero | `<p class="hero-date">` |
| Ceremony date/time/venue text | first `.card` in the Details section |
| Reception date/time/venue text | second `.card` in the Details section |
| Countdown target date/time | `const WEDDING_DATE = new Date("2026-12-12T15:00:00")` near the bottom |
| Google Maps embed | `<iframe class="map-frame" src="...">` |
| "Get Directions" link | `<a class="directions-btn" href="...">` |
| RSVP contact | `<a class="rsvp-btn" href="mailto:...">` — swap for a WhatsApp link or Google Form URL if you prefer |
| RSVP deadline text | `<p class="rsvp-deadline">` |

### Getting your Google Maps embed link
1. Go to [Google Maps](https://maps.google.com) and search for your venue.
2. Click **Share** → **Embed a map** → copy the `src="..."` URL from the code shown.
3. Paste it into the `iframe`'s `src` attribute in `index.html`.
4. For the "Get Directions" button, just copy the venue's normal shareable Google Maps link instead.

### Optional: remove the Arabic line
There's a line near the top of the hero (`بِسْمِ اللَّهِ...`) — delete that
`<p class="arabic-line">` tag entirely if you'd rather not include it.

### Changing colors
All colors are defined once, at the top of the `<style>` block, as CSS
variables (`--ink`, `--emerald`, `--gold`, `--cream`, etc). Change the hex
values there and the whole site updates.

## 2. Host it on GitHub Pages (free)

1. **Create a GitHub account** if you don't have one: https://github.com/join
2. **Create a new repository**
   - Go to https://github.com/new
   - Name it e.g. `youssef-oumayma-mariage`
   - Set it to **Public** (required for free GitHub Pages)
   - Click **Create repository**
3. **Upload the file**
   - On the new repo page, click **"uploading an existing file"**
   - Drag in `index.html` (and `README.md` if you want it visible)
   - Click **Commit changes**
4. **Turn on GitHub Pages**
   - Go to the repo's **Settings** tab → **Pages** (left sidebar)
   - Under **Build and deployment → Source**, choose **Deploy from a branch**
   - Branch: `main`, folder: `/ (root)` → **Save**
5. **Wait ~1 minute**, then refresh that Pages settings page. GitHub will
   show your live URL, in the form:
   ```
   https://<your-username>.github.io/youssef-oumayma-mariage/
   ```
6. Share that link with your guests — done.

### Optional: a custom domain
If you own a domain (e.g. `youssefetoumayma.com`), you can point it at
GitHub Pages: in the same **Settings → Pages** screen, enter it under
**Custom domain**, then add a `CNAME` DNS record at your domain registrar
pointing to `<your-username>.github.io`. GitHub will show exact instructions
once you type in the domain.

### Making future edits
Any time you want to change something, edit `index.html` directly on
GitHub (click the pencil icon on the file) or re-upload it — the site
rebuilds automatically within a minute of every commit.

## 3. Suggestions to consider

- **Photo**: the design currently uses an ornamental gold monogram instead
  of a photo, to keep load times fast and the aesthetic consistent. If
  you'd like an engagement photo in the hero, it's a straightforward
  addition — just ask.
- **RSVP tracking**: a `mailto:` link is the simplest option, but a free
  [Google Form](https://forms.google.com) will let you actually collect
  and count responses — swap the RSVP button's `href` for the form URL.
- **Language**: the copy is in French. If you'd like an Arabic and/or
  English version (or a language switcher), that's easy to add.
- **Multiple events**: if there's a henna night / engagement party in
  addition to the ceremony and reception, the Details section can take a
  third card without changing the layout.
- **Password-lite privacy**: GitHub Pages sites are public by default —
  anyone with the link can view it, but it won't appear in search results
  unless linked elsewhere, which is usually enough privacy for an invite.
# youssef-oumayma-mariage
