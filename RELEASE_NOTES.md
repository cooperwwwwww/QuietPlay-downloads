# QuietPlay 1.53.4 Beta

One ready-to-use Windows installer, optional extras in setup, and a clearer
first-use library. Libraries and listening data are stored locally for each
Windows user.

## Changes

- Consistent QuietPlay Beta branding for the download, installer and app version.
- The download file is QuietPlay-1.53.4-Beta-Setup.exe, not a development kit.
- Added SmartScreen guidance: inspect More info, verify the source, and only
  choose Run anyway for a file you trust. Smart App Control blocks remain distinct.
- The public download is a Windows Setup EXE, not app ZIPs or a developer kit.
- Setup offers unchecked VB-CABLE and WebView2 options. VB-CABLE opens its
  original signed installer with Windows administrator approval.
- Empty libraries have Add files, Add folder and in-app Search music buttons.
- Native Tcl/Tk file drops replace the legacy Windows drag-and-drop hook.
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

Choose **Download QuietPlay for Windows** for the complete app. Optional driver choices
are inside setup. No Python, terminal commands or developer tools are needed.
New releases publish only this installer and its verification files. Historical
releases retain their original assets, but are not recommended current downloads.

SHA256SUMS.txt lists the exact published file hashes. See the repository's user
guide for search modes, complete playlists, audio routing, and troubleshooting.

## Important Limits

This is an **unsigned Beta build**, published as a prerelease, not a
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
