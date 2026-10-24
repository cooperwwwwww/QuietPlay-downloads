# QuietPlay 2.2.14

QuietPlay 2.2.14 works properly offline and plays without crackling.

- **Works offline:** online recommendations used to retry every few seconds while your PC was offline, keeping QuietPlay busy and filling its logs. They now wait before trying again (2 minutes, growing to 30), show that you are offline, keep what you already had, and come back as soon as you reconnect.
- **No more crackling:** QuietPlay now gives your speakers or headphones a larger audio buffer, so a busy moment in the app no longer interrupts the sound. Measured on a real PC under load: 51 audio dropouts in 10 seconds before, none after.
- **Bluetooth:** Bluetooth headphones and speakers get an extra-safe buffer. If Windows plays through a headset's hands-free (phone call) connection, which always sounds muffled and crackly, QuietPlay tells you which output to choose instead.
- Includes everything from 2.2.13 and earlier, including the optional Navidrome add-on.

**Already on 2.2.7, 2.2.8, 2.2.9, 2.2.11, 2.2.12 or 2.2.13:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **8.0 MB**). **On 2.2.4:** the same steps (about **25.0 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.2 MB**). Your music, library, playlists and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.14-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.13

QuietPlay 2.2.13 gives the Navidrome add-on its own Settings tab and makes it reconnect on its own.

- **Settings → Navidrome:** once the add-on is installed it gets a tab of its own with everything in one place: connection, library, streaming quality, what is shared with your server, and storage.
- **Automatic reconnect:** if your server goes offline, its songs leave your library and QuietPlay checks every minute, bringing them back automatically when the server returns.
- **New settings:** streaming quality (original down to 96 kbps), check for new songs automatically, connect when QuietPlay starts, use server songs in mixes and radio, and separate switches for sending plays, now playing and likes to your server.
- **Tools:** test the connection, clear the listening history kept on this PC, and clear the cover art cache.
- **Fixed:** with a lower streaming quality, songs now fall back to original quality on servers that cannot convert them (servers without FFmpeg), instead of not playing.
- Tested against a real Navidrome 0.64.2 server: sign-in, browsing, MP3 and FLAC playback, cover art, likes, play counts, and the server going offline and coming back.

**Already on 2.2.7, 2.2.8, 2.2.9, 2.2.11 or 2.2.12:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **7.9 MB**). **On 2.2.4:** the same steps (about **25.0 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.2 MB**). Your music, library, playlists and settings stay in place, including your Navidrome sign-in.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.13-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.12

QuietPlay 2.2.12 adds an optional **Navidrome add-on**, so you can play music from your own music server alongside the songs on your PC.

- **Optional, off by default:** tick **Navidrome music server support** during setup, or install it any time in **Settings → Advanced → Add-ons**. Works with Navidrome and other Subsonic-compatible servers.
- **Mixed or separate:** choose whether server songs join your library (Home, artists, albums, liked songs and search) or stay on their own **Navidrome** page with albums, artists, playlists and search.
- **Seamless when offline:** if the server goes offline or you sign out, its songs quietly leave your library and come back when it returns. What you listened to is kept, so recommendations keep learning from it.
- Plays and likes are sent back to your server. Your password is never saved; QuietPlay keeps a sign-in token protected by Windows.
- Includes everything from 2.2.11 and earlier: more cover art, Retry for failed downloads, playback that follows your sound device, and downloads that try other sources.

**Already on 2.2.7, 2.2.8, 2.2.9 or 2.2.11:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **7.9 MB**). **On 2.2.4:** the same steps (about **25.0 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.2 MB**). Your music, library, playlists and settings stay in place. Updating does not turn the add-on on.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.12-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.11

QuietPlay 2.2.11 finds more cover art and tidies up song titles.

- **More cover art:** when MusicBrainz is unavailable or finds nothing, QuietPlay looks for the same song and album on **Apple Music**, then **Deezer**. Songs whose catalogue title lists featured artists, and downloads saved without album details, are matched too.
- **Cleaner titles:** fixed songs showing a download tag such as "[qp-1a2b…]" in their title when they were added while still downloading. Your music files are not changed.
- Includes everything from 2.2.9 and earlier: Retry for failed downloads, a collapsible **Made for you**, playback that follows your sound device, and downloads that try other sources.

**Already on 2.2.7, 2.2.8 or 2.2.9:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **7.9 MB**). **On 2.2.4:** the same steps (about **24.9 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.1 MB**). Your music, library, playlists and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.11-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.9

QuietPlay 2.2.9 makes a few everyday things easier.

- **Retry failed downloads:** a song that failed now has a **Retry** button in the Downloads panel. It reuses the same playlist and skips songs already saved.
- **Collapse Made for you:** the arrow in the box header shrinks it to one line, so your songs come first on smaller screens. QuietPlay remembers your choice.
- **Clearer output setting:** Settings → Audio now shows **Follow Windows (System default)** and explains what your choice does.
- Includes everything from 2.2.8, 2.2.7 and 2.2.4: playback that follows your sound device, downloads that try other sources, and the **Made for you** Home.

**Already on 2.2.7 or 2.2.8:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **7.9 MB**). **On 2.2.4:** the same steps (about **24.9 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.1 MB**). Your music, library, playlists and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.9-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.8

QuietPlay 2.2.8 plays where your PC plays.

- **Follows your sound device:** with **Output** set to **System default** (Settings → Audio), playback follows the device Windows is using. Connect headphones, a speaker or Bluetooth device and the music moves there automatically, keeping your song and position; disconnect it and it moves back.
- **No manual refresh:** the output device list in Settings updates by itself when devices are connected or removed.
- **Missing device, no silence:** if the device you chose is not connected, QuietPlay plays through your PC's current device and switches back when yours returns.
- Includes everything from 2.2.7 and 2.2.4: downloads that try other sources when one fails, the **Made for you** Home and the redesigned Downloads, Update center and updater.

**Already on 2.2.7:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **7.8 MB**). **On 2.2.4:** the same steps (about **24.8 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.1 MB**). Your music, library, playlists and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.8-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.7

QuietPlay 2.2.7 makes downloads keep trying when a source fails.

- If a song cannot be downloaded from your chosen source, QuietPlay now tries **YouTube Music**, **YouTube**, **SoundCloud** and **Bandcamp**, then a broader search, before reporting it as failed. Songs that already downloaded are not fetched again, and the Downloads panel shows which source is being tried.
- **Fixed:** the YouTube Music source could not start in earlier versions.
- **Works when Spotify is down:** if Spotify cannot provide song details (for example "Could not get client token"), searches and Spotify song links use Apple's public music catalogue instead, preferring the original recording over covers and remixes. Album and playlist links still need Spotify.
- Includes everything from 2.2.4: the **Made for you** Home, reliable recommended playlist downloads and the redesigned Downloads, Update center and updater.

**Already on 2.2.4:** open **Settings → Updates → Check for updates → Download update → Update and restart** (about **24.8 MB**). **On 2.2.2 or 2.2.3:** the same steps, with **Download changed files** (about **40.1 MB**). Your music, library, playlists and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.7-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. Only download music you have permission to save. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.4

QuietPlay 2.2.4 gives **Home** one clear **Made for you** box and makes recommended playlist downloads reliable.

- **Made for you** brings together your local mixes, new songs and full 50–60-song recommended playlists. Your songs sit right below, with **Play** and **Shuffle** where they were. In your rotation is removed.
- Recommendations stay loaded when you switch tabs instead of reloading each time, and rows remember where you scrolled. Click a recommended song to preview it.
- **Fixed:** recommended playlist downloads failing with "Could not get client token". Playlists use the song details QuietPlay already has, keep their order, and continue if one song cannot be found.
- Redesigned **Downloads** panel, **Update center** and official updater window.

**Already on 2.2.2 or 2.2.3:** open **Settings → Updates → Check for updates → Download changed files → Update and restart**. This release downloads about **40.1 MB** of changed files. Your music, library, playlists and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **40.2 MB**. **On 2.2.0:** install `QuietPlay-2.2.4-Windows-Setup.exe` once over the existing app to enable file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and every changed file's SHA-256 is checked. QuietPlay is still not Windows Authenticode-signed, so Windows may show a SmartScreen warning; see the [Windows security guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/FAQ.md#windows-protected-your-pc). Verify downloads with `SHA256SUMS.txt`. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.3

QuietPlay 2.2.3 adds compact, always-visible recommendations to **Home**, between **Made for you** and your library.

- Your local rotation, Made for you mixes and library remain available to play without another download.
- **Songs recommended for you** combines new discoveries and more from your favorite artists, using the same listening-based recommendations as Discover.
- **Playlists picked for you** has complete 50–60-song mixes. Open one to see every song, preview, download a song, or **Download & save** the full playlist.
- Left/right arrows scroll your rotation, local mixes, recommended songs and recommended playlists, with smooth movement, hover animations, keyboard controls and reduced-motion support.
- Recommendations stay open with no dropdown. Small cards keep your library within reach. **See all recommendations** opens Discover; **Refresh recommendations** updates the shared selection.

**Already on 2.2.2:** open **Settings → Updates → Check for updates → Download changed files → Update and restart**. This release downloads about **7.9 MB**, replacing five changed files and removing one obsolete app asset. Your music and settings stay in place.

**On 2.2.1:** run `QuietPlayUpdater.exe` from this release for a direct changed-file upgrade of about **23.1 MB**. **On 2.2.0:** install `QuietPlay-2.2.3-Windows-Setup.exe` once over the existing app to enable future file updates. Full setup is available for new PCs and repairs.

Windows 10/11, 64-bit. Official release manifests are signed and hashes are checked. Windows Authenticode signing is still pending. The OBS appearance editor remains unreleased.

---

# QuietPlay 2.2.2

QuietPlay 2.2.2 adds the **official changed-file updater**.

- Open **Settings → Updates → Check for updates → Download changed files → Update and restart**.
- Updates download the files changed for your installed version, instead of the whole Windows installer.
- The updater verifies an Ed25519-signed official release manifest, package size and SHA-256 hashes, then checks the installed app before reopening it.
- Downloads show progress and can be cancelled. Duplicate update jobs are blocked. Failed or interrupted updates restore the previous files.
- Your music, library, playlists, likes, history and settings stay in place.

**Upgrade from 2.2.1:** download `QuietPlayUpdater.exe` below and run it. It finds your installation and downloads about **23 MB** of changed files. Choose **Update and restart** when verification finishes. You can also use the full setup.

**Upgrade from 2.2.0:** install `QuietPlay-2.2.2-Windows-Setup.exe` once over the existing app. After that, future published file updates use the new update screen. The old 2.2.0 update checker cannot install this new updater itself.

The full installer is also available for new PCs and repairs. Windows 10/11, 64-bit. QuietPlay is still not Windows Authenticode-signed; its release-key signatures do not replace Windows publisher signing or bypass Windows security.

Only updates published with matching packages and the trusted QuietPlay release signature can be applied. The updater does not create future releases by itself. The OBS appearance editor remains unreleased.

[User guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/USER_GUIDE.md#updates-and-help) · [Report a problem](https://github.com/cooperwwwwww/QuietPlay-downloads/issues)

---

# QuietPlay 2.2.1

QuietPlay 2.2.1 adds complete playlists and more music discovery.

- Search a Spotify playlist or album link to see every returned song, with **Download all**.
- Discover builds personalized playlists of **50–60 unique songs** from your listening habits when enough matches are available.
- Browse more recommended songs, explore related artists, preview tracks, and **Download & save** an entire recommended playlist as one job.
- App and installer labels now show **2.2.1**.

**Windows 10/11, 64-bit.** Download `QuietPlay-2.2.1-Windows-Setup.exe` below and run it over the existing installation. Normal upgrades keep your music, playlists, likes, history and settings. WebView2 installation needs internet only if the runtime is missing. The optional VB-CABLE driver archive is included for OBS audio routing.

Recommendations depend on listening history and catalog availability. Downloads use catalog metadata and matching audio providers; only save recordings you have permission to download. This release does not include the unreleased OBS appearance editor or in-app Update now flow.

The installer is unsigned. Compare its SHA-256 against `SHA256SUMS.txt`. Follow the repository's Windows security notice if Windows displays a warning.

[User guide](https://github.com/cooperwwwwww/QuietPlay-downloads/blob/main/USER_GUIDE.md) · [Report a problem](https://github.com/cooperwwwwww/QuietPlay-downloads/issues)

---

# QuietPlay 2.2.0

Genres you can trust, recommendations from the real world, and a steadier
lyrics preview. Install over 2.1: your library, playlists, likes, history and
settings carry over.

## New

- **Genres by artist.** Each artist now gets one genre for all of their songs,
  decided from what listeners tag them with on MusicBrainz, their albums on
  Deezer and Apple Music. QuietPlay confirms it found the right artist through
  one of your own songs, so a different artist with the same name can't change
  your genres. For example, Jack Johnson is Folk, not Rock.
- **Genres are saved into your song files.** Each song's genre is written into
  the file's own tags, so other players show the same genre. Only the genre is
  changed, and never while the song is playing. Turn it off in Settings →
  Library → *Save genres into song files*.
- **One genre system.** The old song-by-song genre check, which often guessed
  Rock or Pop from store categories, is gone. Every artist is checked again with
  the new method the first time 2.2.0 opens (about 20 minutes in the background).
  Artists the stores only call Rock, Pop or Alternative take the genre their
  similar artists in your library share.
- **Review genres.** Settings → Library → *Genres by artist* → **Review genres**
  lists every artist with their genre and how sure QuietPlay is. *Check these*
  shows the ones worth a look. Pick a genre to change all of an artist's songs
  at once; your choice is kept for songs you add later.
- **Artists you might like.** Discover suggests songs by artists you don't have
  yet, based on the artists you actually play most and what their listeners
  also play (from Deezer). Each card says which of your artists it came from.

## Fixed and improved

- The lyrics preview in the Now Playing panel always shows the line being sung,
  and never shows the previous song's lyrics after a song changes.
- The same fix stops other parts of the window from briefly showing the
  previous song's details after skipping.
- Quick play (Ctrl+K) puts the cursor in its search box again.
- Closing a dialog returns the keyboard focus to where you were.
- Searching settings highlights the exact settings that match.
- A screen that fails to draw shows a message instead of an empty window, and
  the rest of QuietPlay keeps working.

## Good to know

- Windows 10 or 11, 64-bit. QuietPlay is not code-signed yet, so Windows
  SmartScreen may show "Windows protected your PC"; see the README's security
  notice. Settings → Updates tells you when a new version is here.
- Genre and recommendation lookups send artist names and song titles to
  MusicBrainz, Deezer and Apple. Turn off *Check song genres automatically* or
  *Suggest new songs* in Settings to stop them.
- Online search and downloads use the bundled spotDL companion. It does not
  download protected Spotify audio. Only save music you have permission to download.

Created and product-directed by Cooper W. Engineering and design developed in
collaboration with OpenAI Codex; the 2.0 redesign developed in collaboration
with Claude by Anthropic. Independent of Spotify and Apple, and not endorsed by
OpenAI or Anthropic.
