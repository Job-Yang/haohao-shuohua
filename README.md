# Job Yang AI Skills

Practical agent Skills by Yangquan, built around one rule: an AI assistant should not only generate an answer, it should leave evidence that the answer stands.

This repository is my public Skill index. It collects the Skills I use for writing, reading media, debugging, and VDD-style agent work.

## Skills

| Skill | What it does | Status |
| --- | --- | --- |
| [haohao-shuohua](./skills/haohao-shuohua/) | Cleans Chinese writing so it sounds like a person wrote it: keeps facts, removes AI flavor, restores Chinese rhythm, and blocks fake profundity. | Active |
| [video-reader](./skills/video-reader/) | Turns video into timestamped keyframes and a motion timeline, so an image-only LLM can reason about what happened at which second. | Active |
| VDD Skill | Evidence-first development workflow: plan, observe, change, verify, and close the loop with reproducible proof. | In progress |

## Why This Repo Exists

Most prompt libraries stop at "say the right thing to the model." That is too weak for real work.

These Skills are meant to be small, installable working habits:

- Write in Chinese without drifting into translationese.
- Read a video by turning it into concrete frames and timestamps.
- Make development decisions with evidence instead of confidence.
- Keep each Skill narrow enough to be useful, but documented enough to be reused.

## Install

Clone the repository and copy the Skill directory you need into your agent's Skills directory.

```bash
git clone https://github.com/Job-Yang/ai-skills.git
cp -R ai-skills/skills/haohao-shuohua ~/.claude/skills/haohao-shuohua
cp -R ai-skills/skills/video-reader ~/.claude/skills/video-reader
```

Claude Code's default user-level directory is:

```text
~/.claude/skills/
```

Keep each Skill directory intact. Do not copy only `SKILL.md`, because some Skills read files under `references/`, `scripts/`, or `assets/`.

### Backward Compatibility

The old `haohao-shuohua` repository has become this Skill index. Existing links to:

```text
https://github.com/Job-Yang/haohao-shuohua
```

will redirect here after the GitHub rename. The repository root still contains a compatibility `SKILL.md` for `haohao-shuohua`, so old installs keep working.

## Repository Layout

```text
.
├── README.md
├── SKILL.md                         # compatibility entry for haohao-shuohua
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

## Design Rules

- One Skill should do one real job.
- A Skill should say when to trigger, what evidence to produce, and where its limits are.
- Scripts are allowed when pure prompting is not enough.
- Documentation should be readable by humans, not only by agents.
- VDD-style Skills must distinguish observation from inference.

## License

MIT
