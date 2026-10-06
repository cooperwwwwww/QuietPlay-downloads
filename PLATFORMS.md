# QuietPlay Platforms

[QuietPlay](README.md) | [Downloads](README.md#get-quietplay) | [User guide](USER_GUIDE.md)

Use only the installers listed in the current release. A build target in this
guide does not mean a download is available: packages are published only after
their checks pass. All current packages are Beta releases.

## Windows

Windows 10 or 11, Intel/AMD 64-bit. Use the Setup EXE. The installer contains
the player runtime, FFmpeg and optional spotDL downloader. Optional VB-CABLE
and WebView2 choices are off by default and apply only to Windows.

See the [Windows installation and security guide](README.md#install-quietplay).
Unsigned packages may be blocked; do not disable Windows security.

## macOS

Experimental native build targets: Apple Silicon on macOS 14 or newer, and
Intel on macOS 15 or newer. These are the native runner versions used for
checks, not a claim that older macOS versions have been tested.

When a matching DMG is listed, open it and drag QuietPlay into Applications.
The app includes its Python runtime, decoder and optional downloader; no
developer setup is needed. Command shortcuts mirror the app's Control shortcuts.

Mac packages are not Developer ID signed or Apple notarized. macOS may block
them. Do not disable Gatekeeper or run commands that remove security protection.
Follow Apple's guidance only for a specific app you trust, or wait for a signed
release: [opening apps safely](https://support.apple.com/en-us/102445).

## Linux

Experimental native build targets: Ubuntu 22.04+ or Debian 12+, Intel/AMD
64-bit and ARM64, with a graphical desktop and an audio service. Other
distributions are not currently packaged or tested.

When a matching DEB is listed, open it in the system's package installer.
It installs QuietPlay and a launcher into the desktop's application menu.
Use the package manager for removal. For desktops without a graphical package
installer, this command installs a downloaded package and its system dependencies:

```sh
sudo apt install ./QuietPlay-<version>-Beta-Linux-<architecture>.deb
```

Replace the filename with the downloaded DEB. Package installation requires
administrator approval. The app runtime and downloader are included; a separate
Python installation is not required. QuietPlay uses PulseAudio or ALSA through
miniaudio; PipeWire desktops may provide PulseAudio compatibility.

## Chromebook

There is no native ChromeOS, Android or browser version. The Linux package is
the Chromebook route, for devices that support the Linux development environment.
Managed school/work devices may restrict that environment. Do not bypass policy.

1. Follow Google's [Linux setup guide](https://support.google.com/chromebook/answer/9145439).
2. Choose the DEB matching the Chromebook's Linux CPU architecture. In the Linux
   Terminal, `uname -m` shows `x86_64` for Intel/AMD or `aarch64` for ARM64.
3. Move the DEB into **Linux files**, then use its **Install with Linux** action.
   If that action is unavailable, use the Linux installation command above.
4. Launch QuietPlay from **Linux apps**. Share the music folder with Linux
   before importing songs stored outside Linux files.

ChromeOS-specific audio, file access, window behavior and performance still
need testing on a physical Chromebook. Native Linux CI is not Chromebook
hardware verification. [Google's file-sharing guide](https://support.google.com/chromebook/answer/9093741).

## Feature Differences

| Feature | Windows | Experimental Mac / Linux |
| --- | --- | --- |
| Local music, playlists, lyrics, live EQ and real-audio visualizer | Available | Included in native build targets |
| In-app search and optional spotDL downloads | Bundled | Native bundled companion; provider availability can vary |
| Mini player and opacity | Available | Included; behavior depends on the window manager |
| Song/position restoration | Local | Local; waits for Play by default |
| Windows taskbar thumbnail buttons | Available | Windows-only; native media controls are listed below |
| System Now Playing / desktop media controls | Windows media integration | macOS Now Playing / Linux MPRIS adapters; headset delivery depends on the OS |
| In-app keyboard controls | Control shortcuts | Command on Mac; Control on Linux |
| OBS now-playing Browser Source | Local overlay | Local overlay; OBS integration needs platform testing |
| Separate OBS audio and dual output | Supported routing devices | Needs an OS-specific virtual device; no Windows drivers included |
| Embedded Windows WebView2 tools | Optional Windows runtime | Not available |
| Updates | Manual Beta installer | Manual native installer |

The native checks exercise packaged UI navigation at three sizes, settings,
empty-library actions, isolated saved data, FFmpeg decoding, live EQ calculations,
and downloader startup. They do not verify physical speakers, Bluetooth headsets,
OBS audio routing, or a real provider download on Mac/Linux. Read each release's
verification file for the actual packages and checks.

Starting with 1.54.1, each native package must also pass library search, playlist
creation/cancel, likes/dislikes, shuffle history, lyrics view, mini-player volume
and opacity, session checkpointing, file drops, settings, audio controls and
system-media command checks at all three window sizes. Native media registration
is checked too. Linux has a real session-bus roundtrip test for MPRIS metadata,
transport, seeking and volume. This is not a guarantee that a particular headset
or desktop delivers media keys. Chromebook host keys may not reach the Linux app.

## Shared Features and OS Exceptions

Every installer uses the same library, playlists, artist/album views, local mixes,
ratings, queue/history, playback speed, sleep timer, lyrics, artwork/genre
matching, live EQ, real-audio visualizer, themes, mini player, optional spotDL
downloads, backups and saved-session code. Metadata/provider services can still
fail or return ambiguous results on any OS; manual correction remains available.

Some integrations cannot be identical: Windows taskbar thumbnail buttons,
WebView2 and VB-CABLE are Windows-specific. Mac and Linux use native media
frameworks and their own audio-device configuration. OBS overlay support is
included, but virtual audio routing requires a suitable device on the relevant
OS. Automatic signed production updates remain disabled on all current Beta
packages. No native ChromeOS/Android app is included; Chromebook support uses
the Linux environment and inherits its window/audio limitations.

## Local Data

Each operating-system user has an independent local library and preferences.
No music or personal profiles are included in any installer.

| Platform | Standard saved-data location |
| --- | --- |
| Windows | `%APPDATA%/QuietPlay` |
| macOS | `~/Library/Application Support/QuietPlay` |
| Linux / Chromebook Linux | `$XDG_DATA_HOME/QuietPlay`, normally `~/.local/share/QuietPlay` |

Existing legacy Unix data folders are preserved rather than silently abandoned.
An installer does not move music between computers or turn a local library into
a public server. Back up important files before upgrading.
