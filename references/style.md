# Bad MS Paint Style

Paste this style layer into every generation prompt unless the user explicitly asks for a different style.

```text
Redraw the requested scene as if there was a normal reference picture, but someone incompetently copied it with a mouse in old MS Paint. Use a 16:9 horizontal canvas and a plain white background. The image should look like a failed redraw of a real picture, not a diagram or explainer graphic. Keep one complete awkward scene with a main subject, crude background, ugly perspective, and a few props from the article. Make it clumsy, rough, pitiful, and oddly wrong: recognizable enough to understand, but inaccurate, embarrassing, and strangely off. Use crooked shapes, shaky outlines, uneven proportions, blunt flat colors, careless fills, jagged pixel-ish edges, and visible one-pixel-at-a-time low-quality reconstruction. It should feel like the artist tried to copy a reference image, failed badly, then gave up. Do not make it polished, clean, cute, infographic-like, label-heavy, or neatly educational. If short required text is included, put it naturally on an object and make it readable but awkwardly mouse-drawn.
```

## Aspect Ratio Guidance

- Use `16:9` for every image by default.
- If a section feels too complex for one readable `16:9` failed-redraw scene, split it into multiple `16:9` scenes instead of turning it into a diagram.

## Scene Guidance

- Prefer concrete scenes and failed redraws over abstract icons.
- Fill roughly `45-65%` of the canvas with the scene while keeping the background white.
- Include a main subject plus `2-4` scene props from the article.
- Make props part of the picture: on a desk, wall, screen, box, floor, doorway, shelf, road, hand, bag, or messy room.
- Make the image feel like a bad copied picture, not a sparse icon, logo, tutorial graphic, UI map, or overloaded poster.
- Keep the scene readable even when it is intentionally bad. The best result is a colorful, clumsy, specific scene that looks embarrassingly mouse-drawn, not an empty joke sketch or a clean instructional graphic.
- For software topics, prefer physical anchors such as file cabinets, paper forms, cardboard boxes, roads, storefronts, garage objects, levers, shelves, stamps, mailboxes, and messy meeting tables.
- Use deliberately wrong scale, stiff poses, off-center placement, and uneven spacing.
- It is acceptable for lines to wobble, fills to leak slightly, and simple objects to look weird.
- Avoid glossy lighting, realistic textures, cinematic composition, vector polish, clean infographic style, callouts, floating labels, flowcharts, timelines, product UI maps, minimal whitespace-heavy composition, crowded poster composition, complex infographic style, or a single isolated object.

## Bad Output Signals

Regenerate if the image looks like a diagram, flowchart, tutorial screenshot, UI map, label board, simple icon, or knowledge-card graphic. Also regenerate if it has huge empty white areas, lacks article-specific clues, could be reused for many unrelated articles, or is too cluttered to understand quickly.

## Good Output Signals

Keep an image when it looks like a bad redraw of a specific article picture: one awkward scene, a visible main subject, a few contextual props, ugly mouse lines, wrong proportions, white background, and very little text.

## Reference Safety

When a source image, screenshot, meme, logo, character, or branded visual is mentioned, preserve only the rough idea and composition needed for article context. Do not reproduce protected details, exact logos, exact character designs, or a living artist's style.
