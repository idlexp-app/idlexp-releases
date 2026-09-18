<p align="center">
  <a href="README.md">Português</a> · <b>English</b>
</p>

<p align="center">
  <img src="imagens/goblin.png" width="136" height="128" alt="IdleXP">
</p>

<h1 align="center">IdleXP</h1>

<p align="center">
  <strong>Four Huntera accounts in a single window — and your PC barely notices.</strong>
</p>

<p align="center">
  <a href="https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP-Setup.exe"><img src="https://img.shields.io/badge/Windows-IdleXP--Setup.exe-2ea043?style=for-the-badge&logo=windows&logoColor=white" alt="Download for Windows"></a>
  <a href="https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP.dmg"><img src="https://img.shields.io/badge/macOS-IdleXP.dmg-2ea043?style=for-the-badge&logo=apple&logoColor=white" alt="Download for macOS"></a>
  <a href="https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP.AppImage"><img src="https://img.shields.io/badge/Linux-IdleXP.AppImage-2ea043?style=for-the-badge&logo=linux&logoColor=white" alt="Download for Linux"></a>
</p>

<p align="center">
  <a href="https://github.com/idlexp-app/idlexp-releases/releases/latest"><img src="https://img.shields.io/github/v/release/idlexp-app/idlexp-releases?label=version&color=2ea043" alt="Version"></a>
  <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fidlexp-app%2Fidlexp-releases%2Finsignias%2Fdownloads.json" alt="Downloads">
  <img src="https://img.shields.io/badge/Windows_%C2%B7_macOS_%C2%B7_Linux-0078d4" alt="Windows, macOS and Linux">
  <img src="https://img.shields.io/badge/price-free-555" alt="Free">
</p>

<p align="center">
  Free · no sign-up · updates itself
</p>

---

<p align="center">
  <img src="imagens/painel-economia.png" alt="The economy mode panel: XP per hour, profit, preys, the hunt's bestiary and your gear's imbuements">
  <br>
  <sub>The economy mode panel. Illustrative image, with sample data.</sub>
</p>

## Why IdleXP

Playing several characters in the browser means opening several tabs, signing in over and over,
and watching the computer heat up. IdleXP puts the four accounts in one window, remembers the
four logins and, with **economy mode**, closes the browser of the accounts you are not looking
at — without stopping their hunt.

### What changes on your PC

With all four accounts in economy mode, compared to the same four accounts open normally:

| | Without economy mode | With economy mode | |
| --- | --- | --- | --- |
| **Processor** | 310% of one core | 13% of one core | **−96%** |
| **Memory** | 5.4 GB | 1.85 GB | **−66%** |
| **Graphics card** | 6.5% usage | 0.1% usage | **−98%** |

And each account that leaves the screen, on its own: from **776 MB and 27% of one core** to
**64 MB and under 0.5%** — while still earning experience.

<sub>Measured on the developer's PC on 04/09/2026: four screens, three accounts signed in to the
same hunt and one signed out, two 60-second windows, the only difference being economy mode. The
numbers on your PC will be different; the ratio is what counts.</sub>

## What it does

- **Four accounts, four saved logins.** Each account has its own space: one cannot see another, and
  you do not have to sign in again every time you open the app.
- **The screen your way.** From 1 to 4 screens side by side, or one large one with the others
  alongside. Adjustable zoom and full screen.
- **Economy mode.** The account keeps hunting, but with no browser open. In place of the game there
  is a panel with what matters: health, mana, stamina, level, **XP/h**, **Profit/h**, the active
  **preys**, the hunt's **bestiary**, with how much is left for each stage, and your gear's
  **imbuements**, with the time left on each one and a warning at 20 minutes or less.
- **Automatic economy.** In the 1-to-3-screen layouts, accounts that stay off screen enter economy
  mode on their own after 2 minutes.
- **Tells you when something goes wrong.** If the character dies or stamina runs out, the account
  card shows it right away.
- **In Portuguese or English.** Pick the language on the globe in the opening window, before the
  accounts load. The first time, the app follows your system's language.
- **Hides names for screenshots and streams.** One click blacks out the character names in the app
  and, inside the game, on the map, in the party and in the header.
- **Updates itself.** On opening, IdleXP checks for a new version, downloads and installs it before
  any account opens. You download once. (On the Mac it tells you and brings you here — see below.)

> Economy mode follows the character while it hunts offline (VIP). It does not keep a hunt going
> that the game would not keep going.

## Install

IdleXP runs on **Windows, macOS and Linux**, 64-bit. Pick yours:

### Windows 10 or 11

1. Download **[IdleXP-Setup.exe](https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP-Setup.exe)**.
2. Open the file. The first time, Windows shows a blue warning (see below why): click **More info**
   and then **Run anyway**.
3. Accept the license, choose the folder and that is it. At the end you can open the app and create
   the shortcut.

The installer never asks for an administrator password and installs for your user only.

### macOS (Intel and Apple Silicon)

1. Download **[IdleXP.dmg](https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP.dmg)** — a single file that works on both kinds of Mac.
2. Open the `.dmg` and drag IdleXP into the **Applications** folder.
3. The first time, macOS says the developer could not be verified. Go to **System Settings ›
   Privacy & Security**, scroll to the IdleXP warning and click **Open Anyway**. Once only.

**On the Mac, IdleXP does not update itself.** It checks whether a new version exists and says so on
the opening screen, with the address of this page for you to download it. The reason is under "Is it
safe?", below.

### Linux (64-bit)

1. Download **[IdleXP.AppImage](https://github.com/idlexp-app/idlexp-releases/releases/latest/download/IdleXP.AppImage)**.
2. Give it permission to run — through your file manager (Properties › Permissions › "Allow
   executing") or in the terminal:
   ```
   chmod +x IdleXP.AppImage
   ```
3. Open the file. There is no installation, no password prompt and no system warning at all.

The AppImage does not create a menu entry on its own, and IdleXP will not offer to create one: if
you want that integration, your distribution's AppImageLauncher already asks. Keep the file
somewhere it can stay — the update replaces that same file in place.

## Is it safe?

**Yes — and you do not have to take just our word for it.**

### Why your system shows a warning

IdleXP does not yet have a **paid digital signature**, and each system reacts to that differently:

| System | What appears | What it means |
| --- | --- | --- |
| **Windows** | "Windows protected your PC" (the blue SmartScreen screen) | "Windows does not know this file yet", not "this file is dangerous". As more people download it, the warning tends to go away |
| **macOS** | "cannot verify the developer" | Apple charges US$99/year to identify developers, and we do not pay it. That is also why the Mac does not update itself: macOS refuses to install an update to an unsigned app |
| **Linux** | nothing | the AppImage opens straight away, and updates itself |

### How to check that the file is the original

- **Immutable badge.** Every release published here is locked by GitHub itself: once published,
  nobody — not even us — can swap the files. You see the **Immutable** padlock on the release page,
  and GitHub signs an attestation that anyone can check with the
  [GitHub CLI](https://cli.github.com/):
  ```
  gh release verify-asset IdleXP-Setup.exe -R idlexp-app/idlexp-releases
  ```
- **Checksum (SHA-256).** Each release's notes carry the checksum of all three files, with the
  command for each system beside it. The result has to match the notes. If it differs, do not
  install.
- **This repository is the only official address.** An IdleXP downloaded anywhere else is not ours.

### What IdleXP never does

- **It does not keep your password.** You sign in on Huntera's own page, inside the app, just as you
  would in a browser. The password goes to Huntera.
- **It does not send anything to us.** There is no IdleXP server, no sign-up, no telemetry and no
  advertising. The app talks only to Huntera and to this repository, to check for a new version.
- **It does not play for you.** Economy mode only **reads** what happens to the character. IdleXP
  cannot send any game action: that part does not exist in the program.
- **It does not touch your logins when removed.** They stay in a folder of yours, and reinstalling
  gives all four accounts back, signed in.
- **It does not install an update without checking it.** Updates come only from this repository, and
  are applied only if the downloaded file's checksum matches the one published here.

The details are in the [privacy notice](PRIVACY.md) and in the [security policy](SECURITY.en.md).

## Common questions

**Does it work on the Mac?** It does, on Intel and Apple Silicon, from the same file. The difference
is that on the Mac it does not install updates by itself: it tells you one is out and brings you
here.

**And on Linux?** Yes, through the 64-bit AppImage — no installation and no password prompt. This is
IdleXP's first release for Linux; if something does not work on your distribution, tell us in an
issue.

**Where are my logins kept?** On your computer: `%APPDATA%\idlexp` on Windows,
`~/Library/Application Support/idlexp` on macOS and `~/.config/idlexp` on Linux. Nothing leaves it.

**How do I remove it?** On Windows, in Settings › Apps, look for IdleXP. On macOS, drag IdleXP.app
to the Trash. On Linux, delete the `IdleXP.AppImage` file. In all of them, the logins stay put for
when you come back.

**I found a problem.** [Open an issue](https://github.com/idlexp-app/idlexp-releases/issues/new/choose)
telling us the version, your system and what happened. For a security problem, report it
[privately](https://github.com/idlexp-app/idlexp-releases/security/advisories/new).

---

<sub>IdleXP is free and is not affiliated with Huntera. Use is subject to the license
([Português](LICENSE) · [English](LICENSE.en.txt)). Huntera is a trademark of its respective owners.</sub>
