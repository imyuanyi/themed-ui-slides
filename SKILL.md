---
name: themed-ui-slides
description: Enhance browser-based HTML presentations with polished, topic-specific micro UI and generated visual assets while using frontend-slides as the base workflow. Use when creating or refining an HTML slide deck, pitch, class presentation, product launch, report, or converted presentation where the user wants a more premium look, a reference-image-driven color and art direction, generated interface fragments, thematic asset kits, app cards, game HUD elements, chat panels, timelines, receipts, itinerary cards, or other small UI visuals matched to the subject.
---

# Themed UI Slides

Create refined HTML presentations whose generated UI assets and interface details share one deliberate visual world.

## Base Workflow

Use this skill alongside `frontend-slides`.

1. Run the dependency bootstrap below before designing or generating assets.
2. Load and follow the `frontend-slides` skill for presentation creation, conversion, navigation, inline editing, motion, delivery, and viewport-fitting rules.
3. Load a supported image-generation capability whenever generating new bitmap UI assets, visual motifs, transparent cutouts, or style-matched decorative elements. In Codex, use the bundled `imagegen` skill and tool.
4. Treat every invariant from `frontend-slides` as mandatory, especially single-file HTML delivery, slide density limits, `clamp()` sizing, `overflow: hidden`, responsive height checks, and required supporting CSS.
5. Apply this skill as an enhancement layer for art direction, image-generated assets, and micro UI composition only. Do not replace or weaken the base workflow.

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

### 2. Plan a Small Asset Kit

Choose at most three component families for a short or medium deck, and at most four for a long deck. Reuse the same visual grammar rather than inventing a new widget on every slide.

Use micro UI only when it does at least one job:

- turns an abstract claim into a visible signal
- provides a setting or user perspective
- makes a comparison easier to grasp
- creates a memorable hero moment

Do not insert interface panels merely to fill space. A cultural essay, emotional speech, or highly photographic story may need almost no UI.

Define the asset kit before calling image generation:

- one visual-style lock: palette, materials, shapes, line weight, depth, and mood
- two to four subject-specific asset families
- intended use for each family: hero object, text-card shell, atmospheric background, divider, evidence accent, or transition element

When the intended style depends heavily on generated imagery, create a compact style-board preview first, then generate selected assets as separate usable cutouts. Do not rely on cropping many finished assets from one crowded board.

### 3. Generate Theme-Matched Visual Assets

Use the available supported image-generation capability for visually rich bitmap elements that benefit from a coherent illustrated, material, or object-like appearance, such as a controller, keyboard key set, ticket, phone fragment, product card shell, or decorative HUD ornament. In Codex, this means `imagegen`.

- Keep every generated asset consistent with the locked palette and visual style as well as the presentation topic.
- Prefer text-free assets or blank UI shells with deliberate text areas.
- Keep important titles, labels, numbers, and factual statements as HTML text layered over or beside images, not baked into generated pixels.
- Generate isolated objects or clusters suitable for composition in HTML. For transparent elements, follow the chosen provider's supported transparent-output or background-removal workflow and validate the alpha result.
- Treat any unsourced numbers or outcomes shown in decorative UI as illustrative only, or omit them entirely.

Use native HTML/CSS/SVG instead of image generation for crisp live text, factual charts, exact icons already available in code, progress values, and layout elements that must remain editable and responsive.

### 4. Compose Assets into the Story

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

### 5. Check the Finished Deck

After implementation, verify:

- every slide still fits its viewport at the sizes required by `frontend-slides`
- interface text is readable and never competes with the main headline
- UI style matches the topic rather than looking like a generic software dashboard
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
