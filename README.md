# agent-tooling

A Claude Code plugin with one skill, `build-tooling`, for creating, editing, and improving skills, plugins, agents, hooks, and the scripts a skill drives. It covers:
- splitting work between scripts and the model
- token budget and performance
- safe writes, and handling untrusted content
- portability, and readiness for CI later
- self-improvement without churn
- verifying changes with dry runs

[`improve.md`](skills/build-tooling/improve.md) holds the rules for turning a run's notes into a change. It's self-contained, so other skills' "Improving the skill" sections can point to its raw URL without requiring this plugin:

https://raw.githubusercontent.com/zcorpan/agent-tooling/main/skills/build-tooling/improve.md

## Install

From Claude Code, either from this repo's marketplace:

```
/plugin marketplace add zcorpan/agent-tooling
/plugin install agent-tooling@agent-tooling
```

or alongside `web-platform-skills` and `httparchive`, from that marketplace:

```
/plugin marketplace add zcorpan/web-platform-skills
/plugin install agent-tooling@web-platform-skills
```

Auto-update is off by default for these marketplaces. To turn it on, open `/plugin`, go to Marketplaces, select the marketplace, and choose Enable auto-update.

Or clone it and symlink it into your skills directory, where it loads as `agent-tooling@skills-dir`:

```
git clone https://github.com/zcorpan/agent-tooling ~/git/zcorpan/agent-tooling
ln -s ~/git/zcorpan/agent-tooling ~/.claude/skills/agent-tooling
```
