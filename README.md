# Coretree Writing

Language: English | [한국어](README.ko.md)

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

Before: prose notes

> We tested app dictation first. At first, it looked like dictation into other apps was not supported, so we considered replacing it with a separate transcription tool. Later, we found that the problem was not a feature limitation but an execution permission issue.
>
> We also tested two transcription tools. Tool A was fast, but its accuracy dropped too much on long Korean sentences. Tool B handled long sentences better, but punctuation was inconsistent and would increase review work. For now, the team decided to keep app dictation after fixing permissions, reject Tool A, and leave Tool B as a possible fallback for offline notes.

After:

```text
- App dictation test
    - Initial assumption: dictation into other apps was not supported
    - Actual cause: execution permission issue

- Current decision: keep app dictation after fixing permissions

- Tool A decision: rejected
    - Fast enough for live notes
    - Accuracy drops too much on long Korean sentences

- Tool B status: fallback candidate
    - Handles long sentences better than Tool A
    - Inconsistent punctuation => higher review work

- Core outcome
    - No replacement tool needed yet
    - Fix permissions first
```

## Files

- `SPEC.md`: primary specification in English.
- `SPEC.ko.md`: Korean companion specification.
- `EXAMPLES.md`: primary examples in English.
- `EXAMPLES.ko.md`: Korean companion examples.
- `AGENTS.md`: short instructions for AI agents.
- `skills/coretree/SKILL.md`: standalone `coretree` skill file. The repository is named `coretree-writing`; the installable skill is named `coretree`.

## Language

- Primary language: English.
- Korean documents are companion versions for readers who prefer Korean.
- If English and Korean documents differ, use the English document.

## Status

Coretree is intentionally small. The goal is not to define a broad writing framework, but to provide a clear convention that people and AI agents can apply consistently.
