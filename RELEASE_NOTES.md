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
