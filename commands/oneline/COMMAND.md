# /oneline

**Version:** 1.0.0  
**Type:** visual-language / thought-series  
**Default action:** create

## Intent

Create one finished bilingual artwork for **一線一念 · One Line, One Thought**: a recurring visual series that turns a simple subject into one concise thought about confidence, growth, resilience, work or everyday life.

> Small Characters. Big Insights.

## Default workflow

```text
Subject → Metaphor → Chinese Thought → English Interpretation → Visual Composition → Master Artwork → Registry Update
```

`/oneline` continues with the next suitable unused subject when registry state is available.

`/oneline [subject]` creates the next artwork using the supplied subject.

Default create output is **exactly one finished master artwork**.

## Syntax

```text
/oneline
/oneline [subject]
/oneline [subject] [--modifier]
```

`/online` MAY be supported as a typo-friendly alias.

## Visual rules

- Use minimalist continuous-line or hand-drawn illustration as the dominant visual language.
- Keep subjects cute, simplified and expressive without becoming visually busy.
- Prefer a warm white or lightly textured background and generous negative space.
- Use dominant black/charcoal linework with only 1–3 restrained accent colours.
- Use Chinese calligraphy as a major visual anchor.
- Always provide a clear English translation or interpretation of the Chinese thought.
- A small red Chinese seal MAY be used as a recurring signature element.
- Environmental elements SHOULD support the metaphor rather than become a detailed background.
- Maintain a warm, thoughtful, optimistic and slightly playful tone.
- Avoid preachy or overly generic motivational language.
- Preserve the series identity: **一線一念 · One Line, One Thought** and **Small Characters. Big Insights.**

## Subject categories

Implementations SHOULD support:

- `--animal`
- `--food`
- `--object`
- `--nature`
- `--people`
- `--work`
- `--tech`
- `--random`

## Theme modifiers

Example modifiers:

- `--confidence`
- `--growth`
- `--resilience`
- `--deep`
- `--gentle`
- `--fun`

Modifiers MAY be combined with a subject or category.

## Actions

- `--caption` — generate a publishing-ready caption for the current artwork.
- `--info` — return artwork number, subject, thought, translation, theme, filename and metadata.
- `--list` — return the known series registry.

Motion is intentionally a separate composable CCL command. A future `/motion` command MAY consume an approved /oneline master artwork as input.

## Composition

A typical artwork SHOULD contain:

1. Series identity.
2. Hero subject or character.
3. Large Chinese thought/calligraphy.
4. English interpretation.
5. Optional smaller supporting thought.
6. Minimal recurring signature/branding.

The subject MAY be an animal, food, object, natural element, person, workplace concept or technology concept. The visual system, not the subject category, creates continuity.

## Publishing package

Publishing metadata SHOULD include:

- ID
- subject
- theme
- Chinese thought
- English interpretation
- optional supporting thought
- social caption
- artwork description
- filename
- status

Recommended filename:

```text
one-line-one-thought-###-<subject>.png
```

## Registry

Recommended IDs: `OLT-001`, `OLT-002`, ...

A production implementation SHOULD persist registry state outside conversational memory.

When no subject is supplied, use registry state to select the next suitable unused entry. Do not intentionally repeat a subject unless requested.

The reference registry is stored in `registry.json`.

## Portability

AI systems do not natively know CCL commands. The command specification must be loaded or otherwise made available to the AI system.

If persistent registry state is unavailable, the implementation MUST NOT silently invent prior entries. It SHOULD state what state is missing or ask for the registry.
