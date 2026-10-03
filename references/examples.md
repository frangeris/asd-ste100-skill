# Before and after rewrites

Four rewrites in a software setting. Each one shows the source text, the STE text, and the rules that caused the changes. Read them to see the typical moves: split, restructure, replace, and make the hidden facts explicit.

---

## 1. Procedure with a risk

Not STE:

> Before you rotate the API key, you'll need to ensure that nobody is deploying, because rotation invalidates the old credentials and may break running jobs. Then go to Settings > Keys, hit Rotate, and wait for the banner before updating your .env file.

STE:

> CAUTION: BEFORE YOU REPLACE THE API KEY, MAKE SURE THAT NO DEPLOYMENT OPERATES. AFTER THE CHANGE, THE PREVIOUS KEY DOES NOT OPERATE. THE JOBS THAT USE THE PREVIOUS KEY CAN STOP.
>
> 1. Open "Keys" in "Settings".
> 2. Click "Rotate".
> 3. Wait for the message "Key rotated".
> 4. Write the new key in the .env file.

What changed:

- The risk moved from the middle of a sentence to a CAUTION at the start (7.1 to 7.3). It names the condition first, then the result.
- "ensure" became "make sure that" (dictionary). "may" became "can" (dictionary). "hit" is slang and became "click" (1.10).
- "rotate" is not an approved verb, so the prose says "replace" (1.3). The word "Rotate" stays only in the quoted button label (8.6).
- "you'll need to" is a contraction with a vague verb (4.2). The steps are imperative (5.3), one instruction each (5.2).
- "banner" and "message" would name one thing in two ways. The step now uses the quoted label that the screen shows (1.11, 8.6).
- "updating" is an -ing form (3.5). The step uses "Write".

---

## 2. Description

Not STE:

> The retry middleware, which wraps every outbound HTTP call, is configured with a maximum attempt count and a backoff strategy, and it will automatically re-issue requests that failed due to transient errors such as timeouts or 503 responses, waiting progressively longer between attempts until the limit is reached, at which point the original error is surfaced to the caller.

STE:

> The retry middleware controls each outbound HTTP request. The middleware has two settings: the maximum number of retries and the wait time between the retries.
>
> When a request does not complete because of a timeout or a 503 response, the middleware sends the request again. Before each retry, the middleware waits for a longer time. When the middleware sends the maximum number of retries, the middleware gives the error to the caller.

What changed:

- One 59-word sentence became five sentences of 25 words or fewer (6.3).
- Two paragraphs, each with a topic sentence and one topic: what the middleware is, and what it does (6.4, 6.5).
- Passive and progressive forms ("is configured", "is reached", "waiting") became active verbs with an agent (3.4, 3.5, 3.6).
- "the middleware" repeats instead of "it", so the reader never has to guess the referent (GR-3, 6.2).
- "wraps", "failed", and "surfaced" are not approved. The new sentences say what happens (9.1).
- "call" and "attempt" became "request" and "retry", so each thing has one name (1.11).
- "such as" followed by a list became a direct "because of a timeout or a 503 response" (4.1).

---

## 3. Error and UI messages

Not STE:

> Oops! We couldn't save your changes. Please try again later or contact support if the problem persists.

STE:

> The system cannot save your changes. Try again. If the problem continues, contact support.

What changed:

- "Oops!" gives no information. Remove it (4.1).
- "couldn't" is a contraction (4.2). "persists" became "continues".
- One sentence with two actions became three short sentences. The condition is first (5.4).
- The message has no "please". Politeness words add length and carry no instruction.

Also keep a message short. If you must tell the reader what to do, write the instruction as a command. If you cannot tell the reader what to do, give only the information.

---

## 4. README quick start and commit message

Not STE:

> ## Quickstart
> Simply clone the repo, run `npm install` and you're good to go! Make sure you've got Node 20+ installed (older versions might not work).

STE:

> ## Installation
> 1. Make sure that the version of Node.js is 20 or higher.
> 2. Clone the repository.
> 3. In the repository folder, type `npm install`.
>
> If the version of Node.js is less than 20, errors can occur.

What changed:

- "Simply" and "you're good to go" carry no instruction. The steps are numbered and imperative (5.2, 5.3).
- "run" is not an approved verb for a command (dictionary). "type" is a technical verb for input (1.12, category 2).
- "might not work" is vague and uses "might". The new sentence names the versions and says what can happen (4.1, dictionary).
- "Make sure you've got" lacks "that", has a contraction, and uses "got" (GR-1, 4.2).
- "Quickstart" is a compound that has no dictionary entry, and "quick" is not an approved adjective. The heading is a technical noun, "Installation" (3.5).
- "Node 20+" uses a symbol that a non-native reader can miss. "20 or higher" says the same in words.

Commit messages: the layout comes from Conventional Commits. The words obey STE.

Not STE: `feat(client): adding support for retrying failed requests`

STE: `feat(client): add a limit of retries`

The imperative verb replaces "adding" (3.5). "support for retrying failed requests" was vague. The new text says what changed.
