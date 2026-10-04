# QuietPlay User Guide

[Back to QuietPlay](README.md) | [Downloads](https://github.com/cooperwwwwww/QuietPlay-downloads/releases) | [FAQ](FAQ.md)

## Jump to a Topic

[Install](#install-and-open) | [Add music](#add-existing-music) |
[Playlists](#playlists) | [Full collection downloads](#download-a-complete-playlist-or-album) |
[Shuffle history](#shuffle-and-previous) | [Local data](#your-data-on-this-pc) | [OBS](#obs)

Still stuck? [Ask a setup question](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=help.yml).

## Install and Open

1. Use **Download for Windows** on the main page. Download the Setup EXE, not
   GitHub's automatically generated source-code archives.
2. Run setup. Optional extras are unchecked by default: VB-CABLE is only for
   separate OBS audio; WebView2 is only for embedded web tools. Selecting the
   driver opens its original setup and administrator prompt. See the
   [optional extras guide](OPTIONAL_DRIVERS.md).
3. Use the QuietPlay desktop or Start menu shortcut.
4. Check Settings > Updates for the version and build channel.

If Windows Smart App Control blocks an unsigned build, stop there. A checksum
confirms file identity, not trusted publisher status. Do not disable Smart App
Control or other protections to bypass the block.

The download is a complete end-user app, not a development kit. The runtime,
FFmpeg, playback libraries and optional downloader are included. No separate
Python, terminal commands or developer tools are needed.

## Your Data on This PC

There are no QuietPlay accounts, passwords, sign-in or account switching.
Each PC/Windows user keeps its own library, playlists, preferences, session and
listening data. Installing an update preserves that local data. Sending the
installer to a friend does not send your personal data.

Settings > Library > **Your data on this PC** lets you change a local display
name, view listening insights, export those insights as JSON, or clear that
listening history. Clearing insights does not remove music, playlists or the
library's Recently played list. Library backup/restore also includes the local
profile, so keep exported backups private.

When upgrading from the old Profiles section, QuietPlay retains the selected
profile's name and history and removes switching/passcodes. The complete old
file is preserved in a local migration backup; other profiles are not merged
into the selected history. Nothing from that migration is uploaded.

Local data is in **%APPDATA%/QuietPlay/Data-v1**, separate from the installed app
folder. Copying an installed app folder does not copy this personal data.

## Add Existing Music

On an empty Home library, choose **Add files** or **Add folder**. **Search music**
opens the optional downloader inside QuietPlay. No songs are included with the
app. The sidebar's Add music also opens the integrated import/download panel.

Choose files can select several songs; Choose folder imports a folder.
Importing registers the files in the library; it is not a guarantee
that copies are made in a new location. Avoid moving original files behind the
app's back. Rescan or relink moved files if a song becomes unavailable.

Downloaded songs are saved in Music / QuietPlay Downloads by default. Change
that destination in Search & Downloads before starting new downloads.

## Search, Play, and Browse

Use the top search bar for song titles, artists, and albums. Clearing search
restores the unfiltered library. Click a local song's Play action to listen.

Artists and Albums group saved songs by their metadata. Multi-artist songs can
appear in more than one artist view. Unknown Album is kept when no reliable
album information is available.

Use Back and Forward beside search to navigate pages. They are different from
the Previous and Next playback controls at the bottom of the app.

## Playlists

Create a playlist in Playlists, then select tracks and add the selection to it.
The playlist picker and creation screens have a way back; cancelling should not
change the library. Existing songs can belong to multiple playlists without
requiring extra copies of their audio files.

Song/artist Radio actions create mixes from your saved music. They are not an
unlimited licensed online catalog and are separate from any public radio stream.

For downloading into a playlist, Add music has an Add to menu. Pick an existing
playlist, or New playlist and enter a name. All successfully saved tracks from
that job go to the selected playlist and Home. An unavailable track is reported
without discarding the tracks that succeeded.

## Shuffle and Previous

Previous returns to the song actually heard before the current song, even with
shuffle enabled. If the current song has played for more than four seconds,
Previous restarts it first. Press Previous again near its start to go back.

Next after going back replays the forward listening history before choosing a
new shuffled song. Deleted or unavailable files are skipped. The recent-history
page is a browsing view, not the transport's chronological history trail.

## Reopen Where You Left Off

Playback settings include session restoration. By default, reopening restores
the song, position, shuffle state, queue/context, and supported current page,
but waits for you to press Play. Automatic audio resumption is a separate option.

Do not expect an in-progress download job to survive closing the app. Completed
files remain; retry the song or public playlist link after reopening.

## Online Search

Online search is optional and uses the main search bar, not a separate browser.
The default is local-first: if saved music matches, it stays a local search. Use
the online-search icon beside the bar to request an online search directly.

Online-only songs show Download to listen. Downloading adds a file; it does not
interrupt the song already playing. When ready, the file can be played from Home.

### Search Settings

| Setting | What it changes |
| --- | --- |
| Include online music | Enables online searches. Does not affect offline saved music. |
| When nothing is saved | Automatically searches online only when local results are empty. |
| Every search | Includes online results even when local results exist. |
| Only on request | Searches online only when you use the online-search action. |
| Wait after typing | Avoids repeated network requests while you type. Balanced is a short pause. |
| Results per search | Number of preview results, not the number downloaded from a full playlist. |

## Download a Complete Playlist or Album

1. Copy a public Spotify playlist or album link.
2. Paste it in the main search bar and request an online search.
3. Choose Download full playlist or Download full album.
4. In Add music, choose the file format and destination playlist.
5. Press Download. The entire collection is resolved, not only the preview rows.

You can also paste the link straight into Add music. Song links, artist links,
Spotify URIs, and supported Spotify short links are accepted there. Private
playlists or removed/unavailable recordings may not work without access; this
integration does not use your personal account cookies to bypass restrictions.

The queue shows saved counts and errors. Cancel stops remaining work and keeps
finished files. Retry keeps already matching files rather than overwriting them.
Existing output files are not deleted as part of download synchronization.

## Download Defaults

MP3 is the most broadly compatible format. Opus is efficient, while M4A, OGG,
FLAC, and WAV are also available. FLAC/WAV conversion does not turn lossy internet
audio into genuine lossless source audio.

Match source (auto) uses a bitrate appropriate to the source. Choosing a higher
encoding bitrate may make a larger file without improving its detail.

Spotify provides recording information. Audio is matched on the selected audio
provider. YouTube + Music tries both providers in order; results and availability
depend on the provider and recording.

Include lyrics saves available text and timed lyrics. Embed album artwork stores
the selected recording's cover when provided. Add downloads to Home controls
automatic import; choosing a destination playlist explicitly imports that job
into Home and the playlist even if automatic import is otherwise off.

### Advanced Options

Show advanced exposes filename layout, ASCII-safe filenames, artist tag
separators, lyric providers, explicit-content filtering, network limits, and
audio matching rules. They are not needed for ordinary use.

Use Lightest download performance while gaming. Higher concurrency uses more
network, CPU, and disk resources. Verified matches only may exclude songs that
have a valid audio match but no provider verification badge.

Reset defaults changes preferences, not downloaded songs or existing playlists.
Preferences are snapshotted when a job is queued, so later changes apply to new
jobs rather than modifying a running job halfway through.

Only download recordings you have permission to save. spotDL does not supply
Spotify's protected audio or guarantee the same recording for every title.

## Genres and Covers

Library settings contain metadata repair controls. Automatic lookups prioritize
new tracks and missing information, use cached public music data, and avoid
blocking playback or the UI while waiting for the network.

Check artist/title/album information if a match is wrong. Remasters, covers,
slowed versions, collaborations, and compilations may have different metadata.
Review a reliable match before writing tags to files. A missing or ambiguous
genre is preferable to a fabricated confident label. Some formats do not support
all tag fields, and read-only files cannot be updated.

Online artwork lookup searches for the identified recording's cover. A generic
fallback image is not the original album cover. Online sources may be incomplete
or unavailable, so not every unknown recording can be matched automatically.

## Lyrics

Open Show lyrics to view the current song. Timed lyrics follow the playback
position; plain lyrics do not have real timing. Earlier/Later changes a per-song
offset, and Resume follow returns to automatic line following after manual
scrolling. Different recordings may need different offsets.

If the words are consistently early or late, adjust the offset. If timing varies
throughout the song, the source may be for a different recording or may only have
line-level timing. Highlighting cannot create accurate word timestamps that the
source does not contain.

## Mini Player and Audio

Use Mini player at the top to open the compact always-on-top player. It has song
information, transport controls, volume, and opacity preferences. Close it to
return to the main window; it does not create a separate playback session.

Bass, Mid, and Treble in the bottom bar update live. Very large boosts need
headroom to avoid clipping, and can sound worse than moderate EQ. Flat EQ is a
useful baseline when comparing recordings. EQ or transcoding cannot repair a
poor original recording.

The visualizer reacts to PCM audio from the playback engine. Appearance/audio
settings control its layout, colors, density, sensitivity, and response. Reduced
motion lowers decorative animation without replacing the real audio analysis.

## OBS

The Streaming settings setup flow connects to OBS on this PC. OBS WebSocket must
be enabled in OBS; enter the matching local connection details when requested.
The setup flow changes the current OBS scene only after its final Add action.

For a song-information overlay, add the localhost URL displayed by QuietPlay as
an OBS Browser Source. It displays the current title/artist; it does not capture
the sound by itself.

For separate music audio, choose a stream-output device and add its corresponding
recording device to OBS. With VB-CABLE, QuietPlay sends to CABLE Input and OBS
captures CABLE Output. These names describe opposite ends of the same cable.
Enable Listen on this PC too if you want dual output to headphones and OBS.

The optional virtual driver is not needed for ordinary playback. Install it only
when you need separate routing. Avoid also capturing the same audio through
Desktop Audio, or the stream may hear music twice. Restart audio applications
after driver installation if their device lists have not refreshed.

Song credits and overlays do not grant broadcast rights. Ensure you have the
permission required for the music and streaming platform.

## Updates, Problems, and Privacy

Versioned packages and release notes live on this repository's Releases page.
Unsigned testing builds are prereleases. Signed in-app updates require a trusted
publisher certificate and signed update metadata; those checks are not bypassed
for convenience.

When reporting an issue, include the QuietPlay version/build, Windows version,
what you clicked, and what happened. For search/download errors, include a public
song link when appropriate. Do not post passwords, OBS credentials, private
music, private playlist URLs, or unreviewed diagnostic logs in public issues.

Your music is not automatically uploaded to a shared public server. Online
services receive search terms or recording details when used. Third-party
provider policies and availability still apply.
