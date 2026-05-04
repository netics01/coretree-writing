# Coretree Writing

Language: English | [한국어](README.ko.md)

Coretree is a compact multi-level bullet writing style for quick scanning.

It helps turn scattered notes, decisions, findings, and raw information into structured bullet trees that are easier to scan, compare, and revisit. By using shallow hierarchy, concise labels, and one-line relationships, Coretree makes decisions, causes, risks, and next actions easier to find without rereading long paragraphs.

It is intentionally small: not a template, not a knowledge base system, and not a universal writing method.

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

> We tested app dictation first. At first, it looked like dictation into other apps was not supported, so we considered replacing it with a separate transcription tool. Later, we found that the problem was not a feature limitation but an execution permission issue.<br>
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

## Where To Go Next

- Want more examples? Read [EXAMPLES.md](EXAMPLES.md).
- Want the exact rules? Read [SPEC.md](SPEC.md).
- Want to use it as an agent skill? See [Use As An Agent Skill](#use-as-an-agent-skill).

## Use As An Agent Skill

The GitHub project is named `coretree-writing`; the installable skill is named `coretree`.

The skill file is platform-neutral Markdown. Its `compatibility` field is kept as OpenCode metadata, but other agents can read the same instructions directly.

Install from the skill directory with the `skills` CLI. Use one or both commands depending on your agent:

```bash
# OpenCode
npx skills add https://github.com/netics01/coretree-writing/tree/main/skills/coretree -g -a opencode

# Claude Code
npx skills add https://github.com/netics01/coretree-writing/tree/main/skills/coretree -g -a claude-code
```

Manual paths:

- OpenCode: `~/.config/opencode/skills/coretree/SKILL.md`
- Claude Code: `~/.claude/skills/coretree/SKILL.md`
- Generic agents: copy [skills/coretree/SKILL.md](skills/coretree/SKILL.md) into the agent's skill directory, or provide it as Markdown instructions.

### How To Ask An Agent To Use It

After installing the skill, ask your agent directly:

```text
Write this document in Coretree style.
```

or:

```text
Summarize this in Coretree writing.
```

To make Coretree the default style for a project, add an instruction to that project's agent guidance file, such as `AGENTS.md`:

```text
When writing notes, summaries, decisions, findings, or documentation, use Coretree style unless the user asks for another format.
```

The exact trigger wording depends on the agent, but phrases such as `Coretree style`, `Coretree writing`, or `코어트리 스타일` are intended to load or apply the skill.

## Language

- Primary language: English.
- Korean documents are companion versions for readers who prefer Korean.
- If English and Korean documents differ, use the English document.

## Status

Coretree is intentionally small. The goal is not to define a broad writing framework, but to provide a clear convention that people and AI agents can apply consistently.

## License

MIT License. See [LICENSE](LICENSE).
