# Arabic channel (name to confirm) - channel rules for Claude

This folder is the workspace for the **Arabic channel (name to confirm)** YouTube channel. Language: Arabic.

## Voice file: use this one, not the global one

The YouTube agent skills (`/yt-script`, `/yt-package`, `/yt-comment`, `/yt-seo`, `/yt-plan`, `/yt-audit`, and any other `/yt-*` skill) tell you to read `~/.claude/youtube/voice.md`. **In this folder, ignore that path.**

- Read `./voice.md` (the file next to this CLAUDE.md) instead, every time a skill says to read the voice file.
- If a skill says to write or update the voice file, write `./voice.md`. Never write to `~/.claude/youtube/voice.md` from here.
- Never mix in voice rules from another channel folder or from the global file.
- If `./voice.md` still has `TODO` sections, stop and ask for three transcripts of this channel's own videos. Fill `./voice.md` from them before writing anything. A script in the wrong voice is worse than no script.

## Arabic-specific rules

- Write scripts, titles, descriptions and comment replies in Arabic, in the dialect and register set in `voice.md`. Do not translate from English drafts.
- The Python tools in the skill pack (`hookscore.py`, `title.py`) only read English letters. On Arabic text they count zero words, so their scores are meaningless. Do not run them on Arabic text and do not quote their scores. Judge hooks and titles by hand instead, and say that you did.
- Title length checks: count characters yourself. Arabic is right-to-left; check that numbers and any English words in a title still read in the right order.
