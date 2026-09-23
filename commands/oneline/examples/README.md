# One Line examples

## Default continuation

```text
/oneline
```

Uses the next suitable unused registry entry and creates exactly one master artwork.

## Explicit subject

```text
/oneline snail
/oneline coffee
/oneline lighthouse --deep
```

## Categories

```text
/oneline --animal
/oneline --food
/oneline --object
/oneline --nature
/oneline --work
/oneline --tech
/oneline --random
```

## Themes

```text
/oneline --object --confidence
/oneline bamboo --resilience
/oneline coffee --work
/oneline --random --deep
```

## Publishing and state

```text
/oneline --info
/oneline --caption
/oneline --list
```

## Composition with other CCL commands

/oneline owns creation of the master artwork. Motion should be handled by a separate composable command rather than embedded into this specification.

```text
/oneline
   ↓
master artwork
   ↓
/motion
```

A production implementation should persist registry state outside conversational memory.
