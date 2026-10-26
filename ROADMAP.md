# QuietPlay Development Priorities

[QuietPlay](README.md) | [Changelog](CHANGELOG.md) | [Suggest an improvement](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=feature_request.yml)

This is a direction for future work, not a schedule or a claim that unfinished
features already exist. Scope is decided after feedback and testing. New ideas
start with `needs triage`; only accepted work is marked `planned`.

## Shipped in 2.0-2.2

The redesigned app, Discover mixes, radio and autoplay from your own listening,
listening stats, suggestions from your artists, duplicate and missing-song
tools, playlist tidy-up, faster typo-tolerant search, crossfade, global shortcuts,
and artist-based genre review and recommendations.
Version **2.2.1** adds expanded Discover recommendations, full 50–60-song
personalized playlists, complete playlist search and Download all.
Version **2.2.2** adds official signed manifests and changed-file updates,
with startup verification and recovery.
See the [changelog](CHANGELOG.md).

## Next

- Package the new OBS overlay appearance editor and complete its installer checks.
- Gapless playback between songs.
- Bringing the 2.0 interface to Mac and Linux.

## Reliability Before More Controls

- Keep long-running playback stable, including rapid song changes, shuffle
  history, device changes, and restoring a saved session.
- Reduce navigation and settings latency while keeping scrolling free of
  duplicated or stale content.
- Improve provider failure messages, matching review, and partial download
  recovery without blocking playback.

## A Clearer Listening Experience

- Continue refining small-screen spacing, alignment, and the mini player.
- Make common playlist and library actions easier with fewer repeated controls.
- Keep meaningful visual feedback responsive, with reduced-motion options and
  low-overhead visualizer behavior for gaming.

## Metadata People Can Trust

- Improve recording-aware genre and cover matching, especially collaborations,
  alternate versions, and tracks not represented in public databases.
- Make the source and confidence of a suggested correction clearer.
- Preserve manual corrections rather than repeatedly replacing them.

## Distribution and Support

- Obtain a trusted signing identity for normal public Windows releases.
- Validate the experimental native Mac and Linux packages on physical devices,
  including Chromebook Linux, headsets, audio routing and provider downloads.
- Obtain Mac Developer ID signing and notarization before a production Mac release.
- Continue validating file updates across future app and runtime releases.
- Obtain Windows Authenticode signing separately from release-key signatures.
- Consider binary patching within large changed files; current file updates
  replace each changed file and reuse unchanged files.
- Keep installers, optional prerequisites, setup instructions, and release
  verification easy to find and understand.

## Out of Scope for the Current App

This is not a promise of the full Spotify catalog, protected-audio downloads,
an unrestricted public music-sharing server, or a music-video platform.
QuietPlay's private source workspace is not published in this repository.

See [open feature requests](https://github.com/cooperwwwwww/QuietPlay-downloads/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22feature%20request%22)
for listener ideas. Versioned release notes are the source of truth for what
has actually shipped.


Version **2.2.18** polishes search and adds mood playlists. Version **2.2.17** added mood mixes and a new search. Version **2.2.16** fixed update progress bars and artist names. Version **2.2.15** fixed Next stopping with "End of the list" offline. Version **2.2.14** made QuietPlay work properly offline and removed audio crackling. Version **2.2.13** gave Navidrome its own Settings tab and automatic reconnect. Version **2.2.12** added the optional Navidrome add-on. Version **2.2.11** found more cover art. Version **2.2.9** added Retry for failed downloads and a collapsible Made for you. Version **2.2.8** follows the sound device your PC is using. Version **2.2.7** retried failed downloads on other sources and keeps working
when Spotify is unavailable. Version **2.2.4** brought your mixes, new songs and full 50–60-song playlists
together in one Made for you box on Home, keeps recommendations loaded between
tabs, fixes recommended playlist downloads and redesigns Downloads and updates.
