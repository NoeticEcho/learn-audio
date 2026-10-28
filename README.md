# Сквозь время · narration audio

The spoken lessons of [«Сквозь время»](https://open.noeticecho.space/learn/) ([NoeticEcho/learn](https://github.com/NoeticEcho/learn)), served by GitHub Pages at
<https://open.noeticecho.space/learn-audio/>, the same origin as the textbook.

**The voice is synthetic.** Every file here was rendered by
[Qwen3-TTS](https://github.com/QwenLM/Qwen3-TTS) 0.6B CustomVoice (Apache-2.0), preset speaker
`serena`, on the author's own machine. It is not a recording of a person, and it imitates no one.

## What is here

- `ru/<part>/<lesson>/<section>-<hash>.opus`: one file per section of a lesson, Ogg Opus, mono,
  32 kbps, loudness-normalised to −16 LUFS. `<section>` is `intro` (the title, the «Зачем» and the
  definition) or the section's number among the lesson's `##` headings; `<hash>` is the hash of
  the words spoken in it, so a file never changes: a new text is a new file.
- `ru.json`: the manifest, lesson id → sections → file, duration in seconds, the hash, and the
  start of each sentence. The textbook's build reads its own copy (`content/narration/ru.json`
  in NoeticEcho/learn) and offers «Слушать» only on a lesson whose every section matches its
  current text.

Nothing is built here and nothing runs: the files are rendered by
`tools/narration/render.py` in NoeticEcho/learn and pushed. How, and how to re-render a lesson
after its text changes, is in that repository's `docs/narration.md`.

## Licence

The audio is a reading of the lessons and carries their licence:
[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/), «Сквозь время», NoeticEcho.
Voice model: Qwen3-TTS (Alibaba Qwen team), Apache-2.0.
