# QuietPlay Development Priorities

[QuietPlay](README.md) | [Changelog](CHANGELOG.md) | [Suggest an improvement](https://github.com/cooperwwwwww/QuietPlay-downloads/issues/new?template=feature_request.yml)

This is a direction for future work, not a schedule or a claim that unfinished
features already exist. Scope is decided after feedback and testing. New ideas
start with `needs triage`; only accepted work is marked `planned`.

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
- Complete the signed update path without weakening Windows security.
- Keep installers, optional prerequisites, setup instructions, and release
  verification easy to find and understand.

## Out of Scope for the Current App

This is not a promise of the full Spotify catalog, protected-audio downloads,
an unrestricted public music-sharing server, or a music-video platform.
QuietPlay's private source workspace is not published in this repository.

See [open feature requests](https://github.com/cooperwwwwww/QuietPlay-downloads/issues?q=is%3Aissue%20is%3Aopen%20label%3A%22feature%20request%22)
for listener ideas. Versioned release notes are the source of truth for what
has actually shipped.
