# Changelog

## 0.1.0-alpha.8 — 2026-09-13

- Fix background-tab mute without activation; add an independent monochrome all-window master mute.
- Add separate Daily Markdown folder selection and a real Stillpoint folder tree.
- Keep exactly one live Stillpoint editor, embedded or detached. Its anchor offers Summon Stillpoint; summoning or closing the floating shell reattaches the editor and preserves live workspace state. Unsafe drafts prevent detaching.
- Repair tab grouping and reopen order. Tabs compress to a 56px minimum; the standard window fits 18 instead of 6 before overflow. A compact anchored dropdown lists overflow tabs without replacing the page and closes on Escape, outside click or selection.
- Add persistent None (default), Initial and Site icon tab markers.
- Keep Balanced as the Memory Saver default; add Manual, which alone displays Sleep controls and disables automatic sleeping. Off, Balanced and Aggressive hide manual controls.
- Make Private windows darker and add a persistent default browsing mode while retaining explicit Normal windows.
- Add About information and improve first-profile filter initialization before browsing, retaining cached/fallback protection and honest ad-blocking limits.
- Keep the existing production profile path and prepare a one-time rollback copy before alpha.8 uses an existing profile.

Validation: typecheck, lint, 57 unit tests, 44 functional tests, production build, packaged runtime and Portable smoke checks passed. Repeated live YouTube ASCII → DEEP → ASCII cycles restored comments and secondary content without reloading; the historical alpha.6 report was not reproduced. Short playback tests do not prove universal ad blocking.

Known limits: unsigned Windows x64 alpha; no automatic updates; installed production-profile acceptance is still a user verification step. Live drafts are not crash recovery. Complex sites may need FULL/original view. ASCII/DEEP still use the live renderer; computational savings are not claimed. No guaranteed suppression of every YouTube pre-roll, mid-roll or server-inserted ad. External Markdown files need independent backups.

Close every Wavebreak process before upgrading. Portable and Setup share the normal profile. The one-time rollback snapshot is at `%APPDATA%\Wavebreak.rollback-before-alpha8\profile`; retain it and the previous executable until satisfied. External Markdown files are not rolled back with the browser profile.

## 0.1.0-alpha.7

Memory Saver alpha.

### What ships

- Memory Saver with `Off`, `Balanced` and `Aggressive` modes.
- `Balanced` is the default.
- Eligible inactive tabs can automatically sleep after they have been inactive long enough and are outside the warm recent-tab set.
- Sleeping tabs release their page renderer and restore when selected.
- URL, title and approximate scroll position are preserved across sleep and restore.
- Active tabs, audible/media tabs, active-download tabs, internal/non-HTTP(S) views, loading/restoring/recently restored tabs and tabs with detected editable user input are protected from automatic sleep.
- Manual Sleep remains available for inactive tabs.
- Windows x64 portable and installer builds.

### Internal validation example

In one internal 10-tab same-session validation, Balanced Memory Saver reduced total Wavebreak process-tree RAM from ~3.2 GB to ~1.5 GB by sleeping eligible inactive tabs. Results vary with websites and session state.

### Known alpha limits

- Windows builds are unsigned and may trigger SmartScreen warnings.
- macOS, Linux and mobile builds are not yet publicly available.
- The source code remains proprietary and is not published in this repository.
- Arbitrary web-app/form state is not serialized when a tab sleeps. Automatic sleeping conservatively avoids tabs where editable interaction has been detected.
- Dynamic Mode transformations are not universal and may need original view on complex websites.
- Ad and tracker blocking is not guaranteed to block every ad, tracker or video ad.
- Shared Markdown editing requires manual save/refresh and independent backups.
- Stillpoint is an active direction; deeper integration is future work.

## 0.1.0-alpha.6

Initial public-alpha target.

### What ships

- Secure Electron browsing shell with isolated website views and local browser chrome.
- Tabs, tab groups, bookmarks, history, downloads, find, zoom, mute, print and fullscreen basics.
- Dynamic Mode with `1 FULL`, `2 CLEAR`, `3 ASCII` and `4 DEEP`.
- Fast reversible mode switching for supported pages.
- Local ASCII conversion for eligible images.
- Primary video/player layout preservation in ASCII and simplified supported-player controls in DEEP.
- Per-tab, site, session and global mode scope.
- Private sessions using isolated nonpersistent browsing partitions.
- Ghostery/adblocker-list based protection across modes.
- New-tab page with phthalo-green wave artwork.
- 24 selectable dark color palettes.
- Optional Daily workspace and shared Markdown folder editing.
- Windows x64 portable and installer builds.

### Known alpha limits

- Windows builds are unsigned and may trigger SmartScreen warnings.
- macOS and Linux builds are not yet publicly available.
- Dynamic Mode transformations are not universal and may need original view on complex websites.
- Ad and tracker blocking is not guaranteed to block every ad, tracker or video ad.
- Shared Markdown editing requires manual save/refresh and independent backups.
- Stillpoint is an active direction; deeper integration is future work.
- Memory and performance optimization remain future measured work.

