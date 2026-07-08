---
name: awful-article-picture
description: "Use when creating article illustrations, 给文章配图, making section-by-section article pictures, using optional narrator characters, or redrawing article/reference ideas as low-quality, awkward, clumsy, white-background, pixel-ish, almost-but-not-quite MS Paint scenes. Especially use for AI, GitHub, coding, software, product, tutorial-like, or concept-heavy articles that might otherwise become diagrams, flowcharts, UI maps, timelines, screenshots, or label-heavy explainers."
---

# Awful Article Picture

Turn an article into a coordinated set of intentionally awful `16:9` illustrations that feel like someone tried to redraw a normal article picture in MS Paint and failed. The default output is real images plus a saved prompt log. Use the built-in `imagegen` / `image_gen` workflow; do not create a custom image API client.

Read [references/style.md](references/style.md) before creating prompts. Use the style layer exactly as the visual baseline, then add the article-specific scene.

For software, AI, GitHub, coding, product, or tutorial-like articles, also read [references/prompt_examples.md](references/prompt_examples.md) before planning. These topics easily collapse into diagrams, so use the examples as guardrails.

Read [references/characters.md](references/characters.md) whenever the user mentions a role, narrator, IP character, author avatar, mascot-like figure, or says "角色1", "角色2", "小亮", "阿序", `role-01`, or `role-02`.

## Default Behavior

- Read the full article before planning images.
- Analyze the title, section headings, argument flow, key examples, emotional turns, and conclusion.
- Plan images at the subsection, key paragraph group, or single concept level. Split dense sections into multiple simpler images instead of forcing one complex panel.
- Use `16:9` for every generated image unless the user explicitly asks for another ratio.
- Deliver generated images and a `prompts.md` file when working in a project folder.
- Keep the style consistent across one article unless the user asks for variants.
- The picture must work as article配图, not as a tutorial diagram, UI map, flowchart, icon set, or label board. A good result is a funny failed redraw of a concrete scene tied to one article idea.
- Default to character mode `none`: no recurring protagonist, no repeated Xiaoliang, no repeated Axu, and no fixed face/hair/outfit across the full article unless the user selects a narrator role.

## Image Count

Use these defaults unless the user requests a specific count:

- Short article: `2-4` images.
- Medium article: `6-10` images.
- Long article: `10-16` images.
- Very long article with many distinct sections: split into batches and usually produce `16-24` images.

Reduce the count when sections repeat the same idea. Increase the count when a section would otherwise require more than one main scene or too many labels.

## Planning Workflow

1. Identify an article slug from the title or main topic.
2. Create a concise image plan before generation when producing more than two images.
3. Determine character mode:
   - `none` by default.
   - `narrator` only when the user explicitly asks for a fixed narrator / author avatar / role card.
   - Map "角色1" / "小亮" / "Xiaoliang" to `role-01`.
   - Map "角色2" / "阿序" / "Axu" to `role-02`.
4. For each image, record:
   - image number and filename slug
   - article section or beat
   - concrete scene
   - aspect ratio (`16:9` by default)
   - character mode and role id if any
   - whether it contains short text
5. Make each image a distinct visual idea. Avoid repeating the same person-at-desk, abstract chart, or generic icon scene.
6. If the article includes screenshots, diagrams, or reference-image descriptions, treat generated images as supplemental article illustrations unless the user asks for replacement drawings.

## Character Modes

Use only these two modes:

- `none`: Default. No fixed narrator or recurring protagonist. Use different people, objects, or no person at all depending on the scene. Do not keep reusing Xiaoliang, Axu, a blue-shirt person, a hoodie person, the same hairstyle, the same face, or the same outfit across the set.
- `narrator`: Use one selected role card as a recurring article narrator, observer, author avatar, or scene participant. The user may select `role-01`, `role-02`, "角色1", "角色2", "小亮", or "阿序".

Narrator rules:

- Load the selected role card from `references/character-library/<role-id>.md`.
- If the role card lists reference images under `assets/characters/<role-id>/`, include those paths in the prompt as identity guidance.
- For `role-01`, use the bundled PNG images as the canonical Xiaoliang reference. Preserve the blue shirt, black spiky hair, round eyes, tan face, and rough black outline shown in those PNGs. Do not substitute glasses, black hoodie, dark jacket, or a different narrator design.
- For `role-02`, use the bundled PNG image as the canonical Axu reference. Preserve the round glasses, dark navy hoodie with white drawstrings, messy black hair, calm curious expression, and exploration props. Do not substitute Xiaoliang, a bright blue shirt, a no-glasses face, or the clean character-sheet style from the reference.
- Preserve only the role's key identity markers, such as hair, eyes, clothing, posture, color palette, or signature props.
- The narrator may appear as an observer, operator, confused participant, explainer, or person being overwhelmed by the article topic.
- Do not force the narrator into every image. Use them only when they improve the scene.
- Keep the narrator ugly, mouse-drawn, inconsistent, and subordinate to the failed-redraw style. Do not turn them into a polished character sheet.
- If a user provides their own role card or reference image, use it only if it appears to be original, owned by the user, or clearly authorized. Do not imitate protected existing characters, living artists, animation studios, or branded mascots without authorization.

## Scene Conversion Ladder

For abstract or software-heavy articles, convert concepts into physical scenes before prompting:

1. Name the article idea in plain words.
2. Pick a physical anchor: room, desk, storefront, road, file cabinet, garage, workshop, mailbox, control machine, cardboard box, folder, stamp, sign, shelf, or tiny building.
3. Put a person or awkward object into action: pushing, carrying, stamping, opening, repairing, pulling a lever, staring, dropping papers, or protecting a stable version.
4. Add only `2-4` article-specific props as objects inside the scene.
5. If the draft still reads like a UI, menu, list, timeline, chart, network, or feature board, rewrite it into a physical scene before generating.

## Visual Direction Rules

The default image should feel like a badly redrawn reference picture, not a knowledge diagram.

- First imagine a normal editorial photo, screenshot, poster, or article illustration for this beat; then prompt for a terrible MS Paint redraw of that imagined reference.
- Use one complete scene with a foreground, background, and obvious subject. The image should look like a bad picture, not a board of separate labeled items.
- Fill about `45-65%` of the canvas with the scene while keeping the white background visible.
- Include `2-4` visual props from the article, but make them part of the scene rather than separate floating labels.
- Prefer physical metaphors, awkward people, ugly objects, bad perspective, lopsided rooms, broken-looking devices, paper forms, cabinets, doors, roads, shelves, stamps, boxes, mailboxes, control machines, crude screenshots-inside-the-scene, or badly copied photo compositions.
- For UI-heavy ideas, do not redraw the UI. Turn it into a physical place or object: a repository page becomes a file-cabinet room, a settings page becomes a machine with levers, a form becomes a paper form on a counter, and a pull request becomes a cardboard box of changed code on a meeting table.
- Use short text only when it is naturally on an object in the scene, such as a sign, screen, note, shirt, box, or speech bubble.
- Avoid English labels unless the article itself requires them. For Chinese articles, use no text or very short Chinese labels by default.
- Do not write "diagram", "flowchart", "map", "timeline", "UI overview", "labels around it", "callouts", "icon", "infographic", "many arrows", "page map", "feature list", or "explain the concept" in generated prompts.

## Prompt Template

For every image, create a separate prompt:

```text
Use case: article illustration
Asset type: failed MS Paint redraw of an imagined reference picture
Article beat: <the section, subsection, or argument this supports>
Aspect ratio: 16:9
Character mode: none OR narrator
Narrator role: <role-id and pasted key markers from the selected role card, or "No recurring narrator">
Reference images: <bundled role image paths if any, used as identity guidance only>
Imagined reference picture: <what a normal article image/photo/poster for this beat would roughly show>
Failed redraw scene: <one complete concrete scene, not a diagram>
Subject and action: <main subjects, expressions, physical action, and what looks wrong>
Scene props: <2-4 article-specific props integrated into the scene, not floating labels>
Character placement: <where the narrator appears if useful, or "No fixed character; vary people naturally">
Composition: <16:9 horizontal framing; scene occupies 45-65% of the canvas; white background remains visible>
Text (verbatim): "<short exact text naturally placed on an object>" or "No text"
Style layer: <paste the Bad MS Paint style layer from references/style.md>
Constraints: white background, no watermark, no logo, no signature, no polished illustration finish, no clean character sheet, no tutorial diagram, no flowchart, no UI map, no floating label board, no web-app screenshot recreation.
```

Translate abstract arguments into failed-redraw scenes. One image should have one primary idea and only a few props that make it recognizable.

## Prompt Quality Gate

Before generating, reject and rewrite a prompt if any of these are true:

- The scene could fit almost any article.
- It contains fewer than three concrete article-specific visual details.
- It is a list of labeled items instead of a complete scene.
- It describes a single object on a mostly empty white background.
- It relies on a generic robot, generic cloud, generic box, generic chart, or generic stick person without article-specific props.
- It uses words such as "diagram", "flowchart", "map", "timeline", "UI overview", "callouts", "infographic", "labels", "feature list", "minimal", "clean", "dense poster", or "crowded".
- It describes tabs, menus, settings lists, page sections, commit history, branch arrows, or a product screen as the main visual instead of turning them into objects in a scene.
- In `none` mode, it keeps reusing Xiaoliang, Axu, the same blue-shirt person, the same hoodie person, same face, same haircut, or same outfit as a hidden protagonist.
- In `narrator` mode, it ignores the selected role's core identity markers or makes the narrator too polished.
- It would look more like an icon than an illustration panel.
- It would look like a software tutorial graphic, product UI map, or knowledge-card diagram.
- It would be hard to understand quickly when embedded between article paragraphs.

After generation, inspect the result. Regenerate a panel if it is too empty, too generic, too polished, mostly blank, too cluttered to read, or looks like a labeled diagram instead of a failed redraw of a picture.

## Text In Images

Use image text only for short labels that are naturally printed on objects in the scene, signs, screens, notes, shirts, boxes, or speech bubbles.

- Keep required text short and place it under `Text (verbatim)`.
- Do not put long article paragraphs inside the image.
- Ask for no extra text beyond the required phrase.
- Prefer no text when the scene can carry the idea visually.
- Do not scatter labels around the canvas.
- Inspect the generated result. If text is misspelled or unreadable, regenerate only that image with a targeted correction.

## Reference Redraws

When the user supplies or describes a reference image, label it as a reference and preserve only the loose idea, subject, and broad composition. Do not trace, copy exact details, or imitate any protected character, existing artist, animation studio, brand mascot, or living artist style.

For this skill, the redraw should look like a barely competent memory of the reference: similar enough to understand the relationship, but awkwardly wrong in proportions, placement, and execution.

Even for reference redraws, keep the final image useful as article配图: add a few contextual scene props from the article unless the user requests an isolated redraw.

## Save Outputs

For project-bound work, save final assets under:

```text
outputs/<article-slug>-bad-paint/
```

Use stable filenames:

```text
article-picture-01-cover-bad-paint.png
article-picture-02-<beat>-bad-paint.png
```

Save `prompts.md` in the same folder with:

- article title or source name
- image plan
- character mode and selected role card, if any
- final prompt for each image
- generated image path
- notes about any regeneration or text corrections

Report the saved paths and mention any images that may need manual review for text accuracy.
