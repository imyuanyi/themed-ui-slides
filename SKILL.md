---
name: themed-ui-slides
description: Create or enhance browser-based HTML presentations through an author-confirmed color and art-direction gate followed by a dedicated subagent-only micro UI production pass, while using frontend-slides as the base workflow. Use when a deck, pitch, class presentation, report, product launch, or converted presentation needs a varied, topic-inferred or reference-guided, animation-ready, Figma-friendly themed UI kit such as controllers, keycaps, HUD pieces, app cards, chat panels, timelines, receipts, itinerary cards, or other restrained but distinctive visual components.
---

# Themed UI Slides

Create refined HTML presentations whose small visual designs are confirmed with the author, made for the subject, and animated into the story without competing with it.

## Base Workflow

Use this skill alongside `frontend-slides`.

1. Check and load `frontend-slides` first. Follow its content-discovery, conversion, navigation, inline-editing, motion, delivery, and viewport-fitting rules.
2. Assume there may be no reference image. Analyze the presentation topic, audience, purpose, and tone; use supplied references only as optional guidance.
3. Shortlist three appropriate HTML palette and art-direction options and show three lightweight title-slide previews by default. Ask the author to confirm one direction before producing the full deck or generating UI assets.
4. Record the approved direction as the `Style Lock`.
5. Only after the `Style Lock`, check image-generation capability and obtain any required delegation authorization. Use a dedicated UI-art subagent for every image-generation pass while the main agent builds the HTML skeleton and text layout.
6. Treat every invariant from `frontend-slides` as mandatory, especially single-file HTML delivery, slide density limits, `clamp()` sizing, `overflow: hidden`, responsive height checks, and required supporting CSS.
7. Make the UI art pass central whenever the user requests thematic small designs or generated UI, but keep those assets subordinate to the message.
8. Apply this skill as an enhancement layer for art direction, image-generated assets, and micro UI composition only. Do not replace or weaken the base workflow.

## Compatibility With Frontend Slides

`frontend-slides` remains authoritative for content discovery, style approval, HTML architecture, responsive fitting, interaction, and final delivery. This skill makes its style-choice phase stricter, then inserts a focused art-production workflow after author approval and before the deck is finalized.

- Before style approval, only analyze content, inspect any supplied references, shortlist suitable directions, and produce three lightweight title-slide previews following the `frontend-slides` show-don't-tell principle. Do not produce the final deck or generated UI assets.
- When no visual reference is supplied, proactively infer suitable directions from the presentation subject, audience, purpose, and tone. Do not require the author to provide an image before presenting options.
- Use `frontend-slides` presets and extended template gallery as helpful candidate sources when they fit; do not restrict style options to that library when an original, topic-specific direction would be stronger.
- Even when the author supplies a reference image or describes a palette, summarize the inferred direction and receive confirmation before beginning generated UI production.
- After style approval and subagent authorization, the main agent may build slide structure, live text, CSS tokens, and reserved image slots while art is being produced, but it must not pretend the generated-UI requirement is complete with placeholders alone.
- Keep titles, factual content, charts, labels, and important copy in HTML. Generated UI supplies forms, surfaces, subject objects, frames, ornaments, and atmosphere.
- Treat micro UI as supporting detail across the slide layout, not as a thin asset list: produce a varied themed kit for the deck, then prefer one signature element on a title or closing slide and one small supporting component at most on a normal content slide unless the story specifically needs a UI comparison.
- If an asset makes a slide too dense or steals attention from the message, reduce it, fade it into the background, move it to another slide, or split the slide under `frontend-slides` rules. Never shrink key text to make decoration fit.
- If instructions ever conflict, preserve the mandatory viewport, density, single-file, accessibility, and delivery constraints from `frontend-slides`.

## Dependency Bootstrap

Check `frontend-slides` before beginning the presentation workflow. Defer image-generation checks until after the author approves the `Style Lock`, and run them only when newly generated UI assets are requested.

### Frontend Slides

Require `frontend-slides` for the HTML presentation workflow.

- If it is already available, load it and continue.
- If it is missing, retrieve it only from the public repository `https://github.com/zarazhangrui/frontend-slides`.
- In Codex, use the installed `skill-installer` workflow, using the repository root as the skill folder and the installed name `frontend-slides`.
- In Claude Code or another host, use that host's supported plugin/skill installation or repository-reading workflow. If the host requires the user to run an install or authorization step, explain the trusted repository source and ask for that required confirmation before continuing.
- After installing, read its `SKILL.md` directly and continue the current task when local file access allows it. Tell the user when their host needs a restart or reload for normal discovery in later conversations.
- If installation fails or network access is unavailable, stop before producing the final deck and state that the required HTML presentation foundation could not be retrieved.

### Image Generation Capability After Style Lock

Require an actual image-generation capability whenever the requested design uses newly generated UI assets. A Markdown skill describes a workflow; it does not provide a model or grant tool access by itself.

- In Codex, if `imagegen` is available, load it and continue. Treat it as a Codex system skill, not a third-party visual pack; do not silently download an unrelated replacement with the same name.
- In Claude Code or another host, use a configured image-generation tool, plugin, MCP integration, or user-approved API workflow only when that capability is actually accessible in the environment.
- If an API-based image provider needs credentials, ask the user to configure the secret locally; never ask them to paste an API key into chat.
- If no image-generation capability is available, do not claim that generated thematic UI was produced. Explain the missing capability and ask the user to either configure an image-generation integration or provide prepared visual assets.
- Offer a CSS/SVG-only approximation only as an explicit fallback, and use it only after the user agrees that the result will not contain image-generated UI assets.

## Design Process

### 1. Recommend and Confirm the Visual World Before Production

Do not build the full presentation and do not generate UI assets until the author confirms one visual direction. Default to a no-reference starting point unless the author provides imagery. First extract:

- subject, audience, and purpose
- language used in the deck
- mood and style cues inferred from the topic, audience, purpose, and tone, plus any optional supplied reference image
- palette, contrast, texture, edge treatment, dimensionality, icon style, and motion character
- concrete objects associated with the topic, such as transactions, routes, messages, inventory, lessons, metrics, bookings, or model outputs

Based on the presentation topic, audience, purpose, and tone, filter out unsuitable directions and generate three distinct lightweight title-slide previews by default. If references exist, incorporate them; if not, generate the candidates independently. Accompany each preview with a short summary of its palette, material feeling, typography direction, micro UI vocabulary, and why it fits the subject.

Use text-only options only when the host cannot create or open HTML previews. State that limitation clearly instead of silently skipping the visual comparison.

Consult suitable `frontend-slides` presets or extended-gallery templates as inspiration where useful, but allow a newly composed visual direction when it matches the presentation better than existing themes.

Ask the author to select or adjust one direction. Record the approved direction as the `Style Lock`; all HTML and UI assets must follow it.

Example visual theses:

- Campus coffee marketing: mobile order cards, coupon chips, footfall pulse, membership tier badge.
- AI customer service: chat transcript, confidence status, routing queue, resolution timer.
- Travel proposal: boarding pass strip, day-plan card, map stop chip, budget receipt.
- Soft editorial esports: frosted ivory surfaces, dusty blue/gold/red accents, rounded outlined keycaps, controller pieces, target markers, trophy dividers.

If the author supplies an image as the palette or style reference, use it as visual guidance rather than an edit target unless explicitly asked to change that image. Still confirm the interpreted style lock before generating assets.

Read [references/micro-ui-patterns.md](references/micro-ui-patterns.md) and [references/generated-ui-assets.md](references/generated-ui-assets.md) before implementation.

### 2. After Confirmation, Build the Layout Skeleton and UI Art Brief

Only after the author approves the `Style Lock`, have the main agent read the mandatory Phase 3 supporting files required by `frontend-slides`, then begin the HTML structure and text typography using that workflow. It should establish CSS variables, slide hierarchy, live text, and intentional slots for generated assets before final composition.

At the same time, write a concise `UI Art Brief` for the art-production pass. Follow [references/generated-ui-assets.md](references/generated-ui-assets.md) for the detailed brief, required asset manifest, handoff format, quality filters, and Figma-friendly delivery rules. At minimum include:

- presentation subject and narrative purpose
- approved palette, materials, shapes, line weight, depth, and motion mood
- optional reference-image role, when present: style reference, not edit target, unless explicitly requested
- two to four topic-specific asset families
- three or more individual component targets when thematic generated UI is requested, with each target tied to the presentation subject
- intended slide slot for each asset: dimensions or aspect, approximate placement, foreground or background role, and required empty space
- output requirement: text-free or blank-shell assets, preferably SVG-ready geometric parts or isolated transparent PNG/WebP cutouts where suitable
- animation behavior: subtle entrance, float, mask reveal, line draw, or low-opacity drift that supports rather than leads the slide
- avoid list: generic off-theme UI, watermark, unwanted text, invented data, and visual clutter

Choose at most three component families for a short or medium deck, and at most four for a long deck. Reuse the same visual grammar rather than inventing a new widget on every slide.

Use micro UI only when it does at least one job:

- turns an abstract claim into a visible signal
- provides a setting or user perspective
- makes a comparison easier to grasp
- creates a memorable hero moment

Do not insert interface panels merely to fill space. A cultural essay, emotional speech, or highly photographic story may need almost no UI.

#### Themed UI Kit Minimum

When the author asks for generated thematic UI, plan a coherent kit with multiple usable pieces rather than one generic accent.

- For a short or medium deck, plan at least three distinct usable components across two or three topic-linked families. For a long deck, plan four to six components where the narrative supports them.
- Include at least one unmistakably topic-linked signature component and at least one smaller supporting component that can recur subtly through the deck.
- A plain underline, generic empty card, dot row, or universal rounded panel does not satisfy the kit requirement by itself. It counts only when its silhouette, details, or pairing clearly belongs to the approved topic and visual world.
- Examples: esports may use controller silhouette, directional key cluster, joystick module, tournament badge, target marker, or trophy accent; travel may use ticket stub, luggage tag, route waypoint, boarding-pass segment, or room-key marker; campus coffee may use cup profile, loyalty stamp, order tab, roast dial, or pickup indicator.
- Generate or rebuild final pieces separately so the main agent can place and animate them independently. Do not rely only on a single contact sheet.
- Reject a component that could be reused unchanged in unrelated presentations such as esports, travel, and campus coffee. It is too generic to count toward the themed kit.

When the intended style depends heavily on generated imagery, create a compact style-board preview first, then generate selected assets as separate usable cutouts. Do not rely on cropping many finished assets from one crowded board.

### 3. Require a Dedicated UI Art Subagent for Image Generation

Any image-generation pass for this skill must be delegated to a dedicated UI-art subagent. Never let the main agent generate thematic UI images directly.

- If the author already requested or authorized subagent use, spawn the UI-art subagent after style confirmation.
- If the author requested generated UI but did not explicitly authorize delegation, ask for that authorization after the `Style Lock` is approved and before generating images.
- If the host cannot create subagents, stop the image-generated UI path and explain that this skill's required art workflow is unavailable in that host. Do not silently downgrade to single-agent image generation.
- If the author declines delegation, continue only without image-generated UI, or offer native HTML/CSS/SVG decoration as a separately approved non-generated alternative.

Parallel ownership:

- **Main agent:** build the HTML skeleton, text hierarchy, CSS theme tokens, slide structure, responsive constraints, and clearly sized asset slots. It owns all final HTML editing and viewport validation.
- **UI-art subagent:** use the `UI Art Brief` and supplied references to generate and inspect topic-specific micro UI assets. It owns visual asset generation and a short delivery note, not the slide copy or layout.

Pass the UI-art subagent only the approved `Style Lock`, topic, optional references, requested asset families, intended slide slots, output constraints, and workspace destination. Require the subagent to follow [references/generated-ui-assets.md](references/generated-ui-assets.md), inspect its results, reject generic or attention-stealing assets, and return the required asset manifest. It must never rewrite the narrative, add unsupported claims, or bake important text into imagery.

If the subagent has no image-generation access, do not fake this art pass and do not ask the main agent to generate images instead. State the limitation and follow the fallback rule in Dependency Bootstrap.

### 4. Produce Theme-Matched, Figma-Friendly UI Assets

Follow [references/generated-ui-assets.md](references/generated-ui-assets.md) for generation, transparency, SVG reconstruction, asset storage, and handoff details. Keep important text and factual data in HTML. Use generated images only for visual layers that benefit from coherent object, texture, or material treatment.

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
- Favor quiet animation integration for decorative UI: opacity with small translation, clipped reveal, SVG line draw, gentle drift, or background parallax. Avoid looping motion or oversized foreground movement that competes with the headline.

### 6. Check the Finished Deck

After implementation, verify:

- every slide still fits its viewport at the sizes required by `frontend-slides`
- interface text is readable and never competes with the main headline
- UI style matches the topic rather than looking like a generic software dashboard
- the author approved the `Style Lock` before full HTML production or any image generation
- every image-generated UI pass was performed by a dedicated UI-art subagent, never directly by the main agent
- a requested UI-art pass delivered real selected visual assets, not only placeholder CSS blocks
- generated assets visibly match the locked palette and art direction
- UI remains supporting material, with restrained placement and motion
- the selected UI kit contains multiple topic-specific assets rather than only generic cards, underlines, dots, or dividers
- the required asset manifest lists each selected component, target slide, role, format, transparency status, motion, and SVG-rebuild need
- simple editable ornaments are delivered as SVG when Figma import/editability matters
- transparent assets have clean edges and no visible extraction color fringe
- meaningful text remains selectable/readable HTML unless there is a clear artistic reason otherwise
- repeated components remain visually consistent
- illustrative content cannot be mistaken for sourced facts
- empty decoration can be removed without harming the narrative; if so, remove it

For enhancement of an existing HTML presentation, first preserve the user's content and chosen style. Add micro UI only after checking that each affected slide has enough space; split slides when the base density rules require it.

## Resource

- Read [references/micro-ui-patterns.md](references/micro-ui-patterns.md) to select component families, placement patterns, and topic-specific examples.
- Read [references/generated-ui-assets.md](references/generated-ui-assets.md) to turn an approved topic-derived or reference-guided style lock into generated assets and integrate them into HTML safely.
