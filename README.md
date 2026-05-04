# Coretree Writing

Coretree is a compact multi-level bullet writing style for quick scanning.

It helps turn notes, decisions, findings, and raw information into readable bullet trees. It is not a template, a knowledge base system, or a universal writing method. It is a small writing convention for organizing information so readers can see the structure quickly.

## What It Is

Coretree organizes information with multi-level bullets.

- Main bullets cover core topics, decisions, or outcomes.
- Sub-bullets provide details, causes, conditions, evidence, examples, or follow-up information.
- Bullet depth shows dependency, not importance.
- Important details are promoted upward when they would otherwise be buried.
- Short labels such as `Decision:`, `Cause:`, `Result:`, and `Status:` can make scanning easier when the role of a bullet needs to be explicit.
- For short relationships, use `:` for label-value pairs and `=>` for cause, change, or consequence.

## Why Use It

Use Coretree when a reader needs to scan information quickly.

- Meeting notes become easier to revisit.
- Decision records show the decision, reason, and next action clearly.
- Research summaries separate findings from evidence.
- Bug reports show symptoms, causes, impact, and status without long paragraphs.
- AI agent output becomes more consistent and easier to review.

## Quick Example

Before: prose paragraph

> The team tested app dictation first. At first, it looked like dictation into other apps was not working, but the real cause was an execution permission issue.
>
> The team also tested another transcription tool, but rejected it because transcription accuracy was too low for long Korean sentences.

After:

```text
- App dictation test
    - Dictation into other apps did not work at first
    - Cause: execution permission issue

- Transcription tool decision: rejected
    - Accuracy on long Korean sentences was insufficient
```

## Files

- `SPEC.md`: primary specification in English.
- `SPEC.ko.md`: Korean companion specification.
- `EXAMPLES.md`: primary examples in English.
- `EXAMPLES.ko.md`: Korean companion examples.
- `AGENTS.md`: short instructions for AI agents.
- `skills/coretree/SKILL.md`: standalone Coretree skill file.

## Language

- Primary language: English.
- Korean documents are companion versions for readers who prefer Korean.
- If English and Korean documents differ, use the English document.

## Status

Coretree is intentionally small. The goal is not to define a broad writing framework, but to provide a clear convention that people and AI agents can apply consistently.
