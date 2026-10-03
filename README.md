# asd-ste100

A Claude Code skill that makes Claude write technical content in ASD-STE100 Simplified Technical English (Issue 9, January 2025).

STE is a controlled language for technical writing. Each sentence has one reading, so readers with limited English and machine translators cannot misread it.

## What the skill does

Claude writes in STE every text it produces for a reader to use or understand:

- Documentation, READMEs, guides, runbooks, procedures, setup steps, release notes
- API and reference docs, error, warning, log, and UI messages
- Code comments, docstrings, issue and pull request text
- Commit messages (the wording only; the format convention of the project still decides the layout)

Claude does not apply STE to:

- Its chat replies. They stay in the language of the user.
- Code, commands, paths, tool output, and quoted text.
- Marketing copy, fiction, and legal text.

The skill sorts each block of text into one of four types and applies the matching rules:

| Type | Max words per sentence | Form |
|---|---|---|
| Procedure | 20 | Imperative, one instruction per sentence, condition first |
| Description | 25 | Active voice, one topic per paragraph, six sentences at most |
| Note | 25 | Information only, no instruction or limit |
| Safety instruction | 20 | WARNING or CAUTION, then a command or condition, then the risk |

Before it delivers a text, Claude walks through a review checklist. In chat, it reports only what it could not settle, such as a word it could not verify.

This skill is guidance only. It has no scripts.

## Install

Copy this folder to `~/.claude/skills/asd-ste100/` (all projects) or to `.claude/skills/asd-ste100/` (one project). The folder name must match the `name` in `SKILL.md`.

## Files

| File | Content |
|---|---|
| `SKILL.md` | Scope, workflow, text types, core rules, vocabulary traps, review checklist |
| `references/rules.md` | The 53 writing rules and 8 general recommendations, with software examples |
| `references/vocabulary.md` | How to check words, technical noun and verb categories, software word replacements |
| `references/examples.md` | Before and after rewrites of a procedure, a description, messages, and a README |

## The dictionary

The skill does not include the ASD-STE100 dictionary. ASD owns it and distributes it free of charge with the specification at [asd-ste100.org](https://www.asd-ste100.org). The skill covers the most frequent vocabulary errors in a table.

For a stronger check, give Claude the path of your own copy of the specification. Claude then looks up every doubtful word in Part 2. Without a copy, Claude prefers plain words and tells you which words it did not verify.

## Notice

This is an unofficial summary of the rules in other words. It is not affiliated with, endorsed by, or certified by ASD. ASD-STE100 Simplified Technical English is a registered trademark of the Aerospace, Security and Defence Industries Association of Europe (ASD). The examples are original. Read the official specification for the exact text of the rules.
