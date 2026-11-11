# Slash Launcher — Fork Notice

**Slash Launcher is an unofficial modified version of Cubiq Launcher.**

- **Upstream:** Cubiq Launcher by VivxKumar07
  (https://github.com/VivxKumar07/Cubiq-Launcher), itself an unofficial
  fork of Zalith Launcher 2 by MovTery and the Zalith Team
  (https://github.com/ZalithLauncher/ZalithLauncher2), which is based on
  PojavLauncher (https://github.com/PojavLauncherTeam/PojavLauncher).
- **License:** GNU General Public License v3.0 — see `LICENSE`. This file
  does not replace or remove any license or attribution. All original
  copyright notices, authors (VivxKumar07 and contributors, MovTery and
  contributors), and the acknowledgements in Settings → About are kept
  intact.
- **This fork is NOT affiliated with, endorsed by, or supported by
  VivxKumar07, MovTery, the Zalith Team, Mojang, or Microsoft.** Please do
  not ask the upstream authors for help with this modified version.

## What was changed from upstream

1. **Name:** application name changed from "Cubiq" / "Cubiq Launcher" to
   **"Slash Launcher"** (`launcher_name`, `launcher_app_name`,
   `launcher_short_name` in `CubiqLauncher/gradle.properties`, the app
   label in `AndroidManifest.xml` via `${launcher_name}`, and the
   user-visible name strings in the About screen, landscape footer, and
   profile screen). The app clearly states on its About screen that it is
   an "Unofficial Modified Version — based on Cubiq Launcher".
2. **Icon:** new launcher icon (Minecraft grass block with the letter "S"),
   replacing the upstream yellow-cube logo. The new icon is original
   artwork made for this fork. Replaced: adaptive-icon foreground render,
   `img_launcher.png`, `img_cubiq_emblem.png` (splash + profile emblem),
   all legacy `mipmap-*` launcher icons, and the vector foreground /
   monochrome drawables.
3. **Project home URL:** `url_home` now points to this fork's repository
   (https://github.com/supergoodd/slash-launcher-cubiq).
4. **Update & identity endpoints re-pointed to this fork** (same app, no
   feature change): the in-app update/announcements feed
   (`CubiqGitHubManager`) and the About-screen GitHub link (`URL_PROJECT`)
   now use the fork repository, so the app no longer offers upstream Cubiq
   APKs as "updates" (installing one would replace this fork with the
   original Cubiq, since the package name is unchanged — see below).
5. **Nothing else:** no gameplay, account, renderer, mod, or launcher
   functionality was changed. Version number (1.1.1) is kept from upstream
   so the change is easy to trace.

## What was deliberately NOT changed

- **Package name** (`com.cubiq.app`) is unchanged, because renaming it
  touches native code and many internal references and risks breaking the
  build. Consequence: this fork cannot be installed side-by-side with the
  official Cubiq Launcher — installing one replaces the other.
- **Code namespace** (`com.movtery.zalithlauncher`), internal class names
  (e.g. `CubiqGitHubManager`), the external storage folder
  ("Cubiq Launcher"), and log messages are unchanged for the same reason.
- **LICENSE, copyright headers, and all attributions** (About →
  Acknowledgements, third-party licenses) are unchanged.
- **Microsoft OAuth client ID** is unchanged (it is a public client ID,
  not a secret) so Microsoft sign-in keeps working as before. The fork
  owner may register their own Azure app later if they prefer.
