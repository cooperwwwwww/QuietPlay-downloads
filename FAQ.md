# QuietPlay FAQ

[QuietPlay](README.md) | [User guide](USER_GUIDE.md) | [Downloads](https://github.com/cooperwwwwww/QuietPlay-downloads/releases)

## Which Download Should I Choose?

Use **Download QuietPlay for Windows** on the main page. The Setup EXE installs
the complete app and offers optional extras in the installation wizard.
Current releases do not require ZIP extraction or a developer environment.

GitHub may still display automatically generated "Source code" archives;
those contain this repository's public documentation, not an installable app.
Historical releases retain their original assets, but are not the current
recommended downloads.

## Why Is My Library Empty?

QuietPlay does not include a music collection. On Home, use **Add files** or
**Add folder** for songs you already have, or **Search music** for the optional
in-app downloader. Only save recordings you have permission to download.
Added or automatically imported downloads appear in Home. Every Windows user
starts with an independent local library; the installer contains no songs or
personal listening data.

## Why Does Windows Block QuietPlay?

Current public packages are **unsigned Beta builds**. Smart App
Control can block an unsigned program. A published checksum verifies file
identity; it does not replace a trusted publisher signature. Do not turn off
Windows security. Trusted code signing is still outstanding.

## Windows Protected Your PC

The blue **Windows protected your PC** screen is a Microsoft Defender
SmartScreen warning. QuietPlay is a new, unsigned Beta app with limited download
reputation; that can trigger this warning. It does not prove the file is safe
or malicious. [Microsoft explains SmartScreen reputation](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation).

![Initial Microsoft Defender SmartScreen warning: select More info to inspect the app details](assets/windows-smartscreen.png)

1. Confirm you intentionally downloaded the installer from
   [QuietPlay's official releases](https://github.com/cooperwwwwww/QuietPlay-downloads/releases).
   Compare its SHA-256 with that release's SHA256SUMS.txt. This checks file
   identity, not safety.
2. Select **More info**, on the left of the pictured screen, to see the filename
   and publisher. The current unsigned
   QuietPlay installer may show **Unknown publisher**.
3. Only if you trust that specific file and accept the risk, choose
   **Run anyway**, if offered after More info. It is not visible in the initial
   screen above. If you are unsure, choose **Don't run**.

If **Smart App Control**, a malware detection, or your administrator's policy
blocks it, or Run anyway is unavailable, stop. Do not disable antivirus,
SmartScreen, Smart App Control or administrator protections. Smart App Control
does not provide an individual-app override.
[Microsoft's Smart App Control FAQ](https://support.microsoft.com/en-us/windows/security/threat-malware-protection/smart-app-control-frequently-asked-questions).

### Check the Downloaded File

Open that release's **SHA256SUMS.txt** and find the installer filename. In
PowerShell, run the following with the actual path to the downloaded file:

```powershell
Get-FileHash -LiteralPath "<downloaded-installer-path>" -Algorithm SHA256
```

The displayed hash must match the installer entry in SHA256SUMS.txt, ignoring
letter case. A mismatch means the file is not the published installer: do not
run it. Matching verifies identity, not publisher trust or absence of malware.

## Why Is It Labeled Beta?

QuietPlay Beta is the ready-to-use listener app, not a developer kit. Beta means
it is a prerelease and may still have bugs. The installer is named
`QuietPlay-<version>-Beta-Setup.exe`. Internal release tags and verification files
may still use `development` to keep the existing unsigned-release safeguards;
that does not mean you need development tools to use the app.

## Do I Need an Account, and Where Is My Data Saved?

QuietPlay does not require an account. Each Windows user has a local profile,
history, playlists and settings saved on that computer. Installing on another
computer creates an independent setup; it does not copy another listener's data.
Personal listening data is not uploaded to GitHub or a public library server.
Settings > Library contains the local display name, insights, export and
history controls. See [local data](USER_GUIDE.md#your-data-on-this-pc).

## Do I Need Python, spotDL, or Extra Audio Drivers?

No separate Python or spotDL installation is required. The app runtime,
companion downloader, FFmpeg, and playback libraries are bundled.

Normal playback uses your existing Windows audio device. VB-CABLE is optional
for sending a separate music output to OBS. It is third-party donationware,
with its own terms; installing a driver can require administrator approval and
a restart. QuietPlay does not install it silently.

## Does QuietPlay Stream the Whole Spotify Catalog?

No. QuietPlay primarily plays your saved music. Optional spotDL integration
uses Spotify metadata to find matching audio from other providers. It does not
retrieve protected Spotify audio or guarantee every song. Only save recordings
you have permission to download.

## Can I Download a Whole Playlist?

Paste a public Spotify playlist or album link into the main search bar and
request an online search, then choose **Download full playlist/album**. In Add
music, choose Home, an existing playlist, or a new playlist as the destination.
Search preview limits do not limit full collection jobs. Unavailable tracks
can fail individually; completed tracks remain available.

## Why Is a Genre or Cover Still Missing or Incorrect?

Metadata providers do not cover every release. Remixes, slowed recordings,
collaborations, and similar titles can be ambiguous. Genre labels also vary
between sources. Review the matched recording before writing changes to a file;
manual correction is preferable to a confident but unsupported guess.

For a reproducible matching problem, use the bug form and provide the title,
credited artists, album if known, and expected metadata. Do not upload the song.

## Why Do Lyrics Run Early or Late?

The lyrics may belong to a different recording or edit. Use the in-app timing
adjustment for that song. Line-synchronized lyrics do not necessarily include
accurate timestamps for each individual word. Report persistent issues with
the song details and approximately where the timing drifts.

## How Do I Use QuietPlay With OBS?

Open Streaming settings for the guided OBS setup. A Browser Source displays
the local now-playing overlay; a separate audio output sends music to the
stream. These are different sources. Optional dual output lets you hear the
music on your PC too. See [OBS setup](USER_GUIDE.md#obs).

Showing a song title does not grant permission to broadcast the recording.

## Will Updating Delete My Library?

QuietPlay keeps user data separate from installed app files. Normal upgrades
are intended to preserve the library and settings; back up important files
before an update. Removing a song from the library and deleting its original
audio file are different actions. Read confirmation dialogs carefully.

## How Do I Get Update News?

Check the [Releases page](https://github.com/cooperwwwwww/QuietPlay-downloads/releases)
and [changelog](CHANGELOG.md). GitHub's Watch menu can subscribe to release
notifications. Automatic in-app production updates remain disabled until
trusted signing requirements are met; a new GitHub release is not a forced
installation on your PC.

## Can Other People Change the App or See My Music Here?

No public visitor has write access to this repository. People can submit issues
and comment on requests, but that does not grant access to the private source,
your local files, or anyone's music library. Issues themselves are public, so
remove sensitive information before posting.

## Where Do I Request Something or Get Help?

- [Request a feature](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=feature_request.yml)
- [Report a bug](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=bug_report.yml)
- [Ask a setup question](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=help.yml)

GitHub requires an account to submit an issue. QuietPlay itself does not require
an account. Response times and implementation dates are not guaranteed.
