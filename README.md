<div align="center">

<h1>RapidFetch</h1>

<p><strong>A fast download manager for Windows, with a browser extension and its own video player.</strong></p>

<p>Split every download across many connections, pause and resume at any time,<br>and save videos, audio, playlists and torrents from the pages you visit.</p>

<p>
  <a href="https://github.com/msaleh96/RapidFetch-Releases/releases/latest/download/RapidFetch-Setup.exe"><img src="https://img.shields.io/badge/Download%20RapidFetch%20for%20Windows-2563EB?style=for-the-badge" alt="Download RapidFetch for Windows" height="46"></a>
</p>

<p>
  <a href="https://github.com/msaleh96/RapidFetch-Releases/releases/latest"><img src="https://img.shields.io/github/v/release/msaleh96/RapidFetch-Releases?style=flat-square&label=stable&color=2563EB" alt="Latest stable version"></a>
  <img src="https://img.shields.io/badge/Windows%2010%20%7C%2011-64--bit-334155?style=flat-square" alt="Windows 10 and 11, 64-bit">
</p>

<sub>Installs for your Windows account, no administrator rights needed · <a href="https://github.com/msaleh96/RapidFetch-Releases/releases">All releases</a></sub>

</div>

<br>

## Why RapidFetch?

Browsers download a file over a single connection and lose it when something goes wrong. RapidFetch splits each file into parts that download side by side, so large files finish sooner and can be paused, resumed or picked up again after a restart. Its browser extension hands your downloads and the videos on a page to RapidFetch, so you choose the quality, keep a tidy list and let queues finish the rest while you work.

## Features

| | |
|---|---|
| **Faster, resumable downloads** | Up to 32 connections per file. Pause and resume at any time, also after RapidFetch was closed. |
| **Video and audio from web pages** | Pick the quality, the sound language and subtitles. HLS streams and separate video and audio streams end up as one file. Download only a part of a video, or a whole playlist. |
| **Watch Now** | Play a video from a web page in RapidFetch's own player without downloading it first, with a Download button for what is playing. DRM-protected videos and live streams are not supported. |
| **Torrents** | Open `.torrent` files and magnet links. |
| **Browser extension** | For Chrome, Edge, Opera, Brave and Firefox: takes over browser downloads, adds a video panel to pages and entries to the right-click menu. Each browser is connected once, with your permission. |
| **Stays organised** | Files are sorted into categories by type. Queues and a scheduler start and stop downloads at set times and can sleep or shut down the PC afterwards. |
| **Speed limiter** | One limit for everything, or a limit per download. |
| **Link Grabber** | Collect all the links of a page, or several links copied at once, into one list and download the ones you pick. |
| **Clipboard monitor** | Offers to download a file link as soon as you copy it (can be turned off). |
| **Eight languages** | English, العربية, Français, Español, Deutsch, Português, Türkçe, Русский. |

## Installation

1. **Download** `RapidFetch-Setup.exe` with the button above.
2. **Run it.** Windows may show a SmartScreen notice first; see [Security and Windows SmartScreen](#security-and-windows-smartscreen).
3. **Follow the setup:** accept the license, choose whether you want a desktop shortcut and whether RapidFetch starts with Windows, then click **Install**. It installs for your account in `%LOCALAPPDATA%\Programs\RapidFetch`.
4. **Launch RapidFetch** from the last page of the setup or from the Start menu. On its first start it opens a short guide for adding the browser extension.

To uninstall, use **Settings → Apps** in Windows or **Uninstall RapidFetch** in its Start menu folder. Files you downloaded are not touched.

## Browser extension

The extension comes with RapidFetch: it is in the `extension` folder of the installation (the Start menu has a **Browser extension folder** shortcut). Browsers only add an extension from a folder when you confirm it yourself, so RapidFetch walks you through it: **Help → Add RapidFetch to my browser…** (it also opens by itself on the first start).

**Chrome, Edge, Brave and Opera**

1. Click **Open Extensions Page** in the guide. Your browser opens a new tab and the address (for example `chrome://extensions` or `edge://extensions`) is copied: paste it into the address bar and press Enter.
2. Turn on **Developer mode** on that page. It is needed to add an extension from a folder on your computer, and the browser may remind you of it later.
3. Click **Load unpacked** and select the `extension` folder itself, the one that contains `manifest.json`.
4. RapidFetch asks whether to connect the browser: click **OK**. The RapidFetch icon in the toolbar then shows that it is connected.

**Firefox**

Firefox keeps only add-ons signed by Mozilla. Until a signed version is available, RapidFetch's guide loads the add-on through `about:debugging` as a temporary add-on, which Firefox removes when it closes.

## Updates

RapidFetch looks for new stable versions by itself and asks before it installs one; you can also check at any time with **Help → Check for updates**. Before installing an update, it checks the file's SHA-256 checksum and its digital signature.

Every stable version is also on the [Releases page](https://github.com/msaleh96/RapidFetch-Releases/releases). Running a newer installer updates RapidFetch in place and keeps your settings and download list. Versions marked **Pre-release** there are test builds: they are never offered as updates and are not meant for everyday use.

## Security and Windows SmartScreen

The installer is not signed with a Windows code-signing certificate, so SmartScreen may show **"Windows protected your PC"** when you run it. Before you continue:

- Download RapidFetch only from this page or its [Releases page](https://github.com/msaleh96/RapidFetch-Releases/releases).
- Compare the installer's checksum with the `SHA256SUMS` file attached to the same release. In PowerShell:

  ```powershell
  (Get-FileHash .\RapidFetch-Setup.exe -Algorithm SHA256).Hash.ToLower()
  ```

  The result must match the line for `RapidFetch-Setup.exe` in `SHA256SUMS`.

Only when it matches, choose **More info → Run anyway**. If it does not match, delete the file and download it again from the Releases page.

## Open-source components

RapidFetch uses FFmpeg, mpv, yt-dlp and aria2 as separate programs in its `tools` folder, with their license texts next to them. The complete source code of the GPL and LGPL components shipped in the installer is attached to every release.

## Support and feedback

- **Questions and bug reports:** [Issues](https://github.com/msaleh96/RapidFetch-Releases/issues) (a GitHub account is needed to open one).
- **Downloads and release notes:** [Releases](https://github.com/msaleh96/RapidFetch-Releases/releases).

<br>

<div align="center"><sub>Copyright © 2026 RapidFetch</sub></div>
