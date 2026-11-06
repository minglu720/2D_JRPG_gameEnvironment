# Anime Scene Background Skill

A Codex skill for transforming photographs or scene briefs into restrained anime-inspired game environment backgrounds. It keeps scene structure and visual style as separate inputs, while controlling how much detail is retained.

## Visual direction

- Calm, eye-level medium or long establishing views
- Environment-led compositions with readable architecture and spatial relationships
- Selective detail simplification, from sparse to rich
- No unrequested characters, dramatic camera angles, narrative staging, or character interaction space

## Repository contents

- `SKILL.md` — the complete skill instructions
- `references/prompt-examples.md` — prompt patterns for common scene-restyling requests
- `evals/evals.json` — example requests and expected behaviors for reviewing the skill

## Install

Copy this repository folder into your Codex skills directory as `anime-scene-background`:

- `$CODEX_HOME/skills/anime-scene-background`, if `CODEX_HOME` is set
- Otherwise, `~/.codex/skills/anime-scene-background`

Then invoke it with `$anime-scene-background` when asking Codex to restyle or create a game environment background.
