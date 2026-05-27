---
name: themed-ui-slides
description: Create or enhance browser-based HTML presentations through a dedicated art-directed micro UI production pass while using frontend-slides as the base workflow. Use when a deck, pitch, class presentation, report, product launch, or converted presentation needs a locked color and art direction, reference-image-matched UI illustration, extractable thematic asset kits, controller or HUD pieces, app cards, chat panels, timelines, receipts, itinerary cards, or an authorized parallel UI-art subagent generating assets while the main agent builds HTML typography and layout.
---

# Themed UI Slides

Create refined HTML presentations whose small visual designs are deliberately made for the subject, not added as generic decoration.

## Base Workflow

Use this skill alongside `frontend-slides`.

1. Run the dependency bootstrap below before designing or generating assets.
2. Load and follow the `frontend-slides` skill for presentation creation, conversion, navigation, inline editing, motion, delivery, and viewport-fitting rules.
3. Load a supported image-generation capability whenever generating new bitmap UI assets, visual motifs, transparent cutouts, or style-matched decorative elements. In Codex, use the bundled `imagegen` skill and tool.
4. Treat every invariant from `frontend-slides` as mandatory, especially single-file HTML delivery, slide density limits, `clamp()` sizing, `overflow: hidden`, responsive height checks, and required supporting CSS.
5. Make the UI art pass central whenever the user requests thematic small designs or generated UI: lock a visual world, produce topic-specific UI assets, and compose the selected assets into the deck.
6. Apply this skill as an enhancement layer for art direction, image-generated assets, and micro UI composition only. Do not replace or weaken the base workflow.

## Compatibility With Frontend Slides

`frontend-slides` remains authoritative for content discovery, style approval, HTML architecture, responsive fitting, interaction, and final delivery. This skill inserts a focused art-production workflow after the style direction is chosen and before the deck is finalized.

- Do not begin asset generation before `frontend-slides` style discovery is complete or the user has already supplied a clear visual reference and palette.
- The main agent may build slide structure, live text, CSS tokens, and reserved image slots while art is being produced, but it must not pretend the generated-UI requirement is complete with placeholders alone.
- Keep titles, factual content, charts, labels, and important copy in HTML. Generated UI supplies forms, surfaces, subject objects, frames, ornaments, and atmosphere.
- If an asset makes a slide too dense, reduce the asset, move it to another slide, or split the slide under `frontend-slides` rules. Never shrink key text to make decoration fit.
- If instructions ever conflict, preserve the mandatory viewport, density, single-file, accessibility, and delivery constraints from `frontend-slides`.

## Dependency Bootstrap

Check required skills before beginning the presentation workflow.

### Frontend Slides

Require `frontend-slides` for the HTML presentation workflow.

- If it is already available, load it and continue.
- If it is missing, retrieve it only from the public repository `https://github.com/zarazhangrui/frontend-slides`.
- In Codex, use the installed `skill-installer` workflow, using the repository root as the skill folder and the installed name `frontend-slides`.
- In Claude Code or another host, use that host's supported plugin/skill installation or repository-reading workflow. If the host requires the user to run an install or authorization step, explain the trusted repository source and ask for that required confirmation before continuing.
- After installing, read its `SKILL.md` directly and continue the current task when local file access allows it. Tell the user when their host needs a restart or reload for normal discovery in later conversations.
- If installation fails or network access is unavailable, stop before producing the final deck and state that the required HTML presentation foundation could not be retrieved.

### Image Generation Capability

Require an actual image-generation capability whenever the requested design uses newly generated UI assets. A Markdown skill describes a workflow; it does not provide a model or grant tool access by itself.

- In Codex, if `imagegen` is available, load it and continue. Treat it as a Codex system skill, not a third-party visual pack; do not silently download an unrelated replacement with the same name.
- In Claude Code or another host, use a configured image-generation tool, plugin, MCP integration, or user-approved API workflow only when that capability is actually accessible in the environment.
- If an API-based image provider needs credentials, ask the user to configure the secret locally; never ask them to paste an API key into chat.
- If no image-generation capability is available, do not claim that generated thematic UI was produced. Explain the missing capability and ask the user to either configure an image-generation integration or provide prepared visual assets.
- Offer a CSS/SVG-only approximation only as an explicit fallback, and use it only after the user agrees that the result will not contain image-generated UI assets.

## Design Process

### 1. Lock the Visual World Before Generation

Do not generate UI assets until the deck has one agreed or clearly inferred visual direction. Extract:

- subject, audience, and purpose
- language used in the deck
- mood and style direction chosen through the base workflow or supplied through a reference image
- palette, contrast, texture, edge treatment, dimensionality, icon style, and motion character
- concrete objects associated with the topic, such as transactions, routes, messages, inventory, lessons, metrics, bookings, or model outputs

Choose one clear visual thesis. Examples:

- Campus coffee marketing: mobile order cards, coupon chips, footfall pulse, membership tier badge.
- AI customer service: chat transcript, confidence status, routing queue, resolution timer.
- Travel proposal: boarding pass strip, day-plan card, map stop chip, budget receipt.
- Soft editorial esports: frosted ivory surfaces, dusty blue/gold/red accents, rounded outlined keycaps, controller pieces, target markers, trophy dividers.

If the user supplies an image as the palette or style reference, use it as visual guidance rather than an edit target unless the user explicitly asks to change that image. If no style has been chosen, finish `frontend-slides` style discovery before generating assets.

Read [references/micro-ui-patterns.md](references/micro-ui-patterns.md) and [references/generated-ui-assets.md](references/generated-ui-assets.md) before implementation.

### 2. Build the Layout Skeleton and UI Art Brief

After the visual direction is locked, have the main agent read the mandatory Phase 3 supporting files required by `frontend-slides`, then begin the HTML structure and text typography using that workflow. It should establish CSS variables, slide hierarchy, live text, and intentional slots for generated assets before final composition.

At the same time, write a concise `UI Art Brief` for the art-production pass:

- presentation subject and narrative purpose
- approved palette, materials, shapes, line weight, depth, and motion mood
- reference-image role: style reference, not edit target, unless explicitly requested
- two to four topic-specific asset families
- intended slide slot for each asset: dimensions or aspect, approximate placement, foreground or background role, and required empty space
- output requirement: text-free or blank-shell assets, preferably isolated PNG or WebP cutouts where suitable
- avoid list: generic off-theme UI, watermark, unwanted text, invented data, and visual clutter

Choose at most three component families for a short or medium deck, and at most four for a long deck. Reuse the same visual grammar rather than inventing a new widget on every slide.

Use micro UI only when it does at least one job:

- turns an abstract claim into a visible signal
- provides a setting or user perspective
- makes a comparison easier to grasp
- creates a memorable hero moment

Do not insert interface panels merely to fill space. A cultural essay, emotional speech, or highly photographic story may need almost no UI.

When the intended style depends heavily on generated imagery, create a compact style-board preview first, then generate selected assets as separate usable cutouts. Do not rely on cropping many finished assets from one crowded board.

### 3. Run the Dedicated UI Art Production Pass

Use a dedicated UI-art worker when the host supports subagents and the user has explicitly requested or approved delegation or parallel production.

Parallel ownership:

- **Main agent:** build the HTML skeleton, text hierarchy, CSS theme tokens, slide structure, responsive constraints, and clearly sized asset slots. It owns all final HTML editing and viewport validation.
- **UI-art subagent:** use the `UI Art Brief` and supplied references to generate and inspect topic-specific micro UI assets. It owns visual asset generation and a short delivery note, not the slide copy or layout.

Pass the UI-art subagent only the material it needs:

- the locked theme and palette
- the presentation topic
- reference image(s), identified as style references
- asset family list and HTML role for each asset
- target aspect or approximate slot size
- text-free, transparency, factual-accuracy, and no-watermark constraints
- a destination folder in the presentation workspace for selected project-bound assets

The UI-art subagent must:

1. Use an actually accessible image-generation capability; in Codex use `imagegen` when it is available to the subagent.
2. Generate a style-board preview only when needed to establish direction, then generate final useful assets individually.
3. Produce small artistic UI pieces like the user's chosen world suggests: for soft editorial esports, this can mean outlined controllers, keycaps, joystick modules, trophy marks, target dividers, and blank match-card shells in the approved restrained palette.
4. Inspect results, reject off-style or generic assets, and return selected asset paths, intended HTML roles, transparency status, and any required cropping or layering note.
5. Never rewrite the deck narrative, add unsupported claims, or bake important text into imagery.

If a subagent is unavailable, has no image-generation access, or has not been authorized, do not fake this parallel pass. The main agent should either request delegation approval when needed or perform the identical UI-art production pass itself in sequence. If image generation itself is unavailable, follow the fallback rule in Dependency Bootstrap.

### 4. Generate Theme-Matched Extractable UI Assets

Use the available supported image-generation capability for visually rich bitmap elements that benefit from a coherent illustrated, material, or object-like appearance, such as a controller, keyboard key set, ticket, phone fragment, product card shell, or decorative HUD ornament. In Codex, this means `imagegen`.

- Keep every generated asset consistent with the locked palette and visual style as well as the presentation topic.
- Prefer a usable set of extractable art pieces over a single decorative collage: isolated hero object, empty card shell, divider or badge, and optional soft background fragment.
- Prefer text-free assets or blank UI shells with deliberate text areas.
- Keep important titles, labels, numbers, and factual statements as HTML text layered over or beside images, not baked into generated pixels.
- Generate isolated objects or clusters suitable for composition in HTML. For transparent elements, follow the chosen provider's supported transparent-output or background-removal workflow and validate the alpha result.
- Keep selected project-bound assets inside the presentation workspace before referencing them in HTML; do not leave final dependencies only in a generator's default output folder.
- Treat any unsourced numbers or outcomes shown in decorative UI as illustrative only, or omit them entirely.

Use native HTML/CSS/SVG instead of image generation for crisp live text, factual charts, exact icons already available in code, progress values, and layout elements that must remain editable and responsive.

### 5. Compose Assets into the Story

Reserve micro UI for meaningful moments:

- opening: one signature object that establishes the world
- evidence or analysis: compact metric, comparison, or process fragments
- solution or experience: a product, chat, timeline, map, receipt, or task view
- closing: a concise outcome or next-action element

Prefer one strong UI composition on a slide over several tiny unreadable panels. Keep body copy readable first.

Generated assets may be used as:

- a blank visual card with real HTML text positioned inside it
- a faded or masked background motif behind the message
- a cropped hero object entering from an edge
- a divider, badge, corner ornament, or navigation-like marker
- a floating object with a restrained angled entrance, parallax, reveal, or glow

These are starting patterns, not limits. Arrange assets creatively when the result strengthens the slide story and still fits the viewport.

Build readable and data-sensitive elements directly with semantic HTML, CSS, and small inline SVG where useful. Match the selected typefaces, colors, radii, borders, spacing, and motion across slide layout, HTML overlays, and generated imagery.

- Use design tokens through CSS variables.
- Use believable labels and states appropriate to the subject.
- Use the presentation's language inside UI elements.
- Keep visualized data illustrative unless the user supplied real figures.
- Never present invented numbers, rankings, reviews, or outcomes as facts.
- Preserve the single-file HTML default by embedding final project-bound images as data URLs when practical. Use a relative asset folder only when the user explicitly accepts a multi-file deliverable or the media quantity makes a single file unreasonable.
- Animate only meaningful states, such as a progress fill, route reveal, message arrival, or number emphasis; respect reduced-motion requirements from the base skill.

### 6. Check the Finished Deck

After implementation, verify:

- every slide still fits its viewport at the sizes required by `frontend-slides`
- interface text is readable and never competes with the main headline
- UI style matches the topic rather than looking like a generic software dashboard
- a requested UI-art pass delivered real selected visual assets, not only placeholder CSS blocks
- generated assets visibly match the locked palette and art direction
- transparent assets have clean edges and no visible extraction color fringe
- meaningful text remains selectable/readable HTML unless there is a clear artistic reason otherwise
- repeated components remain visually consistent
- illustrative content cannot be mistaken for sourced facts
- empty decoration can be removed without harming the narrative; if so, remove it

For enhancement of an existing HTML presentation, first preserve the user's content and chosen style. Add micro UI only after checking that each affected slide has enough space; split slides when the base density rules require it.

## Resource

- Read [references/micro-ui-patterns.md](references/micro-ui-patterns.md) to select component families, placement patterns, and topic-specific examples.
- Read [references/generated-ui-assets.md](references/generated-ui-assets.md) to turn a palette or style reference into generated assets and integrate them into HTML safely.
