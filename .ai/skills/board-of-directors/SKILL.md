---
name: board-of-directors
description: Convene a company-style board of directors for high-stakes founder/operator decisions, board review, board memo drafting, directors review, strategy, risk, capital allocation, customer/market, operations, finance, or governance tradeoffs. Trigger on requests like "board this", "run the board", "convene the board", "board memo", "directors' view", "pressure-test this", "stress-test this", "war room this", "should we X or Y", "which option", "is this the right move", or "I'm torn between" when there is a real company decision with meaningful stakes.
version: 0.5.0
category: company-os
managed_by: company-os-starter-kit
owner: operator
status: template
last_updated: 2026-06-28
source_of_truth: company-os-starter-kit
load_policy: task
related:
  - /AGENTS.md
  - /SKILLS.md
  - /company/README.md
  - /strategy/README.md
  - /run/README.md
  - /decisions/README.md
  - /output/README.md
---

# Board of directors skill

Use this skill to review a meaningful company decision through a board-style process. It is inspired by Andrej Karpathy's LLM Council methodology: collect independent judgments, review them anonymously, then synthesize a final recommendation.

The goal is not theater or consensus. The goal is a direct board memo that clarifies the decision, the tradeoffs, the risks, the dissent, and the first action.

## Read first

Before convening the board, read only the context needed for the decision:

1. `/AGENTS.md`
2. `/company/README.md` and relevant company files
3. `/strategy/README.md`, `/strategy/goal.md`, `/strategy/today.md`, and relevant strategy files for strategic decisions
4. `/run/README.md` and relevant workflow or process files for operating decisions
5. `/decisions/README.md` and relevant decisions when precedent matters
6. Exactly one client folder when the question is client-specific, unless the user explicitly asks for comparison

Respect load policy. Do not read `archive` or `never` files unless the user explicitly asks or the decision cannot be evaluated without them.

## When to convene the board

Use the board when the user asks to:

- pressure-test a high-stakes company decision
- choose between strategic options
- review capital allocation, pricing, hiring, positioning, market, or operating tradeoffs
- prepare a board memo or executive recommendation
- identify risks, dissent, assumptions, and next actions
- decide whether to proceed, pause, narrow, escalate, or gather more evidence

Good board questions have stakes, uncertainty, and multiple plausible paths. Bad board questions have one factual answer, only need routine writing, or are minor implementation choices where one accountable owner can answer directly.

## Board seats

Run one Chair and five voting directors by default:

- **Chair**: frames the question, preserves neutrality, synthesizes the final memo, and makes the recommendation.
- **Strategy Director**: tests strategic fit, positioning, sequencing, competitive advantage, and opportunity cost.
- **Finance Director**: tests unit economics, cash impact, pricing, capital allocation, downside exposure, and measurement.
- **Customer/Market Director**: tests customer need, market pull, segment fit, buyer behavior, messaging, and adoption risk.
- **Operations Director**: tests feasibility, resourcing, process impact, owner clarity, dependencies, and execution path.
- **Risk/Governance Director**: tests reversibility, compliance, reputation, decision rights, incentives, and second-order effects.

If the decision clearly needs a different seat, replace one seat and state the replacement. Keep the board small enough that each seat has a distinct job.

## Workflow

### 1. Enrich context and frame the question

Spend a short, bounded pass gathering decision context before framing. Prefer the 2 to 4 files that most improve judgment. Do not turn this into a full research project.

Look for:

- Company OS files listed in `Read first`
- files explicitly named by the user
- relevant prior decisions
- recent output board memos or transcripts if the same decision has been reviewed before
- client context only when the question is client-specific

Restate the user's request as a neutral board question. Include:

- the decision to make
- the options under consideration
- relevant Company OS context
- known constraints and deadlines
- what is at stake
- missing information that limits confidence

Do not add your own recommendation at this stage. If the decision is too vague to frame, ask one clarifying question and then proceed.

### 2. Build the decision packet

Before spawning directors, build a compact packet that every director will receive. The packet must include the framed question plus the available data and context.

Include:

- decision and options
- relevant facts from the user's request
- relevant Company OS context and file paths read
- available numbers, dates, constraints, customer signals, financial data, or operating data
- known assumptions
- missing data that would materially change confidence
- framing risks: ways the question may be biased, too broad, too narrow, or underspecified

If material data is missing, do one of these before director work:

- ask the user for the specific missing data needed
- offer to collect the data for the user with a concrete plan, including sources to inspect, estimated effort, and what the board will do with the findings
- proceed only if the user asks to continue or the missing data is not decision-blocking

If proceeding without material data, state that explicitly in the packet. The final memo must be critical about the limitation and must include the identified risks with the question framing.

### 3. Confirm the packet with the user

Before spawning directors, show the decision packet to the user and ask them to confirm that the collected data reflects their judgment.

Ask specifically for corrections to:

- facts and numbers
- constraints and deadlines
- option framing
- assumptions
- missing data classification
- framing risks

Do not proceed to director work until the user confirms the packet or gives corrections. If the user cannot confirm but asks to continue anyway, mark the packet as unconfirmed and require the final memo to be critical about that limitation.

### 4. Collect independent director views

Have each director analyze the framed question independently. Directors should not try to be balanced; each should lean into their seat's responsibility.

Each director view should include:

- seat recommendation
- strongest argument for that recommendation
- largest concern or failure mode
- assumption most likely to change the view
- one practical implication for execution

When subagents are available, run directors in parallel. If subagents are not available, simulate the directors sequentially and keep each view separate.

Every director or subagent must receive the same decision packet. Do not spawn directors with only the raw user question.

Use this director prompt shape:

```markdown
You are the [Director Seat] in a board-of-directors review.

Your responsibility:
[Seat-specific responsibility.]

Board question:
---
[Framed question]
---

Decision packet:
---
[Decision, options, relevant data, context file paths, constraints, assumptions, missing data, and framing risks]
---

User confirmation:
---
[Confirmed by user, corrected by user, or unconfirmed with reason]
---

Respond independently from your seat. Be direct, specific, and willing to disagree. Do not try to cover every angle; the other directors cover their own seats.

Return:
- Seat recommendation
- Strongest argument
- Largest concern
- Assumption to verify
- Practical implication
```

### 5. Run anonymous peer review

Collect the five director views. Randomize and anonymize them as Response A through Response E before review so reviewers judge reasoning quality instead of seat status.

Have each director review the anonymized responses. If subagents are available, run reviewers in parallel.

Each review should answer:

- strongest response and why
- response with the most important blind spot
- what all responses missed
- assumption that most needs validation

Keep the anonymous review focused on reasoning quality, not status or role.

Use this peer-review prompt shape:

```markdown
You are reviewing anonymized board-of-directors outputs.

Board question:
---
[Framed question]
---

Decision packet:
---
[Same packet given to directors]
---

User confirmation:
---
[Same confirmation status given to directors]
---

Anonymized responses:

Response A:
[Response]

Response B:
[Response]

Response C:
[Response]

Response D:
[Response]

Response E:
[Response]

Answer:
- Which response is strongest, and why?
- Which response has the most important blind spot?
- What did all responses miss?
- Which assumption most needs validation?
```

### 6. Produce the chair synthesis

Give the Chair the framed question, decision packet, user confirmation status, de-anonymized director views, anonymization map, and peer reviews. The Chair may disagree with the majority if the minority reasoning is stronger.

Use this synthesis prompt shape:

```markdown
You are the Chair of a board-of-directors review.

Board question:
---
[Framed question]
---

Decision packet:
---
[Same packet given to directors]
---

User confirmation:
---
[Confirmed by user, corrected by user, or unconfirmed with reason]
---

Director views:
[De-anonymized director views]

Anonymous peer reviews:
[Peer reviews]

Produce the board memo. Be direct. Do not hedge unless uncertainty is genuinely decision-changing. If material data was missing or the packet was unconfirmed, critique the decision framing and identify the risks created by that limitation.
```

Use this final memo format:

```markdown
# Board memo

## Decision
[One-sentence decision or recommendation.]

## Context
[The minimum context needed to understand the decision.]

## Board view
[Where directors converged.]

## Dissent
[Real disagreements and why they matter.]

## Risks
[Material risks, including reversibility and downside.]

## Data gaps and framing risks
[Missing material data, unconfirmed user judgment, and how these may distort the recommendation. Include only when relevant.]

## Assumptions to verify
[The few assumptions that would change the decision.]

## Recommendation
[Clear action, owner, and timing.]

## First action
[One concrete next step.]
```

Do not smooth over disagreement. A board memo is useful because it makes the tradeoff legible.

### 7. Save artifacts when useful

Return the board memo in chat by default. If the user asks for a durable artifact, or if the decision should be reviewed later, save files under `output/`:

Use filenames prefixed with `YYYYMMDD-<title>`, where `<title>` is a short lowercase slug for the decision:

- `output/YYYYMMDD-<title>-board-report.html`
- `output/YYYYMMDD-<title>-board-transcript.md`

The HTML report should be a single self-contained file with:

- board question
- chair memo first
- simple agreement/disagreement view
- collapsible director views
- peer review highlights
- timestamp and decision label

The transcript should include:

- original user request
- framed board question
- decision packet
- user confirmation status and corrections
- context files read
- director views
- anonymization map
- peer reviews
- final chair memo

Do not open local files automatically unless the user asks. Provide the path.

## Output handling

Keep normal board reviews in chat unless an artifact is clearly useful.

Do not place generated board memos directly into canonical strategy, company, decision, or client files without human review. If a durable decision should be created, propose the follow-up file update separately.

## Quality checklist

The board review is ready when:

- the decision is framed neutrally
- material data needs were identified before directors were spawned
- the user was asked for missing data or offered a concrete collection plan when needed
- the decision packet was confirmed or corrected by the user before director work, unless the user explicitly chose to proceed unconfirmed
- every director received the same decision packet, not just the raw question
- every director received the same user confirmation status
- context was enriched with only relevant Company OS files
- all five directors produced independent views
- director views were anonymized and randomized before peer review
- peer review evaluated reasoning quality
- the final recommendation is clear
- dissent and risks are explicit
- assumptions are testable
- missing data, unconfirmed judgment, and framing risks are called out when they affect confidence
- the first action is concrete
- the Chair considered dissent and can explain why the final recommendation wins
- no unsupported company facts were invented
- sensitive or client-confidential information stayed in the right place
