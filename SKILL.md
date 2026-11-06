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

At every level, protect the large spatial read first. Use clear anime-background shapes, selective edge accents rather than ink outlines, layered atmospheric perspective, and a palette derived from the source or supplied style references. Render surfaces with fine integrated tonal grain and airbrush shading rather than photoreal microdetail or coarse brush marks. Distribute detail according to light and depth: preserve the most information in the brightest focal area, simplify shadowed areas and distant forms. Do not invent signage text; keep existing text illegible or omit it unless the user needs it preserved.

## Preserve the source's color and light

- Treat the source image's overall color cast, saturation, and value balance as scene facts. Do not warm, cool, brighten, darken, or otherwise recolor the whole image unless the user requests it. In particular, preserve muted or gray-leaning palettes instead of defaulting to vivid golden anime light.
- Preserve the source's light direction, distribution, haze, and atmospheric depth. Keep painterly bloom and diffusion when visible. Maintain clear value contrast, but use broad airbrush transitions to soften the boundary between light and shadow; reserve crisp edges for selected material or cast-shadow boundaries that are visibly sharp in the source.
- Group shadows into stable, intentional masses. When the source lacks a broad shadow shape, identify a plausible occluded region already present in the composition (such as the underside of a canopy, a deep arcade, or the area beneath an overhang) and unify it into a coherent shadow plane. Keep its boundary tied to the architecture and light direction; avoid scattered, disconnected dark patches or unstable shifts in shadow value. Preserve enough reflected light and structural detail within the mass to keep the form readable.
- Reduce fine detail in shadowed regions by about 50% compared with the main lit area. Keep the large shadow shapes stable and legible, but merge small fixtures, textures, and edges into broad value groups. Shadow color should be less saturated than lit color unless the source clearly shows otherwise; retain the source's shadow hue in a restrained form rather than defaulting to vivid blue or teal.
- Reduce fine detail in the far distance by about 70% compared with the main lit focal area. Use layered, spatially broad airbrush veils in front of distant forms to soften their contrast and detail and push them farther back. Let this airbrush atmospheric treatment reduce information, not merely add a uniform blur; preserve the distant silhouette and large spatial cues.
- Keep the brightest area as the scene's primary detail anchor. Concentrate the clearest edges, strongest local contrast, and most secondary information there. Let information density taper through midtones, shadow masses, and distant planes.
- Use a polished CG-like game-art finish with fine, subtle tonal grain and layered airbrush shading. Grain should feel integrated into the paint, like a delicate stippled rendering texture rather than literal digital noise. Keep texture fine and controlled; avoid broad, chunky, visibly streaked brush marks.
- Define forms through grouped color, value, and selective edges. Do not add uniform ink outlines or strong contour linework. Keep the painted surface and subtle airbrush transitions visible without making the image look rough or unfinished.
- Determine the dominant light color from the source's time of day and overall color cast. Dawn light may lean softly pink, sunset light may lean yellow-orange, midday light should generally stay neutral or near-white, and night lighting should follow the scene's actual cool or artificial light sources. These are cues, not mandatory filters; do not assign warm highlights and cool shadows automatically.
- If the source has a clear overall color bias (for example, cool, greenish, or another distinct cast), carry that dominant hue through the overall palette in a controlled way. Preserve that source color identity instead of imposing a generic warm/cool scheme.
- Keep shadow saturation subdued by default while allowing lit colors to retain the source's saturation. Maintain any real cool-warm relationship in the source, but do not invent one when the source does not support it.
- Preserve the source's overall palette and tonal identity unless the user asks to change them. By default, create a full, clearly legible tonal range: deep shadow masses approach near-black and the brightest lit planes approach near-white, with enough midtones to retain form, haze, and atmosphere.
- Let highlights follow the observed light color and retain their appropriate saturation. Add a restrained airbrush glow around the brightest areas only when supported by the source. Keep the glow within the source's light pattern; do not invent light sources, flatten shadows, or add dramatic shafts.
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
4. Generate or edit using the available image-generation tool, with the source and style references explicitly labeled by role. Preserve the source's aspect ratio unless asked to change it. Specify fine airbrush grain, controlled CG-like rendering, the source-appropriate light color, reduced shadow saturation, soft light-shadow transitions, shadow detail reduction, distant detail reduction, and the brightest area's information priority.
5. Review the result against the source and brief: Is the location still recognizable? Is the view eye-level and medium/long? Are architecture and spatial relations legible? Are shadow details simplified by about half and distant details by about 70%? Does the brightest area hold the most information? Are airbrush veils pushing distant forms back? Are light-shadow transitions appropriately soft? Does light color match the source's time of day and overall cast? Revise only the failing aspect.

## Prompt scaffold

Use and adapt this compact specification when it helps:

```text
Use case: anime game environment background
Scene source: [what the source image controls]
Style reference: [what the reference controls; omit if none]
Scene: [place and defining structures]
Composition: calm eye-level medium/long establishing view; preserve [key spatial relations]
Information density: [Sparse / Balanced / Rich]; simplify [details] while retaining [landmarks]
Style: polished CG-like anime game background, fine airbrush-rendered tonal grain, soft value transitions, low-detail shadow masses, no ink outlines, selective edge accents
Lighting and palette: preserve [source palette and light pattern]; subdued shadow saturation; light color appropriate to [time of day and source color cast]; broad atmospheric airbrush veils reduce distant detail; brightest area carries the most information
Constraints: environment only; no characters or interaction staging; no dramatic camera; unobtrusive foreground; no text, logos, UI, or watermark
```

Treat this as guidance, not a requirement to add every phrase to every prompt. Follow the user's explicit artistic direction when it differs from the defaults.
