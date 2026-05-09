# LARPGame Builder

[中文](README.md)

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

## License

MIT License. See [LICENSE](LICENSE).
