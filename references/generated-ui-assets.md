# Generated UI Asset Workflow

Use this reference when the presentation should contain image-generated micro UI, subject objects, or decorative interface fragments.

## Required Sequence

1. Identify the presentation subject and inspect any supplied style or reference image.
2. Let the main agent filter the strongest palette and art-direction candidates based on the subject, then present options or `frontend-slides` style previews to the author.
3. Obtain author confirmation of one `Style Lock` before making the full HTML deck or generating UI imagery.
4. Write down the approved `Style Lock`:
   - palette and contrast
   - surface or material feeling
   - geometry and border style
   - icon or object language
   - animation mood
5. Have the main agent build the HTML text skeleton and reserve intentional asset slots under `frontend-slides` constraints.
6. Map the subject to two to four restrained asset families and at least three distinct topic-linked component targets for a short or medium deck; decide each asset's HTML role and quiet animation behavior.
7. For any image generation, require authorization for and spawn a dedicated UI-art subagent. The main agent must not generate thematic UI images directly.
8. Have that subagent use the supported image-generation capability selected during dependency bootstrap, inspect results, and keep only assets that match the approved style, subject, and supporting role. In Codex, the subagent uses `imagegen`.
9. Integrate selected assets into HTML with real layout, text, and restrained animation.
10. Validate author approval, subagent use, visual match, readability, import-ready format, transparency, and viewport fit.

## UI Art Brief And Handoff

The main agent owns the deck. The dedicated art subagent owns only generated visual assets.

Give the art subagent:

- presentation topic and the author-approved `Style Lock`
- palette, materials, geometry, line style, depth, and mood
- reference image(s) labeled as style guidance unless an edit was requested
- two to four assets to produce and the HTML role of each
- enough distinct pieces to form a usable themed kit rather than a single universal decoration
- approximate asset slot size, placement, and needed blank space
- output constraints: supporting visual role only, no meaningful text, no invented values, no watermark, transparent or removable background where appropriate
- format preference: SVG-ready/simple geometric UI where possible; transparent PNG/WebP for textured or material-rich pieces
- motion intent: gentle entrance, line draw, fade, mask reveal, or low-opacity background drift
- a workspace destination for final selected images

Require this handoff back:

| Returned Item | Purpose |
| --- | --- |
| Selected asset path | lets the main agent integrate an actual project file |
| HTML role and target slide | avoids decorative dumping |
| Transparency or background status | confirms whether it can float cleanly in the deck |
| Format recommendation | states SVG reconstruction or transparent image delivery |
| Placement note | states crop, opacity, mask, or entrance suggestion |
| Rejected or unresolved item | makes missing or unsuitable UI visible rather than silently omitted |

If the subagent cannot access image generation, it should return the prepared prompts and state the limitation. The main agent must not take over image generation for this skill. It may offer a separately approved non-generated SVG/CSS route.

## Distinctive Themed Kit Rule

Do not accept a generated UI result merely because it matches the palette. It must carry recognizable subject matter.

- A normal generated kit should provide at least three separately placeable, topic-linked pieces for a short or medium deck; use more only when the narrative has space for them.
- One piece should establish the subject immediately, such as a controller form for esports, a boarding-pass fragment for travel, or a coffee pickup tab for a campus cafe.
- Supporting pieces can be quieter, such as a trophy marker, waypoint chip, loyalty stamp, or target reticle, but they still need contextual meaning.
- Plain dividers, underlines, dots, empty rounded cards, and generic pills can accompany the kit; they must not be the entire kit.
- If a generic card shell is required for HTML text, customize its silhouette, corner mark, status ornament, or object pairing so it belongs to the subject.
- Keep variety across the full deck and restraint per slide: multiple available assets do not mean showing all of them at once.

## Asset Roles

| Role | Generate | Build in HTML |
| --- | --- | --- |
| Hero object | styled thematic object or UI cluster with no required text | title, subtitle, placement, crop, entrance motion |
| Text-card shell | empty or nearly empty visual card frame | all copy, figures, labels, responsive padding |
| Background motif | large soft object, pattern, lines, or faded device fragment | opacity, blur, mask, layering, movement |
| Accent kit | badges, controls, target marks, trophy, ticket, icon-like objects | positioning, repetition, hover or slide animation |
| Data evidence | optional blank frame or ornament | actual chart bars, values, sources, and legends |

## Generation Guidance

Treat supplied images as style and palette references unless asked to edit them. The generated subject must also fit the presentation topic.

For example:

- Reference style: warm off-white ground, frosted pale blue panels, muted gold and dusty red accents, thin outline work.
- Presentation topic: esports.
- Suitable generated assets: rounded keyboard fragments, controller forms, directional keycaps, target dividers, achievement emblems, empty match-card shells.
- Unsuitable result: generic dark neon gaming dashboard that ignores the reference style.
- Also unsuitable: a matching-color collection made only of blank cards and divider lines without controllers, keys, tournament or play-related forms.

For asset prompts, specify:

- intended HTML role and available blank space
- topic-specific object
- locked palette and material treatment
- transparent or removable-background requirement where needed
- no watermark and no unwanted text
- no factual numbers unless supplied by the user

Prefer separate usable assets for final composition. A contact-sheet or style board is useful for choosing direction, but individual assets are easier to place, animate, mask, and reuse in HTML.

## Figma-Friendly Delivery

Treat `Figma-friendly` as import-ready and cleanly editable where feasible, not as automatic conversion of generated pixels into editable Figma components.

- Prefer SVG or inline SVG for thin-outline dividers, targets, keycaps, badges, geometric shells, and other simple pieces that need editability or line-draw animation.
- Prefer transparent PNG or WebP for frosted, textured, shaded, or softly rendered objects that do not need vector editing.
- When image generation establishes the style for a simple UI form, recreate the selected final part as SVG rather than embedding a blurry raster ornament.
- Avoid tiny baked-in labels, numbers, or dense screens; keep live content in HTML or Figma text layers.

## Image Format And Transparency

Generated images are bitmap assets, not editable HTML components. Use them as visual layers inside HTML.

- Prefer final PNG or WebP with alpha for foreground objects, card shells, ornaments, and floating fragments.
- In Codex, follow the installed `imagegen` skill for transparent-output generation and alpha validation. In another host, use only a transparency or background-removal workflow supported by its configured image provider.
- Prefer ordinary opaque images only for full-bleed panels or backgrounds where transparency is unnecessary.
- Keep important text out of generated images because it may render inaccurately and cannot adapt responsively.
- Store final selected project-bound assets in the presentation workspace before HTML integration. Do not reference temporary or generator-default output locations as final project assets.

For a single-file presentation, embed selected final assets as data URLs in the HTML when practical. For an accepted multi-file deck, store selected assets beside the HTML and reference them with relative paths.

## HTML Composition Ideas

These patterns are examples rather than restrictions:

- Overlay live HTML copy on a generated blank card shell.
- Place a transparent object partly outside a slide edge and reveal it with a slight angled entrance.
- Use a large low-opacity generated fragment behind the title as atmosphere.
- Mask or blur a generated panel to create depth behind a statistic or quote.
- Repeat one small generated marker as a navigation rhythm or section divider.
- Pair a generated product or game object with native HTML indicators and factual labels.
- Animate small SVG marks with line draw or mask reveal, and soften decorative bitmap elements with low-opacity entrance or gentle drift.

Do not let a bitmap become a substitute for layout reasoning. The final HTML must still establish hierarchy, spacing, animation, accessibility, and readable information.

## Review Checklist

- Does every chosen asset match the approved style and palette?
- Does every asset clearly relate to the presentation topic?
- Does the final kit contain multiple independently usable topic-linked pieces rather than generic framework decoration alone?
- Was style approved before any image-generation pass?
- Was every image-generation pass run by the dedicated UI-art subagent?
- Are key words, numbers, and sourced claims still HTML rather than unreliable image text?
- Are simple editable UI pieces SVG-ready where Figma use matters?
- Are alpha edges clean when the asset floats above the slide background?
- Does each animation support the narrative rather than distract from it?
- Would removing an asset weaken the message or sense of world? Remove it if not.
