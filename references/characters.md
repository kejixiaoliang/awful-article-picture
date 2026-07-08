# Character Modes

Awful Article Picture supports only two character modes: `none` and `narrator`.

## `none`

Default mode. Use this when the user does not ask for a recurring role, author avatar, IP-like figure, or narrator.

Rules:

- Do not use a fixed protagonist.
- Do not repeatedly generate the same blue-shirt little person.
- Do not preserve the same face, hair, clothes, or body type across the whole article.
- Let each scene decide whether it needs a person, object, room, animal-free prop, machine, desk, or no living character at all.
- If people appear, vary them naturally and redraw them badly.

Prompt line:

```text
Character mode: none
Narrator role: No recurring narrator. Do not reuse the same blue-shirt character, face, hairstyle, or outfit across images.
Character placement: No fixed character; vary people naturally and omit people when the scene works without them.
```

## `narrator`

Use this only when the user explicitly selects a fixed narrator / author avatar / role card.

Supported role ids:

- `role-01`, also called `角色1`
- `role-02`, also called `角色2`

Load the selected file from `references/character-library/`.

Rules:

- Preserve only the core identity markers from the role card.
- The narrator can be a viewer, operator, confused participant, author avatar, or person being overwhelmed by the article topic.
- The narrator does not need to appear in every image.
- The narrator must remain in the awful MS Paint failed-redraw style.
- Do not make the narrator cute, polished, consistent like a model sheet, or more important than the article scene.

Prompt line:

```text
Character mode: narrator
Narrator role: <role-id>; preserve these key markers: <paste key markers from role card>.
Character placement: Use the narrator only when they help the scene; otherwise keep the scene focused on the article beat.
```

## User-Supplied Roles

Users may replace `role-01.md` and `role-02.md` with their own original or authorized characters.

Acceptable:

- Original author avatar.
- User-owned mascot.
- Internal brand character with permission.
- A text role card written by the user.
- User-supplied reference images they own or are allowed to use.

Avoid:

- Copying a famous anime, game, movie, or comic character.
- Copying a living artist's style.
- Recreating a branded mascot without authorization.
- Treating an unauthorized IP as a reusable narrator.
