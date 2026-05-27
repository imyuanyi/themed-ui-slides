# Thematic Micro UI Patterns

Use this reference after identifying the presentation topic and visual direction, and before generating assets or building the HTML. Select only the components that support the story.

## Selection Rules

1. Choose components from the user's real context before borrowing generic product UI.
2. Keep a shared visual language: one radius system, one border treatment, one accent behavior, and one type hierarchy.
3. Use no more than one hero component or one compact cluster on a normal content slide.
4. Keep small labels short enough to remain readable at presentation distance.
5. Mark invented numbers as illustrative, sample, concept, or scenario unless supplied as source content.
6. For image-generated components, create text-free objects or blank card shells and place important copy in HTML.

## Topic Map

| Topic | Strong Component Families | Good Uses | Avoid |
| --- | --- | --- | --- |
| Business and marketing | KPI tile, customer segment chip, campaign funnel, conversion sparkline, loyalty card | market insight, strategy, proposed campaign | unlabeled finance charts or fake performance claims |
| Retail and food service | order receipt, menu card, delivery status, coupon, member tier | customer journey, promotion, service concept | crowded app screens with tiny menus |
| Product launch and startup | device preview, feature toggle, waitlist badge, review snippet, roadmap status | feature reveal, product value, launch plan | repeating full dashboards on every page |
| AI and technology | prompt-response panel, processing state, model comparison bar, workflow nodes, alert log | explaining interaction and automation | meaningless code wallpaper or false benchmark scores |
| Finance and operations | budget split, invoice line, inventory row, cash-flow pulse, approval status | process or scenario explanation | invented returns or compliance assertions |
| Education | lesson module, progress ring, quiz choice, timetable strip, feedback bubble | learning journey, course proposal, student experience | trivial gamification where the talk is academic |
| Travel and hospitality | itinerary card, booking confirmation, fare strip, weather chip, route timeline, expense receipt | plans, experience flow, destination pitch | map-like visuals without route meaning |
| Health and wellbeing | appointment card, habit streak, symptom check-in, progress timeline | service journey or behavior concept | diagnostic-looking results without evidence |
| Sustainability and public topics | footprint meter, resource counter, policy timeline, before-after indicator | showing a proposal or measured change | made-up impact figures presented as proof |
| Culture, arts, and personal stories | archive tag, ticket stub, audio player, exhibition label, calendar trace | adding context subtly | default SaaS dashboards that flatten the mood |
| Esports and gaming | keycap set, controller silhouette, match badge shell, crosshair divider, achievement marker | title atmosphere, competition structure, feature framing | neon overload unrelated to the selected art direction |

## Component Recipes

### Evidence UI

Use on analysis slides to make information scannable.

- A KPI tile needs one value, one label, and an optional change cue.
- A sparkline or bar needs a meaningful comparison label.
- A segment chip set should communicate audience categories, not arbitrary tags.

### Experience UI

Use on problem, solution, or scenario slides to put the audience into a moment.

- A mobile card should show one primary task, such as order, book, learn, or message.
- A chat panel should include only the exchange required for the point.
- A receipt or booking card should highlight the decision-driving detail.

### Process UI

Use on journey, implementation, or timeline slides.

- A status tracker should show a short ordered sequence.
- A route or timeline should emphasize the present step or transition.
- A queue or workflow should reveal cause and outcome, not merely arrows.

### Atmospheric UI

Use sparingly on title or closing slides.

- A ticket, ID strip, notification, cursor, stamp, or media control can establish the setting.
- Keep it secondary to the title and avoid adding unsupported data.
- A generated controller, keyboard crop, booking ticket, product fragment, or archival object can provide a stronger thematic anchor when it matches the art direction.

## Composition Patterns

| Slide Purpose | Recommended Placement |
| --- | --- |
| Title slide | One partially cropped hero UI object at an edge or behind the title |
| Problem slide | One broken-state, queue, complaint, or friction panel beside the key statement |
| Insight slide | One compact evidence cluster aligned to the main finding |
| Solution slide | One focused product or service experience panel |
| Comparison slide | Two matching UI cards with clear contrast |
| Roadmap slide | A single horizontal or vertical status sequence |
| Closing slide | One outcome chip, next-step panel, or memorable artifact |

## Generated Asset Cues

Translate the chosen visual language into every generated component:

| Art Direction | Carry Into Assets |
| --- | --- |
| Soft frosted editorial | low-contrast surfaces, delicate outlines, muted accent colors, rounded corners, airy negative space |
| Dark cinematic technology | deep surfaces, selective emissive strokes, restrained glass layers, sharp focus points |
| Warm paper travel | textured cards, stamped edges, route lines, ticket perforations, faded ink accents |
| Playful education | friendly modules, calm progress cues, simplified icons, tactile cards |

Example: for a soft editorial esports deck with dusty blue, muted gold, and faded red accents, generate rounded keycaps, controllers, target lines, trophy markers, and empty UI panels in that exact restrained material language rather than switching to standard neon gaming graphics.

## Quality Filter

Remove or revise a component when:

- it could be dropped into any unrelated topic unchanged
- its labels are too small or numerous to read during a presentation
- it forces headline or essential evidence to shrink
- it implies real evidence the user did not provide
- its motion attracts more attention than the message

The intended result is not a webpage disguised as slides. It is a presentation strengthened by a few believable interface moments.
