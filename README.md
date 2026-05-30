# Themed UI Slides

先看三种画风，再用主题化小 UI 提升 HTML 演示稿。  
Compare three visual directions first, then enrich HTML slides with distinctive themed micro UI.

## 中文

### 这是什么

`themed-ui-slides` 是基于 [`frontend-slides`](https://github.com/zarazhangrui/frontend-slides) 的增强 skill。即使你没有参考图，它也会先根据演示主题、受众、用途和氛围筛选合适的色系与画风，并展示 3 张轻量标题页预览供你选择。确认后，再制作一套与主题一致的小 UI 素材，并克制地融入 HTML 演示稿。

`frontend-slides` 内置主题和模板库可以作为灵感来源，但不是限制。如果现成主题不够贴合，skill 应主动提出新的风格方向。

### 工作流程

1. 加载 `frontend-slides`，先确认演示内容、用途和受众。
2. 即使没有参考图，也要根据主题自主筛选 3 种色系与画风，并默认展示 3 张标题页预览。
3. 让作者确认最终 `Style Lock`：颜色、材质、线条、组件类型和动画感觉。
4. 只在确认后检查生图能力，并请求必要的分身授权。
5. 主智能体负责 HTML 结构和文字排版；UI 美术分身负责生成和筛选主题素材。
6. 将筛选后的 UI 素材用轻量动画融入演示稿，并检查页面可读性和屏幕适配。

如果当前环境不能创建或打开 HTML 预览，可以退回文字方案，但必须明确说明限制。

### UI 素材标准

- 短/中篇演示至少规划 3 个可单独使用的主题组件。
- 组件必须让人看出主题，例如电竞中的手柄、键位簇、摇杆、赛事徽章或目标标记。
- 普通下划线、空卡片、圆点和通用分隔线只能辅助，不能作为整套 UI 的主要内容。
- 使用替换测试：如果一个组件不改内容就能同时放进电竞、旅游和校园咖啡演示稿，它就太普通，不能算作主题组件。
- UI 是配角：每页少量使用，不能抢过标题、正文或真实数据。
- 简洁线条型组件优先使用 `SVG`，方便导入 Figma 和在 HTML 中制作线条动画。
- 带磨砂、阴影或材质感的对象可使用透明 `PNG/WebP`。
- 生图图片不会自动变成 Figma 可编辑组件；需要编辑性的简单图形应重建为 `SVG`。

### 分身交付清单

每个选中的素材都要记录：素材名称、对应页面、HTML 用途、文件格式、是否透明背景、动画方式、是否需要重建为 `SVG`，以及实际文件路径。

### 使用示例

```text
使用 $themed-ui-slides 和 $frontend-slides 制作一份电竞主题 HTML 演示稿。
我没有参考图。请先根据赛事介绍的主题和受众，展示 3 种色系与画风的标题页预览；
可以参考 frontend-slides 内置主题，但不要局限于现成模板。等我确认后再开始制作。
确认后，创建 UI 美术分身，生成同色系的手柄、键位簇、摇杆模块、赛事徽章等多个主题组件；
让这些组件以轻量动画融入页面，但不要盖过主要文字，并返回逐个素材的交付清单。
```

### 依赖

- `frontend-slides`：负责 HTML 演示稿的基础流程、结构、动画和屏幕适配。
- 分身能力：生图阶段必须创建专门的 UI 美术分身。
- 生图能力：在 Codex 中由分身使用内置 `imagegen`；其他环境需要可访问的生图工具。

如果环境不能创建分身，不能执行本 skill 的生图流程。如果没有生图能力，也不能假装已生成素材；可以在你同意后改用不含生图的 HTML/CSS/SVG 方案。

## English

### What it is

`themed-ui-slides` extends [`frontend-slides`](https://github.com/zarazhangrui/frontend-slides). Even without a reference image, it infers suitable palette and art-direction options from the presentation topic, audience, purpose, and tone, then shows three lightweight title-slide previews for approval. After approval, it builds a restrained but distinctive themed UI kit for the HTML deck.

The built-in `frontend-slides` themes and template gallery are useful inspiration, not a limit. The skill may propose a new topic-specific direction when existing options are not strong enough.

### Workflow

1. Load `frontend-slides` and confirm the presentation content, purpose, and audience.
2. Even without a reference image, infer three suitable palette and art-direction options and show three title-slide previews by default.
3. Ask the author to confirm the final `Style Lock`: colors, materials, line work, component language, and motion mood.
4. Only after approval, check image-generation access and request any required delegation authorization.
5. The main agent builds the HTML structure and typography while a dedicated UI-art subagent generates and filters themed assets.
6. Integrate selected assets with quiet motion and validate readability and viewport fit.

If the host cannot create or open HTML previews, text-only options are allowed only when the limitation is stated clearly.

### UI Asset Standard

- Plan at least 3 independently usable, topic-linked components for a short or medium deck.
- Components should reveal the subject: for esports, use elements such as a controller form, key cluster, joystick module, tournament badge, or target marker.
- Generic underlines, empty cards, dots, and dividers may support the system, but they cannot be the whole kit.
- Use the swap test: if a component can move unchanged between esports, travel, and campus-coffee decks, it is too generic to count as a themed component.
- UI remains secondary to headlines, body copy, and factual data.
- Prefer `SVG` for clean line-based parts that need Figma import or HTML animation.
- Use transparent `PNG/WebP` for frosted, shaded, or material-rich objects.
- Generated raster images do not automatically become editable Figma components; rebuild simple editable forms as `SVG` when needed.

### Asset Manifest

For every selected component, record its name, target slide, HTML role, file format, transparency status, motion behavior, SVG-rebuild need, and actual workspace path.

### Example Prompt

```text
Use $themed-ui-slides with $frontend-slides to create an esports-themed HTML presentation.
I do not have a reference image. First show three title-slide previews with suitable palette and art-direction options
inferred from the topic and audience. Use frontend-slides themes as inspiration, but do not limit the options to existing templates.
Wait for my approval. After approval, create a UI-art subagent to generate multiple matching components such as a controller,
key cluster, joystick module, and tournament badge. Integrate them with quiet motion without overpowering the copy,
and return an asset manifest for the selected components.
```

### Requirements

- `frontend-slides` for the core HTML presentation workflow and viewport rules.
- Subagent support, required for all image-generation passes.
- Image-generation capability; in Codex, the UI-art subagent uses built-in `imagegen`.

If subagents or image generation are unavailable, the generated-UI workflow cannot run. A non-generated HTML/CSS/SVG alternative may be offered only with the author's agreement.

## Files

- `SKILL.md`: main workflow and hard rules
- `references/generated-ui-assets.md`: art-subagent and asset-delivery workflow
- `references/micro-ui-patterns.md`: themed component guidance
- `agents/openai.yaml`: interface metadata
