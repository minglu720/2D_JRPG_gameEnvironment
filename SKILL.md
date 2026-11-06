---
name: anime-scene-background
description: Transform supplied photographs or scene descriptions into restrained anime-style game environment backgrounds, preserving legible spatial structure while simplifying visual detail. Use when creating or restyling environment art with calm, eye-level medium or long shots and no character-centered staging.
metadata:
  short-description: Style game environment backgrounds
---

# Anime Scene Background

Turn a real place or scene brief into a coherent anime-inspired game background. Treat scene structure and visual style as separate inputs: the source photo or scene description defines what is there and how spaces connect; style references define how forms, light, color, and detail are rendered.

## Default visual direction

- Make the environment the subject. Use an eye-level, medium-to-long establishing view that lets the viewer read the place as a whole.
- Keep the camera calm and observational. Avoid low or high angles, dutch tilt, extreme wide-angle distortion, close foreground framing, aggressive vanishing-point emphasis, and strong first-person staging.
- Give the scene no imposed emotional or plot beat. Do not add dramatic weather, theatrical light shafts, suspense cues, or a focal prop unless the user asks for them. Lighting can be beautiful and atmospheric while remaining plausible and restrained.
- Do not add people, character silhouettes, vehicles as protagonists, implied conversations, or empty space designed for a character to stand or interact. If the source contains people, remove them or reduce them to unobtrusive environmental traces only when that can be done without changing the requested scene.
- Keep foreground unobtrusive. Do not introduce framing branches, blurred objects, oversized props, or other close objects that compete with the architecture and environment.
- Preserve the source's recognizable spatial facts: major building masses, openings, paths, floor levels, horizon, and the relationship between foreground, middle distance, and background. Simplify incidental detail, not the scene's identity.

## Manage information density

Read the requested information density as a level of detail, not as permission to change the camera or add story.

- **Sparse:** retain major silhouettes, large planes, and a few distinctive landmarks; merge small objects and surface variation into broad shapes.
- **Balanced (default):** keep the main architecture, visible infrastructure, and a few characteristic details; simplify repetitive windows, clutter, foliage, and texture into grouped shapes.
- **Rich:** preserve more secondary fixtures, material cues, and local variation, while keeping edges, values, and detail selective so the scene remains readable.

At every level, protect the large spatial read first. Use clean anime-background shapes, controlled linework where appropriate, layered but subtle atmospheric perspective, and a limited palette derived from the source or supplied style references. Render surfaces with selective texture rather than photoreal microdetail. Do not invent signage text; keep existing text illegible or omit it unless the user needs it preserved.

## Image roles

When several images are supplied, assign each a role before composing the request:

- **Scene source:** controls subject matter, layout, architecture, and perspective to preserve.
- **Style reference:** controls rendering treatment, palette, edge quality, value grouping, and detail density. Do not copy its scene or composition unless requested.
- **Mood or lighting reference:** controls only the specified light or atmosphere.

The user's written constraints take priority over conflicting incidental content in references. Synthesize common visual traits across references instead of reproducing logos, captions, watermarks, interface frames, or identifiable franchise designs.

## Workflow

1. Identify the scene source, style references, requested information density, and any explicit changes such as season or time of day. If a density level is not specified, use Balanced.
2. Keep the source's camera height and broad composition unless the user requests reframing. If the source is a close or character-led image, adapt to a calm environment view only when the scene can be reconstructed reliably; otherwise state the limitation briefly and preserve the most useful environmental context.
3. Describe the main spatial structure in plain terms, then specify what to retain and what to simplify. Keep lighting, mood, and palette separate from scene content.
4. Generate or edit using the available image-generation tool, with the source and style references explicitly labeled by role. Preserve the source's aspect ratio unless asked to change it.
5. Review the result against the source and brief: Is the location still recognizable? Is the view eye-level and medium/long? Are architecture and spatial relations legible? Did people, foreground framing, dramatic narrative cues, or character interaction space appear without request? Is the detail level consistent across the scene? Revise only the failing aspect.

## Prompt scaffold

Use and adapt this compact specification when it helps:

```text
Use case: anime game environment background
Scene source: [what the source image controls]
Style reference: [what the reference controls; omit if none]
Scene: [place and defining structures]
Composition: calm eye-level medium/long establishing view; preserve [key spatial relations]
Information density: [Sparse / Balanced / Rich]; simplify [details] while retaining [landmarks]
Style: restrained hand-painted anime background, clear grouped forms, selective linework and texture, subtle depth separation
Lighting and palette: [source-faithful or requested conditions]
Constraints: environment only; no characters or interaction staging; no dramatic camera; unobtrusive foreground; no text, logos, UI, or watermark
```

Treat this as guidance, not a requirement to add every phrase to every prompt. Follow the user's explicit artistic direction when it differs from the defaults.
