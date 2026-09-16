<a href="SECURITY.md">Português</a> · <b>English</b>

# IdleXP security

## Where to download

The only official place is this repository:
**https://github.com/idlexp-app/idlexp-releases/releases/latest**

An IdleXP downloaded from another site, group or message is not ours. The app itself only updates
from here.

Every release carries three files, one per system: `IdleXP-Setup.exe` (Windows), `IdleXP.dmg`
(macOS, Intel and Apple Silicon in the same file) and `IdleXP.AppImage` (Linux 64-bit).

## How to check a download

1. **Immutable badge.** Every published release is locked by GitHub and shows the **Immutable**
   padlock on its page. Once published, the files cannot be swapped. To check the attestation
   signed by GitHub, with the [GitHub CLI](https://cli.github.com/):

   ```
   gh release verify-asset v1.2.3 IdleXP-Setup.exe -R idlexp-app/idlexp-releases
   ```

   Replace `v1.2.3` with the version you downloaded, and the file name with the one for your system.

2. **Checksum (SHA-256).** Each release's notes carry the checksum of all three files. The command
   differs per system:

   | System | Command |
   | --- | --- |
   | Windows (PowerShell) | `Get-FileHash .\IdleXP-Setup.exe` |
   | macOS | `shasum -a 256 IdleXP.dmg` |
   | Linux | `sha256sum IdleXP.AppImage` |

   If the result differs from the published one, do not install it and let us know.

## Your system's warning

IdleXP does not yet have a paid digital signature, and each system reacts to that differently:

- **Windows.** SmartScreen shows "Windows protected your PC" the first time. It is the warning for a
  new file, not for a dangerous one. Click **More info** and then **Run anyway**.
- **macOS.** Gatekeeper says the developer could not be verified. Go to **System Settings › Privacy
  & Security** and click **Open Anyway**. For the same reason, on the Mac the app does **not**
  install updates by itself: it tells you one exists and brings you to this page.
- **Linux.** There is no warning at all, and updating is automatic.

## What protects the people who use it

- The four accounts are isolated from one another, and the logins exist only on your computer.
- The app has no server, no sign-up and no telemetry. See the [privacy notice](PRIVACY.md).
- The economy mode connection only reads. The program cannot send any game action.
- An update is installed only if the downloaded file's checksum (SHA-512) matches the one published
  here; if it does not match, the app opens on the version you already have.
- On Windows the installer never asks for administrator; on Linux the AppImage does not either.
  Removing the app does not delete the logins on any of the three.

## Reporting a security problem

**Do not open a public issue.** Use
[Report a vulnerability](https://github.com/idlexp-app/idlexp-releases/security/advisories/new):
only we see the report until it is resolved.

Tell us the IdleXP version, your system, what happens and how to reproduce it. If you attach
`diagnostico.log` — which lives in the app's data folder, described in the privacy notice — delete
your characters' names from it first.
