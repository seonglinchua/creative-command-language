# Creating a Command

Promote a prompt into a CCL command when it has repeatable:

- intent
- inputs
- vocabulary
- rules
- state
- outputs
- transformations

Start from `templates/command-template.md`.

Prefer a small stable interface over many special-case flags. Keep model-specific implementation details outside the core command whenever possible.
