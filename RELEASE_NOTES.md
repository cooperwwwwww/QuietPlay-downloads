# QuietPlay 1.53.2 - Testing Build

This release removes account-style controls. Each person's copy stores their
own profile and saved data on the computer where they use QuietPlay.

## Changes

- No accounts tab, sign-in, passcodes, switching or analytics-sharing toggle.
- One local profile per Windows user, with display name, insights, export and
  clear-history controls in Settings > Library.
- Existing selected profile history is retained; the original multi-profile
  file is backed up locally before migration. No personal data is uploaded.
- Library backups now include the local profile, and public ZIP verification
  rejects bundled personal profile, library, settings and session files.
- Legacy saved account settings pages redirect to Library.
- Previous follows the songs you actually heard while shuffle is enabled.
- Next can replay forward listening history after going back.
- History restores with the playback session. Reopening waits for Play by default.
- Clearer Search & Downloads settings, with advanced controls tucked away.
- Download complete public playlists and albums directly from their search link.
- Save a download job into Home, an existing playlist, or a new playlist.
- Bundled spotDL, FFmpeg, and companion dependencies: no separate Python setup.

## Downloads

Choose the Setup EXE for a normal installation. The testing ZIP bundles that
installer with setup notes, the optional VB-CABLE audio driver package, and the
WebView2 bootstrapper. The portable ZIP is available for use without a normal
installation; extract all of it first.

SHA256SUMS.txt lists the exact published file hashes. See the repository's user
guide for search modes, complete playlists, audio routing, and troubleshooting.

## Important Limits

This is an **unsigned development build**, published as a prerelease, not a
signed production release. Smart App Control may block it. Do not disable
Windows protections. Trusted Authenticode signing remains outstanding, and
automatic in-app production updates remain disabled.

spotDL uses Spotify metadata and matches audio from other providers; it does not
retrieve protected Spotify audio or grant music rights. Only download recordings
you have permission to save. Matching and lyrics depend on public providers and
cannot be guaranteed for every recording. Public music servers and the retired
Find Music page are not restored by this release.

Created and product-directed by Cooper W., with engineering and design developed
in collaboration with OpenAI Codex. Independent of Spotify and not endorsed by
OpenAI.
