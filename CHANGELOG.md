# QuietPlay Changes

## Unreleased - OBS Customization

These features are not included in 2.2.12.

### OBS Overlay Appearance

- Six visual pickers for background, accent, title, artist/album, progress and
  border colors, plus background opacity and independent border opacity.
- Font styles, title and artwork sizes, left/right artwork, canvas position,
  card width, margin, corner rounding and progress thickness.
- Separate visibility for artwork, label, title, artist, album, progress and
  elapsed/total time; optional shadow, fades and hide-on-pause.
- Cyan, glass and text-only presets, an appearance-only reset, and automatic
  saving that does not restart OBS or change audio routing.
- A sandboxed preview using the actual OBS renderer, even when the overlay
  server is off. Small browser sources scale the complete card instead of
  clipping its text. Existing saved colors and visibility choices are preserved.

## 2.2.12 - Navidrome Add-on

Released October 23, 2026 for Windows 10/11 (64-bit).

- New optional Navidrome add-on for Navidrome and other Subsonic-compatible
  servers: an unchecked setup option, and **Settings → Advanced → Add-ons** to
  install, turn on or off, connect, sign out or remove it later.
- Server songs can be mixed into the library or kept on a separate Navidrome
  page with albums, artists, playlists and search. They stream through the
  normal player, with cover art, likes (starred on the server) and play
  reporting (scrobbles).
- Disconnecting or a server going offline removes server songs from the
  library without errors; listening history is kept locally so recommendations
  keep learning from it, and unreachable songs are not suggested.
- Uses Subsonic token sign-in; the password is not stored and the token is
  protected with Windows data protection.
- Signed changed-file packages support direct upgrades from 2.2.1 to 2.2.4,
  2.2.7 to 2.2.9, and 2.2.11.

## 2.2.11 - More Cover Art

Released October 23, 2026 for Windows 10/11 (64-bit).

- When MusicBrainz is unavailable or finds nothing, cover art lookup falls back
  to Apple Music, then Deezer. It accepts only the same lead artist and song
  (ignoring featured artists and bracketed notes), skips live and remix
  versions unless requested, requires the same album when one is known, and
  downloads images only from Apple's and Deezer's image servers.
- Downloads saved without album details (named after the song) are matched by
  artist and song alone.
- Song titles no longer show the downloader's "[qp-…]" file tag when a song was
  added to the library while it was still downloading. Files are not changed.
- Signed changed-file packages support direct upgrades from 2.2.1 to 2.2.4 and
  2.2.7 to 2.2.9. Version 2.2.10 was not published; 2.2.11 includes its changes.

## 2.2.9 - Small Things Made Easier

Released October 23, 2026 for Windows 10/11 (64-bit).

- Failed song downloads have a **Retry** button in the Downloads panel; it reuses
  the same playlist and skips songs already saved. Recommended playlists reopen
  from Discover instead.
- The Made for you box on Home can be collapsed to one line; the choice is
  remembered.
- Settings → Audio shows "Follow Windows (System default)" and explains what the
  selected output does, instead of naming the audio engine.
- Signed changed-file packages support direct upgrades from 2.2.1 to 2.2.4, 2.2.7
  and 2.2.8 (about 7.9 MB from 2.2.7 or 2.2.8).

## 2.2.8 - Plays Where Your PC Plays

Released October 21, 2026 for Windows 10/11 (64-bit).

- With Output set to System default, playback follows the device Windows is
  using. Connecting or disconnecting headphones, speakers or Bluetooth devices
  moves playback within about two seconds, keeping the song, position and
  play/pause state, with a short "Now playing on" notice.
- If a chosen output device is not connected, QuietPlay plays through the PC's
  current device instead of failing, and returns to the chosen device when it
  reconnects. Separate stream outputs are not redirected.
- The output device list in Settings updates automatically when devices change.
- Signed changed-file packages support direct upgrades from 2.2.1 to 2.2.4 and
  from 2.2.7 (about 7.8 MB).

## 2.2.7 - Downloads That Keep Trying

Released October 21, 2026 for Windows 10/11 (64-bit).

- If a song cannot be downloaded from your chosen source, QuietPlay tries
  YouTube Music, YouTube, SoundCloud and Bandcamp, then a broader YouTube
  search, before reporting it. Songs already saved are not fetched again, and the
  Downloads panel shows which source is being tried.
- Fixed the YouTube Music source, which could not start in the packaged app.
- When Spotify cannot provide song details, searches and Spotify song links use
  Apple's public music catalogue. "Artist - Title" searches only use an exact
  match and otherwise keep your words; free-text searches prefer the original
  recording by the artist you named over covers and remixes. Album and playlist
  links still need Spotify and now say so clearly.
- Signed changed-file packages support direct upgrades from 2.2.1 to 2.2.4
  (about 24.8 MB from 2.2.4).

## 2.2.4 - Made for You

Released October 20, 2026 for Windows 10/11 (64-bit).

- Home has one **Made for you** box with your local mixes, new songs and full
  50–60-song recommended playlists. In your rotation is removed so your songs
  sit right below, with Play and Shuffle in their usual place.
- Recommendations stay loaded when you switch tabs and refresh on their own only
  after 30 minutes or when you press refresh. Rows remember their scroll
  position; queued and dismissed songs keep their state.
- Click a recommended song to preview it. Discover playlist cards are tidier.
- Fixed recommended playlist downloads failing with "Could not get client token".
  Playlists use the song details QuietPlay already has instead of looking each
  song up again, keep their order, and continue past a song that cannot be found.
  Missing song codes no longer leave downloaded files without tags.
- Redesigned Downloads panel (active and finished downloads, counts, progress),
  Update center (one status and one main action) and official updater window.
- Signed changed-file packages support direct upgrades from 2.2.1, 2.2.2 and
  2.2.3 (about 40 MB).

## 2.2.3 - Home Recommendations

Released October 20, 2026 for Windows 10/11 (64-bit).

- Home keeps local rotation, Made for you mixes and library, and adds compact,
  always-visible song and playlist recommendations between the mixes and library.
- Songs combine fresh discoveries and familiar artists using Discover's ranking.
  Playlist details retain every one of their 50–60 songs and full-list download
  and save. See all recommendations opens Discover; Home also has Refresh.
- Left/right arrows, smooth scrolling and hover animations on local and online
  shelves. Keyboard scrolling and reduced-motion support are included.
- Loading, disabled recommendations, refresh errors and sparse history are handled
  without repeating songs to pad playlists.
- Signed changed-file packages support direct upgrades from 2.2.1 and 2.2.2.
  The 2.2.2 package is about 7.9 MB; the official updater is reused unchanged.

## 2.2.2 - Official Changed-File Updater

Released October 19, 2026 for Windows 10/11 (64-bit).

- Official stable-release checks in the background; downloads and installation
  require user action in the existing update screen.
- Differential ZIP packages contain changed app files for each supported source
  version. The 2.2.1 → 2.2.2 package is about 23 MB; unchanged runtime files are reused.
- A pinned Ed25519 release key verifies the manifest. Package size, SHA-256 and
  individual file hashes are checked before installation and checked again at apply.
- Safe paths, expected-file lists, original file checks, duplicate-job guards,
  cancellable downloads and a separate updater process protect the update flow.
- Changed files are backed up. Startup verification runs before committing;
  failures and interrupted transactions restore the previous app files.
- The standalone official updater can move 2.2.1 to 2.2.2. Version 2.2.0 needs
  one manual 2.2.2 setup to gain the new updater.
- User music, library, playlists, history and settings are not update targets.
- Release signatures are separate from Windows Authenticode. Windows security
  checks remain enabled; Windows publisher signing is still pending.

## 2.2.1 - Full Playlists and More Discovery

Released October 19, 2026 for Windows 10/11 (64-bit).

### Personalized Discovery

- A larger recommendation pool combines songs by related artists with music
  from the artists you already play most. Ranking uses the local taste model:
  completed plays, likes and recent listening help; skips and dislikes reduce
  affinity. Existing owned-song and dismissed-suggestion filters remain.
- Full playlists contain **50–60 different songs** when enough matches are
  available: Your discovery mix, New horizons, More from your favorites,
  Because you play… and The next chapter.
- Daily variation, artist-diversity penalties and an overlap check keep the
  playlists varied. Sparse results are not padded with repeated songs.
- Every playlist opens its complete song list, with catalog previews and
  **Download & save**. A whole playlist uses one cancellable download job and
  completed songs are added to a new local playlist.
- **Show more** reveals further song recommendations. **Refresh recommendations**
  updates the candidate pool; normal catalog results are cached for six hours.

### Playlist Downloads

- Spotify playlist and album links show their complete returned song list
  in search, including supported Spotify URIs and short links.
- **Download all** queues the full collection. Collection results are no longer
  truncated by the song-search or metadata preview limits.
- Individual downloads share their queued state with the collection action.
  Duplicate submissions are guarded, and failed requests can be retried.
- The existing download panel still supports choosing a destination playlist.

### Packaging and Version Labels

- App, setup and download links consistently identify version 2.2.1.
- Installer upgrades the existing app and keeps user data outside the app folder.
- Optional VB-CABLE driver is supplied as an archive; normal playback needs no driver.

## 2.2.0 - Genres by Artist and Real Recommendations

- One genre per artist from MusicBrainz listener tags, Deezer and Apple Music,
  confirmed through your own songs so namesakes can't change it.
- Genres are written into the song files' own tags (can be turned off).
- The old per-song genre guessing is removed; every artist is checked again.
- Artists only labeled Rock/Pop/Alternative by stores take the genre of their
  similar artists in your library.
- Review genres screen: every artist, how sure QuietPlay is, and a one-click
  change for all of an artist's songs.
- Artists you might like: suggestions from what listeners of your most-played
  artists also play.
- Lyrics preview always matches the playing song and line.
- Ctrl+K quick play focus, focus return after dialogs, settings search
  highlights, and a safe message when a screen fails to draw.

## 2.1.0 - Crossfade and Global Shortcuts

- Crossfade between songs (3 to 12 seconds, off by default).
- Ctrl+Alt global shortcuts for play/pause, next/previous and volume from any app.
- Edit genre, album or artist for several songs at once, including all songs by
  an artist; genre fields suggest existing genres.
- Reopening goes back to the page you were on instead of lyrics or search.
- Discover shows whole rows of mixes with Show all.
- Songs with no artist get one when their title includes a known artist.
- The genre fill keeps going through catalog rate limits.

## 2.0.0 - First Official Release

- Completely redesigned app with a black, white and grey interface, a Now
  Playing panel with lyrics and visualizer, and themes including custom colors.
- Discover mixes, song radio, artist mixes, autoplay and smart shuffle built
  from your own listening history on your PC.
- New from your artists: songs you don't have by your most-played artists, with
  30-second previews and download. Artist pages show popular missing songs.
- Your listening stats page, per-song listening stats and a full play History.
- Duplicate songs merge, automatic reconnection of moved songs, missing-song
  repair and Tidy up playlists (with backup and undo).
- Faster search that ignores accents and punctuation, ranks results and
  tolerates typos. Album sorting and a full-albums filter.
- Per-song lyric timing with reset, full lyrics view for any song.
- Update check against the official downloads page. Windows-only; the 1.54.1
  Beta packages remain available for Mac and Linux.
- Not yet code-signed; SmartScreen may warn. Your data carries over from 1.x.

## 1.54.1 - Cross-Platform Feature Checks

- Native macOS Now Playing and Linux MPRIS adapters expose playback metadata,
  play/pause, next/previous and seeking without touching Tk from system callbacks.
- Linux desktop controls also route volume, shuffle, repeat and speed changes
  through the actual player, not a separate playback implementation.
- Repeated system Play/Pause requests are idempotent and stale queued seeks
  cannot affect the next song. Native adapters unregister during shutdown.
- Mac mini-player Return-to-app shortcut supports Command+Return.
- Packaged native checks now exercise 11 shared feature workflows at all three
  supported sizes, including search, playlists/cancel, ratings, lyrics, mini-player
  volume/opacity, session checkpointing, file drops, settings and shuffle history.
- Publication rejects native packages that lack those workflow checks or fail
  native system-media registration. Headsets, OS media-key delivery, hardware
  audio, provider downloads and physical Chromebook behavior still need testing.
- Frozen validation uses explicit checks that remain active in optimized builds.

## 1.54.0 - Cross-Platform Beta

- Added native Mac and Linux build targets, with separate Intel/AMD and ARM64
  packages gated by native runner checks. Availability is listed on the release.
- Chromebook installation uses a compatible ChromeOS Linux environment, not
  an Android app or Chrome extension; physical Chromebook checks remain pending.
- Native CoreAudio on Mac and PulseAudio/ALSA on Linux replace Windows-only
  backend selection. Existing Windows WASAPI behavior is preserved.
- Local data uses the operating system's standard user-data directory, while
  preserving existing legacy Unix data. No accounts or personal data are bundled.
- Native file opening, Trash removal, file drops, single-instance activation
  and downloader cancellation now have platform-specific implementations.
- Mac Command shortcuts, manual native update links and platform-appropriate
  settings replace unavailable Windows integrations.
- Private native builders receive source-only snapshots, not music, profiles,
  credentials or workspace history. Public downloads remain installer-only.
- Added platform installation instructions, feature differences and explicit
  unsigned/notarized and hardware-testing limitations.

## 1.53.4 - Beta

- Listener-facing downloads, installer windows and app versions use QuietPlay
  Beta branding instead of development/testing wording.
- The Windows installer filename uses Beta, with optional driver choices retained.
- Added clear SmartScreen guidance and separate instructions for Smart App
  Control or administrator-policy blocks, without disabling Windows security.
- No developer environment is needed. Signing warnings remain clear; internal
  development-channel safeguards and prerelease status are unchanged.

## 1.53.3 - Windows Installer Update

- Public downloads now use one ready-to-use Windows installer, not app ZIPs.
- Optional driver/runtime choices are in setup, off by default. VB-CABLE uses
  its original signed interactive installer and Windows administrator approval.
- Empty libraries offer Add files, Add folder and in-app Search music actions.
- Updated first-use instructions and optional-driver guide for ordinary users.
- Replaced the legacy Windows file-drop hook with native Tcl/Tk drag-and-drop.
- Local data stays on each PC; no accounts or personal data are distributed.
- Unsigned packages remain development prereleases pending trusted signing.

## 1.53.2 - Development / Testing

- Removed the Profiles/accounts settings tab, profile switching, account
  creation/deletion, passcodes and the unused analytics-sharing toggle.
- Kept one local profile and listening history per PC/Windows user. No sign-in
  or uploading personal data to another computer or GitHub.
- Added local display name, listening insights, export and clear-history
  controls under Library settings.
- Safely migrates the selected legacy profile after preserving the original
  file in a local backup. Unselected histories are not mixed together.
- Included local profiles in library backup/restore and added a distribution
  gate rejecting personal profile/library/settings/session files in ZIPs.
- Old saved Profiles/Accounts settings pages now restore to Library.

## 1.53.1 - Development / Testing

- Fixed Previous with shuffle: it follows actual listening history instead of
  the current library's sorted order.
- Next replays forward history after going back. Rapid requests reserve the
  appropriate history position without recording a song that never started.
- Listening history persists with the playback session, using stable track
  identities rather than list row numbers. Missing files are skipped.
- Search & Downloads settings use clearer choices, a smaller everyday section,
  and an optional Advanced section.
- Full public playlist/album links have a direct download action in main search.
  Preview limits do not limit complete collection downloads.
- Added new-playlist destinations to the integrated download queue.
- Explicit playlist destinations import their saved songs even when general
  automatic Home import is disabled.
- Restoring a session also supports the Search & Downloads settings category.
- Published public documentation, installation guidance, and versioned downloads.

## 1.53.0 - Development / Testing

- Bundled spotDL in a separate runtime; Python and separate spotDL installation
  are not required on a listener's computer.
- Integrated optional online matches into the main search bar, with Play for
  local songs and Download to listen for online-only results.
- Added an in-app queue with progress, cancellation, retry, and partial-failure
  reporting. Completed files automatically import into Home by default.
- Added supported formats, sources, lyrics/artwork preferences, file rules, and
  network/performance controls.
- Isolated search/download provider dependencies from the main playback process.
- Added companion dependency/license inventory and vulnerability checks.

## Before This Public Repository

QuietPlay's local development included library browsing, multi-artist views,
playlists and generated mixes, lyrics, real PCM visualization, live EQ, taskbar
and headset media controls, OBS tools, themes, a compact mini player, and session
restoration. This page does not imply that older versions were signed public
releases.

