# Prompt Examples

Use these examples to avoid turning article illustrations into tutorial diagrams.

## Software Article Example

Bad direction:

```text
Scene: a GitHub repository page map with Code, Issues, Pull requests, Actions, Settings, file list, README preview, and green Code button.
```

Why it fails: this produces a UI map or tutorial screenshot, not a failed redraw of an article picture.

Better direction:

```text
Imagined reference picture: a confused beginner sitting at a messy desk, looking at a laptop while trying to understand a new GitHub repository.
Failed redraw scene: a badly mouse-drawn room with a wobbly laptop on the desk, the beginner leaning too close to the screen, and a crooked paper notebook beside them.
Scene props: a laptop screen with one ugly folder shape, a sticky note saying "repo?", a coffee cup knocked sideways, and a tiny cardboard box labeled "code".
Text (verbatim): "repo?"
```

Stronger direction when the article mentions a real product UI:

```text
Imagined reference picture: a beginner looking lost inside a physical room that represents the repository home page.
Failed redraw scene: a badly mouse-drawn file-cabinet room with uneven drawers for Code, Issues, Pull Requests, Actions, and Settings; the beginner holds a clone-address paper and stares blankly.
Scene props: a green Code handle on one drawer, a README welcome mat, gray commit note papers taped beside drawers, and a crooked username/repo-name sign above the cabinet.
Text (verbatim): "Code"
```

Why it works: it keeps the GitHub-specific details but turns the UI into a physical scene instead of a page map.

## Version Control Example

Bad direction:

```text
Scene: a commit history timeline with save 1, save 2, save 3, branch arrows, v1-v4 labels, and message boxes.
```

Why it fails: this becomes a timeline infographic.

Better direction:

```text
Imagined reference picture: someone saving their work before making a risky change.
Failed redraw scene: a nervous programmer holding a floppy disk like a life raft while a broken-looking computer smokes on a desk.
Scene props: a crooked floppy disk, a cracked monitor, three messy paper scraps on the floor, and a tiny trash can full of rejected code.
Text (verbatim): "save"
```

Better direction for branch concepts:

```text
Imagined reference picture: a road splitting into one stable main road and one chaotic side road where a risky feature is being built.
Failed redraw scene: a crooked road scene with a calm main road leading to a tiny stable house, and a side road leading to a messy work area where a boxy coding robot hammers on a login door.
Scene props: a road sign saying "main", a side sign for feature-login, a bug trapped in a jar, and a merge cone near the road split.
Text (verbatim): "main"
```

Why it works: it is still about branching, but the image is a place with action, not branch arrows.

## GitHub Workflow Example

Bad direction:

```text
Scene: a Pull Request page with diff files, green added lines, red deleted lines, comments, reviewers, and a Merge button.
```

Why it fails: this becomes a tutorial screenshot or UI overview.

Better direction:

```text
Imagined reference picture: a team reviewing a cardboard box of proposed code changes at a messy meeting table.
Failed redraw scene: a nervous developer pushes a box labeled PR onto a table while reviewers point at red and green paper strips spilling out of it.
Scene props: cardboard PR box, green added paper strips, red removed paper strips, comment sticky notes, and a huge crooked Merge stamp.
Text (verbatim): "PR"
```

Better direction for settings and deployment:

```text
Imagined reference picture: a beginner in a control room pulling a lever that publishes a tiny website.
Failed redraw scene: a boxy settings machine with knobs and drawers; the beginner pulls a crooked Pages lever and a small github.io website sign pops out of the top.
Scene props: Pages lever, github.io sign, key-shaped Secrets drawer, and branch protection padlock.
Text (verbatim): "Pages"
```

## Open Source Example

Bad direction:

```text
Scene: many people connected by lines to a center repo with Star, Fork, PR, Merge, and open source universe labels.
```

Why it fails: this becomes a network diagram.

Better direction:

```text
Imagined reference picture: strangers awkwardly helping repair one small broken project.
Failed redraw scene: several badly drawn people gathered around a tiny cardboard house labeled with a crooked code symbol, each trying to patch a different broken wall.
Scene props: a tape roll, a loose screw, one yellow star sticker on the roof, and a paper fork stuck in the ground.
Text (verbatim): No text
```

## General Rewrite Rule

If the draft prompt contains a product page, menu, settings list, timeline, cloud diagram, arrows between labels, or labeled feature boxes, rewrite it as a physical scene with a person, room, desk, object, doorway, road, shop, box, broken machine, or other tangible setup.

## Physical Anchor Cheat Sheet

Use these conversions for concept-heavy articles:

| Abstract idea | Physical failed-redraw scene |
| --- | --- |
| Repository | Overstuffed project folder or cardboard project box |
| New repository form | Paper form on a counter with a stamp |
| Repository home page | File-cabinet room with drawers and taped notes |
| README | Storefront door, welcome mat, or project resume poster |
| Branch | Road split or parallel work area |
| Commit | SAVE button, floppy disks, or sticky-note message |
| Fork / Star | Workshop shelf, copied project box, star sticker |
| Pull Request | Cardboard box of changed code at a review table |
| Settings / Pages | Control machine with levers and drawers |
| AI-generated project | Robot feeding code bundles into a mailbox or project box |
