<p align="center">
  <img src="logo.png" alt="Mixify logo" width="120">
</p>

<h1 align="center">Mixify for Linux</h1>

<p align="center">
  A fast, good-looking and highly customisable music player for Linux.<br>
  Play your own music files, build playlists, restyle the whole app and keep track of your listening.
</p>

---

## Get it

Mixify for Linux is built from source with one command (no installer, nothing to set up first).

```bash
git clone https://github.com/mixio1/mixify-linux.git   # or unpack the zip
cd mixify-linux
./build.sh --install      # build and add Mixify to your app menu
./build.sh --app          # or: build and just open it
```

`build.sh` installs the .NET 8 SDK into `~/.dotnet` if you don't have one (needs internet once). If the build fails, it saves the errors to `build-errors.txt`. Please attach that file to an issue.

Prefer not to install anything? Every push runs the GitHub Actions build, and the finished app is attached to the run as `mixify-linux-app`.

**Requirements**
- 64-bit Linux with a desktop (X11, or Wayland through XWayland)
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
- **Sound Island**: hide Mixify and keep a small always-on-top player with cover, seek and volume lines, and its own look (colours, gradients, blurred cover, liquid glass, visualizer, scrolling titles)
- Visualizer in the title bar with many looks, colours and gradients
- Waveform seek bar with your own colours
- Song list with Added, Plays, Hours and Length columns, and quick buttons (add to playlist, tags, edit, show in folder) when you hover a song
- Search bar (Ctrl+F) for songs and playlists

**Make it yours**
- Themes: Windows XP, Windows 95, Media Player 10 and 6.4, Winamp, Aero Glass, Synthwave, Terminal, Paper Light, Spotify Look, Soundlookalike and more, or make and share your own
- Custom fonts, text colours and background pictures
- Playlist icon editor with gradients and symbols
- Tags with emoji, custom song names, artists and pictures
- Library as a list or grid, foldable sidebar, pinned and hidden playlists, player bar position
- Custom keyboard shortcuts (they work while Mixify has the focus)

**Your listening**
- Profile page with hours listened, plays, top 10 songs and your day streak
- **Achievements** with progress bars and popups

**Extras**
- Download songs from YouTube as mp3 (see the note below)
- Low Performance Mode for older computers
- Start with your session (an entry in `~/.config/autostart`, optionally started hidden)
- Update check with a button in the title bar when a new version is out

**Not on Linux yet**
- Tray icon (closing the window works as set in Settings, but there is no tray)
- Media keys / MPRIS pop-up, taskbar mini player, guided tour, Miximonth recap
- Animated GIFs show their first frame only

## Updates

New versions are published on the [Releases](../../releases) page. Mixify tells you in Settings > About > Version (and with an **Update** button in the title bar) when one is out. Pull the new source or zip and run `./build.sh --install` again. Your settings, playlists and statistics are kept in `~/.config/Mixify`, so nothing is lost.

## YouTube downloads

Mixify can convert YouTube links to mp3. The first time you use it, it offers to fetch two free helper tools (yt-dlp and ffmpeg) into `~/.config/Mixify/tools`. If they are already on your `PATH`, those are used instead.

**Only download music you have the right to download.** You are responsible for following the laws and the terms of the services you use.

## Privacy

Mixify works offline and keeps everything on your computer. It doesn't collect data or send your listening history anywhere. The only network use is the optional update check (github.com, once at startup; you can turn it off in Settings > About > Version) and the YouTube helper downloads you ask for.

## Using your Windows settings

Settings and playlists use the same format as the Windows version. You can copy a `settings.json` over to `~/.config/Mixify`, but Windows paths like `C:\Music\...` won't exist on Linux, so pick your music folder again.

## About this project

Mixify was "vibe coded": it was built with the help of an AI assistant (Claude by Anthropic), with me deciding what it should do and testing the result. The Linux version is a port of the Windows app and has had less testing, so expect the occasional bug and please report it.

## Support

Found a bug or have an idea? Open an [issue](../../issues) on this page. For a bug, say which desktop and session you use (for example GNOME on Wayland) and, for a crash, attach the newest file from `~/.config/Mixify/crashlogs`.

## Licence

Mixify is free to use for personal, non-commercial purposes. You may not sell it, or redistribute modified copies. It is provided "as is", without any warranty. All rights reserved.

Mixify uses the open-source libraries [Avalonia](https://avaloniaui.net) (MIT), [NAudio](https://github.com/naudio/NAudio) (MIT), [NLayer](https://github.com/naudio/NLayer) (MIT) and [TagLibSharp](https://github.com/mono/taglib-sharp) (LGPL).
