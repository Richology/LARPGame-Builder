# LARPGame Builder

`LARPGame Builder` is a Codex Skill for generating complete, playable scripted mystery / 剧本杀-style social deduction games from a short prompt.

It is designed for:

- Team-building workshops
- Training courses
- Offline interest classes
- Classroom simulations
- Corporate retrospectives
- Role-based investigation games
- Light murder-mystery or LARP-style events

The Skill helps an agent produce a full game package:

- Host guide with rules, true timeline, clue release timing, and final reveal script
- Private character scripts with immersive opening stories and hidden objectives
- Evidence cards that look like real artifacts rather than narrator explanations
- Printable-ready material structure when document generation tools are available

## Install

Copy the skill folder into your Codex skills directory:

```bash
cp -R scripted-mystery-builder ~/.codex/skills/
```

Then invoke it by name:

```text
Use $scripted-mystery-builder to create a 6-player mystery game for a team-building workshop about cross-team communication failure.
```

## Example Prompts

```text
Use $scripted-mystery-builder to create a 45-minute workplace mystery game about a failed product launch for 6 players.
```

```text
Use $scripted-mystery-builder to create a classroom mystery game that teaches students how misinformation spreads.
```

```text
Use $scripted-mystery-builder to create a team-building 剧本杀 for a sales team, focused on handoff mistakes and incentive conflicts.
```

## Design Principles

The Skill is built around several playability rules:

- Every character should have pressure, agency, and something to hide.
- The main answer should be discoverable but not obvious.
- Evidence cards should feel like physical or digital artifacts: chat screenshots, logs, reports, document snippets, call transcripts, receipts, or dashboards.
- Player-facing clue cards should not contain host commentary or direct accusations.
- The host guide should explain the true incident clearly enough that the host can run the game without improvising the logic.
- Final reveals should distinguish who created the incident, who failed to catch it, who amplified it, and who only looked suspicious.

## Repository Structure

```text
scripted-mystery-builder/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── evidence_patterns.md
    ├── facilitation_patterns.md
    └── game_blueprint.md
```

## Validation Note

The Skill itself has no runtime dependency on PyYAML. Codex loads `SKILL.md` and its referenced Markdown files directly.

During local development, the optional `quick_validate.py` helper from the system skill-creator package may require `PyYAML` in the Python environment. If validation fails with `ModuleNotFoundError: No module named 'yaml'`, install PyYAML in that environment or run validation in an environment that already includes it. This does not affect normal Skill usage.

## License

No license has been added yet. Add one before publishing broadly if you want to define reuse terms clearly.
