# Generated UI Asset Workflow

Use this reference when the presentation should contain image-generated micro UI, subject objects, or decorative interface fragments.

## Required Sequence

1. Identify the presentation subject and the selected style or reference image.
2. Write a short art-direction lock before generating anything:
   - palette and contrast
   - surface or material feeling
   - geometry and border style
   - icon or object language
   - animation mood
3. Have the main agent build the HTML text skeleton and reserve intentional asset slots under `frontend-slides` constraints.
4. Map the subject to two to four suitable asset families and decide each asset's HTML role.
5. If parallel delegation has been requested or approved and is supported, hand a `UI Art Brief` to a dedicated art subagent while the main agent continues typography and layout. Otherwise run the same art pass sequentially.
6. Use the supported image-generation capability selected during dependency bootstrap, generate previews or selected assets, inspect them, and keep only assets that match both style and subject. In Codex, use `imagegen`.
7. Integrate selected assets into HTML with real layout, text, and animation.
8. Validate visual match, readability, transparency, and viewport fit.

## UI Art Brief And Handoff

The main agent owns the deck. The dedicated art subagent owns only generated visual assets.

Give the art subagent:

- presentation topic and the approved visual thesis
- palette, materials, geometry, line style, depth, and mood
- reference image(s) labeled as style guidance unless an edit was requested
- two to four assets to produce and the HTML role of each
- approximate asset slot size, placement, and needed blank space
- output constraints: no meaningful text, no invented values, no watermark, transparent or removable background where appropriate
- a workspace destination for final selected images

Require this handoff back:

| Returned Item | Purpose |
| --- | --- |
| Selected asset path | lets the main agent integrate an actual project file |
| HTML role and target slide | avoids decorative dumping |
| Transparency or background status | confirms whether it can float cleanly in the deck |
| Placement note | states crop, opacity, mask, or entrance suggestion |
| Rejected or unresolved item | makes missing or unsuitable UI visible rather than silently omitted |

If the subagent cannot access image generation, it should return the prepared prompts and state the limitation. The main agent may then run image generation itself if available, but must not claim that generated UI already exists.

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

For asset prompts, specify:

- intended HTML role and available blank space
- topic-specific object
- locked palette and material treatment
- transparent or removable-background requirement where needed
- no watermark and no unwanted text
- no factual numbers unless supplied by the user

Prefer separate usable assets for final composition. A contact-sheet or style board is useful for choosing direction, but individual assets are easier to place, animate, mask, and reuse in HTML.

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

Do not let a bitmap become a substitute for layout reasoning. The final HTML must still establish hierarchy, spacing, animation, accessibility, and readable information.

## Review Checklist

- Does every chosen asset match the approved style and palette?
- Does every asset clearly relate to the presentation topic?
- Are key words, numbers, and sourced claims still HTML rather than unreliable image text?
- Are alpha edges clean when the asset floats above the slide background?
- Does each animation support the narrative rather than distract from it?
- Would removing an asset weaken the message or sense of world? Remove it if not.
