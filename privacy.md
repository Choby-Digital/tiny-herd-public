# Tiny Herd — Privacy Policy

_Last updated: 8 August 2026_

Tiny Herd is a virtual pet that lives at the bottom of your web pages.
It is designed to work **entirely on your device**. No data is transmitted,
collected, or sold — there are no servers, no analytics, and no tracking of
any kind.

## What the extension stores (on your device only)

- **Settings** — your pet's species, colour, name, size, speed, per-site
  hide list, and on/off toggles (including break reminders and their
  interval, and fun announcements). Stored in Chrome's extension storage
  (`chrome.storage.sync`), which Chrome may sync between your own signed-in
  browsers. We never see it.
- **Progress** — your pet's XP/level, your daily visit streak, unlocked
  achievements, the date of its last greeting, and a one-time update notice.
  Stored locally (`chrome.storage.local`).
- **Play statistics** — simple counters used to award achievements: how many
  balls you've thrown, how many focus blocks you've completed, how many
  downloads have finished, and the highest number of tabs you've had open at
  once. These are plain numbers with no detail about *what* you downloaded or
  *which* tabs were open. Stored locally.
- **Focus session state** — whether a focus session is running, whether
  you're in the focus or break phase, and when the current phase ends.
  Stored locally so the session survives your browser restarting the
  extension in the background.
- **Break timer state** — the numeric ID Chrome assigns to your current tab,
  plus timestamps for when you arrived and when you were last reminded.
  **No URL, page title, or page content is stored** — only a temporary tab
  number and the clock times needed to measure a duration.
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
- **How long you stay on one tab** — to offer the optional break reminder,
  the extension measures how much uninterrupted time you spend on the
  currently active tab. It notices *when* you switch tabs or navigate, so it
  can restart the timer — it does not record where you went, and it keeps no
  history of visited sites.
- **Whether you're at your keyboard** — Chrome tells the extension only
  whether your computer is "active", "idle", or "locked", so the pet can nap
  while you're away and your break timer can pause. The extension cannot see
  what you are doing, in or out of the browser.
- **How many tabs are open** — a count only, used for the optional milestone
  announcement ("whoa, 20 tabs?") and one achievement. The extension does not
  read the list of tabs or their addresses for this.
- **Free system memory** — so the pet can warn you when your computer is
  running low on RAM, the extension reads how much memory is free versus
  total, once a minute. This is a single whole-machine ratio: it reveals
  nothing about individual programs, tabs, or what you have open. The reading
  itself is never stored — only the time of the last warning and whether it
  was the mild or the urgent one, so the pet doesn't repeat itself.
- **Completed downloads** — the filename of a finished download is shown in
  the pet's speech bubble, and a running total is counted for an achievement.
  Filenames are never stored or transmitted.
- **The current site's hostname** — used for the "hide pet on this site"
  option and stored in your settings only if you use it.

## Photo cards

The "photo card" feature draws an image of your pet on your device and saves
it straight to your downloads. It is generated locally and never uploaded.

## What we never do

- No data leaves your device. The extension makes **zero network requests**.
- No analytics, no fingerprinting, no ads, no selling of anything.
- No browsing history. The extension never builds a record of the sites you
  visit or how long you spent on each one — break timing is a single live
  countdown that resets when you move, and is never written down.
- No reading of page content — the pet draws itself *over* pages; it does
  not read what's on them.

## Permissions, in plain words

| Permission | Why |
|---|---|
| `storage` | Save your settings, XP, streak, and achievements on your device |
| `alarms` | A once-a-minute timer that awards browsing XP and checks whether a focus phase, break reminder, memory warning, or hourly check-in is due |
| `downloads` | Notice when a download finishes so the pet can announce it |
| `tabs` | Read tab titles for unread-count announcements, the current site's hostname for per-site hide, tab switches to time break reminders, and the number of open tabs for milestones |
| `idle` | Pause break and focus timers, and let the pet nap, while you're away from your computer |
| `system.memory` | Read how much system memory is free so the pet can warn you when it's running low |

## Clearing your data

Everything lives in your browser. Removing the extension from
`chrome://extensions` deletes all of it — settings, XP, streaks,
achievements, and timers. There is nothing stored anywhere else.

## Contact

Questions or concerns: open an issue at
[github.com/gtrtuugii/tiny-herd-public](https://github.com/gtrtuugii/tiny-herd-public/issues)
or email **chobydev@gmail.com**.

Changes to this policy will be posted on this page with an updated date.
