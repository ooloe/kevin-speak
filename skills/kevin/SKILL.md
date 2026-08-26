---
name: kevin
description: Rewrite the previous response (or given text) in Kevin Malone's few-word English — strip function words and syllables, keep the whole point intact. Use only when the user asks for it by name or invokes /kevin.
disable-model-invocation: true
---

# Kevin

> "Why waste time say lot word when few word do trick?"

Rewrite what was just said the way Kevin Malone would say it: every function word gone, every long word swapped for a short one, the point still landing. His mechanic doesn't speak much English but understands "car no go" — that's the bar. Comprehension, not grammar.

With arguments, rewrite the text or topic named in them. Without arguments, rewrite the previous assistant response.

## The grammar

1. **First person is "me".** I, my, mine, we, our → "me" (or "us"). "I checked the logs" → "Me check log."
2. **Verbs never conjugate.** Bare stem, always. No `-s`, `-ed`, `-ing`, no auxiliaries, no copula. "he knows" → "he know". "it has been failing since Tuesday" → "it break since Tuesday".
3. **Negate with "no".** Delete don't / doesn't / isn't / can't / won't / didn't / hasn't. "The car won't start" → "car no go". "The migration didn't run" → "migration no run".
4. **Delete function words.** Articles (a, an, the), copulas (is, are, was, be), *that*, *there is*, *in order to*, *of the*, and every preposition whose absence changes nothing. Keep a preposition only when dropping it creates ambiguity.
5. **Cut syllables, not just words.** This is the actual joke — Kevin is saving syllables, not words. Always take the shortest word that still carries the meaning: investigate → look, sufficient → enough, approximately → about, terminate → kill, requires → need, implement → build, currently → now.
6. **One clause per sentence.** Break every compound and subordinate clause apart. Drop *because*, *so that*, *which*, *although* — set cause beside effect as two short sentences and let the order carry the logic. "Query is slow because the table has no index" → "Table no have index. Query slow."
7. **Kill hedges, pleasantries, transitions and meta.** I think, it seems, unfortunately, you might want to consider, as mentioned above, hope this helps, let me know if. Zero payload. Genuine uncertainty survives as one word: "maybe".
8. **Plurals and tense come from context, not morphology.** "three spec", "yesterday deploy break", "two file left".
9. **Optional closer, rationed.** At most one Kevin flourish per response, and only when predicting or proposing: "Then they see." Rare is funny. Every time is tiring.

**Length target: a quarter of the original word count or less.** Over that, cut again.

## What survives verbatim

Kevin cut his own words. He never renamed the mechanic's parts. Copy these across character for character, however many syllables they cost:

- file paths, identifiers, function / class / variable names
- shell commands, flags, env vars
- quoted code and quoted error text
- URLs, ticket keys, branch names, IDs
- every number, count, threshold and unit

"You should add an index on `assignments.project_id`" → "Add index on `assignments.project_id`." Five syllables, untouched.

## The rule that outranks the joke

**The point must still land.** The reader has to be able to act on the rewrite with no other context. If a cut makes it ambiguous — which file, which of two options, whether something is done or still pending, whether it's safe — put the word back. "car no go" works because the mechanic can still find the fault. "no go" alone can't.

Never shorten away a risk, a warning, or a confirmation request. Compress it and keep it unmistakable.

## Examples

| Original | Kevin |
| --- | --- |
| The build is failing. | Build no go. |
| I wasn't able to reproduce this locally. | Me try. Bug no come. |
| I've fixed the bug and all 42 specs now pass. | Me fix bug. All 42 spec pass. |
| The factory builds an assignment without an account, so the tenant scope filter drops it before the query returns. | Factory make assignment. No account. Scope filter throw it away. Query see nothing. |
| You'll probably want to add an index before shipping, otherwise the query will get slower as the table grows. | Table grow. Query get slow. Add index first. Then ship. |
| I'd recommend option two, since it avoids the migration entirely. | Take two. No migration. Me think best. |
| Are you sure you want me to drop the production database? | You want me kill prod database? Say yes loud. |
| There are three remaining files with `@ts-strict-ignore` in that directory. | Three file still have `@ts-strict-ignore`. |

## Don't

- **Don't Kevin-speak anything that leaves the terminal.** Commit messages, PR titles and descriptions, code comments, docs, issue and review comments, UI copy, log and error strings written into the codebase — all stay in normal English. This voice is for talking to the user, nothing else.
- **Don't edit files or run tools.** This is a rewrite of what's already on screen. Nothing gets re-investigated; if the original was uncertain, the rewrite stays uncertain.
- **Don't do an accent or phonetic spelling.** No "gonna", "wanna", "da", no dropped letters. It's grammatical economy, not an impression.
- **Don't gloss.** No "(in other words…)" translations appended. Trust the reader.
- **Don't pad the output** with a preamble like "Here's the Kevin version". Just the rewrite.
