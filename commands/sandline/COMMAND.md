# /sandline

**Version:** 1.0.0  
**Type:** visual-language  
**Default action:** create

## Intent

Create artwork using the Sandline visual language: expressive physical-looking sand combined with restrained line illustration.

> The line describes what we see. The sand expresses what we feel.

## Default workflow

```text
Create → Preview → Refine → Approve → Caption → Publish
```

`/sandline [subject]` creates and previews an artwork.

`/sandline --caption` packages the current approved artwork for publishing.

## Visual rules

- Sand is a major artistic medium, not a decorative filter.
- Prefer black/charcoal linework, warm natural sand and off-white paper.
- Preserve generous negative space.
- Use restrained accent colour.
- Consider grain size, density, direction, accumulation and dispersion.
- Let selected edges dissolve from precise line into sand.
- Avoid drifting into conventional full watercolor rendering.
- Keep some architecture or forms intentionally incomplete when appropriate.

## Actions

- `--refine` — improve the current work.
- `--caption` — generate publishing metadata for the current work.
- `--motion` — develop a motion treatment.
- `--carousel` — create a social carousel concept.
- `--interactive` — develop an interactive-web treatment.
- `--product` — explore physical/digital applications.

## Example modifiers

- `--more-sand`
- `--less-color`
- `--less-text`

Subject aliases MAY be implementation-specific, e.g. `--mbs` for Marina Bay Sands.

## Publishing package

The caption action SHOULD produce:

- ID
- title
- quote
- social caption
- artwork description
- collection
- filename
- status

Quote, caption and description are distinct:

- **Quote** — emotional/philosophical thought.
- **Caption** — audience-facing social story.
- **Description** — archival/portfolio explanation.

Do not automatically place the full caption or description inside the artwork.

## Registry

Recommended IDs: `SL-001`, `SL-002`, ...

A production implementation SHOULD persist registry state outside conversational memory.
