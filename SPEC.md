# CCL Specification v0.1

## Purpose

Creative Command Language (CCL) is a lightweight convention for defining repeatable AI creative workflows independently from any single model or vendor.

## Grammar

```text
/<command> [subject] [--modifier] [value]
```

Examples:

```text
/sandline Singapore River
/sandline --caption
/sandline --refine --more-sand
```

## Command contract

A command SHOULD define:

1. **Intent** — what workflow it represents.
2. **Inputs** — subject and optional parameters.
3. **Vocabulary** — domain terms understood by the workflow.
4. **Rules** — persistent creative/operational constraints.
5. **State** — current item and registry behavior when applicable.
6. **Outputs** — artifacts produced.
7. **Transformations** — actions such as refine, caption, motion or carousel.

## State

CCL syntax may refer to current workflow state. For example, after creating a Sandline artwork, `/sandline --caption` refers to the current approved Sandline work.

Implementations that cannot retain state SHOULD persist it externally, such as in a registry JSON file.

## Portability

CCL does not assume that an AI model natively understands a command. An implementation MUST first provide or load the command specification.

## Design principle

Commands should hide repetitive instruction, not hide human judgment.
