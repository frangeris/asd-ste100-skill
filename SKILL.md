---
name: asd-ste100
description: Write, rewrite, and review technical English in ASD-STE100 Simplified Technical English (Issue 9) - short sentences (20 words in procedures, 25 in descriptions), approved words, active voice, imperative steps, structured warnings. Use this skill whenever you write or edit technical prose that a person reads to do something or to understand something - documentation, READMEs, guides, procedures, runbooks, install and setup steps, API and reference docs, error, log and UI messages, code comments, release notes, work instructions, maintenance manuals - even when the user never says "STE" or "Simplified Technical English". Also use it when the user mentions ASD-STE100, STE, controlled language, simplified English, S1000D, or wants text that non-native readers and machine translation cannot misread. Chat replies stay in the user's language; this skill governs the content you produce.
---

# ASD-STE100 Simplified Technical English

ASD-STE100 is a controlled-language standard for technical writing (Issue 9, January 2025). It has 53 writing rules and a dictionary of about 875 approved words. The goal is one reading per sentence, so a reader with limited English, or a machine translator, cannot misread it.

This skill is an unofficial summary in other words. ASD owns the specification and the dictionary, and it distributes them free of charge at asd-ste100.org. Do not copy dictionary entries or long passages of the specification into your output or into this skill.

## Scope

Write in STE every text you produce for a reader to use or understand:

- Documentation, READMEs, guides, runbooks, procedures, setup and install steps, release notes
- API and reference docs, error, warning, log and UI messages, help text
- Code comments, docstrings, issue and pull request text
- Commit messages (wording only - see Precedence)

Leave these outside STE:

- **Your chat replies.** Answer in the user's language. Use chat only to report what you could not settle (see Delivery).
- **Code and literal strings.** Do not change identifiers, commands, flags, paths, tool output, UI labels, or third-party titles. Each one counts as one word and may be non-STE.
- **Marketing copy, fiction, legal text.** STE removes the nuance these texts need. Ask first.
- **Other languages.** STE is English only. If the artifact must be in another language, say so, then apply the shared principles (short sentences, active voice, one term per thing) without the dictionary.

**Precedence.** Format conventions of the project or the user (Conventional Commits, a CLAUDE.md, a style guide) decide layout, case and markup. STE decides words and sentence construction. `fix(auth): reject expired tokens` obeys both: imperative verb, no -ing form.

## Workflow

1. **Get the facts first.** STE rejects vague statements such as "no leaks are permitted" or "different values change the result". If you lack a number, a tool name, a result, or the identity of what acts, read the code or ask. Do not hide a gap behind abstract words.
2. **Classify each block** with the table below. A document can contain all four types. Never mix procedure and description in one list.
3. **Write** with the rules in this file. Read `references/rules.md` when a rule is unclear or the case is unusual.
4. **Check the words** (see Words). Do this before you review the sentences, because a word change often forces a new sentence.
5. **Review** with the checklist at the end. Fix, then review again - a fix often breaks another rule.
6. **Deliver** the text. Mention in chat only what you could not settle.

When you rewrite existing text, keep its meaning and technical names. Do not add facts. If the source is ambiguous, ask or flag the doubt - do not guess.

## Text types

| Type | Use | Max words per sentence | Form |
|---|---|---|---|
| Procedure | Tell the reader what to do | 20 | Imperative, active. One instruction per sentence. Condition first, then a comma. |
| Description | Tell what something is or how it works | 25 | Active. Passive only when you do not know the agent. No imperative. Paragraph: one topic, topic sentence first, 6 sentences at most. |
| Note | Give information during a procedure | 25 | Descriptive. No instruction, no limit, no required result. |
| Safety instruction | Warn of a risk | 20 | Command or condition first, then the risk. WARNING = injury or death. CAUTION = damage to equipment. Both = WARNING. |

**Counting words.** Count as one word: text in parentheses, numbers, a number with its unit, abbreviations, alphanumeric identifiers (`v2.1`, `ERR_42`), quoted text, titles and labels, names of people and organizations, hyphenated words. Do not count step numbers. A colon before a vertical list ends the sentence, and each list item is a new sentence with the same limit. The text inside parentheses is a separate sentence with its own count.

## Core rules

These are the rules and general recommendations that writers break most often. The tag at the end of each item gives the specification rule (or general recommendation, GR) that it comes from. `references/rules.md` explains each one.

**Verbs**

1. Use only these forms: infinitive, imperative, simple present, simple past, simple future, and the past participle as an adjective ("the installed package"). Do not use perfect forms ("has failed"), progressive forms ("is running"), or "be + participle" ("is stored"). *[3.2, 3.3, 3.4]*
2. Do not use -ing forms as verbs or nouns. Rewrite: "When you start the script" not "When starting the script". Allowed: an -ing word that is part of a technical noun ("grinding wheel") or a heading ("Cleaning"), and these approved words: lighting, opening, routing, servicing, mating, missing, remaining, something, during. *[3.5]*
3. Use the active voice. To fix a passive sentence: make the agent the subject, use the imperative, or use "you" or "we". Keep a passive sentence only in descriptions, and only when you do not know the agent. *[3.6]*
4. Name the action with a verb, not a noun: "Before you delete the table" not "Before the deletion of the table". *[3.7]*
5. Use `can` for what is possible and `must` for what is required. Do not use should, may, might, would, shall. In procedures, do not write `must` before an imperative, except in safety instructions or for a key condition. *[5.3]*

**Sentences**

6. One instruction per sentence in procedures, unless two actions occur at the same time ("Stop and erase the job."). One topic per sentence in descriptions. *[4.1, 5.2]*
7. Do not shorten a sentence by dropping words. Keep the subject, the verb, and the articles. Do not use contractions. Write "that" after "make sure", "show", and "recommend". *[4.2, GR-1]*
8. Put a condition before the instruction and end it with a comma: "If the build does not complete, read the log." *[5.4]*
9. Put many items or actions in a vertical list instead of one long sentence. End the lead-in with a colon. Start each item with a capital letter. End the last item with a period. *[4.3]*
10. Join related sentences with "and", "but", "then", "thus", "as a result", "at the same time". Repeat the same key word instead of using a synonym. *[4.4, 6.2]*
11. Use an article or "this"/"these" before a noun. Omit it in general statements ("Solvents cause damage") and before an identifier ("ticket 4821"). *[4.5]*
12. Use a pronoun only if it has one clear referent. If "it" or "this" could point to two things, repeat the noun. *[GR-3, GR-4]*
13. Do not use semicolons. Write two sentences. Do not use e.g., i.e., etc. - write "for example", "that is", "or other items". Do not make phrasal verbs ("give off", "put out") - use one verb. *[8.1, 9.3, GR-6]*
14. Use the same wording each time the same action or thing occurs. *[9.4]*

**Nouns and spelling**

15. Keep multi-word nouns to three words. For a longer one, use a preposition ("the retry limit of the client" not "client retry limit setting value"), or write the full name once and then a shorter name or an abbreviation. *[2.1, 2.2]*
16. Use one name for one thing in the whole text. Do not use slang or jargon ("nuke", "spin up", "brick"). *[1.10, 1.11]*
17. Use American spelling. Use gender-neutral language: no "he" or "she"; "man" and "woman" only where the subject needs them. *[1.14, GR-7]*

## Words

Every word must be an approved dictionary word, a technical noun, or a technical verb. An approved word has one part of speech and one meaning. "Test" is a noun only: write "do a test", not "test the build". "Follow" means "come after": write "obey the instructions".

A **technical noun** names a thing in your subject field and is not in the dictionary. In software, this covers terms such as file, database, network, interface, token, and menu. A **technical verb** names a process in the field. In software, this covers input and output actions (click, type, press), interface actions (open, save, copy, delete, scroll), and system actions (install, download, boot, update). Rules for both:

- Use a term the project already uses. If there is none, choose a short, well-known one.
- Do not use a technical noun as a verb ("to script a task" - say "write a script for the task").
- Do not use a technical verb as a noun.
- Use an approved verb when one says the same thing. "Find broken links" not "detect broken links".

**Traps.** These words look harmless and are not approved, or they are approved only in a narrow meaning.

| Do not write | Write instead | Note |
|---|---|---|
| check (verb), verify, confirm, ensure | make sure that ... / do a check of ... | "check" is a noun only |
| test (verb) | do a test of ... | noun only |
| damage (verb) | cause damage to ... | noun only |
| work (verb) | do the work | noun only |
| help (noun) | aid | "help" is a verb only |
| follow (instructions) | obey | "follow" = come after |
| perform, execute | do | |
| should, shall | must | only if it is a real requirement; else write an imperative |
| may, would | can | |
| might, ought | rewrite: "it is possible that ..." | |
| allow, permit, enable | let | "enable" is allowed as a technical verb for a setting |
| provide | give | |
| require, need | is necessary | "The step is necessary" |
| begin, restart | start | |
| utilize | use | "use" as a noun: operation |
| display (verb) | show | "display" is allowed as a noun |
| run (a program) | start, operate | |
| create | make | |
| choose | select | |
| main | primary | |
| acceptable | permitted, satisfactory | |
| therefore, however, since (cause) | thus, but, because | |
| fail, failure | "if ... does not operate" | restructure |
| above, below (for a limit) | more than, less than | "above" and "below" mean physical position only |
| turn (to a color or state) | change to | "turn" = rotate around a point |
| see (to learn) | make sure that ... | "see" = look with the eyes |
| wear (clothes) | put on, use | |

Three levels of vocabulary check, from cheap to strong:

1. **This table.** It covers the most frequent errors.
2. **The official dictionary, if the user has it.** In Part 2, an UPPERCASE headword is approved. A lowercase headword is not approved, and its alternatives column shows what to write. Look up every doubtful word. Read `references/vocabulary.md` for the method. Take the dictionary only from the user or from asd-ste100.org, never from mirror sites.
3. **No copy available.** Prefer the plainest everyday word with one meaning, and say in the delivery note that you did not verify the vocabulary. Your memory of "approved" words is not reliable evidence.

## Safety instructions

Use this order: level word, command or condition, risk. Obey the 20-word limit.

STE: WARNING: DISCONNECT THE POWER CABLE BEFORE YOU OPEN THE UNIT. HIGH VOLTAGE CAN CAUSE INJURY OR DEATH.

STE: CAUTION: DO NOT FORMAT THE DISK DURING THE UPDATE. THE UNIT CAN STOP AND NOT START AGAIN.

In a list, put "DO NOT" in each item, not once in the lead-in. Do not put a safety instruction in a note. The capitals above are a layout choice, not an STE rule - follow the project's layout.

## Review checklist

Run every item on the final text. Fix and run again.

- [ ] Each sentence has the right type and length: 20 words (procedure, safety), 25 (description, note).
- [ ] No semicolon, contraction, or Latin abbreviation (e.g., i.e., etc.).
- [ ] No -ing form except the allowed ones. No perfect or progressive tense.
- [ ] No passive sentence in a procedure. Descriptions: passive only when you do not know the agent.
- [ ] Procedure steps are imperative, with one instruction each. Conditions come first.
- [ ] Notes contain no instruction, limit, or result. The procedure works without them.
- [ ] No should, may, might, would, shall. `must` only where it is required.
- [ ] No word from the traps table. Doubtful words checked at level 2 or reported at level 3.
- [ ] Multi-word nouns have three words at most. One name for each thing.
- [ ] Paragraphs: one topic, topic sentence first, six sentences at most.
- [ ] No sentence depends on an omitted article, subject, or "that".
- [ ] No "he" or "she". American spelling.

## Delivery

Put the STE text in the file or message the user asked for. Then, in the user's language, add one short line only if something remains open: a word you could not verify against the dictionary, a technical noun you chose without a project glossary, or a literal string you kept because it is quoted text. If nothing remains open, say nothing about STE.

## Reference files

- `references/rules.md` - all 53 rules and the 8 general recommendations, with the reason for each and software examples. Read it when a case is unclear, when you review a long document, or when the user asks why a rule exists.
- `references/vocabulary.md` - how to use the official dictionary, the technical noun and technical verb categories, and more word replacements for software text.
- `references/examples.md` - before and after rewrites of a procedure, a description, a safety instruction, and a README paragraph. Read it when you rewrite existing text.
