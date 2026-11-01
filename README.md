<p align="center">
  <img src="logo.png" alt="Mixify logo" width="120">
</p>

<h1 align="center">Mixify</h1>

<p align="center">
  A fast, good-looking and highly customisable music player for Windows and Linux.<br>
  Play your own music files, build playlists, restyle the whole app and keep track of your listening.
</p>

---

## Download

Get the latest version from the **[Releases](../../releases/latest)** page. Mixify needs no installer: download, unpack if needed, and run it.

### Windows

Download `Mixify.exe` (or the `.zip`) and run it.

- Windows 10 (version 1809) or newer, 64-bit
- Your own music files: mp3, wav, flac, m4a, aac, wma

### Linux

Download the Linux file (`mixify-linux`, a `.zip` or `.tar.gz`), unpack it and run it:

```bash
unzip mixify-linux.zip -d ~/Mixify      # or: tar xzf mixify-linux.tar.gz
cd ~/Mixify
chmod +x Mixify
./Mixify
```

- 64-bit Linux with a desktop (X11, or Wayland through XWayland)
- The [.NET 8 runtime](https://dotnet.microsoft.com/download/dotnet/8.0) (`dotnet-runtime-8.0` in most package managers)
- PulseAudio or PipeWire (`libpulse0` / `pulseaudio-libs` / `libpulse`)
- Your own music files: mp3 and wav play out of the box; flac, ogg, opus, m4a, aac, wma, aiff, mka and webm need **ffmpeg** (install it from your package manager, or Mixify can fetch it for you, see YouTube downloads)

## Getting started

1. Open Mixify and type a username. Optionally add a profile picture.
2. Pick your music folder. Every subfolder becomes a playlist.
3. Press play. Create your own playlists with **+**, drag songs in from your file manager, or right-click a song to add it to a playlist.

## Features

**Player**
- Playlists from your folders, plus your own playlists with custom names and pictures
- Queue with drag-and-drop, shuffle, loop, and sort by name, author or your own order
- Crossfade between songs, a 6-band equalizer and Auto EQ, stereo/mono output
- Full-screen "Now playing" view
- **Sound Island**: hide Mixify and keep a small always-on-top player with its own look (colours, gradients, blurred cover, liquid glass, visualizer, scrolling titles)
- Visualizer in the title bar with many looks, colours and gradients
- Waveform seek bar with your own colours
- Song list with Added, Plays, Hours and Length columns, and quick buttons (add to playlist, tags, edit, show in folder) when you hover a song
- Search bar (Ctrl+F) for songs and playlists
- Windows only: taskbar mini player, media keys, Bluetooth headset buttons and the Windows media pop-up

**Make it yours**
- Themes: Windows XP, Windows 95, Media Player 10 and 6.4, Winamp, Aero Glass, Synthwave, Terminal, Paper Light, Soundlookalike and more, or make your own
- Custom fonts, text colours and background pictures (GIFs on Windows, first frame only on Linux) with blur
- Playlist icon editor with gradients and symbols
- Tags with emoji, custom song names, artists and pictures (you can copy a picture from another song)
- Rearrangeable Home screen, library grid or list, foldable sidebar, pinned and hidden playlists
- Custom keyboard shortcuts (on Linux they work while Mixify has the focus)

**Your listening**
- Profile page with hours listened, plays, top 10 songs and your day streak
- **Achievements** with progress bars, popups and sound
- **Miximonth** (Windows only): a monthly recap in the style of Spotify Wrapped

**Extras**
- Download songs from YouTube as mp3 (see the note below)
- Low Performance Mode for older computers
- Starts with your computer if you want (Windows: runs in the tray; Linux: an entry in `~/.config/autostart`, no tray yet)
- Update check with an **Update** button in the title bar when a new version is out
- Settings backup and import (Windows)

## Updates

New versions are published on the Releases page. Mixify tells you in Settings > About > Version (and with an **Update** button in the title bar) when one is out. Download the new version and replace the old files with it.

Your settings, playlists and statistics are kept outside the app, so nothing is lost:

| | Where |
|---|---|
| Windows | `%AppData%\Mixify` |
| Linux | `~/.config/Mixify` |

Both versions use the same format. You can copy a `settings.json` from Windows to Linux, but paths like `C:\Music\...` won't exist there, so pick your music folder again.

## YouTube downloads

Mixify can convert YouTube links to mp3. The first time you use it, it offers to fetch two free helper tools (yt-dlp and ffmpeg) into `%AppData%\Mixify\tools` (Windows) or `~/.config/Mixify/tools` (Linux). On Linux, tools already on your `PATH` are used first.

**Only download music you have the right to download.** You are responsible for following the laws and the terms of the services you use.

## Privacy

Mixify works offline and keeps everything on your computer. It doesn't collect data or send your listening history anywhere. The only network use is the optional update check (github.com, once at startup; you can turn it off in Settings > About > Version) and the YouTube helper downloads you ask for.

## About this project

Mixify was "vibe coded": it was built with the help of an AI assistant (Claude by Anthropic), with me deciding what it should do and testing the result. It works well for me, but it hasn't had the review a professionally written app would get, so expect the occasional bug and please report it. The Linux version is a port of the Windows app and has had less testing.

## Support

Found a bug or have an idea? Open an [issue](../../issues) on this page. Please say whether you use Windows or Linux (on Linux, which desktop and session, for example GNOME on Wayland). For a crash on Linux, attach the newest file from `~/.config/Mixify/crashlogs`.

## Licence

Mixify is free to use for personal, non-commercial purposes. You may not sell it, or redistribute modified copies. It is provided "as is", without any warranty. All rights reserved.

Mixify uses the open-source libraries [NAudio](https://github.com/naudio/NAudio) (MIT), [TagLibSharp](https://github.com/mono/taglib-sharp) (LGPL) and [WpfAnimatedGif](https://github.com/XamlAnimatedGif/WpfAnimatedGif) (Apache 2.0) on Windows, and [Avalonia](https://avaloniaui.net) (MIT), [NAudio](https://github.com/naudio/NAudio) (MIT), [NLayer](https://github.com/naudio/NLayer) (MIT) and [TagLibSharp](https://github.com/mono/taglib-sharp) (LGPL) on Linux.
