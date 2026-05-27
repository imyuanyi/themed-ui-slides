# Themed UI Slides

让 HTML 演示稿拥有统一画风和贴合主题的小 UI 素材。  
Create polished HTML presentations with a consistent art direction and topic-matched micro UI assets.

## 中文

### 它能做什么

`themed-ui-slides` 是一个演示稿增强 skill。它会：

1. 先识别你的演示主题和参考画风。
2. 确定整套 HTML 的色系、材质感和视觉语言。
3. 生成符合主题的小 UI 素材，例如电竞手柄、旅行票据、商品卡片或学习进度组件。
4. 将素材以标题装饰、文字卡片、背景图层或动态元素的方式组合进 HTML 演示稿。

重要文字和真实数据保留为 HTML 文本，方便阅读和修改。

### 使用方式

示例提示词：

```text
使用 $themed-ui-slides，做一份电竞主题的 HTML 演示稿。
画风参考我提供的浅色磨砂图片，生成同色系的手柄、按键和赛事卡片小 UI。
```

### 依赖

- `frontend-slides`：负责 HTML 演示稿的基础结构、动画和页面适配。
- 生图能力：负责生成主题化 UI 素材。在 Codex 中可使用内置 `imagegen`。

如果环境没有生图能力，skill 会提示你接入生图工具或提供现成素材；经你同意后，也可以退回到较简单的 CSS/SVG 效果。

## English

### What it does

`themed-ui-slides` is an enhancement skill for HTML presentations. It helps an agent:

1. Understand the presentation topic and visual reference.
2. Set a coherent palette, material feel, and art direction.
3. Generate topic-matched micro UI assets, such as esports controls, travel tickets, product cards, or learning progress elements.
4. Compose those assets into the HTML deck as title accents, text-card shells, atmospheric layers, or animated objects.

Important copy and factual data remain live HTML text for clarity and editability.

### Usage

Example prompt:

```text
Use $themed-ui-slides to create an esports-themed HTML presentation.
Match the soft frosted reference style and generate controller, keycap, and match-card UI assets in the same palette.
```

### Requirements

- `frontend-slides` for the core HTML presentation workflow, animation, and viewport fitting.
- An image-generation capability for thematic UI assets. In Codex, the built-in `imagegen` capability can be used.

If image generation is unavailable, the skill should ask for an integration or prepared assets. It may offer a simpler CSS/SVG-only fallback only with user agreement.

## Files

- `SKILL.md`: main workflow
- `references/generated-ui-assets.md`: generated asset workflow
- `references/micro-ui-patterns.md`: topic and component guidance
- `agents/openai.yaml`: interface metadata

## Credits

Built as an enhancement layer for [frontend-slides](https://github.com/zarazhangrui/frontend-slides).
