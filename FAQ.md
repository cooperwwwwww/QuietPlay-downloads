# QuietPlay FAQ

[QuietPlay](README.md) | [User guide](USER_GUIDE.md) | [Downloads](https://github.com/cooperwwwwww/QuietPlay-downloads/releases)

## Which Download Should I Choose?

Use the **Windows installer** for a normal installation. To send QuietPlay to a
friend, use the **Installer + optional drivers ZIP**. It includes the same
installer plus setup notes and optional prerequisite packages. Extract it first.

The **Portable ZIP** is a complete app folder for running without a normal
installation. Keep its `_internal` directory next to the EXE. Downloading only
GitHub's automatically generated "Source code" ZIP does not install the app:
that archive contains this repository's public documentation, not QuietPlay.

## Why Does Windows Block QuietPlay?

Current public packages are **unsigned development/testing builds**. Smart App
Control can block an unsigned program. A published checksum verifies file
identity; it does not replace a trusted publisher signature. Do not turn off
Windows security or bypass a block. Trusted code signing is still outstanding.

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
