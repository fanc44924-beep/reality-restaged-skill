# Reality Restaged Prompt Library

这些提示词用于测试 ZEEJAYZINE / 拾景 zine 作品集提炼出的视觉语法。它们描述共同的艺术规律，不复制任何一张具体作品。

## 使用方法

把“基础编辑约束”放在提示词前面，再选择一个“风格提示词”，最后追加一个“强度模块”。如果只想快速测试，也可以直接使用下面的完整风格提示词。

默认：不添加文字、不添加 logo、不添加水印。用户没有明确要求时，不要生成海报标题或装饰性伪文字。

---

## 基础编辑约束

```text
Use the supplied image as the edit target, not as a loose inspiration. Preserve the main subject's semantic identity and make the transformation intentional. Keep believable perspective, coherent light direction, and a readable focal point. Do not add logos, watermarks, random text, invented labels, or unrelated objects. The result should feel like a considered art-book or independent zine image, not a generic filter preset.
```

## 自动判断风格

```text
Analyze the supplied image before editing. Choose the single best visual direction from these seven profiles: cinematic narrative poster, vintage editorial still life, perler pixel mosaic, watercolor travel journal, minimal paper-and-ink vignette, surreal photographic collage, or neon night documentary. Score the image by subject, geometry, color, texture, and narrative potential. Prefer an art-forward transformation over a simple color grade when the user asks for an artistic restyling. For portraits, pets, and important objects, keep the semantic subject recognizable unless the user requests a stronger re-authorship. For ordinary landscapes, architecture, streets, and generic snapshots, allow more aggressive re-composition. Default to no text.
```

---

## 1. 电影感叙事海报

```text
Transform the supplied image into an art-forward cinematic narrative poster in the visual language of a quiet independent travel film. Preserve the main subject as a readable story anchor, but redesign the atmosphere with restrained cinematic contrast, layered atmospheric depth, directional practical light, and a deliberate moment of solitude. Use muted blue, charcoal, stone, and smoke tones with one controlled amber or rust accent. Introduce subtle printed-paper grain, imperfect ink density, and a tactile zine surface. Compose with strong negative space, asymmetrical balance, and a sense that the image is one frame from a larger story. Do not add typography unless exact user copy is supplied. No logos, no watermark, no generic blockbuster grading, no excessive lens flare, no centered hero pose, no plastic skin.
```

## 2. 复古杂志静物拼贴

```text
Transform the supplied image into a tactile vintage editorial still-life collage. Preserve the main object or subject clearly, then stage it like a thoughtful independent magazine spread on warm aged stock. Use cut-paper layers, printed-paper edges, restrained editorial geometry, deep espresso or olive ink fields when appropriate, cream highlights, and one or two controlled accent colors. Add subtle halftone, ink spread, paper fibers, and slight registration imperfection. Decorative stars or geometric marks are allowed only when they support the composition. Keep negative space intentional and the object visually dominant. No random stickers, no cluttered scrapbook look, no plastic 3D rendering, no invented text, no logos, no watermark.
```

## 3. 珠串 / 像素马赛克

```text
Rebuild the supplied image as a handmade perler-bead pixel mosaic. Reduce the subject into a clear iconic silhouette and discrete bead-like cells with stepped edges, a limited deliberate palette, controlled dithering, and visible small-scale handmade irregularity. Keep the subject recognizable but let photographic detail resolve into a grid of colored pieces. Use a dark or neutral ground so the mosaic structure remains legible. The result should feel crafted, tactile, and slightly imperfect, not like a smooth pixel-art filter. No smooth painterly gradients, no photorealistic micro-detail, no random noise that hides the cell structure, no text, no logo, no watermark.
```

## 4. 水彩旅行画册

```text
Transform the supplied image into a tactile watercolor travel-journal plate. Preserve the key place, building, landscape, or gesture so it remains readable, but allow photographic information to dissolve into painted atmosphere. Use warm ivory paper, diluted mineral blue and blue-green pigment, pale stone, restrained ochre or coral accents, soft watercolor blooms, dry-brush edges, selective graphite and ink linework, and subtle torn or deckled paper boundaries. Keep large breathing areas and an asymmetrical art-book composition. Retain the original sense of place and believable geometry. No saturated digital gradients, no HDR sharpness, no uniform blur, no cartoon outlines, no invented buildings or people, no typography, no logos, no watermark.
```

## 5. 极简纸面与线稿

```text
Re-compose the supplied image as a minimal paper-and-ink vignette. Reduce the scene to one meaningful figure, object, garment, vehicle, branch, or gesture with warm off-white paper, thin graphite and ink lines, sparse wash, and one muted secondary color such as blue, violet, or moss. Use abundant blank space, quiet asymmetry, delicate scale cues, and the feeling of an artist's annotated page. Keep only the visual information that strengthens the subject's emotional or poetic meaning. Do not fill the background with detail. Avoid polished vector illustration, photorealistic facial rendering, multiple unrelated symbols, decorative clutter, text, logos, and watermarks.
```

## 6. 超现实摄影拼贴

```text
Transform the supplied image into an art-forward surreal photographic collage. Keep one or two recognizable photographic anchors, then create one clear impossible relationship through altered scale, displacement, cut-out sky, image-within-image, torn paper boundaries, painted inserts, or an unexpected material transition. The surreal intervention must feel designed and legible, not random. Combine documentary photographic texture with hand-painted marks, empty paper fields, restrained collage seams, and believable shared light direction. Preserve the emotional meaning of the main subject while allowing the environment, proportion, and narrative to be substantially re-authored. No random object multiplication, no incoherent perspective, no gore, no generic fantasy background, no invented typography, no logo, no watermark.
```

## 7. 霓虹夜景纪实

```text
Transform the supplied image into an art-directed neon night documentary with cinematic narrative. Preserve the central subject, event context, and spatial cues, then shape the image with deep blue-black shadows, concentrated cyan and amber practical lights, restrained magenta or violet accents, selective bloom, controlled motion or film grain, and tactile printed-zine texture. Use documentary framing and a sense of being physically present in the scene. The result must contain a visible artistic treatment beyond a basic color grade: introduce purposeful atmospheric layering, graphic light rhythm, and editorial framing while keeping the subject readable. No synthetic cyberpunk overlays, no excessive chromatic aberration, no crushed faces, no plastic skin, no text, no logo, no watermark.
```

---

## 强度模块

### Anchor mode：主体优先

```text
Anchor mode: keep the subject's silhouette, placement, pose, and key objects recognizable. Change palette, lighting, surface, texture, and presentation, but do not substantially rebuild the scene. If a person is present, preserve the requested identity only when the user explicitly asks to preserve their appearance.
```

### Restaged mode：重新编排

```text
Restaged mode: preserve the subject's meaning and focal importance, but permit meaningful changes to crop, scale, pose, surrounding atmosphere, background material, and visual layering. Keep the result coherent and readable.
```

### Re-authored mode：强艺术再创作

```text
Re-authored mode: use the supplied image as a visual seed and rebuild the composition, spatial relationships, material language, and narrative around the chosen style. Keep at least one recognizable anchor from the source, but allow bold changes to scale, environment, perspective, collage boundaries, and painted or printed material.
```

---

## 文字模块

默认不添加文字。用户要求文字时追加：

```text
Text policy: add typography only from exact user-supplied copy. Preserve the wording, spelling, punctuation, language, and requested line breaks. Do not invent titles, labels, credits, brand names, or pseudo-text. Keep typography secondary to the image unless the user explicitly requests a text-led cover or poster.
```

如果用户还没有提供文案，但希望你推荐，可以先单独输出候选文案，等待用户选定后再生成，不要直接把推荐文案写进图片。

---

## 第一张夜景照片的加强测试词

这一张不建议只用“霓虹夜景纪实”。建议使用“超现实摄影拼贴 + 电影感叙事海报”，并采用 Re-authored mode：

```text
Use the supplied snowy night photograph as the edit target. Re-author it as a surreal photographic collage with the visual grammar of a quiet independent zine and cinematic narrative poster. Keep the white-dressed woman in the snowy square as the unmistakable emotional anchor, including her ornate costume silhouette and open-hand gesture, but redesign the surrounding space into a deliberate dreamlike stage. Turn the dark foreground spectators into layered cut-paper silhouettes that frame the subject rather than obscure her. Let amber street lights become small constellations of warm printed marks, while the snow becomes a pale blue-gray paper field with watercolor and ink abrasion. Introduce one clear impossible relationship: the woman's illuminated figure appears slightly detached from the ground as if emerging from a torn photographic aperture, with a soft painted shadow reconnecting her to the snow. Use deep indigo, charcoal, amber, muted cream, and a restrained violet accent; combine documentary grain, paper fibers, hand-painted edges, and subtle collage seams. Preserve believable light direction and the readable human gesture. The result must feel materially transformed and art-directed, not merely color graded. No added people, no random objects, no text, no logos, no watermark, no gore, no cyberpunk overlays, no excessive lens flare, no plastic skin, no crushed facial detail.
```

## 第二张建筑照片的测试词

```text
Use the supplied architectural photograph as the edit target. Re-compose it as a watercolor travel-journal art-book page with warm ivory paper, torn pigment edges, visible paper fibers, diluted cobalt and mineral blue washes, pale ochre stone, selective graphite and ink contours, and generous negative space. Keep the domed historic building, diagonal upward perspective, ornate facade, and clock clearly readable as the primary subject. Allow the blue sky to dissolve into layered watercolor atmosphere and let a few architectural details fade into dry-brush texture, while preserving the strong geometry and sense of place. Add subtle imperfect registration and hand-painted variation, but no decorative clutter. No added buildings, no people, no text, no logos, no watermark, no HDR sharpness, no synthetic digital gradient, no uniform blur, no cartoon outline.
```

---

## 输出检查

```text
Before finalizing, check that the selected style is visible in materials, composition, and narrative treatment, not only in color. Check that the main subject remains readable at a glance, that light and perspective are coherent, that no unwanted text or watermark appeared, and that the result is not a generic filter preset. Report the selected profile, intensity, what was preserved, what was re-authored, and whether text was added.
```

