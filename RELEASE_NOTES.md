# QuietPlay 1.54.0 Beta

Native platform support without changing QuietPlay's familiar layout or local
library model. Each user keeps independent saved data on their own computer.

## Changes

- Native Mac and Linux build targets, with separate Intel/AMD and ARM64 packages.
- CoreAudio on Mac and PulseAudio/ALSA on Linux, while retaining Windows WASAPI.
- Standard local-data locations, with legacy Unix folders preserved.
- Native file opening, safe Trash removal and single-instance activation.
- Bundled native spotDL, FFmpeg and Deno; no separate Python setup for listeners.
- Mac Command shortcuts and platform-appropriate integrations/update settings.
- Background downloader cancellation terminates only its owned process group.
- Windows installer retains optional VB-CABLE and WebView2 choices, off by default.
- No accounts, public music servers, personal data uploads or bundled songs.
- Empty Home offers Add files, Add folder and optional in-app Search music.
- Added platform requirements, installation instructions and feature differences.

## Downloads

Use the installers actually listed on this release. Windows uses a Setup EXE;
experimental Mac packages use DMG and Ubuntu/Debian Linux packages use DEB.
Chromebooks require a compatible Linux environment and the matching Linux DEB.
No source ZIP or developer environment is required.

[Platform guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/PLATFORMS.md).
SHA256SUMS.txt identifies each published package. VERIFICATION.json records the
checks and untested areas for that particular build.

## Important Limits

This is a Beta prerelease. Windows packages remain unsigned and may be blocked
by Smart App Control. Mac packages are not Developer ID signed or notarized.
Do not disable operating-system security protections to run these packages.
Automatic production updates remain disabled pending trusted signing.

Native runner checks do not substitute for physical Mac/Linux/Chromebook
testing. Headsets, hardware outputs, OBS audio routing and real provider
downloads remain unverified on those platforms. Windows taskbar/global media
integration and WebView2 are not offered on Mac/Linux. Virtual audio devices
must be set up separately for each OS; Windows drivers are not shipped with
Mac/Linux packages.

spotDL uses Spotify metadata and matches audio from other providers; it does not
retrieve protected Spotify audio or grant music rights. Only download recordings
you have permission to save. Matching and lyrics depend on public providers and
cannot be guaranteed for every recording. Public music servers and the retired
Find Music page are not restored by this release.

Created and product-directed by Cooper W., with engineering and design developed
in collaboration with OpenAI Codex. Independent of Spotify and not endorsed by
OpenAI.
