# Themed UI Slides

先确认画风，再用主题化小 UI 提升 HTML 演示稿。  
Confirm the visual direction first, then enrich HTML slides with distinctive themed micro UI.

## 中文

### 这是什么

`themed-ui-slides` 是基于 [`frontend-slides`](https://github.com/zarazhangrui/frontend-slides) 的增强 skill。它不是把普通卡片和分隔线堆进页面，而是帮助你制作一套与演示主题、色系和画风一致的小 UI 素材，并克制地融入 HTML 演示稿。

### 工作流程

1. 根据演示主题和参考图，先筛选适合的色系与风格方向。
2. 让作者确认最终 `Style Lock`：颜色、材质、线条、组件类型和动画感觉。
3. 确认后，主智能体负责 HTML 结构、文字排版和页面适配。
4. 只要需要生图，就必须由专门的 UI 美术分身生成素材，主智能体不直接单线生图。
5. 将筛选后的 UI 素材用轻量动画融入演示稿，并检查页面可读性和屏幕适配。

### UI 素材标准

- 短/中篇演示至少规划 3 个可单独使用的主题组件。
- 组件必须让人看出主题，例如电竞中的手柄、键位簇、摇杆、赛事徽章或目标标记。
- 普通下划线、空卡片、圆点和通用分隔线只能辅助，不能作为整套 UI 的主要内容。
- UI 是配角：每页少量使用，不能抢过标题、正文或真实数据。
- 简洁线条型组件优先使用 `SVG`，方便导入 Figma 和在 HTML 中制作线条动画。
- 带磨砂、阴影或材质感的对象可使用透明 `PNG/WebP`。
- 生图图片不会自动变成 Figma 可编辑组件；需要编辑性的简单图形应重建为 `SVG`。

### 使用示例

```text
使用 $themed-ui-slides 和 $frontend-slides 制作一份电竞主题 HTML 演示稿。
先根据我提供的浅色磨砂参考图给出色系与画风方案，等我确认后再开始制作。
确认后，创建 UI 美术分身，生成同色系的手柄、键位簇、摇杆模块、赛事徽章等多个主题组件；
让这些组件以轻量动画融入页面，但不要盖过主要文字。
```

### 依赖

- `frontend-slides`：负责 HTML 演示稿的基础流程、结构、动画和屏幕适配。
- 分身能力：生图阶段必须创建专门的 UI 美术分身。
- 生图能力：在 Codex 中由分身使用内置 `imagegen`；其他环境需要可访问的生图工具。

如果环境不能创建分身，不能执行本 skill 的生图流程。如果没有生图能力，也不能假装已生成素材；可以在你同意后改用不含生图的 HTML/CSS/SVG 方案。

## English

### What it is

`themed-ui-slides` extends [`frontend-slides`](https://github.com/zarazhangrui/frontend-slides). It builds a restrained but distinctive themed UI kit for an HTML presentation, instead of filling slides with generic cards and dividers.

### Workflow

1. Evaluate the presentation topic and reference images, then shortlist suitable palette and art-direction options.
2. Ask the author to confirm a final `Style Lock`: colors, materials, line work, component language, and motion mood.
3. After approval, the main agent builds the HTML structure, typography, and responsive layout.
4. Any image-generation pass must be handled by a dedicated UI-art subagent; the main agent does not generate thematic UI images directly.
5. Integrate selected assets with quiet motion and validate readability and viewport fit.

### UI Asset Standard

- Plan at least 3 independently usable, topic-linked components for a short or medium deck.
- Components should reveal the subject: for esports, use elements such as a controller form, key cluster, joystick module, tournament badge, or target marker.
- Generic underlines, empty cards, dots, and dividers may support the system, but they cannot be the whole kit.
- UI remains secondary to headlines, body copy, and factual data.
- Prefer `SVG` for clean line-based parts that need Figma import or HTML animation.
- Use transparent `PNG/WebP` for frosted, shaded, or material-rich objects.
- Generated raster images do not automatically become editable Figma components; rebuild simple editable forms as `SVG` when needed.

### Example Prompt

```text
Use $themed-ui-slides with $frontend-slides to create an esports-themed HTML presentation.
First propose palette and art-direction options from my soft frosted reference image, and wait for my approval.
After approval, create a UI-art subagent to generate multiple matching components such as a controller, key cluster,
joystick module, and tournament badge. Integrate them with quiet motion without overpowering the copy.
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
