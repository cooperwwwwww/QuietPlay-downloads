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
See the [changelog](CHANGELOG.md).

## Next

- Finish packaged upgrade checks for the user-approved GitHub **Update now** flow.
  The implementation is in development, not in the current 2.2.0 download.
- Package and verify expanded Discover recommendations and full **50–60-song
  personalized playlists**, including the single-job **Download & save** flow.
  The development build has focused recommendation, batch-download and
  interface checks; these features are not in the current 2.2.0 installer.
- Package complete playlist search, **Download all**, and the new OBS overlay
  appearance editor, with installer and upgrade checks before publication.
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
- Complete the signed update path without weakening Windows security.
- Investigate smaller delta downloads after the full-installer upgrade flow is
  verified. Delta updates are not implemented or promised for the next release.
- Keep installers, optional prerequisites, setup instructions, and release
  verification easy to find and understand.

## Out of Scope for the Current App

This is not a promise of the full Spotify catalog, protected-audio downloads,
an unrestricted public music-sharing server, or a music-video platform.
QuietPlay's private source workspace is not published in this repository.

See [open feature requests](https://github.com/cooperwwwwww/QuietPlay-downloads/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22feature%20request%22)
for listener ideas. Versioned release notes are the source of truth for what
has actually shipped.

