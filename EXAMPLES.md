# Coretree Examples

Language: English | [한국어](EXAMPLES.ko.md)

This document contains examples for Coretree writing. `SPEC.md` is the primary specification.

## Notes

Before:

```text
We discussed the onboarding flow. The current welcome screen is too long, and users often skip the setup step. We decided to shorten the welcome copy and move setup guidance into the first task screen.
```

After:

```text
- Onboarding flow decision: shorten welcome copy
    - Welcome screen is too long
    - Users often skip the setup step
    - Move setup guidance into the first task screen
```

Rule shown: labels are optional; clear hierarchy can carry most of the structure.

## Decision Records

Before:

```text
The team chose the smaller release scope because the larger version would require more review and delay the launch. The excluded reporting feature should be reconsidered after the first release.
```

After:

```text
- Release scope decision: smaller scope selected
    - Larger scope would require more review and delay launch
    - Reporting feature deferred until after the first release
```

Rule shown: important decisions are promoted upward.

## Research Summaries

Before:

```text
Three transcription tools were tested. Tool A was fast but inaccurate for long Korean sentences. Tool B handled long sentences better but produced inconsistent punctuation. Tool C was accurate enough but too slow for live note-taking.
```

After:

```text
- Transcription tool research
    - Tool A
        - Strength: fast
        - Weakness: inaccurate for long Korean sentences
    - Tool B
        - Strength: better long-sentence handling
        - Weakness: inconsistent punctuation
    - Tool C
        - Strength: accurate enough
        - Weakness: too slow for live note-taking
```

Rule shown: same-depth bullets should contain the same type of information.

## Bug Reports

Before:

```text
Users cannot save settings after changing notification preferences. The save request returns 403. The likely cause is that the settings endpoint checks the wrong permission name. The issue blocks preference changes but does not affect login or reading existing settings.
```

After:

```text
- Settings save bug
    - Symptom: users cannot save notification preference changes
    - Error: save request returns 403
    - Likely cause: endpoint checks the wrong permission name
    - Impact: preference changes blocked
    - Not affected: login, reading existing settings
```

Rule shown: causes, symptoms, and impact should be separated.

## AI Agent Output

Before:

```text
I reviewed the configuration and found that validation already runs before release. I also found that formatting checks run in a separate step, so combining them with release would make failures harder to understand.
```

After:

```text
- Configuration review
    - Found: validation already runs before release
    - Found: formatting checks run in a separate step

- Implementation decision
    - Avoid: combining formatting checks with release
    - Reason: failures would be harder to understand
```

Rule shown: separate findings from decisions.
