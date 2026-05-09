# LARPGame Builder

[English](README_EN.md)

`LARPGame Builder` 是一个面向 Codex / Claude Code 等 AI coding agent 的 Skill，用来从一句话目标生成完整、可玩的剧本杀 / LARP / 社交推理游戏。

它适合用于：

- 团队建设
- 企业培训
- 线下兴趣班
- 课堂模拟
- 工作坊活动
- 角色扮演式案例复盘
- 轻量剧本杀或社交推理活动

这个 Skill 会帮助 Agent 生成一整套可运行材料：

- 主持人手册：规则、完整真相、故事线、线索发放节奏、最终复盘讲稿
- 玩家角色剧本：沉浸式开局故事、隐藏目标、已知信息、可用说法
- 证据卡 / 线索卡：以聊天截图、日志、文档截屏、录音转写等“真实证据”形式呈现
- 可打印文档结构：当 Agent 具备文档生成能力时，可输出角色剧本、线索卡、主持人手册等独立文件

## 安装

把 `larpgame-builder` 文件夹复制到你的 Skill 目录。

### Codex

```bash
cp -R larpgame-builder ~/.codex/skills/
```

使用方式：

```text
Use $larpgame-builder to create a 6-player mystery game for a team-building workshop about cross-team communication failure.
```

### Claude Code

Claude Code 也支持 Agent Skills。个人 Skill 可以放在 `~/.claude/skills/`；项目共享 Skill 可以放在项目内的 `.claude/skills/`。

个人安装：

```bash
mkdir -p ~/.claude/skills
cp -R larpgame-builder ~/.claude/skills/
```

项目安装：

```bash
mkdir -p .claude/skills
cp -R larpgame-builder .claude/skills/
```

示例提示词：

```text
Use the larpgame-builder skill to create a 45-minute LARP mystery game for a leadership training workshop.
```

不同版本的 Claude Code 对 Skill 目录位置和加载方式可能略有差异，请以 Claude Code 当前官方文档为准。

## 示例提示词

```text
Use $larpgame-builder to create a 45-minute workplace mystery game about a failed product launch for 6 players.
```

```text
Use $larpgame-builder to create a classroom mystery game that teaches students how misinformation spreads.
```

```text
Use $larpgame-builder to create a team-building 剧本杀 for a sales team, focused on handoff mistakes and incentive conflicts.
```

中文也可以：

```text
用 $larpgame-builder 生成一个 6 人职场剧本杀，用于团队建设，主题是跨部门沟通失败导致项目事故。
```

## 设计原则

这个 Skill 的核心来自一套可玩性原则：

- 每个角色都要有压力、行动空间和想隐藏的事情。
- 真相应该能被推理出来，但不能一眼看穿。
- 线索卡应该像真实证据，而不是主持人的旁白。
- 玩家可见线索不能写“某某就是凶手”或“这证明某某犯错”。
- 主持人手册必须把完整真相讲清楚，让主持人能够顺利控场。
- 最终复盘要区分：谁制造了事故、谁没拦住事故、谁放大了事故、谁只是看起来可疑。

## 仓库结构

```text
larpgame-builder/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── evidence_patterns.md
    ├── facilitation_patterns.md
    └── game_blueprint.md
```

## License

MIT License. See [LICENSE](LICENSE).
