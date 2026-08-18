# Job Yang AI Skills

杨权的 AI Agent Skills 技能表。

这里收的是我自己长期使用、持续维护的 Agent 技能：中文写作、视频理解、VDD 工作流，以及后续更多能在真实任务里复用的能力。

[English](./README.en.md)

## 技能列表

| Skill | 用来做什么 | 状态 |
| --- | --- | --- |
| [haohao-shuohua](./skills/haohao-shuohua/) | 把中文写得更像人说的：保事实、去 AI 味、加中文味、不许造词充深刻。 | Active |
| [video-reader](./skills/video-reader/) | 把视频转成带时间戳的关键帧和运动时间线，让只能看图的大模型也能判断第几秒发生了什么。 | Active |
| VDD Skill | 基于证据的开发闭环：计划、观察、改动、验证、收口，每个结论都留下可复核证据。 | In progress |

## 为什么要有这个仓库

很多 prompt 仓库只解决“怎么对模型说话”。这不够。

我更关心的是：一个 Agent Skill 能不能变成稳定的工作习惯，能不能在真实任务里少犯错，能不能把结论建立在证据上。

所以这个仓库里的技能会尽量保持几个原则：

- 一个 Skill 只解决一个清楚的问题。
- 触发条件、工作边界、产物形态都写清楚。
- 纯 prompt 不够时，可以带脚本和参考资料。
- 文档给人看也要顺，不只给模型解析。
- VDD 类技能必须区分观察和推断，推断不能冒充证据。

## 安装

克隆仓库后，把需要的技能目录复制到你的 Agent Skills 目录。

```bash
git clone https://github.com/Job-Yang/jobbyang-ai-skills.git
cp -R jobbyang-ai-skills/skills/haohao-shuohua ~/.claude/skills/haohao-shuohua
cp -R jobbyang-ai-skills/skills/video-reader ~/.claude/skills/video-reader
```

Claude Code 的默认用户级目录：

```text
~/.claude/skills/
```

安装时要保留完整技能目录，不要只复制 `SKILL.md`。有些技能会读取 `references/`、`scripts/` 或 `assets/`。

## 目录结构

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
