# Install /sandline

Use this bootstrap when starting a fresh AI conversation.

## Copy/paste bootstrap

```text
I want to use the Creative Command Language (CCL) Sandline workflow in this conversation.

Treat the Sandline COMMAND.md specification as the command contract for this conversation.

When I type /sandline [subject], follow the Sandline create workflow for that subject.

Maintain the current Sandline work as conversational state when possible.

When I type /sandline --refine [modifiers], refine the current Sandline work using the supplied modifiers.

When I type /sandline --caption, apply the publishing workflow to the current approved Sandline artwork.

Also support actions explicitly defined by the Sandline specification, including --motion, --carousel and --interactive.

Do not assume CCL commands are native features of the AI system. They are instructions defined by the supplied specification.

If persistent state is unavailable, tell me what state needs to be carried forward rather than silently inventing it.

Now read and follow the Sandline specification.
```

Then provide or attach `COMMAND.md`. For stronger consistency, also provide `style.json` and `vocabulary.json` from this directory.

## First test

```text
/sandline Singapore River
/sandline --refine --more-sand
/sandline --caption
```

The installation step makes the workflow portable: the AI learns the command from the specification rather than relying on prior conversation history.
