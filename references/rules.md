# ASD-STE100 Issue 9 - the 53 writing rules and 8 general recommendations

This is an unofficial summary in other words. The rule numbers follow the specification, so you can find the full text in the official PDF (asd-ste100.org). The examples are original and use software scenarios. "STE" marks a compliant sentence. "Not STE" marks a sentence that breaks the rule.

Contents: 1 Words - 2 Multi-word nouns - 3 Verbs - 4 Sentences - 5 Procedures - 6 Descriptions - 7 Safety - 8 Punctuation and word count - 9 Writing practices - General recommendations

---

## 1 Words

**1.1 Allowed words.** Use only approved dictionary words, technical nouns, and technical verbs. *Why:* a closed vocabulary leaves fewer words that the reader can misunderstand.

**1.2 Part of speech.** Give each approved word the one part of speech that the dictionary lists for it. "Test" is a noun.
- Not STE: Test the connection.
- STE: Do a test of the connection.

**1.3 Approved meaning.** Use an approved word only with the meaning that the dictionary gives. Many words have a narrower meaning than in everyday English.
- Not STE: Follow the setup instructions.
- STE: Obey the setup instructions.

**1.4 Verb and adjective forms.** Use only the forms that the dictionary lists. A regular verb gives you the base form, the "-s" form, and the "-ed" form. An irregular verb gives its own forms. An adjective gives its comparative and superlative forms only if the dictionary lists them ("more" and "most" make the others).

**1.5 Technical nouns.** Use a word that is not in the dictionary only if it fits a technical noun category (list in `vocabulary.md`). The dictionary does not list technical nouns, because each field has its own.

**1.6 Non-approved words as technical nouns.** A word that the dictionary rejects is still allowed when, in its context, it is a technical noun or a part of one.
- STE: Copy the build to the staging area. ("staging area" is a computing term.)

A rejected word that is not a technical noun in its context stays rejected.

**1.7 Technical nouns are not verbs.** You can use that word as a verb only when it also qualifies as an approved verb or a technical verb.
- Not STE: Cache the response.
- STE: Put the response in the cache.

**1.8 Use the field's accepted term.** If your company, industry, or project has an approved name for a part or a process, use it.

**1.9 Short, clear technical nouns.** When no accepted term exists, choose a short one of not more than three words, and one that the reader knows.

**1.10 No regional words, slang, or jargon.** A term that only a small group knows causes confusion.
- Not STE: Spin up two more replicas.
- STE: Start two more replicas. (Say what the action does.)

**1.11 One name for one thing.** Do not call the same item by different names in the same text.
- Not STE: Stop the worker. Then check the daemon log.
- STE: Stop the worker. Then examine the log of the worker.

**1.12 Technical verbs.** Use a verb that is not in the dictionary only if it fits a technical verb category (list in `vocabulary.md`). Use an approved verb when one says the same thing. Do not use a technical verb that is too general.

**1.13 Technical verbs are not nouns.** You can use the past participle as an adjective ("the compiled file").

**1.14 Spelling.** Use American spelling ("color", "initialize") unless an official directive of the project says differently. Do not change spelling inside quoted text.

---

## 2 Multi-word nouns

**2.1 Three words at most.** A group of nouns and adjectives that works as one noun is hard to read when it is long, because the reader must guess how the words connect. Use prepositions to make it shorter.
- Not STE: Session token refresh retry limit value
- STE: The limit of retries for the refresh of the session token

**2.2 A longer technical noun.** If an official name is longer than three words, write all of it at first use. Then do one of these:
- Give a shorter form, and use it after that. Explain the link between the two names once.
- Use hyphens to group words that work as one unit (a hyphenated group counts as one word). Do not hyphenate more than three words together. Do not remove hyphens from an official name.

Do not replace short names (three words or fewer) with abbreviations. A procedure full of abbreviations is hard to read.

---

## 3 Verbs

**3.1 Dictionary forms only.** Use the verb forms that the dictionary gives. Do not make others.

**3.2 Six forms and tenses.** Use only:
1. the infinitive,
2. the imperative,
3. the simple present,
4. the simple past,
5. the simple future,
6. the past participle as an adjective.

Do not use the present perfect ("has changed"), the past perfect ("had changed"), the progressive ("is changing"), or any longer verb group.

**3.3 Past participle as an adjective.** It describes the state of a thing. Place it before a noun, or after "be", "become", or "stay". Do not use a participle that the dictionary does not list.
- STE: Examine the installed packages.
- STE: When the service is stopped, delete the lock file.

**3.4 No auxiliary verb groups.** Do not build a verb with "have", or with "be" and a participle.
- Not STE: The configuration has been changed.
- STE: The installer changed the configuration. (Name the agent. If it is unknown, see 3.6.)
- Not STE: The setting can be changed by the administrator.
- STE: The administrator can change the setting.

**3.5 -ing forms.** One -ing word can work as a verb, an adjective, or a noun, and the reader cannot always tell which. Allow it only as a technical noun (for example, a heading) or as the modifier in a technical noun.
- Not STE: When you are installing the package, close the editor.
- STE: When you install the package, close the editor.
- STE: Cleaning (a heading). The grinding wheel (a technical noun with a modifier).
- Approved -ing words: lighting, opening, routing, servicing, mating, missing, remaining, something, during.

**3.6 Active voice.** In passive sentences the reader must ask "by whom?". Use the active voice. In descriptions you may use the passive only if the agent is unknown. Four ways to fix a passive sentence:
1. Make the agent the subject: "The scheduler starts the job."
2. Replace "is used to" with a direct verb: "The server calculates the cost from these values."
3. In a procedure, use the imperative: "Continue the test."
4. If no agent exists, use "you" (the reader) or "we" (the organization): "You can open the port with the admin tool."

If an unknown agent is really the cause, use "something" as the subject: "During the upload, something changed the file."

**3.7 Verb for the action.** Use an approved verb, not a noun, to say what happens.
- Not STE: The report makes a statement of the total, 450.
- STE: The report shows the total, 450.
- Not STE: Before the deletion of the table, ...
- STE: Before you delete the table, ...

If a verb is not approved, do not use it. Change the sentence: "Do a check of the disk."

---

## 4 Sentences

**4.1 Short and clear.** In procedures, speak directly to the reader. In descriptions, give one topic in each sentence and add information step by step. Say exactly what happens - do not write abstract sentences.
- Not STE: No data loss is permitted.
- STE: Make sure that you keep all the data. (Better: say how, and with which command.)
- Not STE: Different loads change the response time.
- STE: When the load increases, the response time increases.

**4.2 Do not omit words.** Keep nouns, verbs, subjects, and articles. A shorter sentence is not a clearer one. Do not use contractions.
- Not STE: If enabled, clear the cache.
- STE: If the cache is enabled, clear it.
- Not STE: Don't touch the config file.
- STE: Do not touch the config file.

**4.3 Vertical lists.** Use a list when a sentence has many items or actions.
- End the lead-in with a colon.
- Mark each item with a number, a letter, a dash, or a bullet.
- Start each item with a capital letter.
- End an item that is a full sentence with a period. Do not end other items with a mark, except the last item, which ends with a period.
- Do not end an item with a comma or a semicolon.
- Do not mix procedural and descriptive items in one list.
- In safety lists, put "DO NOT" in each item that needs it.
- Make sure that each item completes the lead-in correctly, and keep one list level.

**4.4 Connecting words.** Use "and", "but", "then", "thus", "as a result", and "at the same time" to show how sentences relate. You can also use "this" with a noun.

**4.5 Articles.** Put "the", "a", "an", "this", or "these" before a noun when it needs one. Omit it in general statements ("Solvents cause damage."). In a long list, use one article before the first item. In a short list, use one before each item when the meaning of an adjective can be unclear. Do not write an article before a noun and its identifier ("Open ticket 4821", "Close issue 214").

---

## 5 Procedural writing

**5.1 20 words.** A sentence in a procedure has 20 words at most. This limit also applies to warnings and cautions. Split a long sentence into two sentences, in the same step, if the actions occur at the same time. See Section 8 for counting.

**5.2 One instruction per sentence.** Put each action in its own step, with a number or a letter. Two actions can share a sentence only if they occur at the same time.
- Not STE: Stop the service and delete the cache.
- STE: (a) Stop the service. (b) Delete the cache.
- STE: Hold the lever and push the button. (Both actions occur together.)

A step can have more than one sentence when actions occur together, or when a result follows an action immediately: "Measure the latency. The latency must be less than 200 ms."

**5.3 Imperative.** Write instructions as commands. Other forms leave the reader in doubt: must someone do it, did someone do it, or is it for later? Do not put "must" before an imperative unless the instruction is critical for safety or states a key condition.
- Not STE: The cache can be cleared.
- STE: Clear the cache.
- Not STE: Before you remove the volume, you must unmount it.
- STE: Before you remove the volume, unmount it.

**5.4 Condition first.** Start with the condition, then a comma, then the command.
- Not STE: Start the server again if the health check does not complete.
- STE: If the health check does not complete, start the server again.

The position of a comma can change the meaning, so check it.

**5.5 Notes.** A note gives information only: no instruction, no requirement, no limit, no required result. Each sentence has 25 words at most. Do not use the imperative in a note. Test your notes: read the procedure without them. If the reader cannot do the work, move the missing text into a step. If a note describes a risk of damage or injury, make it a safety instruction. Limits and results belong in the step they apply to.
- Not STE: NOTE: The upload must not take more than 5 seconds.
- STE (in the step): Start the upload. The time of the upload must be less than 5 seconds.

---

## 6 Descriptive writing

A description gives information and never instructions, so it has no imperative.

**6.1 Give information step by step.** One subject per sentence. Do not put much information in one sentence. The reader must not need to read a sentence twice.

**6.2 Key words and connecting words.** Repeat the same key word in the next sentence to show the link, and use connecting words as signs: "and" (more of the same), "but" (different), "thus" and "as a result" (consequence), "then" (next in time). Do not change a key word for a synonym, because the reader will think it is a new thing.

**6.3 25 words.** A sentence in a description has 25 words at most.
- Not STE: The gateway validates each request, adds trace headers, forwards it to the nearest healthy node, and writes the result to the audit log.
- STE: The gateway validates each request and adds trace headers to it. Then it sends the request to the nearest available node. The gateway writes the result to the audit log.

**6.4 Paragraphs.** Use paragraphs to group related information. Start each paragraph with a topic sentence. The next sentences explain it or add detail.

**6.5 One topic per paragraph.** The topic sentences, read alone, must give an outline of the text.

**6.6 Six sentences at most.** If a paragraph is longer, split it at a change of topic.

---

## 7 Safety instructions

Use WARNING when a person can suffer injury or death. Use CAUTION when equipment or data can suffer damage. If one action creates both risks, use WARNING. Other fields can use other words (for example, DANGER or NOTICE), but the content must still obey rules 7.1 to 7.3. STE does not set layout, capitals, or symbols - follow the project's style guide.

**7.1 Show the level.** Start with the level word (or a symbol). Do a risk analysis first. Say what the risk really is: an abstract statement ("Extreme cleanliness is imperative") does not say what can happen.

**7.2 Start with the command or the condition.** The reader must know how to prevent the accident. If a condition must come first, give it first.
- STE: CAUTION: WHEN YOU DELETE A VOLUME, MAKE SURE THAT NO SERVICE USES IT. THE SERVICE CAN STOP.

**7.3 Say the risk or result.** If you can, tell the reader what happens if they do not obey. A specific risk makes the reader more careful. All safety instructions keep to the 20-word limit.

---

## 8 Punctuation and word count

**8.1 Punctuation.** All standard English punctuation is allowed, but not the semicolon. A semicolon makes long sentences possible and is hard to use correctly. Write two sentences.
- Not STE: The job did not complete; start it again.
- STE: The job did not complete. Start it again.

**8.2 Hyphens.** Use a hyphen to join words that work together as one unit before a noun ("low-latency link", "read-only mode", "three-node cluster"), in two-word numbers, in a letter or number with a noun ("T-junction", "3-prong plug"), in verbs formed from a noun ("heat-treat"), and between a prefix that ends in a vowel and a root that starts with one. A hyphen is not a dash.

**8.3 Parentheses.** Use them for references to figures or text, for identifiers of items, for step identifiers, for abbreviations, for a singular and plural together ("the file(s)"), to explain a word or part of a sentence, and to give an alternative.
- STE: Open the first (second) tab.
- STE: Add replicas slowly (one replica each minute).

**8.4 The colon before a list.** The colon that introduces a vertical list closes the sentence for counting. The lead-in is one sentence and each item is another. The limit (20 or 25 words) applies to each.

**8.5 Parentheses count as one word.** The words inside the parentheses are a separate sentence for counting: "Make sure that the job is stopped (the status shows "Stopped")." has 8 words in the main sentence and 4 in the sentence in parentheses.

**8.6 One word each.** For the word count of a sentence, each of these items is one word:
- numbers (also spelled out, like "twenty-one"),
- a number with its unit ("20 kg", "10 ms"),
- abbreviations and acronyms,
- alphanumeric identifiers,
- quoted text (including formulas and placards),
- titles, headings, and labels,
- names of people, organizations, and countries.

Do not count the numbers that identify steps or paragraphs.

**8.7 Hyphenated words.** A hyphenated word is one word in the count.

---

## 9 Writing practices

**9.1 Use a different sentence when a word swap does not work.** The dictionary gives an alternative for many rejected words. Use it directly only if it has the same part of speech and keeps the meaning. Otherwise ask: "What is the meaning in this context? What must the reader do?" Then write a new sentence, often shorter.
- Not STE: The endpoint must be reachable from the build agent.
- STE: Make sure that the build agent can connect to the endpoint.

Do not accept a swap that gives a sentence that is poor English or means something else. When you change one part, check the rest of the text.

**9.2 Use approved words with care.** An approved word usually has one meaning and one part of speech. Read its dictionary definition before you use it.
- Not STE: When the load goes down, ... STE: When the load decreases, ...
- Not STE: The label turns red. STE: The label changes to red.
- Not STE: Keep the temperature below 80 degrees. STE: Make sure that the temperature is less than 80 degrees.
- Not STE: Check that the latency is low. STE: Make sure that the latency is low.

**9.3 No phrasal verbs.** A verb plus a preposition often has a meaning that differs from its parts. "Put out the fire" - use "extinguish". "Give off fumes" - use "release". A few phrasal verbs are approved (for example, "put on", "come on"); the dictionary lists them with a restricted meaning.

**9.4 Consistent style.** Use the same words and sentence for the same type of step. If you write "Delete the cache folder" in one step, do not write "Remove the cache folder" in another step for the same action.

---

## General recommendations (not rules, but they prevent typical errors)

**GR-1 "that".** Write "that" after verbs such as "make sure", "show", and "recommend". It marks the start of the second clause.
- Not STE: Make sure the port is open. STE: Make sure that the port is open.

**GR-2 "with".** It has three meanings: association ("the panel with green fasteners"), help or sharing, and means. Read the sentence again to make sure that it has one meaning. Put the primary action verb in the step.
- Not STE: Use the linter to examine the code. STE: Examine the code with the linter.

**GR-3 Pronouns.** Use only approved pronouns ("he" and "she" are not approved). If a pronoun can point to more than one noun, repeat the noun.
- Not STE: If the client connects to the proxy, it can stop.
- STE: If the client connects to the proxy, the client can stop.

**GR-4 "this".** Make sure that the reader knows what "this" points to. Prefer "this" with a noun, or write the cause again.

**GR-5 False friends.** A word that looks like a word in your language can have a different English meaning. Examples for speakers of Spanish: "actually" is not "actualmente" (use "now" or "at this time"); "eventually" is not "eventualmente"; "library" is not "librería"; "assist" is not "asistir" (to attend); "sensible" is not "sensible" (sensitive); "carpet" is not "carpeta" (use "folder"); "realize" is not "realizar" (use "do" or "make"). Check the meaning of every word you are not sure about.

**GR-6 Latin abbreviations.** Do not use e.g., i.e., etc. Write "for example", "that is", or finish the list with a clause. If the extra words are not necessary, omit them.

**GR-7 Inclusive language.** Use gender-neutral language. Do not use "he" or "she". Do not use "man" or "woman" unless the context needs them (for example, in a medical text).

**GR-8 Possessive.** The possessive ("the user's account") is allowed. If you are not sure that it is correct, use "the account of the user" or a different sentence.
