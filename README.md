# Terminal Player

A lightweight terminal music player for Linux. It scans `~/Music`, plays tracks through an installed audio backend, and renders animated visualizations directly in the terminal.

## Features

- playlist built automatically from `~/Music`
- play, pause, next, previous, and rescan controls
- normal and shuffled (`mix`) playback modes
- pulse, wave, and rain visualizations
- rename and delete actions for tracks
- popup menus with proper terminal clipping
- no Python packages required

## Requirements

- Python 3.10+
- one playback backend: `ffplay`, `mpv`, `vlc`, `cvlc`, `mpg123`, or `play`
- optional: `ffprobe` for track duration detection

On Debian/Ubuntu, the simplest setup is:

```bash
sudo apt install python3 ffmpeg
```

## Install

```bash
git clone https://github.com/Lazergeen/terminal-player.git
cd terminal-player
chmod +x player
mkdir -p ~/.local/bin
ln -sf "$PWD/player" ~/.local/bin/player
```

Make sure `~/.local/bin` is in your `PATH`, then launch:

```bash
player
```

## Controls

| Key | Action |
| --- | --- |
| `Enter` | Play selected track |
| `Space` | Pause or resume |
| `Up` / `Down`, `k` / `j` | Select track |
| `n` / `b` | Next / previous track |
| `s` | Stop |
| `r` | Rescan `~/Music` |
| `E` | Edit selected track |
| `M` | Playback mode and animation |
| `q` or `Esc` | Close menu or quit |

Supported formats: MP3, FLAC, WAV, OGG, M4A, AAC, OPUS, WMA, AIFF, and ALAC.

## License

MIT
