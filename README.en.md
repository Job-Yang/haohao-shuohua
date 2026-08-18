# Job Yang AI Skills

AI Agent Skills by Yangquan.

This repository is my personal Skill index. It collects the Agent Skills I use and maintain for writing, video understanding, VDD workflows, and other reusable work patterns.

[简体中文](./README.md)

## Skills

| Skill | What it does | Status |
| --- | --- | --- |
| [haohao-shuohua](./skills/haohao-shuohua/) | Cleans Chinese writing so it sounds like a person wrote it: keeps facts, removes AI flavor, restores Chinese rhythm, and blocks fake profundity. | Active |
| [video-reader](./skills/video-reader/) | Turns video into timestamped keyframes and a motion timeline, so an image-only LLM can reason about what happened at which second. | Active |
| VDD Skill | Evidence-first development workflow: plan, observe, change, verify, and close the loop with reproducible proof. | In progress |

## Why This Repo Exists

Most prompt repositories stop at "how to talk to the model." That is not enough.

I care more about whether an Agent Skill can become a stable working habit: whether it works in real tasks, reduces mistakes, and keeps conclusions grounded in evidence.

The Skills in this repository follow a few rules:

- One Skill should solve one clear problem.
- Trigger conditions, boundaries, and outputs should be explicit.
- Scripts and references are allowed when pure prompting is not enough.
- Documentation should be readable by humans, not only by agents.
- VDD-style Skills must distinguish observation from inference.

## Install

Clone the repository and copy the Skill directory you need into your agent's Skills directory.

```bash
git clone https://github.com/Job-Yang/jobbyang-ai-skills.git
cp -R jobbyang-ai-skills/skills/haohao-shuohua ~/.claude/skills/haohao-shuohua
cp -R jobbyang-ai-skills/skills/video-reader ~/.claude/skills/video-reader
```

Claude Code's default user-level directory is:

```text
~/.claude/skills/
```

Keep each Skill directory intact. Do not copy only `SKILL.md`, because some Skills read files under `references/`, `scripts/`, or `assets/`.

## Repository Layout

```text
.
├── README.md
├── README.en.md
└── skills/
    ├── haohao-shuohua/
    │   ├── SKILL.md
    │   ├── README.md
    │   ├── assets/
    │   └── references/
    └── video-reader/
        ├── SKILL.md
        ├── README.md
        ├── README.zh-CN.md
        └── scripts/
```

## License

MIT
