# QuietPlay User Guide

[QuietPlay](README.md) | [FAQ](FAQ.md) | [Downloads](https://github.com/cooperwwwwww/QuietPlay-downloads/releases)

This guide is for **QuietPlay 2.2** on Windows. Sections marked in development
describe upcoming features, not the current download.

## Jump to a Topic

[Install and open](#install-and-open) · [Your data](#your-data-on-this-pc) ·
[Add music](#add-existing-music) · [Find and play](#find-and-play) ·
[Discover and radio](#discover-radio-and-autoplay) · [Your listening](#your-listening) ·
[Playlists](#playlists) · [Library care](#library-care) · [Lyrics](#lyrics) ·
[Search and download](#search-and-download-music) · [Audio and mini player](#audio-and-mini-player) ·
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

- **Home** shows your rotation, mixes made for you and your whole library.
  Filter by genre and sort by recently added, title, artist and more.
- **Search** (Ctrl+F or the search bar) finds songs, artists, albums and
  playlists, ranks the best matches first, ignores accents and punctuation,
  and shows similar spellings when nothing matches exactly.
- **Ctrl+K** opens quick play: type and press Enter to play a song or run a command.
- Right-click any song for Play next, Add to queue, Add to playlist, Song
  radio, Show lyrics, **Listening stats**, Edit song info and more.
- **Artists** and **Albums** sort by most played; Albums can show only full
  albums. Artist pages list your most played songs by that artist.
- **Recently played** has a Songs view and a **History** view of every play by
  day, showing what you finished and what you skipped.

## Discover, Radio and Autoplay

Everything here is calculated on your PC from what you play, finish and skip.

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

Paste a public Spotify playlist or album link in the search bar, then choose
**Download full playlist/album** and the destination playlist. Individual
tracks can fail; finished ones are kept.

Downloads use the bundled spotDL companion: Spotify provides the song details
and the audio is matched from other providers. It does not download protected
Spotify audio. Only save music you have permission to download. File format,
quality, provider, lyrics and artwork options are in Settings → Search &
Downloads, with more under **Show advanced**.

## Audio and Mini Player

- Bass, Mid and Treble sliders change sound live. Normalization and
  ReplayGain even out loudness. Speed changes keep pitch.
- **Settings → Audio** picks the output device and visualizer style.
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

### Update the Current 2.2.0 App

1. Open **Settings → Updates → Check for updates**.
2. If a newer version is available, choose **Official downloads**.
3. Download its Windows installer and run it over the existing installation.
   Do not uninstall QuietPlay first. Normal upgrades keep your music, playlists,
   likes, listening history and preferences.

### In Development: Update From Inside QuietPlay

This is **not included in the current 2.2.0 download**. The planned flow is an
in-app notification and an **Update now** button, followed by your approval.
QuietPlay will check the downloaded installer's published SHA-256 and size, then
start a quiet upgrade. Windows security prompts and blocks remain in effect.
Checking for updates alone will never start installation.

The first release with this updater requires a one-time manual install. The
updater will initially download the full installer, not a changed-files-only
patch. See the [changelog](CHANGELOG.md) to check whether a feature has shipped.

### Get Help

For problems, **Settings → Advanced → Diagnostics → Copy summary** copies a
summary without personal file paths. Then
[report a bug](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=bug_report.yml)
or [ask for help](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=help.yml).
