# QuietPlay User Guide

[QuietPlay](README.md) | [FAQ](FAQ.md) | [Downloads](https://github.com/cooperwwwwww/QuietPlay-downloads/releases)

This guide is for **QuietPlay 2.2.17** on Windows. Sections marked in development
describe upcoming features, not the current download.

## Jump to a Topic

[Install and open](#install-and-open) · [Your data](#your-data-on-this-pc) ·
[Add music](#add-existing-music) · [Find and play](#find-and-play) ·
[Discover and radio](#discover-radio-and-autoplay) · [Your listening](#your-listening) ·
[Playlists](#playlists) · [Library care](#library-care) · [Lyrics](#lyrics) ·
[Search and download](#search-and-download-music) · [Navidrome](#navidrome-add-on) · [Audio and mini player](#audio-and-mini-player) ·
[OBS](#obs) · [Settings](#settings) · [Shortcuts](#keyboard-shortcuts) · [Updates and help](#updates-and-help)

## Install and Open

1. Download `QuietPlay-<version>-Windows-Setup.exe` from the
   [Releases page](https://github.com/cooperwwwwww/QuietPlay-downloads/releases).
2. Open it and follow setup. If Windows shows **Windows protected your PC**,
   read the [warning guide](FAQ.md#windows-protected-your-pc) first.
3. Setup installs the Microsoft Edge WebView2 Runtime if your PC doesn't have it.
   VB-CABLE is optional and only for separate OBS audio.
4. Open **QuietPlay** from the desktop or Start menu.

Only one QuietPlay window runs at a time; opening it again brings it to the
front. Reopening restores the last song and position and waits for Play
(turn on **Start music automatically** in Settings → Playback to change that).

### If Windows Shows a Security Warning

For **Windows protected your PC**, inspect **More info** and check the official
installer filename. Only choose **Run anyway** if it is offered and you trust
that specific download. Choose **Don't run** if you are unsure. If Smart App
Control, antivirus or an administrator blocks it, stop and keep protections on.

[Open the illustrated Windows warning guide](FAQ.md#windows-protected-your-pc).


## Your Data on This PC

Your library, playlists, likes, listening history, lyrics and artwork caches
and settings are stored in `%APPDATA%\QuietPlay`. Upgrades keep them.

- **Settings → Library → Library data**: back up, restore, export or import
  your library, playlists and settings.
- **Settings → Library → Listening history**: see your stats, export, or clear history.
- QuietPlay never deletes your music files. Removing songs only removes them
  from the library; they are listed under **Removed songs** and can be restored.

## Add Existing Music

- Select **Add music** or **Add folder** at the bottom of the sidebar, or drag
  files and folders onto the window.
- **Watch the Music folder** (Settings → Library, on by default) adds new
  songs from your Music folder automatically.
- **Watch Downloads** can import new audio from Downloads into a playlist and
  move it into Music so it isn't lost when Downloads is cleaned.

Untagged files named like `Artist - Title.mp3` are read as artist and title.

## Find and Play

- **Home** starts with one **Made for you** box: **Your mixes** (local mixes
  you can play straight away), **New songs for you** and **Playlists for you**.
  Use the left/right arrows to scroll each row; rows remember where you were.
  The arrow at the right of the box header collapses it to one line.
  Click a recommended song to preview it, or use its download button. Open a
  recommended playlist to see every song, preview, download a song, or
  **Download & save** the full mix. **See all** opens Discover, and the refresh
  button fetches new picks. Recommendations stay loaded when you switch tabs.
- **Your songs** below the box lists your whole library with **Play** and
  **Shuffle**. Filter by genre and sort by recently added, title, artist and more.
- **Search** (Ctrl+F or the search bar) finds songs, artists, albums and
  playlists, ranks the best matches first, ignores accents and punctuation,
  and shows similar spellings when nothing matches exactly.
- **Click the search box** (from 2.2.17) to open a panel with mood chips,
  recent searches, quick picks and a **Paste link** button for Spotify
  playlist, album and song links. While you type, it offers shortcuts to a
  mood ("chill"), an artist, a playlist or a genre; press the shortcut or keep
  reading the full results below.
- **Search** in the sidebar opens a browse page: a **How are you feeling?** box,
  11 mood mixes, **Browse by genre** and quick picks (**Surprise me**, **Never
  played**, **Forgotten favorites**, **Most played**, **Recently added**).
- **Mood mixes** use your songs, picked with Deezer's editorial mood playlists
  and your listening, and suggest new songs to preview or download. Use
  **Save as playlist** to keep one. They work offline with saved mood data.
- Recommended playlists on Home and Discover have **Save & download**, which
  adds the playlist to your playlists and downloads every song into it.
- **Ctrl+K** opens quick play: type and press Enter to play a song or run a command.
- Right-click any song for Play next, Add to queue, Add to playlist, Song
  radio, Show lyrics, **Listening stats**, Edit song info and more.
- **Artists** and **Albums** sort by most played; Albums can show only full
  albums. Artist pages list your most played songs by that artist.
- **Recently played** has a Songs view and a **History** view of every play by
  day, showing what you finished and what you skipped.

## Discover, Radio and Autoplay

Your listening signals and rankings are calculated on your PC. Optional catalog
lookups supply songs and related artists for online recommendations.

- **Discover** has Made for you, a time-of-day mix, On repeat, Because you
  played…, Forgotten favorites, Deep cuts, New to you, Never skipped, Recently
  added, genre mixes and your top artist's essentials. Mixes refresh daily.
  Save any mix as a playlist.
- **Artists you might like** suggests songs by artists you don't have yet,
  picked from what listeners of your most-played artists also play (Deezer).
  Each card says which of your artists led to it.
- **New from your artists** shows songs by the artists you play most that
  aren't in your library. Point at a card to preview 30 seconds, download it,
  or dismiss it. Artist pages show popular songs you're missing too.
  (Settings → Search & Downloads → **Suggest new songs**.)
- **Song radio** and **Artist mix** start from songs you usually play together.
- **Autoplay** (Settings → Playback) keeps playing similar songs when a list ends.
- **Crossfade** (Settings → Playback) blends each song into the next over 3 to
  12 seconds. Songs shorter than three times the crossfade play in full.
- **Shuffle** plays recently heard songs last and avoids the same artist twice in a row.
- **Dislike** keeps a song out of shuffle, autoplay and mixes. **Often skipped**
  in Discover lists songs you keep skipping.

### Personalized Playlists

Available in QuietPlay **2.2.1 and later**; also on Home since **2.2.3**.

1. Open **Home → Made for you → Playlists for you**, or **Discover → Playlists picked for you**. QuietPlay ranks recommendations
   from your plays, completed listens, likes, recent listening, skips and
   dislikes, then combines them with related-artist catalog results.
2. Choose a playlist to see its complete list of **50–60 different songs**.
   Your discovery mix blends familiar and new artists; New horizons emphasizes
   new artists; More from your favorites finds songs you do not own yet.
   Because you play… mixes focus on an artist from your listening history.
3. Use **Preview** for a catalog sample, or **Download** for an individual song.
   Previews are samples, not full-length streaming.
4. Choose **Download & save N songs** to queue the whole playlist as one job.
   Completed downloads appear together in a new local playlist. Use the
   Downloads panel for progress or cancellation; downloaded songs play in full.
5. Choose **Show more** under the song shelves to reveal more recommendations,
   or **Refresh recommendations** to update the catalog pool.

Picks use artist variety, daily ordering and overlap checks. The app does not
repeat songs to reach the playlist length: a full playlist appears only when
at least 50 eligible recommendations are available. Results depend on your
listening history and catalog availability; counts can vary. Catalog results
normally refresh after six hours. Existing owned-song, dislike and dismissed
recommendation filters still apply. Turn off **Suggest new songs** in
Settings → Search & Downloads to disable online recommendations.

## Your Listening

**Your listening** in the sidebar shows listening time, plays, how many songs
you finish, your favorite hour, your streak, top songs, artists and genres,
minutes per day (or per week for a year), and plays by hour. Choose 7 days,
30 days, a year or all time.

For one song, right-click it and choose **Listening stats**: plays, time
listened, first and last play, plays by month, songs you often play it after,
and songs that go well with it.

## Playlists

- Create playlists with **New playlist** or by right-clicking songs.
- Drag songs to reorder, pin playlists to the sidebar, rename, describe,
  duplicate, export (M3U8 or JSON) and import.
- Removing songs from a playlist and deleting a playlist can be undone.
- **Tidy up** on the Playlists page finds copies of the same playlist, empty
  playlists and radios the previous version saved automatically. A backup is
  saved before anything is deleted.

## Library Care

Settings → Library:

- **Duplicate songs**: songs you have more than once (for example in Music and
  Downloads). QuietPlay suggests the best quality copy; plays, likes and
  playlist spots from the others move to it. Extra files stay on disk.
- **Missing songs**: songs whose file moved or was deleted. **Find in a folder**
  looks for them by file name, then by title and artist. Songs moved into your
  library again reconnect automatically.
- **Removed songs**: restore songs you removed.
- **Cover artwork** and **genre checks** fill in missing covers and genres
  online. Edit a song's details with **Edit song info**.
- **Genres by artist**: each artist gets one genre for all their songs, from
  MusicBrainz listener tags, Deezer and Apple Music. QuietPlay only trusts a
  catalog when it finds one of your songs there, so an artist with the same
  name can't change your genres. Settings → Library → **Review genres** shows
  every artist and how sure QuietPlay is; **Check these** lists the ones worth
  a look. Choose a genre to change all of an artist's songs; your choice is kept
  for songs you add later. A genre you set on a single song always wins.
- **Edit several songs at once**: select songs (Ctrl or Shift click), right-click
  and choose **Edit info for N songs**, or select **Edit genre…** on an artist
  page. Fill in only what should change; blank fields keep each song as it is.

## Lyrics

Lyrics appear in the Now Playing panel; **Open** shows the full view. Timed
lyrics follow the song. Use **Earlier/Later** if a song's lyrics are early or
late; each song remembers its own timing (Settings → Lyrics → **Reset all**).
Lyrics come from files saved beside the song, the song's tags, or LRCLIB
online. The next song's lyrics are fetched ahead of time.

## Search and Download Music

Online search is optional (Settings → Search & Downloads). Online results show
a **Download** button; downloads go to `Music\QuietPlay Downloads` and are added
to your library and, if you choose, a playlist. The download panel (cloud icon
at the top) shows progress and lets you cancel.

### Download a Complete Playlist or Album

Paste a public Spotify playlist or album link into the main search bar to
see the complete returned song list. Choose **Download all** to queue the full
collection, or **Download** beside one song. Collection links are not truncated
by the short text-search or metadata preview limits. Supported Spotify URIs
and short links work too.

For a specific local playlist destination, open the download panel using the
cloud icon at the top, paste the link and choose the destination playlist.
Individual tracks can fail; finished downloads are kept.

Downloads use the bundled spotDL companion: Spotify provides the song details
and the audio is matched from other providers. It does not download protected
Spotify audio. Only save music you have permission to download. File format,
quality, provider, lyrics and artwork options are in Settings → Search &
Downloads, with more under **Show advanced**.

### If a Download Fails

If a song cannot be downloaded from your chosen source, QuietPlay tries
YouTube Music, YouTube, SoundCloud and Bandcamp, then a broader search, before
reporting it as failed. When Spotify cannot provide song details, searches and
Spotify song links use Apple's public music catalogue instead.
Songs that already downloaded are not fetched again. Use **Retry** on a failed
song in the Downloads panel to try it again. Album and playlist links
still need Spotify; if it is unavailable, try again later or search by name.

## Navidrome Add-on

Play music from your own Navidrome (or other Subsonic-compatible) server. The
add-on is optional and off by default.

1. Tick **Navidrome music server support** during setup, or open
   **Settings → Advanced → Add-ons** and choose **Install**.
2. Open **Settings → Navidrome** (it appears once the add-on is installed), enter
   your server address, username and password, then choose **Connect**.
3. Open **Navidrome** in the sidebar to browse **Albums**, **Artists**,
   **Playlists** and **Search**. Right-click a song to queue, like or dislike it.

**Settings → Navidrome** has every add-on option:

- **Connection:** status and server version, **Test connection**, **Reconnect**,
  **Connect when QuietPlay starts**, **Reconnect automatically** and **Sign out**.
- **Library:** **Mix into my library** (on by default) shows server songs
  together with your own; **Check for new songs** (from never to once a day)
  and **Refresh songs now**.
- **Playback:** **Streaming quality** (original down to 96 kbps; your server
  needs FFmpeg to convert) and whether server songs can appear in mixes, radio
  and autoplay.
- **Listening:** switches for sending plays, what you are playing and likes to
  your server, and **Clear** for the listening history kept on this PC.
- **Storage:** clear the cover art cache. **Add-on:** turn it off without
  forgetting anything, or **Remove add-on** to forget the server.

When the server is unreachable or you sign out, its songs leave your library
without errors; with **Reconnect automatically** on they come back when the
server returns. Your listening history is kept for recommendations.

## Audio and Mini Player

- Bass, Mid and Treble sliders change sound live. Normalization and
  ReplayGain even out loudness. Speed changes keep pitch.
- **Settings → Audio** picks the output device and visualizer style.
  **Follow Windows (System default)** follows the device Windows is using as you connect and
  disconnect headphones or speakers, keeping your place. A specific device is
  used while it is connected; otherwise QuietPlay uses your PC's current device.
  The list updates by itself.
- The **mini player** (button at the bottom right) is a small always-on-top
  window with adjustable opacity.
- **Sleep timer** pauses after 15–90 minutes or at the end of the song.
- Media keys, headset buttons and the taskbar thumbnail buttons control
  playback. Repair them in Settings → Integrations if they stop responding.

## OBS

Settings → Streaming → **Set up OBS** connects to OBS on this PC (enable OBS
WebSocket in OBS first). It adds a **Browser Source** for the now-playing
overlay and an audio source for the music.

For separate music audio, choose a **Stream output** such as CABLE Input
(VB-CABLE) and capture CABLE Output in OBS. Turn on **Listen on this PC** to
hear the music too. Use **Test tone** to check routing. Avoid also capturing
the music through Desktop Audio, or it plays twice on stream.
[Optional driver guide](OPTIONAL_DRIVERS.md).

Showing a song title doesn't grant permission to broadcast the recording.

### Overlay Customization (Unreleased)

The following controls are implemented in the development build and are **not
in the current 2.2.17 installer**. The existing download still has the basic
overlay options in Streaming settings.

Open **Settings → Streaming → Overlay appearance** in the upcoming build:

- Choose background, accent, title, artist/album, progress and border colors
  with visual pickers. Use **Background opacity** for transparency.
- Let the progress bar and border follow the accent, or give each its own color.
- Pick Compact, Text or Banner; change artwork position, font, sizes, card
  width, canvas position and margin, corner rounding and border thickness.
- Choose which song details appear, including separate artist and album text,
  progress and elapsed/total time. Shadow, fades and hide-on-pause are optional.
- Start from Cyan, Glass or Text only, or reset just the overlay appearance.

Changes save automatically and appear in the live preview and the existing OBS
source without restarting OBS. Preview works locally, even with the overlay
server off, and shows a labeled sample if no song is selected. Small source
heights scale the complete card rather than cut off its text. Source dimensions
and local server repair controls remain under **Show advanced**.

Customizing the visual overlay does not change your audio routing or OBS scene.

## Settings

Settings has a search box. Categories: Playback, Audio, Library, Search &
Downloads, Lyrics, Appearance (themes, custom colors, motion), Streaming,
Integrations, Updates and Advanced (Gaming Mode, caches, diagnostics).

## Keyboard Shortcuts

| Keys | Action |
| --- | --- |
| Space | Play or pause |
| Ctrl+Left / Ctrl+Right | Previous / next song |
| Left / Right | Back or ahead 5 seconds |
| Ctrl+Up / Ctrl+Down | Volume |
| L | Like the playing song |
| Ctrl+K | Quick play |
| Ctrl+F | Search |
| Ctrl+J | Jump to the playing song |
| Ctrl+M | Mini player |
| Ctrl+O / Ctrl+Shift+O | Add files / add a folder |
| Alt+Left / Alt+Right | Back / forward |
| Ctrl+Shift+G | Gaming Mode |
| Ctrl+Alt+Space | Play or pause from any app |
| Ctrl+Alt+Left / Ctrl+Alt+Right | Previous / next song from any app |
| Ctrl+Alt+Up / Ctrl+Alt+Down | Volume from any app |

The Ctrl+Alt shortcuts work while another app or a game is in front. If another
app already owns one, QuietPlay uses a backup (Ctrl+Alt+P, Ctrl+Alt+N or
Ctrl+Alt+B) and Settings → Integrations → **Global shortcuts** shows which; turn
them off there too. Press **F1** to see every shortcut.

## Updates and Help

### Official File Updates (2.2.2 and Later)

1. Open **Settings → Updates → Check for updates**. QuietPlay also checks in
   the background and shows a notice when an official stable update is available.
2. Review the available version and changed-file download size.
3. Choose **Download changed files** (**Download update** from 2.2.4). You can
   cancel while downloading.
4. When verification finishes, choose **Update and restart** and approve.
   QuietPlay closes, updates its changed app files, checks startup and reopens.

The update replaces changed files, not the whole app installation. It may remove
obsolete files that belonged to the previous release. Unchanged runtime files
and your music, library, playlists, history and preferences stay in place.

The official release manifest is signed with QuietPlay's pinned release key.
The updater checks signatures, sizes and SHA-256 hashes, backs up changed files,
and restores the previous version if applying the update or startup verification
fails. It also recovers an interrupted update before normal startup continues.
Backups are retained for the two most recent update transactions.

The release signature is separate from Windows Authenticode; QuietPlay is still
not Windows code-signed, and Windows security warnings and blocks still apply.

### Updating to 2.2.17

Use the update screen above. From **2.2.16** the download is about **8.0 MB**,
from **2.2.7 to 2.2.15** about **23.2 MB**, and from **2.2.2, 2.2.3 or 2.2.4** about **40.2 MB**.
A bar shows the check, the download, verification and, in the updater window, each file as it is installed. It reuses the unchanged runtime
files, so no full installer is needed for a healthy installation.

### First Upgrade From an Older Version

- **2.2.0:** download the official **2.2.17 Windows Setup** and run it over the
  existing installation once. Do not uninstall first. This enables file updates.
- **2.2.1:** download **QuietPlayUpdater.exe** from the official **2.2.17 release**,
  run it, choose **Download changed files**, then **Update and restart**. This
  transfers about 40 MB instead of the full setup. Full setup is also available.

Future releases must publish a signed package matching your installed version.
If no matching package exists, or an app file is damaged or modified, the updater
stops and directs you to **Official downloads** for repair or a manual upgrade.
An offline PC can keep using the installed app and check again when connected.

### Get Help

For problems, **Settings → Advanced → Diagnostics → Copy summary** copies a
summary without personal file paths. Then
[report a bug](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=bug_report.yml)
or [ask for help](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=help.yml).


