---
name: scripted-mystery-builder
description: Generate complete playable scripted mystery / murder-mystery-style social deduction games for team building, training courses, classrooms, workshops, offline interest groups, corporate simulations, and themed events. Use when the user asks to create a 剧本杀, mystery game, social deduction game, role-based investigation game, workshop game, training scenario, team-building case, host script, character scripts, evidence cards, clue cards, or printable game materials from a short goal, theme, industry, lesson, or event context.
---

# Scripted Mystery Builder

## Core Promise

Turn a short goal or theme into a complete playable mystery game package:

- Host guide with true timeline, rules, facilitation notes, clue release timing, and final reveal script.
- Private character scripts with immersive opening stories, role constraints, hidden mistakes, goals, and talking points.
- Evidence cards that look like physical artifacts, not narrator explanations.
- Optional printable DOCX/PDF materials when the user asks for downloadable files.

Default to a light social-deduction structure: every character has pressure, only one or a few characters are the main culprit(s), and the game is won by identifying the primary cause while navigating partial truths.

## First Clarify Only What Matters

If the user gives a one-line request, proceed with reasonable defaults. Ask only when missing information would materially change the game:

- Audience and occasion: team building, training, classroom, family party, interest club.
- Player count and duration.
- Learning goal or emotional tone: serious training, satire, collaboration, conflict resolution, fun mystery.
- Domain sensitivity: workplace, school, medical, legal, finance, safety, DEI, harassment, or other high-stakes themes.

Default assumptions when unspecified:

- 6 players + 1 host.
- 30-60 minutes.
- One incident, one primary responsible party, every character has a smaller hidden issue.
- No gore, no real-person defamation, no trauma-heavy content unless explicitly requested.

## Build Workflow

1. Define the design brief.
   Capture audience, setting, player count, duration, desired lesson, tone, and constraints.

2. Create the incident.
   Pick a concrete failure with visible stakes. Make it easy to explain in one sentence, then build a hidden causal chain behind it.

3. Create the responsibility model.
   Decide:
   - Primary cause: the direct mechanism that created the incident.
   - Secondary causes: missed checks, ambiguous decisions, rushed process, weak communication, bad incentives.
   - Amplifiers: actions that increased damage but did not create the root issue.
   - Red herrings: suspicious facts that create discussion without becoming unfair.

4. Design the roles.
   Give each role:
   - Name, age, role/title, personality, responsibilities.
   - Communication limits or relationship map when useful.
   - Immersive opening story written in second person.
   - Public stance.
   - Hidden mistake or secret.
   - Known facts.
   - Personal goal.
   - Suggested phrases and defensive angles.

5. Design the evidence deck.
   Evidence must be artifact-like. Use screenshots, logs, receipts, chat transcripts, meeting notes, calendars, call transcripts, forms, test reports, version histories, photos, maps, account pages, sensor logs, invoices, or emails.

   Do not write evidence as narrator conclusions such as “the engineer made the main mistake.” Evidence may pressure a role, but must remain interpretable.

6. Write the host guide.
   Include:
   - Opening speech.
   - Full truth and causal chain.
   - Phase-by-phase flow.
   - Private communication rules.
   - Public discussion and questioning rules.
   - Voting and win conditions.
   - Evidence release timing.
   - Host steering principles.
   - Final reveal script that clearly explains the incident.

7. Check playability.
   Ensure the game is solvable, but not obvious; every role has something to say; no single early clue kills a player’s experience; the host can explain the truth without domain jargon.

8. Produce deliverables.
   If the user asks for files, create separate documents:
   - Character scripts.
   - Evidence cards, one card per page if printing.
   - Host guide.

## Evidence Rules

Evidence cards are the main quality lever. Follow these rules strictly:

- Evidence is a physical or digital artifact, not an explanation.
- The card title should name the artifact: “Order Log Screenshot,” “Project Chat Transcript,” “Budget Approval Email.”
- Evidence can include names if that artifact naturally contains names, but it should not say “this proves X is guilty.”
- Prefer ambiguous phrasing that creates pressure and debate.
- Keep evidence short enough to read aloud in under 45 seconds.
- Each evidence card should do one job: pressure one role, clarify one mechanism, or connect two facts.
- Include at least one mechanism card that explains how the incident was technically or practically possible.
- Include at least one amplifier card showing why damage spread.
- Delay decisive mechanism cards until mid/late game.

When the user is building a printable game, evidence cards should be page-isolated and player-facing. Host-only release notes belong in the host guide, not on the card.

## Character Script Rules

Write character scripts for immersion and play, not just facts.

Each character script should contain:

- Identity block.
- Opening story: 2-5 paragraphs, second person, concrete moment before/after the incident.
- Communication permissions or relationship constraints.
- Public stance: what they can plausibly say in the meeting.
- Hidden mistake: what they want to conceal.
- Known information: partial truth, never complete truth unless needed.
- Goal: both collective and personal.
- Talking points: useful lines, accusations, defenses.
- If main culprit: special danger questions and suggested evasions.

All characters should have agency. Avoid making non-culprits passive witnesses.

## Host Guide Rules

The host guide must be more explicit than player materials. The host should never be confused about what really happened.

Include a “one sentence truth” and a step-by-step causal chain:

- Trigger: what was being attempted?
- Pressure: why did people rush, hide, or miscommunicate?
- Ambiguity: what was unclear?
- Direct mechanism: what exactly produced the bad outcome?
- Missed detection: why was it not caught?
- Amplification: why did damage grow?
- Responsibility ranking: main culprit, secondary responsibility, amplifiers, red herrings.

The final reveal must explain the difference between:

- Who created the incident.
- Who failed to catch it.
- Who made it worse.
- Who merely looked suspicious.

Use plain language. Avoid unnecessary domain jargon, and translate technical terms into everyday analogies.

## Printable Document Guidance

When producing DOCX/PDF materials:

- Use the local document-generation skill or available document tooling when present.
- Make character scripts easy to split by role.
- Make evidence cards one per page when the user asks for printing.
- Remove host notes from player-facing evidence cards.
- Put evidence release timing in the host guide.
- Run structural checks: page size, page breaks, evidence count, and title count.
- If visual render QA cannot run, say so clearly.

## References

Read these only when needed:

- `references/game_blueprint.md` for the full output structure and checklists.
- `references/evidence_patterns.md` for artifact-style clue examples and anti-patterns.
- `references/facilitation_patterns.md` for host flow, timing, and debrief guidance.
