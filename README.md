# econ-paper-style

A Claude Code skill for writing and editing economics papers in a plain, precise register, with AI writing patterns removed.

## Install

```
git clone https://github.com/matyasfarkas/econ-paper-style ~/.claude/skills/econ-paper-style
```

Then ask Claude Code for a style pass on a draft, or type `/econ-paper-style`.

## Files

- `SKILL.md`: the rules (claims, structure, words) and the steps of a style pass.
- `references/patterns.md`: the patterns to remove, with before and after examples.

## Sources

- The humanizer skill by Siqi Chen, <https://github.com/blader/humanizer> (v4.0.0, MIT licence). The pattern numbers and the list of overused AI words in `references/patterns.md` come from it. Humanizer credits Wikipedia's ["Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).
- The econ-write writing guide, which the author used for the rules on the abstract, introduction and conclusion. It is not reproduced here, and its source is not recorded.
- The target register is the prose of Lawrence J. Christiano and Jesper Lindé. No text from their papers is reproduced.
- The other rules and all examples come from editorial passes on an unpublished economics working paper by the author and a coauthor (2026). Numbers in the examples are replaced by x and y.

The skill was written with Claude Code (Anthropic). The author is responsible for its content.

## Licence

MIT. See `LICENSE`.
