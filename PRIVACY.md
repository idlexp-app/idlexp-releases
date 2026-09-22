<a href="PRIVACIDADE.md">Português</a> · <b>English</b>

# IdleXP privacy notice

Last updated: 16/09/2026.

**IdleXP has no server, no account and sends nothing to us.** Everything it keeps
stays on your computer, and the only thing it talks to is Huntera itself — the
same site you would open in your browser.

There is no sign-up, no IdleXP login, no telemetry, no analytics, no advertising
and no tracker. There is no database on our side with you in it, because there is
no server of ours at all.

## What the app keeps, and where

Everything of yours lives in a single folder on your computer. Where that folder
is depends on the system:

| System | The folder |
| --- | --- |
| Windows | `%APPDATA%\idlexp` |
| macOS | `~/Library/Application Support/idlexp` |
| Linux | `~/.config/idlexp` |

Inside it:

| Folder or file | What it is |
| --- | --- |
| `Partitions/idlexp-account-{1..4}` | The four game logins — cookies and storage that **Huntera's own site** writes. IdleXP does not read those credentials: it only keeps the four apart, so that one account cannot see another |
| `settings.json` | Your screen preferences, and nothing else: the zoom, how many screens, the arrangement (grid or main), which accounts are in economy mode and whether the name-hiding eye is on |
| `sprites/` | A cache of the monster images the economy panel shows, downloaded from Huntera itself |
| `diagnostico.log` | A technical log of what the app did, for investigating a problem. See the section below |
| `Cache`, `GPUCache`, `Local Storage` and the other loose folders | What the embedded browser writes on its own for the app window: cached downloads and drawing, and its own preferences. The game logins are not in these — they are in `Partitions` |

**How the logins are stored.** The cookies in `Partitions` are written to disk **unencrypted**,
on all three systems. The Chrome browser encrypts its own with the system's protection; the
browser embedded in IdleXP ships with that encryption off, and it stays off on purpose: turning
it on would change how the four logins already saved are stored, and those must not be touched.
What protects the folder is your account on the computer — another account without
administrator rights cannot open it. Anyone using your account, an administrator, or a program
running as you can. If the computer is shared, each person should have their own account.

IdleXP takes up more space outside that folder, and none of it holds anything of
yours: the program itself, and wherever the update leaves what it already
downloaded.

| System | The program | The update |
| --- | --- | --- |
| Windows | `%LOCALAPPDATA%\Programs\IdleXP` | `%LOCALAPPDATA%\idlexp-updater`, with a copy of the installer that is used to download only what changed next time |
| macOS | the `IdleXP.app` you dragged into Applications | nothing: on the Mac the app does not install updates on its own, it only tells you one exists |
| Linux | the `IdleXP.AppImage` file, wherever you left it | `~/.cache/idlexp-updater`, used while the update downloads |

We keep no password, e-mail address, payment method or anything of the sort —
IdleXP never asks for those. You type your game password on Huntera's own page
inside the app, exactly as you would in a browser, and it goes to Huntera.

## Who the app talks to

- **`huntera.com.br`** — the game page, the read-only connection that follows the
  character in economy mode, and the images the panel shows.
- **Whatever login provider Huntera itself uses**, if the game sends you to an
  external service to sign in. The game picks that service, not us.
- **GitHub, to ask whether a new version exists.** This happens every time the app
  opens, and only then. That request carries what any download carries — the IP
  address of your connection and which version was asked for — and, when there is
  a new version, also which version you have installed, so that only what changed
  is downloaded. Whoever may log that is GitHub, under its own terms. None of it
  reaches us, and the app sends along no information about you, your computer or
  your accounts — not even a number identifying your installation.

No other address. The app fetches no font, icon, script or advertising from
anywhere: the entire interface is packaged inside the executable.

**There is one thing the app asks YOUR browser to open, and only on your click:**
the support window has a button that hands `ko-fi.com/idlexp` to the system
browser, and stops there. IdleXP does not talk to Ko-fi and sends it nothing —
from that point on the conversation is between you and Ko-fi, under its own
terms. The address is written on screen before the click, and without the click
nothing happens.

## About `diagnostico.log`

It is the file we ask for when you report a problem, and it deserves to be
described in full:

- It is written **always**, not only when something goes wrong.
- It has a 2 MB ceiling. Past that, the old one becomes `diagnostico.log.1` and
  the app starts over — it does not grow forever.
- It records what the app did: accounts opening, entering and leaving economy
  mode, connection errors and error messages Huntera returned.
- It does **not** record the body of the game's responses, nor any password,
  cookie or anything that would let someone into your account.
- **It does record your characters' names.** That is on purpose: without knowing
  which account a line belongs to, the file is useless for investigating
  anything. Note that the eye that hides names covers the screen and the game,
  but does **not** cover this file — it is for support, not for streaming.
- **It is never sent anywhere.** It stays on your computer. If you want us to see
  it, you are the one who attaches it.

## The character name

The name on each card is read from the game, live. You do not choose it, it is
kept in no file other than `diagnostico.log` (see above), and it leaves the
screen along with the session — that is how the app knows which accounts are
online. The eye in the toolbar blacks that name out on the four cards, on the
economy panels and inside the game page too, for whoever is about to take a
screenshot or stream.

## How to erase everything

Close IdleXP and delete the data folder from the table above — `%APPDATA%\idlexp`
on Windows, `~/Library/Application Support/idlexp` on macOS or `~/.config/idlexp`
on Linux. That removes the logins, the preferences, the cache and the log in one
go — **and signs all four accounts out.** Removing the app does not delete that
folder, on purpose: someone who uninstalls in order to reinstall should not have
to sign in four times again.

Removing the app differs per system: on Windows, uninstall from Settings › Apps;
on macOS, drag `IdleXP.app` to the Trash; on Linux, delete the `IdleXP.AppImage`
file. The update folder, where there is one, can be deleted by hand at any time —
next time around the app downloads the whole file.

## LGPD

We carry out no processing of your personal data, because nothing leaves your
computer in our direction. What Huntera collects while you play is between you
and Huntera, and their privacy policy applies. (LGPD is Brazil's general data
protection law, the statute IdleXP is written to comply with.)

IdleXP is not affiliated with Huntera — see the [license](LICENSE.en.txt).

## If this notice changes

A future version of the app may come with a different notice. The date at the top
says which one is current, and the version published with each release is the one
that applies to it.

## Contact

Questions about this notice go to the issues of IdleXP's official repository:
https://github.com/idlexp-app/idlexp-releases/issues. They are public: do not
write a password, an e-mail address or your characters' names there. A security
problem is reported privately, through the Security tab of the same repository.
