# Vocabulary in ASD-STE100

This file explains how to choose and check words. It does not contain the approved word list. ASD owns the dictionary and distributes it free of charge with the specification at asd-ste100.org. Do not paste dictionary entries into your output. Take the dictionary only from the user or from asd-ste100.org, never from mirror sites.

Contents: Decision order - Using the official dictionary - Technical noun categories - Technical verb categories - Software word replacements

---

## Decision order

For every content word, ask in this order. Stop at the first "yes".

1. **Is there an approved word with the same meaning and the same part of speech?** Use it. (An approved word with a narrower meaning is not a match - see rule 1.3.)
2. **Is it a technical noun or a technical verb of the subject field?** Use it, but only as that part of speech, and with one name for each thing.
3. **Neither?** Write a different sentence. Ask: "What does the reader need to know or do?" and say that with approved words (rule 9.1).

A word that the dictionary does not list is **not** approved. Only the rejected words that the dictionary lists come with alternatives. Do not read "not listed" as "allowed".

## Using the official dictionary

If the user gives you a copy of the ASD-STE100 PDF (or a text extraction), use it for every doubtful word. Do not assume where it is - ask once, or use the path that the user gives.

Part 2 has four columns: the word with its part of speech, the approved meaning or the alternatives, an STE example, and a non-STE example.

- **UPPERCASE headword** = approved. Read the meaning column. Use the word only with that meaning and as that part of speech.
- **lowercase headword** = not approved. The alternatives column shows what to write instead. The STE example shows the new sentence, which is often different in structure.
- **(TN)** and **(TV)** in an alternatives column = technical noun or technical verb. You may use it if it fits a category below.
- Nouns are listed in the singular. The plural of a countable noun is allowed.
- Verbs are listed with their forms (for example, "GIVE, GIVES, GAVE, GIVEN"). Use no other form.
- Adjectives are listed with their comparative and superlative forms only if those forms are allowed.
- A headword can appear twice, once approved and once rejected, for example, because only one meaning is allowed. Read both entries.
- The dictionary uses American spelling.

To find a word in a text extraction, search for the headword at the start of a line followed by its part of speech, for example `^main \(adj\)`. A text extraction of the PDF can be rough, so check the page when the result looks wrong.

If you have no copy, say so in your delivery note (see `SKILL.md`). Do not claim that a word is approved only from memory.

## Technical noun categories (rule 1.5)

A word outside the dictionary can be a technical noun if it fits one of these 22 categories. The categories are examples of what counts, not a closed list of words. Prefer the term that your company, industry, or project already uses.

| # | Category (own wording) | Software-related examples (by analogy) |
|---|---|---|
| 1 | Items in official parts lists and drawings | Names in architecture documents and package manifests |
| 2 | Machines, vehicles, and places inside them | - |
| 3 | Tools and support equipment, with their parts | Compiler, debugger, terminal |
| 4 | Materials, consumables, and contaminants | - |
| 5 | Sites, infrastructure, and logistics | Data center |
| 6 | Systems, assemblies, circuits, and how they are set up | Scheduler, gateway, standby mode |
| 7 | Terms from mathematics, science, engineering, and formulas | Latency, hash, checksum |
| 8 | Position, direction, and place | - |
| 9 | Numbers, units, and time | 200 ms, 2 GB |
| 10 | Quoted text that you cannot change | Button labels, text on a screen, a message from a third party |
| 11 | Jobs, people, groups, companies, and countries | Administrator, maintainer, ISO |
| 12 | Body parts | - |
| 13 | Personal items, food, and drink | - |
| 14 | Medical terms | - |
| 15 | Official documents and their sections | Manual, table, figure, note, warning, specification |
| 16 | Weather and operating environment | - |
| 17 | Colors | Red, green |
| 18 | Kinds of damage | - |
| 19 | Computing and information technology | File, database, network, interface, token, menu, browser, update |
| 20 | Civil and military activity | Customer |
| 21 | Legal and regulatory text | Contract |
| 22 | Animals, plants, and other living things | - |

The specification's own examples come mainly from hardware. The software column is a judgment by analogy, so prefer your project glossary when it exists.

Rules for technical nouns: use one name for one thing (1.11), keep it short (1.9), do not use slang or jargon (1.10), and do not turn the word into a verb (1.7).

## Technical verb categories (rule 1.12)

A verb outside the dictionary can be a technical verb if it fits one of these four categories. Technical verbs follow the same verb rules as approved verbs (forms, tenses, no -ing).

1. **Manufacturing processes.** Remove, add, or attach material, change its strength or its surface, or change its shape.
2. **Computer processes and applications.**
   - Input and output: click, enter, press, type, print, tap.
   - Interface and application: open, close, copy, paste, delete, save, scroll, sort, enable, disable, zoom.
   - System operations: install, download, upload, update, boot, load, format, debug.
3. **Instructions in a subject field.** Engineering and science, medicine, civil and military operations, navigation, automotive and railway, energy.
4. **Law and regulations.** Verbs that only legal texts need.

Use a technical verb only when no approved verb says the same thing, and only in the sense of its category. For software, categories 2 and 3 matter most.

## Software word replacements

Most of these words appear in the dictionary as rejected words. Each one has an approved alternative that fits many software sentences. Check the alternative against your context (rule 9.1) before you use it.

| Rejected word | Alternative | Example |
|---|---|---|
| ask, request (verb) | tell | Tell the server to close the connection. |
| avoid | prevent | This flag prevents the loss of data. |
| choose | select | Select a region. |
| create | make | Make a new folder. |
| enable, allow, permit | let | The flag lets the client send retries. |
| ensure, verify, confirm | make sure that | Make sure that the port is open. |
| execute, perform | do | Do the migration. |
| log (verb) | record | The service records each error. |
| remain | stay | The connection stays open. |
| run (verb) | operate, start | Start the build. |
| via | through | Connect through the proxy. |
| using | use ... , with | Open the file with the editor. |

Some rejected words are also technical verbs of category 2. In an interface or a system instruction, these are correct: *click*, *enter*, *press*, *type*, *delete*, *save*, *store*, *copy*, *enable*, *disable*, *update*, *download*. In other contexts, use the approved alternative: "erase the old data", "keep the result".

Words that need a new sentence, not a swap:
- *fail, failure* - say what does not happen: "If the job does not complete, ..."
- *should* - decide if it is a requirement ("must") or only advice (write the command, or "We recommend that ...").
- *might, ought* - the dictionary has no entry for them, so they are not approved. Write "it is possible that ...".
- *since* (cause), *therefore*, *however* - because, thus, but.
- *above, below* (for a limit) - more than, less than.
