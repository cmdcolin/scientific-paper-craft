# scientific-paper-craft

A skill for Claude Code that drafts and revises research and software-tool
papers. It covers sentence stress, paragraph arcs, captions, Methods detail,
Discussion order and a revision order, each tied to a published source. The
[SKILL.md](skills/scientific-paper-craft/SKILL.md) file lists the sources.

Run [anti-ai-writing-tropes](https://github.com/cmdcolin/claudish) after this
skill to catch generated-prose habits.

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
for it by name.
