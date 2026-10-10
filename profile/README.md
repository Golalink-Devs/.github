# Golalink Developers

A standalone Discord audio node written in Go, speaking the Lavalink v4 REST and
WebSocket protocol.

Golalink talks to Discord's voice gateway itself. Your bot stays on the main
gateway, forwards the `VOICE_STATE_UPDATE` and `VOICE_SERVER_UPDATE` payloads, and
controls playback over the Lavalink API. No Java, no CGO, and no Discord bot
token. FFmpeg and yt-dlp are optional.

## Projects

| Project | Description |
|---|---|
| [Golalink](https://github.com/Golalink/Golalink) | Standalone Discord audio node, Lavalink v4 compatible. GPL-3.0. |

## Features

- Lavalink v4 track loading, player and session management, `info` and `stats`.
- WebSocket events: `ready`, `stats`, `playerUpdate`, track start/end/exception/stuck, voice closed.
- Session resuming, with events buffered while a client is reconnecting.
- 48 kHz stereo Opus at 20 ms per packet: volume, pause, seek, stop, `endTime`, `noReplace`, `userData`.
- Discord voice gateway, UDP transport and DAVE through DisGo.
- MP3, WAV, FLAC at any bit depth, Ogg Vorbis, Ogg Opus, Ogg FLAC, AAC in ADTS or MP4, and Opus in WebM decoded, resampled and Opus-encoded in process.
- Surround tracks of up to eight channels, folded to stereo by the same mix FFmpeg uses.
- All ten standard filters run in process, `timescale` included.
- Lyrics over the LavaLyrics routes, timed, from LRCLIB and from YouTube Music's own catalogue for what it has nothing for.
- Prometheus metrics, structured console and file logs, graceful shutdown.

## Status

Golalink is actively maintained and under continuous development: fixes, new
source support and Lavalink v4 coverage land regularly. Nightly builds track the
default branch, while tagged releases are the stable ones to depend on.

## Support

- **Discord support server — preparing.** The invite will be posted here as soon as it opens.
- Bugs and feature requests: open an [issue](https://github.com/Golalink/Golalink/issues).

## Getting involved

- Code contributions: read the project's `README.md` and `docs/` first, then send a pull request.
- Licence: GPL-3.0. If you distribute a modified Golalink, you must pass the same freedoms on.

---

<sub>Golalink Developers · Taiwan</sub>
