==============================================================
  DeadFy — Spotify Inspired Music Player
  Version 1.0.0
  © 2026 DeadFy. All rights reserved.
  Dev : t3j0 (Discord) - itz__rayen_ (Instagram)
==============================================================


REQUIREMENTS
──────────────────────────────────────────────────────────────
  • Windows 10 or later (64-bit)
  • .NET 8 Runtime (download at https://dotnet.microsoft.com)
  • Internet connection (optional — for YouTube, Spotify,
    Last.fm, lyrics, and auto-updates)


GETTING STARTED
──────────────────────────────────────────────────────────────
  1. Run DeadFy.exe
  2. On first launch the app checks for updates automatically.
     If an update is available it downloads and installs it
     silently, then relaunches — no action needed from you.
  3. Go to Settings to configure your music folder, theme,
     audio device, and any API keys you want to use.


FEATURES
──────────────────────────────────────────────────────────────
  Playback
    • Local files (MP3, FLAC, WAV, M4A, OGG and more)
    • YouTube streaming (search and play directly)
    • Spotify track preview / search
    • 10-band equalizer
    • Shuffle and repeat modes
    • Crossfade between tracks
    • Volume normalisation
    • Sleep timer
    • Karaoke-style synced lyrics panel

  Library
    • Auto-scans your music folders
    • Reads ID3 / metadata tags (title, artist, album, cover art)
    • Playlists — create, rename, reorder, delete
    • Favourites
    • Recently played history
    • Sort by title, artist, album, date added, play count

  Integrations
    • Discord Rich Presence — shows what you're playing
    • Last.fm scrobbling
    • Lyrics via LRCLIB (synced) with plugin fallback

  Other
    • Dark theme with multiple colour variants
    • System tray support (minimize to tray)
    • Start with Windows option
    • Plugin system (see PLUGINS section below)
    • Auto-updater (see AUTO-UPDATES section below)


AUTO-UPDATES
──────────────────────────────────────────────────────────────
  DeadFy checks for updates every time it launches.

  • If no update is available → opens normally, nothing happens.
  • If a new version is found → a small "Please wait" window
    appears, the update downloads silently, files are replaced,
    and DeadFy relaunches automatically.

  You do not need to do anything. The update is fully silent.
  Your settings, library, and playlists are never affected.


API KEYS (OPTIONAL)
──────────────────────────────────────────────────────────────
  DeadFy works out of the box for local files with no keys.
  To enable online features, add your keys in Settings:

  YouTube Data API v3
    → console.cloud.google.com → Enable "YouTube Data API v3"
    → Create credentials → API Key
    → Paste into Settings → YouTube API Key

  Spotify
    → developer.spotify.com → Dashboard → Create App
    → Paste Client ID and Client Secret into Settings

  Last.fm
    → last.fm/api/account/create
    → Paste API Key and Secret into Settings → enable scrobbling


PLUGINS
──────────────────────────────────────────────────────────────
  DeadFy supports plugins that extend its functionality.
  Plugin types:

    IAudioPlugin     — Custom audio effects / processing
    ILyricsPlugin    — Add a new lyrics source
    ISearchPlugin    — Add a new search tab (e.g. SoundCloud)
    IMetadataPlugin  — Enrich song metadata on import

  Installing a plugin
    1. Copy the plugin .dll into the  Plugins/  folder
       (located next to DeadFy.exe)
    2. Restart DeadFy — it loads automatically
       (hot-reload also works: replace the .dll while running)

  Managing plugins
    → Open the Plugin Manager from the main menu
    → Enable / disable / view plugin info from there

  Creating a plugin
    → See  Plugins/HOW_TO_CREATE_A_PLUGIN.txt  for a full
      guide with code examples


FILE LOCATIONS
──────────────────────────────────────────────────────────────
  Settings       %AppData%\DeadFy\settings.json
  Logs           %AppData%\DeadFy\Logs\
  Stream cache   %AppData%\DeadFy\StreamCache\
  Crash log      %USERPROFILE%\Desktop\DeadFy_CrashLog.txt


TROUBLESHOOTING
──────────────────────────────────────────────────────────────
  App won't start
    → Make sure .NET 8 Runtime is installed
    → Check DeadFy_CrashLog.txt on your Desktop

  No sound
    → Go to Settings → Audio Device and select your device
    → Make sure the volume in DeadFy is not set to 0

  YouTube / Spotify not working
    → Check that your API keys are entered correctly in Settings
    → Make sure you have an active internet connection

  Update stuck on "Please wait"
    → Check your internet connection
    → Delete  version.txt  next to DeadFy.exe and relaunch
      (this forces a fresh update check)

  Something else is broken (contact dev)
    → Check the log at  %AppData%\DeadFy\Logs\
    → The log file is named  deadfy_YYYY-MM-DD.log


==============================================================
  Made by Takana
==============================================================
