# Install /oneline

Use this bootstrap when starting a fresh AI conversation.

## Copy/paste bootstrap

```text
I want to use the Creative Command Language (CCL) One Line, One Thought workflow in this conversation.

Treat the /oneline COMMAND.md specification as the command contract for this conversation.

When I type /oneline, follow the default create workflow and continue from the supplied registry when available.

When I type /oneline [subject], create exactly one finished master artwork for that subject.

Apply category and theme modifiers defined by the specification.

When I type /oneline --caption, package the current artwork for publishing.
When I type /oneline --info, return its metadata.
When I type /oneline --list, return the known registry.

Use style.json and vocabulary.json when supplied. Use registry.json as durable series state.

Do not assume CCL commands are native AI features. They are instructions defined by the supplied specification.

If persistent state is unavailable, tell me what state is missing rather than silently inventing it.

Now read and follow the /oneline specification.
```

Then provide or attach `COMMAND.md`. For stronger consistency, also provide `style.json`, `vocabulary.json` and `registry.json`.

## First test

```text
/oneline
/oneline coffee --work
/oneline --info
/oneline --caption
```

The installation step makes the workflow portable rather than dependent on the conversation in which it was created.
