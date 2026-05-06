---
name: coretree
description: Apply the Coretree multi-level bullet writing style
license: MIT
compatibility: opencode
metadata:
  style_version: 1.0.1
  spec: SPEC.md
---

# Coretree Style Skill

- Version: 1.0.1
- Primary reference: `SPEC.md`
- This skill is platform-neutral Markdown.
- OpenCode can install it as a skill.
- Non-OpenCode agents can read this file directly and follow the same procedure.

## Trigger

Use this skill when the user asks for any of the following:

- `Coretree style`
- `Coretree writing`
- `코어트리 스타일`
- `코어트리 방식`
- Equivalent wording that clearly asks for Coretree-style writing.

## Execution Procedure

1. Confirm that the user requested Coretree style.
2. Read the embedded Coretree rules in this skill.
3. Identify the main topics in the user's information.
4. Group related details under each topic.
5. Promote important conclusions, decisions, causes, and results when they would otherwise be buried.
6. Compress repeated or low-value wording.
7. Indent each nested Markdown bullet level with 4 spaces, not tabs or 2 spaces.
8. Keep hierarchy readable by preferring 1-3 levels.
9. Use 4 levels only when it improves clarity.
10. Avoid 5-level nesting.
11. Output the final document in Coretree style.

## Failure Procedure

- If this skill was loaded, Coretree style can be applied from the embedded rules below.
- If an agent only knows that Coretree style exists but cannot access this skill or the specification, it must stop.
- Do not infer Coretree style from the name alone.
- Do not substitute a generic multi-level bullet style.

## Embedded Coretree Rules

### Definition

Coretree is a writing style that organizes information as readable multi-level bullets.

- Compress information into short units.
- Show relationships between pieces of information.
- Use bullet depth to show dependency.
- Use position, order, and labels to show importance.
- Keep hierarchy shallow enough for fast human scanning.

### Principles

- Prefer bullets over long paragraphs.
- Put one idea in each bullet.
- Put core topics, decisions, outcomes, or categories in upper-level bullets.
- Put details, causes, conditions, evidence, examples, and follow-up information in lower-level bullets.
- Keep bullets at the same depth similar in type.
- Compress repeated or low-value wording.
- Prefer short expressions over conversational flow.

### Bullet Depth

- Depth 1: main topic
- Depth 2: important information about the topic
- Depth 3: necessary detail
- Depth 4: rare, only when it improves clarity
- Depth 5: avoid

Indent each nested Markdown bullet level with 4 spaces. Do not use tabs or 2-space indentation. Keep indentation consistent so hierarchy remains visually clear.

If a tree becomes too deep, reorganize it.

- Split the information into separate topics.
- Combine similar details.
- Rename or remove an unnecessary intermediate label.
- Collapse a short hierarchy into one line.
- Promote important information upward with context.

### Importance vs Dependency

Bullet depth shows dependency. It does not show low importance.

- Important information belongs near the top.
- Important details can be promoted upward when context is included.
- Labels such as `Decision:`, `Result:`, `Cause:`, `Status:`, `Risk:`, and `Next:` can make importance easier to scan.
- Labels are optional; do not force every bullet into `Label: value` form.

### One-Line Relationships

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

Avoid making a new bullet level for a relationship that is clearer on one line.
