# Windows Installer + Optional Drivers

[QuietPlay downloads](README.md#get-quietplay) | [User guide](USER_GUIDE.md) | [FAQ](FAQ.md)

Use **Download for Windows** on the main page. One Setup EXE includes the app
and optional extras. There is no ZIP to extract or developer setup to configure.

## Install QuietPlay

1. Open the downloaded **QuietPlay Setup EXE**.
2. On **Optional extras**, choose only the extras you need. Both are unchecked
   by default: VB-CABLE for separate OBS audio, and WebView2 if missing.
3. Open the **QuietPlay** desktop or Start menu shortcut.

The bundled app already includes its runtime, audio libraries, FFmpeg, and
spotDL companion. Do not install Python or spotDL separately. If Smart App
Control blocks this unsigned testing build, stop. Do not turn off Windows
protections to run it.

## Optional: Separate Music Audio for OBS

Skip this section for normal listening, or if your PC already has the routing
device you want to use.

1. In QuietPlay setup, select **Set up VB-CABLE for separate OBS audio**.
2. Windows asks for administrator approval for VB-Audio's original signed
   installer. Approve only if you intend to install it.
3. In the VB-CABLE window, choose **Install Driver**, then close its setup to
   let QuietPlay finish. You can cancel the driver without needing it for music
   playback. Restart Windows if the driver requests it.
4. Open QuietPlay's **Streaming** settings and select **CABLE Input** as the
   stream output. Enable stream routing, and optionally listen on this PC too.
5. In OBS, use the guided setup or an **Audio Input Capture** source for
   **CABLE Output**. The now-playing Browser Source is a separate visual overlay,
   not the audio source.

VB-CABLE is third-party **VB-Audio donationware**. Its own terms apply and
donations are welcome. [Official VB-Audio licensing](https://vb-audio.com/Services/licensing.htm).
Driver installation can affect Windows audio routing; it is never a requirement
for using QuietPlay's local library.

If you skip the driver, you can select it when running QuietPlay setup again,
or use the app's Streaming setup. The original package is also retained in the
installed app's **Optional Streamer Audio Driver** folder. Silent app updates
do not launch the interactive driver installer.

## Optional: Microsoft WebView2

Most current Windows PCs already have WebView2. QuietPlay setup offers the
checkbox only when it is not detected. Microsoft's signed online bootstrapper
downloads the runtime, so the optional installation needs internet access.
WebView2 is not required for local playback or spotDL downloads.

## What Setup Includes

| Included Item | Purpose |
| --- | --- |
| QuietPlay app | Runtime, playback libraries, FFmpeg, and optional downloader included. |
| VB-CABLE | Original driver package; signed setup files are installed when selected. |
| Microsoft WebView2 | Signed runtime bootstrapper for the optional setup choice. |
| Release Evidence | Third-party licenses and package verification information. |

The optional packages are **included**, but are not silently installed. There
is no single driver that improves every headset or sound card; device-specific
drivers should come from that device's manufacturer or Windows Update.
