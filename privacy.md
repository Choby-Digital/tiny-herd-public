# Tiny Herd — Privacy Policy

_Last updated: 6 August 2026_

Tiny Herd is a virtual pet that lives at the bottom of your web pages.
It is designed to work **entirely on your device**. No data is transmitted,
collected, or sold — there are no servers, no analytics, and no tracking of
any kind.

## What the extension stores (on your device only)

- **Settings** — your pet's species, colour, name, size, speed, per-site
  hide list, and on/off toggles. Stored in Chrome's extension storage
  (`chrome.storage.sync`), which Chrome may sync between your own signed-in
  browsers. We never see it.
- **Progress** — your pet's XP/level, the date of its last greeting, and a
  one-time update notice. Stored locally (`chrome.storage.local`).
- **Pet position** — where the pet was standing, remembered for your current
  browser session only (`chrome.storage.session`).

## What the extension observes (and never records or transmits)

- **Mouse movement and scrolling** on pages you visit — used only so the pet
  can react in the moment (chase your cursor, get startled by fast
  scrolling). These events are processed in memory and immediately
  discarded. They are never stored or sent anywhere.
- **Tab titles** — the extension watches for unread-count patterns like
  "(3) Inbox" in tab titles so your pet can announce new notifications. The
  hostname of the site (e.g. `mail.google.com`) may appear in that speech
  bubble. Titles are compared in memory and never stored or transmitted.
- **Completed downloads** — the filename of a finished download is shown in
  the pet's speech bubble. Filenames are never stored or transmitted.
- **The current site's hostname** — used for the "hide pet on this site"
  option and stored in your settings only if you use it.

## Photo cards

The "photo card" feature draws an image of your pet on your device and saves
it straight to your downloads. It is generated locally and never uploaded.

## What we never do

- No data leaves your device. The extension makes **zero network requests**.
- No analytics, no fingerprinting, no ads, no selling of anything.
- No reading of page content — the pet draws itself *over* pages; it does
  not read what's on them.

## Permissions, in plain words

| Permission | Why |
|---|---|
| `storage` | Save your settings and your pet's XP on your device |
| `alarms` | A once-a-minute timer that awards browsing XP |
| `downloads` | Notice when a download finishes so the pet can announce it |
| `tabs` | Read tab titles for unread-count announcements and the current site's hostname for per-site hide |

## Contact

Questions or concerns: open an issue at
[github.com/gtrtuugii/tiny-herd-public](https://github.com/gtrtuugii/tiny-herd-public/issues)
or email **chobydev@gmail.com**.

Changes to this policy will be posted on this page with an updated date.
