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
- `references/assets/style-references/` — visual references bundled with this skill
- `evals/evals.json` — example requests and expected behaviors for reviewing the skill

## Install in Codex

In Codex, invoke `$skill-installer` and ask it to install the skill from this repository URL: `https://github.com/minglu720/2D_JRPG_gameEnvironment`.

After installation, invoke `$anime-scene-background` or describe an image-restyling task that matches its scope. If it does not appear in the skill selector, restart Codex.
