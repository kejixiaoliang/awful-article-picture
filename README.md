# Awful Article Picture

<p>
  <a href="#中文">中文</a> · <a href="#english">English</a>
</p>

<details open>
<summary id="中文"><strong>中文介绍</strong></summary>

## 烂画文章配图 Skill

`awful-article-picture` 是一个 Codex Skill，用来把文章拆成多张 `16:9` 配图，并生成一种故意失败的 MS Paint 鼠绘风格：白底、笨拙、潦草、低质量、像是照着一张正常参考图临摹失败。

它不是用来画干净的信息图、教程流程图或 UI 页面示意图的。它会尽量把抽象段落转换成具体场景：桌子、房间、纸箱、文件柜、路、门面、机器、便签、人物动作，再把这个场景画成非常糟糕但有趣的鼠绘临摹图。

## 适合做什么

- 给公众号、博客、长文、教程文章生成配图。
- 把软件、AI、GitHub、产品、工作流等抽象内容转成更像“文章场景图”的画面。
- 避免生成标签堆砌、流程图、UI map、知识卡片式说明图。
- 给每张图保存对应 prompt，方便复用、修改或重生成。

## 默认效果

- 默认生成 `16:9` 横图。
- 默认按小节、关键段落组或单一概念拆图。
- 中长文会拆成更多张图，而不是把所有信息塞进一张。
- 每张图只保留一个主要想法和少量文章道具。
- 风格目标是“失败临摹”，不是“可爱手绘插画”。

## 使用方式

在 Codex 中调用：

```text
Use $awful-article-picture to generate illustrations for this article.
```

中文也可以直接说：

```text
用 awful-article-picture 给这篇文章配图。
```

输出建议保存为：

```text
outputs/<article-slug>-bad-paint/
```

其中包含生成图片和 `prompts.md`。

## Skill 结构

```text
SKILL.md
agents/openai.yaml
references/style.md
references/prompt_examples.md
```

`style.md` 定义核心视觉风格；`prompt_examples.md` 专门处理软件、AI、GitHub、教程类文章，避免画成流程图或 UI 说明图。

</details>

<details>
<summary id="english"><strong>English</strong></summary>

## A Bad MS Paint Article Illustration Skill

`awful-article-picture` is a Codex Skill for turning articles into multiple `16:9` illustrations in an intentionally failed MS Paint redraw style: white background, clumsy lines, rough shapes, low-quality mouse-drawn marks, and an awkward almost-but-not-quite resemblance to an imagined reference picture.

It is not meant to create clean infographics, tutorial flowcharts, UI maps, or label-heavy explainer graphics. It converts abstract article ideas into physical scenes: desks, rooms, cardboard boxes, file cabinets, roads, storefronts, machines, sticky notes, and awkward human actions, then redraws those scenes badly.

## Good For

- Creating illustrations for blog posts, newsletters, tutorials, and long-form articles.
- Converting software, AI, GitHub, product, and workflow topics into concrete article scenes.
- Avoiding flowcharts, UI maps, knowledge-card graphics, and label boards.
- Saving final prompts for reuse, editing, and regeneration.

## Defaults

- Generates `16:9` horizontal images by default.
- Splits articles by subsection, key paragraph group, or single concept.
- Produces more images for longer articles instead of overloading one panel.
- Keeps each image focused on one main idea with only a few article-specific props.
- Optimizes for a failed-redraw look, not cute polished sketch art.

## Usage

Invoke it in Codex:

```text
Use $awful-article-picture to generate illustrations for this article.
```

Suggested output folder:

```text
outputs/<article-slug>-bad-paint/
```

The folder should include generated images and a `prompts.md` prompt log.

## Skill Layout

```text
SKILL.md
agents/openai.yaml
references/style.md
references/prompt_examples.md
```

`style.md` defines the core visual direction. `prompt_examples.md` provides guardrails for software, AI, GitHub, and tutorial-like articles so they do not collapse into diagrams or UI explainers.

</details>
