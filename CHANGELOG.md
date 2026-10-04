# QuietPlay Changes

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
