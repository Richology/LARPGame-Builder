# LARPGame Builder

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

## 校验说明

Skill 本身没有运行时依赖。Agent 主要读取：

- `larpgame-builder/SKILL.md`
- `larpgame-builder/references/*.md`

如果你使用某些开发工具校验 Skill，例如 Codex skill-creator 里的 `quick_validate.py`，它可能需要当前 Python 环境安装 `PyYAML`。如果出现：

```text
ModuleNotFoundError: No module named 'yaml'
```

这只是本地校验工具缺依赖，不影响 Skill 正常使用。

## License

MIT License. See [LICENSE](LICENSE).

---

# English Version

`LARPGame Builder` is a Skill for Codex, Claude Code, and similar AI coding agents. It turns a short goal into a complete, playable scripted mystery / LARP / social deduction game.

It is designed for:

- Team-building workshops
- Corporate training
- Offline interest classes
- Classroom simulations
- Facilitated retrospectives
- Role-based investigation games
- Lightweight murder-mystery or LARP-style events

The Skill helps an agent produce a full game package:

- Host guide with rules, true timeline, clue release timing, and final reveal script
- Private character scripts with immersive opening stories and hidden objectives
- Evidence cards that look like real artifacts instead of narrator explanations
- Printable-ready material structure when document generation tools are available

## Installation

Copy the `larpgame-builder` folder into your agent's Skill directory.

### Codex

```bash
cp -R larpgame-builder ~/.codex/skills/
```

Example:

```text
Use $larpgame-builder to create a 6-player mystery game for a team-building workshop about cross-team communication failure.
```

### Claude Code

Claude Code also supports Agent Skills. Personal Skills can be stored in `~/.claude/skills/`; project Skills can be stored in `.claude/skills/` inside your project.

Personal install:

```bash
mkdir -p ~/.claude/skills
cp -R larpgame-builder ~/.claude/skills/
```

Project install:

```bash
mkdir -p .claude/skills
cp -R larpgame-builder .claude/skills/
```

Example:

```text
Use the larpgame-builder skill to create a 45-minute LARP mystery game for a leadership training workshop.
```

Claude Code's Skill loading paths and behavior may vary by version, so check the current Claude Code documentation when installing.

## Example Prompts

```text
Use $larpgame-builder to create a 45-minute workplace mystery game about a failed product launch for 6 players.
```

```text
Use $larpgame-builder to create a classroom mystery game that teaches students how misinformation spreads.
```

```text
Use $larpgame-builder to create a team-building mystery game for a sales team, focused on handoff mistakes and incentive conflicts.
```

## Design Principles

- Every character should have pressure, agency, and something to hide.
- The truth should be discoverable, but not obvious.
- Evidence cards should look like real artifacts: chat screenshots, logs, reports, document snippets, call transcripts, receipts, or dashboards.
- Player-facing clue cards should not contain host commentary or direct accusations.
- The host guide should explain the true incident clearly enough that the host can run the game without improvising the logic.
- Final reveals should distinguish who created the incident, who failed to catch it, who amplified it, and who only looked suspicious.

## Repository Structure

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

## Validation Note

The Skill itself has no runtime dependency. Agents primarily read:

- `larpgame-builder/SKILL.md`
- `larpgame-builder/references/*.md`

Some local validation helpers, such as Codex skill-creator's `quick_validate.py`, may require `PyYAML` in the Python environment. If validation fails with:

```text
ModuleNotFoundError: No module named 'yaml'
```

that means the local validation tool is missing a dependency. It does not affect normal Skill usage.

## License

MIT License. See [LICENSE](LICENSE).
