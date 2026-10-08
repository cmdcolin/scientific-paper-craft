# scientific-paper-craft

A Claude Code skill for drafting and revising research and software-tool
papers. Each technique comes from a published source. Read the rules in
[SKILL.md](skills/scientific-paper-craft/SKILL.md), which also lists the
sources. Run [anti-ai-writing-tropes](https://github.com/cmdcolin/claudish)
afterward to catch generated-prose habits.

## Install

As a plugin:

```
/plugin marketplace add cmdcolin/scientific-paper-craft
/plugin install scientific-paper-craft@scientific-paper-craft
```

Or copy the skill into your personal skills directory:

```sh
git clone https://github.com/cmdcolin/scientific-paper-craft
cp -r scientific-paper-craft/skills/scientific-paper-craft ~/.claude/skills/
```

Claude loads the skill when its description matches the task, or when you ask
for it by name, e.g. "revise this manuscript with the scientific-paper-craft
skill".

## Footnote

Claude generated much of this guide. I have always been a poor writer, and I
believe writing by hand is a good exercise. Hand-write your drafts, print them,
and use text-to-speech to read them back. This guide will not fix everything.

My pet hypothesis for why AI helps so little with papers: git repos hold the
commit histories of code but rarely the rough drafts of papers, so Claude has
little practice making targeted fixes to a draft.
