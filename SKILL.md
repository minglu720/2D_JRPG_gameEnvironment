---
name: anime-scene-background
description: Transform supplied photographs or scene descriptions into polished, CG-like anime game environment backgrounds with fine airbrush-rendered grain, strong cool-warm light contrast, and preserved spatial structure. Use when creating or restyling environment art with calm, eye-level medium or long shots and no character-centered staging.
metadata:
  short-description: Style game environment backgrounds
---

# Anime Scene Background

Turn a real place or scene brief into a coherent, polished anime-inspired game background with a CG-like rendered finish. Treat scene structure and visual style as separate inputs: the source photo or scene description defines what is there and how spaces connect; style references define how forms, light, color, and detail are rendered.

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

At every level, protect the large spatial read first. Use clear anime-background shapes, selective edge accents rather than ink outlines, layered atmospheric perspective, and a palette derived from the source or supplied style references. Render surfaces with fine integrated tonal grain and airbrush shading rather than photoreal microdetail or coarse brush marks. Do not invent signage text; keep existing text illegible or omit it unless the user needs it preserved.

## Preserve the source's color and light

- Treat the source image's overall color cast, saturation, and value balance as scene facts. Do not warm, cool, brighten, darken, or otherwise recolor the whole image unless the user requests it. In particular, preserve muted or gray-leaning palettes instead of defaulting to vivid golden anime light.
- Preserve the source's light distribution, softness, haze, and apparent light density. Keep painterly bloom, diffusion, and atmospheric depth when they are visible; do not clean them away or replace them with crisp, hard-edged illumination.
- Group shadows into stable, intentional masses. When the source lacks a broad shadow shape, identify a plausible occluded region already present in the composition (such as the underside of a canopy, a deep arcade, or the area beneath an overhang) and unify it into a coherent shadow plane. Keep its boundary tied to the architecture and light direction; avoid scattered, disconnected dark patches or unstable shifts in shadow value. Preserve enough reflected light and structural detail within the mass to keep the form readable.
- Use a polished CG-like game-art finish with fine, subtle tonal grain and layered airbrush shading. Grain should feel integrated into the paint, like a delicate stippled rendering texture rather than literal digital noise. Keep texture fine and controlled; avoid broad, chunky, visibly streaked brush marks.
- Define forms through grouped color, value, and selective edges. Do not add uniform ink outlines or strong contour linework. Keep the painted surface and subtle airbrush transitions visible without making the image look rough or unfinished.
- Maintain the source's cool-warm color relationships. Where the source supports it, retain cool ambient shadows against warmer lit stone (or the reverse), without shifting the overall palette.
- Preserve the source's overall palette and tonal identity unless the user asks to change them. By default, create a full, clearly legible tonal range: deep shadow masses approach near-black and the brightest lit planes approach near-white, with enough midtones to retain form, haze, and atmosphere.
- For requested high-contrast sunlight, separate cool, deep shadows from warm highlights. Allow sunlit edges and planes to have selective harder boundaries, with a restrained warm airbrush glow around the brightest areas. Keep the glow within the light's existing spatial logic; do not wash the whole image in warm color or flatten the light-shadow pattern.
- If the user gives a numeric contrast request, treat it as an adjustment to light-shadow separation. A later request for stronger contrast supersedes an earlier lower contrast target. Do not interpret contrast as global saturation.

## Image roles

When several images are supplied, assign each a role before composing the request:

- **Scene source:** controls subject matter, layout, architecture, and perspective to preserve.
- **Style reference:** controls rendering treatment, palette, edge quality, value grouping, and detail density. Do not copy its scene or composition unless requested.
- **Mood or lighting reference:** controls only the specified light or atmosphere.

When installed from this repository, use images in `references/assets/style-references/` as the default rendering and palette guide if the user has not supplied another style reference. Inspect only a few relevant examples. These images guide edge quality, value grouping, palette, and information density; they do not override the user's scene, camera, or constraints.

The user's written constraints take priority over conflicting incidental content in references. Synthesize common visual traits across references instead of reproducing logos, captions, watermarks, interface frames, or identifiable franchise designs.

## Workflow

1. Identify the scene source, style references, requested information density, and any explicit changes such as season or time of day. If a density level is not specified, use Balanced.
2. Keep the source's camera height and broad composition unless the user requests reframing. If the source is a close or character-led image, adapt to a calm environment view only when the scene can be reconstructed reliably; otherwise state the limitation briefly and preserve the most useful environmental context.
3. Describe the main spatial structure in plain terms, then specify what to retain and what to simplify. Keep lighting, mood, and palette separate from scene content.
4. Generate or edit using the available image-generation tool, with the source and style references explicitly labeled by role. Preserve the source's aspect ratio unless asked to change it. Specify the fine airbrush grain, controlled CG-like rendering, tonal endpoints, and cool-warm light relationship directly in the prompt.
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
Style: polished CG-like anime game background, fine airbrush-rendered tonal grain, controlled painted transitions, no ink outlines, selective edge accents
Lighting and palette: preserve [source palette and light pattern]; deep cool shadows approaching near-black, warm lit planes approaching near-white, fine atmospheric haze and restrained airbrush glow
Constraints: environment only; no characters or interaction staging; no dramatic camera; unobtrusive foreground; no text, logos, UI, or watermark
```

Treat this as guidance, not a requirement to add every phrase to every prompt. Follow the user's explicit artistic direction when it differs from the defaults.
