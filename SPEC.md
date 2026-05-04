# Coretree Writing Specification

This document is the primary specification for Coretree writing.

This specification is written in English and defines the Coretree writing style.

## Definition

Coretree is a writing style that organizes information as readable multi-level bullets.

- It compresses information into short, scannable units.
- It shows relationships between pieces of information.
- It uses bullet depth to show dependency.
- It uses position, order, and labels to show importance.
- It keeps hierarchy shallow enough for fast human scanning.

## Principles

- Prefer bullets over long paragraphs.
- Keep one idea per bullet.
- Put core topics, decisions, outcomes, or categories in upper-level bullets.
- Put details, causes, conditions, evidence, examples, and follow-up information in lower-level bullets.
- Keep bullets at the same depth parallel in type.
- Cut repeated or low-value wording.
- Prefer concise phrasing over conversational prose.
- Use labels when they improve scanning; they are not required for every bullet.

## Bullet Depth

Use depth deliberately.

- Depth 1: main topic
- Depth 2: important information about the topic
- Depth 3: necessary detail
- Depth 4: rare, only when it improves clarity
- Depth 5: avoid

Do not preserve deep nesting just because the input material is deeply structured. If a tree becomes too deep, reorganize it.

- Split the information into separate topics.
- Combine similar details.
- Rename or remove an unnecessary intermediate label.
- Collapse a short hierarchy into one line.
- Promote important information upward with context.

## Importance vs Dependency

Bullet depth shows dependency. It does not mean the information is less important.

Important information should not be hidden in a deep sub-bullet. If a detail is important, promote it upward and include enough context.

Less clear:

```text
- Vendor evaluation
    - Tool A
        - Korean accuracy was insufficient
        - Decision: rejected
```

Preferred form:

```text
- Tool A decision: rejected
- Rejection reason: Korean accuracy was insufficient
```

## Labels

Use labels when they make the role of information easier to scan.

Labels are optional. If the role of a bullet is already clear from context, natural bullet text is often better than forcing every line into `Label: value` form.

- `Decision:` for a selected outcome.
- `Result:` for what happened.
- `Cause:` for why something happened.
- `Status:` for current state.
- `Risk:` for a possible problem.
- `Next:` for a follow-up action.

Labels should be short. A label should help the reader scan the tree without rereading surrounding text.

Less clear:

```text
- Onboarding flow discussion
    - Issue: welcome screen is too long
    - User behavior: setup step is often skipped
    - Decision: shorten welcome copy
    - Next: move setup guidance into the first task screen
```

Preferred form:

```text
- Onboarding flow decision: shorten welcome copy
    - Welcome screen is too long
    - Users often skip the setup step
    - Move setup guidance into the first task screen
```

## One-Line Relationships

Short relationships can be collapsed into one line.

Use `:` for label-value relationships.

```text
- Decision: rejected
- Status: blocked
- Cause: missing permission
```

Use `=>` for cause, change, or consequence.

```text
- Missing permission => input failed in other apps
- More transcription errors => higher review cost
```

Avoid adding a bullet level when the relationship is clearer on one line.

Less clear:

```text
- Decision
    - Rejected
```

Preferred form:

```text
- Decision: rejected
```

## When To Use It

Use Coretree for information that should be scanned, revisited, or extended later.

- Meeting notes
- Decision records
- Research summaries
- Bug reports
- Project status updates
- AI agent output
- Checklists with supporting details

## When Not To Use It

Do not force Coretree where prose is better.

- Narrative writing that needs rhythm or voice
- Persuasive essays
- Legal or policy text where exact wording matters
- Short messages with no hierarchy
- Content where a table, diagram, or code block is clearer

## Writing Checklist

- Is the conclusion or decision visible near the top?
- Does each bullet contain one idea?
- Does depth show dependency rather than importance?
- Are labels short and useful?
- Are 4-level bullets rare?
- Are 5-level bullets avoided?
- Can any short hierarchy be converted into a `:` or `=>` line?
