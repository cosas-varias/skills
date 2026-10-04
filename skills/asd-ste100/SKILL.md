---
name: asd-ste100
description: 'Write English technical text in ASD-STE100 Simplified Technical English. Use by default for any English technical writing: documentation, READMEs, code comments, docstrings, commit messages, PR descriptions, changelogs, error messages, procedures and specifications. Not for conversational chat replies or non-English text unless asked.'
metadata:
  tags: "Writing, Documentation, Technical English, STE"
  category: "writing"
---

# ASD-STE100 Simplified Technical English

Write English technical text to the ASD-STE100 rules. The goal: one meaning per word, short sentences, no ambiguity, easy for non-native readers and for translation.

## When to apply

- Apply by default to English technical text that goes into files or into git: docs, READMEs, comments, docstrings, commit messages, PR and issue text, changelogs, UI and error messages, procedures.
- Do not apply to quoted text, code identifiers, API names, log output, legal text, or text the user wrote and did not ask to change.
- Do not force it on chat replies to the user, or on text in other languages. The user can ask for it there too.
- If a project has its own style guide, the project guide wins where the two conflict.

## Words

1. Use approved words only with their approved meaning and part of speech. One word = one meaning. Example: "close" is a verb (to close), not "near".
2. Use technical names (nouns: `cache`, `socket`, `handshake`) and technical verbs (`compile`, `hash`, `serialize`) of the domain freely. Keep them consistent: one name for one thing in the whole text.
3. Do not use synonyms for variety. If you call it "peer", call it "peer" every time.
4. Prefer simple words: use "use" (not "utilize"), "start" (not "initiate"), "make sure" (not "ensure"), "about" (not "approximately"), "show" (not "indicate"), "help" (not "facilitate"), "get" (not "obtain"), "stop" (not "terminate").
5. Do not use phrasal verbs when a single verb exists: "remove" (not "take out"), "find" (not "find out"), "continue" (not "go on").
6. Do not make clusters of more than three nouns. "query cache invalidation" is the limit; break longer ones with "of", "for", "in".
7. Use articles ("the", "a") and "this/that" where possible. Do not drop them to save space (except in titles and lists of items).

## Verbs and tense

8. Use only these tenses: simple present, simple past, simple future. Use the past participle only as an adjective or with "is/are" (passive) in descriptive text.
9. Do not use "-ing" forms as verbs or as nouns, except in technical names (e.g. "routing table").
10. Use the active voice. Use the passive voice only in descriptive text, and only when the agent is not known or not important.

## Sentences

11. Procedural text (instructions): max 20 words per sentence. Descriptive text: max 25 words.
12. One instruction per sentence. Two simultaneous actions can be in one sentence.
13. Write instructions in the imperative: "Run the tests." Not "You should run the tests."
14. Put a condition first: "If the build fails, do a clean build."
15. Write a warning or caution as a short command first, then the reason: "Do not delete the key. The data becomes unrecoverable."

## Paragraphs

16. Descriptive text: one topic per paragraph, max 6 sentences. Start with the topic sentence.
17. Use vertical lists for sequences and for more than two items.

## Commit messages

- Subject: imperative, present tense, max ~72 characters, no final period. "Add canonical hash to query cache".
- Body: short sentences, one fact per sentence. Say what changed and why.

## Self-check before you finish

- Is any sentence longer than 20 (procedure) or 25 (description) words? Split it.
- Is there a passive that can be active? Change it.
- Is there an "-ing" verb, a phrasal verb or a complex word with a simpler form? Replace it.
- Do two different words name the same thing? Pick one.
