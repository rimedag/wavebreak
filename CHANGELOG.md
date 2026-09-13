# Changelog

Public releases should continue in order: `alpha.7`, `alpha.8`, `alpha.9` and onward.

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

