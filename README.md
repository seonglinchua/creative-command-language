# Creative Command Language (CCL)

A human-readable command language for repeatable AI creative workflows.

CCL turns recurring prompt patterns into named, portable creative workflows:

```text
/<command> [subject] [--modifier]
```

Instead of rewriting a long prompt, a command points to a documented set of rules, vocabulary, state and outputs.

## v0.1

The first reference implementation is **Sandline**:

```text
/sandline Singapore River
/sandline --caption
/sandline --motion
/sandline --carousel
```

Sandline principle:

> The line describes what we see. The sand expresses what we feel.

A second reference command, **One Line, One Thought**, demonstrates how another creative workflow can use the same command model.

## Core model

```text
Command → Input → Vocabulary → Rules → State → Output → Transformations
```

See [SPEC.md](SPEC.md) and [Getting Started](docs/getting-started.md).

## Status

Experimental specification — v0.1.

## License

MIT.
