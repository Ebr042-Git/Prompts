# YouTube channels - per-channel voice files

The YouTube agent skill pack (github.com/Jakeschincariol/youtube-agent-skill) reads one global file, `~/.claude/youtube/voice.md`. One file cannot hold three channel voices, so each channel gets its own folder here:

| Folder | Channel | Language |
|---|---|---|
| `factos-042/` | Factos 042 | English |
| `learn-with-ebr/` | Learn with EBR | English |
| `arabic-channel/` | Arabic channel (name to confirm) | Arabic |

Each folder has:

- `CLAUDE.md` - tells Claude to read and write `./voice.md` instead of the global file.
- `voice.md` - the channel's voice profile. Still a template: fill it from 3 real transcripts.

## How to use

1. Open Claude Code **inside the channel folder** (for example `cd youtube-channels/factos-042 && claude`). Claude only loads that folder's `CLAUDE.md` when it starts there or below it. Starting from the repo root will not pick it up.
2. First time: paste 3 transcripts and say "write voice.md from these".
3. Then run any `/yt-*` skill as normal.

## Limits

- This works through `CLAUDE.md` instructions, not by changing the skills. If you also keep a global `~/.claude/youtube/voice.md`, there is a small risk Claude reads it anyway. Safest: delete or rename the global file.
- The skill's Python scorers (`hookscore.py`, `title.py`) only understand English. The Arabic folder's `CLAUDE.md` tells Claude not to use their scores.
