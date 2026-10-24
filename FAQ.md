# QuietPlay FAQ

[QuietPlay](README.md) | [User guide](USER_GUIDE.md) | [Downloads](https://github.com/cooperwwwwww/QuietPlay-downloads/releases)

## Which Download Should I Choose?

Use **Download for Windows** on the main page. The file is named
`QuietPlay-<version>-Windows-Setup.exe` and installs the complete app. There is
no ZIP to extract and no developer setup.

QuietPlay 2.0 is Windows-only. For Mac, Linux and Chromebook, the experimental
1.54.1 Beta packages remain available; read the [platform guide](PLATFORMS.md).
Do not run Windows installers or VB-CABLE drivers on those systems.

GitHub may still display automatically generated "Source code" archives;
those contain this repository's public documentation, not an installable app.
Historical releases retain their original assets, but are not the current
recommended downloads.

## Why Is My Library Empty?

QuietPlay does not include a music collection. Use **Add music** or
**Add folder** for songs you already have, drag files onto the window, or use
the search bar for the optional in-app downloader. Only save recordings you have permission to download.
Added or automatically imported downloads appear in Home. Every Windows user
starts with an independent local library; the installer contains no songs or
personal listening data.

## Why Does Windows Block QuietPlay?

QuietPlay is **not code-signed yet**. Smart App Control can block an unsigned
program, and SmartScreen may warn about a new download. A published checksum
verifies file identity; it does not replace a trusted publisher signature. Do
not turn off Windows security. Code signing is planned.

## Windows Protected Your PC

This is usually a **Microsoft Defender SmartScreen** reputation warning.
QuietPlay 2.2.13 is not Windows code-signed. The warning is a reason to inspect
the file; it is not proof that the file is safe or malicious.

![Illustrated two-step Windows warning guide for the QuietPlay 2.2.13 installer](assets/windows-security-guide.svg)

### If You See More Info

1. Confirm you intentionally downloaded **QuietPlay-2.2.13-Windows-Setup.exe**
   from [the official 2.2.13 release](https://github.com/cooperwwwwww/QuietPlay-downloads/releases/tag/v2.2.13).
   Compare its SHA-256 with **SHA256SUMS.txt** on that release if you want to
   verify the file's identity. A checksum is not a safety guarantee.
2. Select **More info**, then check the app filename and publisher. This build
   may say **Unknown publisher** because Windows publisher signing is pending.
3. If you trust this specific file and accept the risk, choose **Run anyway**,
   if offered. Otherwise, choose **Don't run**. You make this decision yourself.

### If Windows Blocks It Outright

- **Run anyway is missing:** stop. Windows version or policy may prevent it.
- **Smart App Control:** stop. It has no individual-app override.
- **Malware or virus detected:** stop and let your security software handle it.
- **Blocked by your administrator:** ask the administrator who manages the PC.

Do not disable antivirus, SmartScreen, Smart App Control or administrator
protections to install QuietPlay. You can [report the exact wording](https://github.com/cooperwwwwww/QuietPlay-downloads/issues),
but remove private names, paths and account details from screenshots first.

The guide is an illustration, not a screenshot of your PC; wording varies.
[Microsoft explains SmartScreen](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation)
and [Smart App Control](https://support.microsoft.com/en-us/windows/security/threat-malware-protection/smart-app-control-frequently-asked-questions).

### Check the Downloaded File

Open that release's **SHA256SUMS.txt** and find the installer filename. In
Windows PowerShell, run the following with the actual path to the downloaded file:

```powershell
Get-FileHash -LiteralPath "<downloaded-installer-path>" -Algorithm SHA256
```

On Mac, use Terminal:

```sh
shasum -a 256 "<downloaded-installer-path>"
```

On Linux or a Chromebook's Linux Terminal:

```sh
sha256sum "<downloaded-installer-path>"
```

Replace the placeholder with the downloaded EXE, DMG or DEB path.
The displayed hash must match the installer entry in SHA256SUMS.txt, ignoring
letter case. A mismatch means the file is not the published installer: do not
run it. Matching verifies identity, not publisher trust or absence of malware.

## Is QuietPlay Still a Beta?

No. **QuietPlay 2.0 is the first official release.** Versions 1.x were Beta
prereleases; their release tags end in `-development`. The Mac and Linux
packages are still the experimental 1.54.1 Beta. "Official" means this is the
recommended, supported version, not that the installer is code-signed yet.

## Do I Need WebView2?

Yes. QuietPlay 2.0 draws its interface with the Microsoft Edge WebView2
Runtime, which comes with Windows 11 and most up-to-date Windows 10 PCs. If it
is missing, setup offers to install Microsoft's signed runtime.

## Do I Need an Account, and Where Is My Data Saved?

QuietPlay does not require an account. Each operating-system user has a local profile,
history, playlists and settings saved on that computer. Installing on another
computer creates an independent setup; it does not copy another listener's data.
Personal listening data is not uploaded to GitHub or a public library server.
Settings > Library contains the local display name, your stats, export and
history controls. See [local data](USER_GUIDE.md#your-data-on-this-pc).

## Do I Need Python, spotDL, or Extra Audio Drivers?

No separate Python or spotDL installation is required. The app runtime,
companion downloader, FFmpeg, and playback libraries are bundled.

Normal playback uses your existing system audio device. On Windows, VB-CABLE is optional
for sending a separate music output to OBS. It is third-party donationware,
with its own terms; installing a driver can require administrator approval and
a restart. QuietPlay does not install it silently. Mac/Linux use their native
audio backends; Windows drivers are not needed there. See [platform limits](PLATFORMS.md#feature-differences).

## Does QuietPlay Stream the Whole Spotify Catalog?

No. QuietPlay primarily plays your saved music. Optional spotDL integration
uses Spotify metadata to find matching audio from other providers. It does not
retrieve protected Spotify audio or guarantee every song. Only save recordings
you have permission to download.

## Can I Download a Whole Playlist?

Yes. In **2.2.1**, paste a public Spotify playlist or album link into the
main search bar to see every returned song, then choose **Download all**.
For a specific destination playlist, use the download panel (cloud icon at the
top). Individual tracks can fail; completed downloads are kept.
[Download guide](USER_GUIDE.md#download-a-complete-playlist-or-album).

Discover also offers full **50–60-song personalized playlists** when enough
matches are available, with **Download & save** for the whole playlist.
[Personalized playlist guide](USER_GUIDE.md#personalized-playlists).

## Why Is a Genre or Cover Still Missing or Incorrect?

Metadata providers do not cover every release. Remixes, slowed recordings,
collaborations, and similar titles can be ambiguous. Genre labels also vary
between sources. Review the matched recording before writing changes to a file;
manual correction is preferable to a confident but unsupported guess.

For a reproducible matching problem, use the bug form and provide the title,
credited artists, album if known, and expected metadata. Do not upload the song.

## Why Do Lyrics Run Early or Late?

The lyrics may belong to a different recording or edit. Use **Earlier/Later**
in the lyrics view for that song; each song keeps its own timing. Line-synchronized lyrics do not necessarily include
accurate timestamps for each individual word. Report persistent issues with
the song details and approximately where the timing drifts.

## How Do I Use QuietPlay With OBS?

Open Streaming settings for the guided OBS setup. A Browser Source displays
the local now-playing overlay; a separate audio output sends music to the
stream. These are different sources. Optional dual output lets you hear the
music on your PC too. See [OBS setup](USER_GUIDE.md#obs).

Showing a song title does not grant permission to broadcast the recording.

## Can I Customize the OBS Overlay?

The current release has basic overlay options in Streaming settings. A larger
appearance editor is implemented in development, **not in the 2.2.13 download**:
six color pickers, transparency, fonts, artwork placement and sizes, borders,
visible details, presets, reset and a live preview. It saves locally and does
not change the audio route or your OBS scene.
[Upcoming overlay controls](USER_GUIDE.md#overlay-customization-unreleased).

## How Are Mixes and Recommendations Made?

On your PC, from your own listening: what you play, finish, skip, like and
dislike, which songs you play one after another, and the time of day you
listen. Nothing about your listening is uploaded. Dislike a song, or review
**Often skipped** in Discover, to steer them.

Online recommendations send the names of your most-played artists to Deezer's
and Apple's public catalogs to find new songs and related artists. Ranking and
playlist building happen on your PC. Plays, completions, likes, recent listening,
skips and dislikes influence picks, with artist variety and daily ordering.
Turn online suggestions off in Settings > Search & Downloads > **Suggest new songs**.

## Will Updating Delete My Library?

QuietPlay keeps user data separate from installed app files. Normal upgrades
are intended to preserve the library and settings; back up important files
before an update. Removing a song from the library and deleting its original
audio file are different actions. Read confirmation dialogs carefully.

## How Do I Get Update News?

**2.2.2 and later:** open **Settings > Updates > Check for updates**. Background
checks also show a notice. Choose **Download changed files** (**Download update**
from 2.2.4), then **Update and
restart** and approve. The official updater downloads a matching changed-file
package, verifies its signed manifest and hashes, backs up the old files and
checks startup. Failed or interrupted updates restore the previous app.

**2.2.0** needs one manual 2.2.13 setup to gain this updater. **2.2.1** can instead
run `QuietPlayUpdater.exe` from the official 2.2.13 release to download about
40 MB of changed files. No uninstall is needed. New PCs and damaged or unsupported
installations can use the full setup. Windows security checks remain enabled.

[Full update guide](USER_GUIDE.md#updates-and-help).

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

## Why Is QuietPlay Playing on a Different Device?

Open **Settings → Audio** and set **Output** to **Follow Windows (System default)**. From 2.2.8,
QuietPlay then plays through whatever device Windows is using and follows it
when you connect or disconnect headphones, speakers or Bluetooth devices,
keeping your song and position. If you pick a specific device instead,
QuietPlay stays on it while it is connected and uses your PC's current device
while it is not. The device list updates on its own.

## What Happens If a Download Fails?

Since 2.2.7, QuietPlay tries again elsewhere. If a song cannot be downloaded from your
chosen source, it tries YouTube Music, YouTube, SoundCloud and Bandcamp, then a
broader search. Songs that already downloaded are not fetched again, and the
Downloads panel shows which source is being tried. A song is only reported as
failed when no source has it. From 2.2.9, a failed song has a **Retry** button.

If Spotify cannot provide song details (for example "Could not get client
token"), searches and Spotify song links use Apple's public music catalogue
instead. Album and playlist links still need Spotify; try again later or search
for the songs by name.

## Why Does a Song Have No Cover Art?

QuietPlay first uses artwork inside the file. When there is none, it looks the
song up on MusicBrainz, then Apple Music and Deezer (from 2.2.11), and only
accepts the same artist, song and, when known, album. Songs that are not in
those catalogues keep a placeholder. To check your whole library again, open
**Settings → Library → Missing artwork** and choose **Find covers**.

## Can QuietPlay Play Music From My Navidrome Server?

Yes, from 2.2.12, with the optional Navidrome add-on. It works with Navidrome
and other Subsonic-compatible servers. Tick **Navidrome music server support**
during setup, or open **Settings → Advanced → Add-ons** and choose **Install**.
Then open **Settings → Navidrome** and enter your server address (for example
`http://192.168.1.20:4533`), username and password.

- **Mix into my library** puts server songs alongside your own in Home,
  artists, albums, liked songs and search. Turn it off to keep them on the
  **Navidrome** page only.
- If the server goes offline or you sign out, its songs leave your library.
  QuietPlay checks every minute and brings them back when the server returns. Songs you listened to stay in your history, so
  recommendations keep what they learned.
- Plays, what you are playing and likes are sent to your server; each can be
  turned off in **Settings → Navidrome → Listening**. QuietPlay never saves your
  password; it keeps a sign-in token protected by Windows. **Remove add-on**
  forgets the server.
- **Streaming quality** (Settings → Navidrome → Playback) can lower the bitrate
  to save data. Your server needs FFmpeg to convert songs; without it, songs
  play at original quality.

## Can Home Recommend Downloads Too?

Yes. Since 2.2.4, Home has one **Made for you** box with your local mixes, new
songs and full 50–60-song recommended playlists, with your songs right below.
Click a recommended song to preview it, or use its download button. Open a
playlist to see all songs and download one song or download and save the full
mix. **See all** opens Discover. Recommendations stay loaded when you switch tabs.
