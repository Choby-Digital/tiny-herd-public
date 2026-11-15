# Tiny Herd — Privacy Policy

_Last updated: 15 November 2026_

Tiny Herd is a virtual pet that lives at the bottom of your web pages.
It is designed to work **on your device**. Your pet, your progress and your
to-dos never leave your browser — there are no analytics and no tracking of
any kind. The one exception is the optional premium pack: if you choose to buy
it, the extension checks with the payment provider, described under
**Payments** below. If you never open checkout, the extension never contacts
anyone.

## What the extension stores (on your device only)

- **Your to-dos.** The task text you type, its optional deadline, whether it
  repeats (daily, weekdays, weekly, or every few days), and whether it is done.
  Stored in Chrome's extension storage (`chrome.storage.sync`), which Chrome may
  sync between browsers you are signed into — the same as your bookmarks. We
  never see it, and it is never sent anywhere else. Deleting a task removes it.
  For 24 hours after you finish a task, a simplified copy of its title is also
  kept **on this device only** (never synced), so the same task cannot be
  completed over and over for experience. It expires on its own.
- **Settings** — your pet's species, colour, name, size, speed, per-site
  hide list, and on/off toggles (including break reminders and their
  interval, and fun announcements). Stored in `chrome.storage.sync`. We never
  see it.
- **Your herd** — each pet's species, colour, name and hat, for up to three
  pets. Synced.
- **Wardrobe and trinkets** — tokens earned, hats owned, the hat equipped, and
  which trinkets you have found and how many of each. Synced. The date of the
  last daily trinket is also synced, so the once-a-day find is once a day
  across your browsers rather than once per browser.
- **Room lamps** — the lamp brightness you last set in your pet's room. Synced.
- **Progress** — your pet's XP/level, your daily visit streak, unlocked
  achievements, and daily markers such as the last greeting, the hourly
  check-in and the install date. Dates and timestamps only. Stored locally
  (`chrome.storage.local`).
- **Play statistics** — simple counters used to award achievements: how many
  balls you've thrown, how many focus blocks you've completed, how many
  downloads have finished, and the highest number of tabs you've had open at
  once. These are plain numbers with no detail about *what* you downloaded or
  *which* tabs were open. Stored locally.
- **Small bits of popup state** — which intro tip you last saw, which popup tab
  was open last, whether the review prompt has been shown, and which photo-card
  moments have already been offered (a list of keys and dates, capped at 200).
  Stored locally.
- **Focus session state** — whether a focus session is running, whether
  you're in the focus or break phase, and when the current phase ends.
  Stored locally so the session survives your browser restarting the
  extension in the background.
- **Break timer state** — the numeric ID Chrome assigns to your current tab,
  plus timestamps for when you arrived and when you were last reminded.
  **No URL, page title, or page content is stored** — only a temporary tab
  number and the clock times needed to measure a duration.
- **Premium status** — whether this install is on the paid tier, and when that
  was last checked. Stored locally. See **Payments**.
- **ExtensionPay's purchase record** — its install date, a random key for this
  install, and its last purchase-status reply, which includes your email once
  you have paid. Written by ExtensionPay's library into `chrome.storage.sync`,
  not by Tiny Herd. The key exists only once you have opened checkout. See
  **Payments**.
- **Pet positions** — where each pet was standing, remembered for your current
  browser session only (`chrome.storage.session`).
- **Room mirror** — a copy of the pet, lamps and install date kept in the new
  tab page's own `localStorage`, so the room can draw instantly instead of
  flashing empty. Never synced, never read by anything else, cleared with the
  extension.

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

## Your new tab

Tiny Herd replaces the new tab page with your pet's room. The room is drawn
from images inside the extension — nothing on it is loaded from the internet,
and opening a new tab makes no network request. It shows what your pet has
already saved: its level, streak and badges, the trinkets it has found, the
hats you own, and your own to-dos. It does **not** read your history, your
bookmarks, or your most-visited sites, and there is no search box on it — your
address bar keeps the focus, and your default search engine is untouched. The
view through the room's window is worked out on your device from your
computer's clock and time zone; no location is used or requested. Turning the
room off means removing the extension, and Chrome tells you about the change
when you install.

## Photo cards

The "photo card" feature draws an image of your pet on your device and saves
it straight to your downloads when you press Save. It is generated locally and
never uploaded.

## Payments

Tiny Herd is free to use. An optional one-time purchase unlocks the premium
pack: more pets, colours and hats. Payments are processed by ExtensionPay
(extensionpay.com) and Stripe. You enter your email and card details on their
checkout page, never inside the extension, and Tiny Herd never sees your card
details. ExtensionPay holds the email address you pay with.

**The purchase check.** To know whether this install has paid, the extension
contacts extensionpay.com. It only starts once you have opened checkout: that
first visit creates a random key for this install. From then on the extension
sends that key to extensionpay.com about every six hours while Chrome is
running, when you open the popup before unlocking, and right after you pay. If
extensionpay.com cannot be reached, it tries again on its next once-a-minute
tick. The reply says whether the key has paid and, once it has, which email
paid. Nothing about your pet, your to-dos or your browsing is sent. Like any
web request, extensionpay.com also sees your IP address and browser. **If you
never open checkout, the extension never contacts ExtensionPay.**

**What is stored.** ExtensionPay's library keeps that key, the date it was
installed, and its last reply (including your email, once you have paid) in
Chrome's extension storage (`chrome.storage.sync`), which Chrome may sync
between browsers you are signed into. Tiny Herd itself keeps only whether this
install has paid and when that was last checked, on this device. If you are
offline, a paid install stays unlocked for up to 7 days before it needs to
check again.

**On ExtensionPay's checkout pages only**, a small script from ExtensionPay's
library tells the extension when a payment has completed, so the pack unlocks
straight away. It runs on no other site.

## On uninstall

Removing Tiny Herd opens a short feedback page on our website. That is an
ordinary web page visit — no information about you or your pet is attached to
it, and you can close it immediately. The only other thing in the extension
that contacts a server is the premium pack's purchase check, described under
**Payments**.

## What we never do

- No analytics, no fingerprinting, no ads, no selling of anything.
- No network requests other than the two described above: the purchase check
  (only if you open checkout) and the feedback page (only when you uninstall).
- No browsing history. The extension never builds a record of the sites you
  visit or how long you spent on each one — break timing is a single live
  countdown that resets when you move, and is never written down.
- No reading of page content — the pet draws itself *over* pages; it does
  not read what's on them.

## Permissions, in plain words

| Permission | Why |
|---|---|
| `storage` | Save your settings, to-dos, XP, streak, and achievements on your device |
| `alarms` | A once-a-minute timer that awards browsing XP and checks whether a focus phase, break reminder, memory warning, hourly check-in or purchase re-check is due |
| `downloads` | Notice when a download finishes so the pet can announce it — the filename and nothing else — and write a photo card to your downloads when you press Save |
| `tabs` | Read tab titles for unread-count announcements, the current site's hostname for per-site hide, tab switches to time break reminders, and the number of open tabs for milestones |
| `idle` | Pause break and focus timers, and let the pet nap, while you're away from your computer |
| `system.memory` | Read how much system memory is free so the pet can warn you when it's running low |
| `notifications` (optional) | Asked for only when you give a to-do a deadline. Used as a fallback to show the reminder when no pet is on screen to speak it. Declining keeps reminders bubble-only |

## Clearing your data

Everything about your pet lives in your browser. Removing the extension from
`chrome://extensions` deletes all of it — settings, to-dos, XP, streaks,
achievements, and timers. The one thing kept elsewhere is your purchase record
at ExtensionPay, which is what lets a paid install be restored later by
logging in with the email you paid with.

## Contact

Questions or concerns: open an issue at
[github.com/Choby-Digital/tiny-herd-public](https://github.com/Choby-Digital/tiny-herd-public/issues)
or email **chobydev@gmail.com**.

Changes to this policy will be posted on this page with an updated date.
