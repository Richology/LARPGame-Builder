# Evidence Patterns

Use this reference when writing clue cards.

## Golden Rule

Evidence cards should feel discovered, not narrated.

Bad:

> The engineer wrote the wrong function and caused the loss.

Good:

> Code repository screenshot: commit `a81c2f`, file `membership_price_service.ts`, comment “please add an extreme price case,” status “Resolved,” linked tests not shown.

## Artifact Types

Use artifacts appropriate to the setting:

- Chat screenshots: team chat, class group, family group, volunteer channel.
- Emails: approvals, warnings, handoffs, customer complaints.
- Logs: order logs, access logs, sensor logs, attendance logs, audit logs.
- Documents: requirements, policies, contracts, lesson plans, checklists.
- Forms: incident forms, sign-up forms, inspection forms, refund forms.
- Screenshots: product pages, dashboards, user accounts, inventory screens.
- Meeting records: agenda, minutes, transcript snippets, call summaries.
- Version histories: design versions, code commits, document edits.
- Physical evidence: receipts, photos, labels, maps, badges, printed notices.
- Audio/video transcripts: short excerpts only, no long walls of text.

## Clue Strength Ladder

Use varied clue strengths.

1. Atmosphere clue
   Shows stakes or mood. Usually public.

2. Pressure clue
   Makes one role look questionable, but has multiple interpretations.

3. Connection clue
   Links two facts or two roles.

4. Mechanism clue
   Explains how the bad outcome could happen.

5. Decisive clue
   Strongly supports the final answer. Release late.

Do not make every clue decisive.

## Evidence Card Template

```text
Card Number
Artifact Title
Artifact Type

[Artifact content]

Optional visible metadata:
Source:
Time:
Status:
Version:
```

Keep host-only notes outside the player-facing card.

## Ambiguity Techniques

Use these to preserve discussion:

- Show a comment without its full resolution.
- Show a timestamp that creates pressure but not certainty.
- Show a missing field, absent test, or unresolved annotation.
- Show two roles in the same artifact.
- Show a system state but not the full conclusion.
- Use realistic labels: “pending,” “resolved,” “draft,” “approved,” “unknown.”

## Anti-Patterns

Avoid:

- “This proves X did it.”
- “The main culprit is X.”
- “Because of X’s mistake, Y happened.”
- Host commentary on player-facing cards.
- Evidence that requires specialist knowledge without explanation elsewhere.
- Huge walls of text that players will not read.
- Evidence that accuses one role so directly they cannot play.

## Example: Transforming Narration Into Evidence

Narration:

> Operations shared the link early and made the loss worse.

Evidence:

```text
Core User Group Screenshot

19:51  Tang You: Anniversary membership preview for old friends first. Official start at 20:00.
19:53  User A: Why does annual membership show 1 yuan?
19:54  User B: Mine also says 1 yuan.
19:55  Tang You: Wait, let me confirm.
19:57  User C: I already bought it.
```

This pressures operations while still allowing a defense: they discovered and reported the problem.
