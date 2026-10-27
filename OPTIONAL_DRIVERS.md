# Windows Installer and Optional Audio Driver

[QuietPlay downloads](README.md#get-quietplay) | [User guide](USER_GUIDE.md) | [FAQ](FAQ.md)

## Install QuietPlay 2.2.22

Download **QuietPlay-2.2.22-Windows-Setup.exe** from the
[official release](https://github.com/cooperwwwwww/QuietPlay-downloads/releases/latest)
and run it, over the existing app if you already have one. Version 2.2.1 and
later can also update from **Settings → Updates** without the full installer. Setup includes QuietPlay, its Python runtime, playback
libraries, FFmpeg and the spotDL companion. No developer tools are needed.
Your library, playlists, history and settings stay in `%APPDATA%\QuietPlay`.

The modern interface requires Microsoft's **WebView2 Runtime**. Setup checks for
it and runs Microsoft's signed online bootstrapper if it is missing. That
prerequisite installation needs internet access. If it fails, install WebView2
from Microsoft and run QuietPlay setup again.

Read the [Windows security notice](README.md#windows-security-notice) if Windows
displays a warning. Do not disable Windows security protections.

## Optional: Separate Music Audio for OBS

Normal playback needs no extra audio driver. For separate OBS audio, QuietPlay
includes VB-Audio's original **VBCABLE_Driver_Pack45.zip**; setup does not install it.

1. Open **Settings → Streaming** and choose **Install VB-CABLE** (from 2.2.20).
   QuietPlay unpacks VB-Audio's own signed installer and runs it.
2. Approve the Windows prompt. Driver installation needs administrator approval
   and may need a Windows restart. VB-Audio's terms apply; review them first.
3. In QuietPlay's Streaming settings, choose **CABLE Input** as the stream output.
   Enable routing, and optionally listen on this PC too.
4. In OBS, add **Audio Input Capture** for **CABLE Output**. The now-playing
   Browser Source is a separate visual overlay.

VB-CABLE is third-party VB-Audio donationware.
[Official information and licensing](https://vb-audio.com/Cable/).
Device-specific drivers should come from the device's manufacturer or Windows Update.

## Included Files

| Item | Purpose |
| --- | --- |
| QuietPlay | App, runtime, playback libraries, FFmpeg and downloader. |
| WebView2 bootstrapper | Microsoft runtime setup, used only when WebView2 is missing. |
| VB-CABLE archive | Optional original driver package for manual OBS audio setup. |
| Release Evidence | Third-party notices, licenses and dependency records. |
