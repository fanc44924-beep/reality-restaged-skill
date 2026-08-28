---
name: reality-restaged
description: Automatically choose and apply a ZEEJAYZINE-inspired visual art direction when editing or restyling an image, adapting between subject-preserving edits and stronger artistic re-composition.
metadata:
  short-description: Auto-route photos into editorial art styles
---

# Reality Restaged

Use this skill for image edits, restyling, or image-to-image generation when the user wants the visual language of the ZEEJAYZINE zine portfolio. Treat the portfolio as a set of visual principles, not as a request to copy any particular artwork.

## Operating contract

- Inspect the supplied image and the user's explicit instructions before choosing a style.
- Automatically select the best matching profile below. Do not ask the user to choose a profile unless the image is genuinely ambiguous or the user asks for options.
- The user's instructions always override the router: explicit style, subject-preservation, composition, palette, aspect ratio, text, and intensity requests take precedence.
- Default to no added text. If the user supplies copy, use that copy exactly. Do not invent titles, logos, labels, credits, or pseudo-brand text. You may suggest optional literary copy, but only as a separate suggestion and only when the user asks for ideas or accepts recommendations.
- Preserve the main semantic subject as an anchor for portraits, pets, and important objects unless the user asks for a stronger transformation. Preservation means keeping the subject recognizable and compositionally intentional; it does not require preserving the person's identity or exact facial/body features unless the user explicitly asks for that.
- For ordinary landscapes, buildings, streets, or generic snapshots, stronger re-composition is allowed by default: alter scale, weather, perspective, collage boundaries, or surrounding narrative when that improves the selected profile.
- When the user asks for an artistic restyling, collage, layered treatment, or stronger art feeling, prefer a materially transformative profile (usually Surreal photographic collage, Watercolor travel journal, or Minimal paper-and-ink) over a simple color-grade profile. A night scene should use Neon night documentary as the base only when documentary realism is the stated priority; otherwise combine its palette with Surreal photographic collage.
- Return one primary treatment unless the user asks for variants. Briefly state the selected profile and intensity after producing the result.

## Automatic routing

Score each profile against the image using subject, geometry, color, texture, and narrative cues. Choose the highest score, then sanity-check that the result will still serve the user's stated intent.

### 1. Cinematic narrative poster

Choose for solitary figures, dramatic mountains/coasts, roads, caves, winter scenes, or images with a strong film-still feeling.

Apply: restrained cinematic contrast, atmospheric depth, directional light, a quiet narrative moment, muted blue/charcoal/stone palettes with one controlled warm accent, generous negative space, and subtle paper/print grain. Compose like a thoughtful independent-film one-sheet or travel zine cover.

Avoid: glossy blockbuster color grading, excessive lens flares, generic centered hero posing, and automatic typography. Add poster text only when requested.

### 2. Vintage editorial still life

Choose for food, drinks, flowers, table scenes, interiors, fashion objects, or a subject that benefits from a designed magazine spread.

Apply: tactile tabletop staging, cut-paper or printed-paper layering, warm aged stock, deep espresso/olive/ink backgrounds when appropriate, cream highlights, one or two accent colors, star or geometric motifs only when they support the composition, and deliberate editorial negative space.

Avoid: cluttered scrapbook effects, random stickers, plastic 3D rendering, and decorative motifs that compete with the object.

### 3. Perler pixel mosaic

Choose for small, graphic, high-contrast subjects, nostalgic scenes, arcade-like colors, or when the source naturally reads as a grid or bead craft.

Apply: discrete bead/pixel cells, stepped edges, limited palette, controlled dithering, visible handmade irregularity, and a dark or neutral ground that makes the color grid legible. Keep the subject silhouette simple and iconic.

Avoid: smooth painterly gradients, photorealistic micro-detail, and noise that obscures the cell structure.

### 4. Watercolor travel journal

Choose for mountains, lakes, sea, snow, city walks, distant horizons, and scenes with calm observational atmosphere.

Apply: soft watercolor blooms, diluted pigment, dry-brush edges, torn or deckled paper boundaries, pale ivory paper, blue-green-gray mineral colors, restrained ochre/coral accents, and large breathing areas. Let some photographic information dissolve into painted atmosphere while retaining a readable place or gesture.

Avoid: saturated digital gradients, hard vector outlines, uniform blur, and over-rendering every surface.

### 5. Minimal paper-and-ink vignette

Choose for a single figure, chair, garment, vehicle, branch, small object, or a quiet gesture that can carry meaning with very few marks.

Apply: warm off-white paper, thin graphite/ink lines, sparse wash, one muted secondary color (often blue, violet, or moss), small scale cues, and asymmetrical placement with abundant blank space. Favor the feeling of an artist's annotated page rather than a finished commercial illustration.

Avoid: dense backgrounds, polished vector illustration, photorealistic faces, and adding multiple unrelated symbols.

### 6. Surreal photographic collage

Choose when the input supports a dreamlike intervention: floating or tiny people, impossible scale, cut-out skies, image-within-image, abrupt material changes, or a tension between documentary reality and illustration.

Apply: preserve one or two recognizable photographic anchors, then introduce a clear impossible relationship through scale, displacement, torn edges, painted inserts, or empty paper fields. Keep the palette coherent and the surreal gesture legible. Use restrained collage seams and believable light direction.

Avoid: random object multiplication, horror gore, incoherent perspective, and effects that make the subject impossible to read.

### 7. Neon night documentary

Choose for night streets, concerts, clubs, illuminated signs, traffic, or images already containing electric blue, magenta, violet, or colored stage light.

Apply: documentary framing, controlled motion/film grain, deep blue-black shadows, concentrated cyan/magenta/violet light, selective bloom, and a sense of being present in the scene. Preserve spatial cues and the authentic event atmosphere.

If the user emphasizes art direction, collage, or visible material layering, use this profile as a lighting/palette layer and combine it with Surreal photographic collage rather than delivering a conventional night color grade.

Avoid: covering the whole image in neon, synthetic cyberpunk overlays, excessive chromatic aberration, and crushing faces or important details into black.

## Intensity and subject handling

Select an intensity separately from the style profile:

- **Anchor mode**: keep the subject's identity, silhouette, pose, and key objects recognizable; change palette, surface, lighting, and presentation.
- **Restaged mode**: preserve the subject's meaning but permit meaningful changes to pose, scale, crop, environment, and material treatment.
- **Re-authored mode**: use the source as a seed and rebuild composition, narrative, and visual material around the selected profile.

Default routing: portraits, pets, and important products start in Anchor or restrained Restaged mode; generic scenery, architecture, street scenes, and non-essential snapshots may start in Restaged or Re-authored mode. A request to preserve the person's appearance or not change the subject forces Anchor mode. A request for bold transformation or a new composition permits Re-authored mode.

When uncertain, make the smallest change that clearly expresses the style and state the uncertainty instead of silently making a destructive transformation.

## Text policy

Text is not a default component of any profile. If the user requests text:

1. Ask for the exact wording if it is not supplied.
2. Preserve the user's language, spelling, punctuation, and line breaks as far as the medium allows.
3. Match typography to the selected profile only after the copy is fixed.
4. Keep text secondary to the image unless the user explicitly wants a cover/poster dominated by typography.

## Output and safety

- Use the image-generation or image-editing capability available in the current environment; do not assume a specific external service.
- Do not download, overwrite, rename, delete, or reorganize unrelated user files. Read only the supplied image and write outputs only to the path the user requests or the current task's designated output folder.
- Do not embed the portfolio's source images in generated instructions or reproduce a specific work verbatim. Describe the shared visual grammar instead.
- For each completed edit, report: selected profile, intensity, what was preserved, what was re-authored, and whether text was added (normally "none").

## Compact prompt scaffold

Use this internal structure when handing the selected direction to an image model or editing tool:

`[subject and non-negotiable user constraints] + [selected profile] + [palette and material] + [composition and narrative change] + [intensity] + [text policy] + [negative constraints]`

Do not expose this scaffold as a rigid template to the user unless they ask for the prompt itself.

