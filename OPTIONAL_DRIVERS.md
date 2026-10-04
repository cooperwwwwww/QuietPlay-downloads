# Windows Installer + Optional Drivers

[QuietPlay downloads](README.md#get-quietplay) | [User guide](USER_GUIDE.md) | [FAQ](FAQ.md)

Use the **Windows installer + optional drivers (ZIP)** download on the main
page. It is the shareable installation bundle, not the portable app archive.

## Install QuietPlay

1. Extract the downloaded ZIP into a normal folder.
2. Open **Install QuietPlay.exe** and follow the installer.
3. Open the **QuietPlay** desktop or Start menu shortcut.

The bundled app already includes its runtime, audio libraries, FFmpeg, and
spotDL companion. Do not install Python or spotDL separately. If Smart App
Control blocks this unsigned testing build, stop. Do not turn off Windows
protections to run it.

## Optional: Separate Music Audio for OBS

Skip this section for normal listening, or if your PC already has the routing
device you want to use.

1. In the extracted bundle, open **Optional Streamer Audio Driver**.
2. Extract **VBCABLE_Driver_Pack45.zip** into another normal folder.
3. On 64-bit Windows, run **VBCABLE_Setup_x64.exe** as administrator and use its
   Install Driver action. Approve Windows' administrator prompt only if you
   intend to install the driver. Restart if the driver setup requests it.
4. Open QuietPlay's **Streaming** settings and select **CABLE Input** as the
   stream output. Enable stream routing, and optionally listen on this PC too.
5. In OBS, use the guided setup or an **Audio Input Capture** source for
   **CABLE Output**. The now-playing Browser Source is a separate visual overlay,
   not the audio source.

VB-CABLE is third-party **VB-Audio donationware**. Its own terms apply and
donations are welcome. [Official VB-Audio licensing](https://vb-audio.com/Services/licensing.htm).
Driver installation can affect Windows audio routing; it is never a requirement
for using QuietPlay's local library.

## Optional: Microsoft WebView2

Most current Windows PCs already have WebView2. If an embedded web component
reports that it is missing, the bundle's **Prerequisites** folder contains
**MicrosoftEdgeWebView2Setup.exe**. This is Microsoft's online bootstrapper,
which downloads the runtime during setup and needs an internet connection.

## What Is in the Bundle?

| Included Item | Purpose |
| --- | --- |
| `Install QuietPlay.exe` | The same QuietPlay app installer as the standalone Setup download. |
| `Optional Streamer Audio Driver/VBCABLE_Driver_Pack45.zip` | Optional virtual audio routing driver package. |
| `Prerequisites/MicrosoftEdgeWebView2Setup.exe` | Optional Microsoft web runtime bootstrapper. |
| `START HERE.txt` and `PACKAGE CONTENTS.txt` | Offline setup notes and package details. |
| `PACKAGE-MANIFEST.json` and `SHA256SUMS.txt` | Package inventory and file-integrity information. |

The optional packages are **included**, but are not silently installed. There
is no single driver that improves every headset or sound card; device-specific
drivers should come from that device's manufacturer or Windows Update.
