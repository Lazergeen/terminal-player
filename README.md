# Terminal Player

A small, stylish terminal music player for Linux.

It scans `~/Music`, lets you choose tracks from a keyboard-driven TUI, and shows a live particle/pulse visualizer while the music is playing.

## Features

- Plays music from `~/Music`
- Recursive folder scanning
- Terminal playlist interface
- Animated particles, rings, and pulse bars
- Keyboard controls for play, pause, next, previous, stop, and rescan
- No Python package dependencies

## Supported Formats

`mp3`, `flac`, `wav`, `ogg`, `m4a`, `aac`, `opus`, `wma`, `aiff`, `alac`

Playback depends on the audio backend installed on your system.

## Requirements

- Python 3.10+
- One of these audio backends:
  - `ffplay`
  - `mpv`
  - `vlc` / `cvlc`
  - `mpg123`
  - `play`

For duration/progress detection, install `ffprobe` from FFmpeg.

On Arch Linux:

```bash
sudo pacman -S ffmpeg
```

On Debian/Ubuntu:

```bash
sudo apt install ffmpeg
```

## Install

Clone the project and make the script executable:

```bash
git clone https://github.com/YOUR_USERNAME/terminal-player.git
cd terminal-player
chmod +x player
```

Optional: install it as a global command:

```bash
ln -s "$PWD/player" ~/.local/bin/player
```

Make sure `~/.local/bin` is in your `PATH`.

## Usage

Put music files into `~/Music`, then run:

```bash
player
```

Or from the project folder:

```bash
./player
```

## Controls

| Key | Action |
| --- | --- |
| `Enter` | Play selected track |
| `Space` | Pause / resume |
| `n` | Next track |
| `b` | Previous track |
| `s` | Stop |
| `r` | Rescan `~/Music` |
| `↑` / `↓` or `k` / `j` | Move selection |
| `q` or `Esc` | Quit |

## Notes

This is a terminal-first player, so the visualizer is generated with text characters and colors directly inside the shell.
