# Creative Command Language (CCL)

**Define once. Invoke simply. Create repeatedly.**

A human-readable command language for repeatable AI creative workflows.

CCL turns recurring prompt patterns into named, portable workflows:

```text
/<command> [subject] [--modifier]
```

Instead of rewriting a long prompt, a command points to documented rules, vocabulary, state and outputs.

## See it in action

The first reference implementation is **Sandline** — a visual language combining expressive sand with restrained line illustration.

![Sandline Singapore example](assets/file_00000000abe4820ba3b36c605ee4a000.png)

> **The line describes what we see. The sand expresses what we feel.**

```text
/sandline Singapore River
/sandline --refine --more-sand
/sandline --caption
/sandline --motion
/sandline --carousel
```

### More Sandline examples

| Parliament House — Detailed Study | Marina Bay & Merlion — Line Study |
| --- | --- |
| ![Parliament House detailed Sandline artwork](assets/file_00000000543c820bba2f9b6e27dae411.png) | ![Marina Bay and Merlion Sandline artwork](assets/file_0000000039f8820bb9b12c8d24036fd5.png) |

## Quick Start

AI systems do **not** natively know CCL commands. Load the command specification first.

### 1. Choose a command

Start with [`/sandline`](commands/sandline/COMMAND.md).

### 2. Load it into your AI conversation

Copy the [Sandline install instructions](commands/sandline/INSTALL.md) into a fresh AI conversation, together with the Sandline command specification when requested.

### 3. Invoke the workflow

```text
/sandline Singapore River
```

Review the result, refine it with `/sandline --refine --more-sand`, and when approved use `/sandline --caption`.

## How CCL works

```text
Command → Input → Vocabulary → Rules → State → Output → Transformations
```

A command is a small interface to a larger creative specification. The specification carries durable knowledge; the short command carries current intent.

CCL is designed to be model-independent. ChatGPT, Claude, Gemini or another capable AI can follow a CCL command after receiving its specification. Results will vary by model and available capabilities.

## Reference commands

### `/sandline`

Sand + line visual storytelling.  
[Command specification](commands/sandline/COMMAND.md) · [Vocabulary](commands/sandline/vocabulary.json) · [Examples](commands/sandline/examples/README.md)

### `/oneline`

A minimalist recurring visual series built around one continuous line and one concise thought.  
[Command specification](commands/oneline/COMMAND.md) · [Examples](commands/oneline/examples/README.md)

## Create your own command

Start from [the command template](templates/command-template.md). See [Creating a Command](docs/creating-a-command.md).

## Specification

Read [SPEC.md](SPEC.md) and [Getting Started](docs/getting-started.md).

## Status

**Experimental specification — v0.1.**

The current goal is to test whether a creative workflow can travel between users and AI systems without depending on the original conversation that created it.

## License

MIT. See [LICENSE](LICENSE).
