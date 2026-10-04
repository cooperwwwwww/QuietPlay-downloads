# QuietPlay Changes

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
