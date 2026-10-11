# Editorial voice

Applies to prose everywhere: the project's own documents, commit messages,
pull request descriptions, comments, docstrings, and any text the system
itself emits.

**VOICE-1.** Engineer to engineer. Straightforward, factual, terse. Never
persuasive, never aphoristic.

**VOICE-2.** State the thing. Do not build up to it, and do not restate it
afterwards. A paragraph that summarises the paragraph above it is deleted.

**VOICE-3.** Prefer the shortest form that stays precise. Terse is not the
same as vague: cutting a qualifier that carried meaning is a defect, not an
edit.

**VOICE-4.** Say who decided and what was rejected. Passive constructions
that hide the actor ("it was determined that") are forbidden in decision
records.

**VOICE-5.** Use the right container. A comparison across more than two
dimensions is a table. A sequence is a list. Everything else is a sentence.
Do not bullet-point prose to make it look organised.

## What not to write

This list is enhanced reflectively. When slop appears in a review, the clause
that would have caught it is added here.

**VOICE-6. Marketing register.** No "robust", "seamless", "powerful",
"elegant", "comprehensive", "battle-tested", "first-class" as praise,
"blazing fast", "delightful", "leverage" as a verb, "utilise". Describe the
property, or say nothing.

**VOICE-7. Self-congratulation.** Do not describe your own output as
"significantly improved", "dramatically simpler", "much cleaner", "a solid
foundation". Describe what changed; the reader grades it.

**VOICE-8. Aphorism and epigram.** A sentence whose work is cadence rather
than content, wherever it sits. No "simplicity is the ultimate
sophistication", no "the best code is no code", no "X is not Y, it is Z"
reversals used as rhetoric, no restatement dressed as a moral. A closing line
is where these collect, but a maxim in the middle of a paragraph, or bolded as
though it were a heading, is the same fault.

The test is rewriting. Put the sentence as a plain statement of fact. If that
statement is already in the text, the maxim repeats it and is deleted. If
there is no statement to be had, the sentence was empty. "The bars passed
twice and failed on the third run, so one pass is not evidence" is the
statement; "a bar that passes twice is not a bar that holds" is the maxim
made from it, and only one of them belongs in the text.

**VOICE-9. Filler openers.** No "Basically", "Essentially", "Simply put",
"At its core", "In essence", "Let's dive in", "In today's landscape". Delete
the opener and start at the noun.

**VOICE-10. Hedging and throat-clearing.** No "it's worth noting that",
"it should be mentioned", "arguably", "somewhat", "fairly", "quite",
"I think", "perhaps". Either the claim holds or it is stated as an open
question with what would settle it.

**VOICE-11. Rhetorical questions.** No headings phrased as questions to the
reader, no "So what does this mean?" as a transition. A list of open
questions is the one place a question mark is load-bearing.

**VOICE-12. Emphasis inflation.** Do not bold for emphasis in running prose.
No exclamation marks. No ALL CAPS. No scare quotes to signal disdain. Emoji
are forbidden everywhere, including commit messages.

**VOICE-13. Fake precision.** No "~40% faster", "roughly 3x", "most users"
unless you measured it and can say how. An unmeasured estimate is labelled as
an estimate.

**VOICE-14. Anthropomorphism.** The workflow does not "want" anything, the
judge does not "feel" that a PR is sloppy, the test suite is not "unhappy".
Say what the code does.

**VOICE-15. Unresolved references.** An identifier is not a substitute for
the thing it names. Do not write "satisfies FR-15", "per ADR-004", "blocked on
question 9", "lands in M0.5" and leave the reader to look it up. Name the
thing, then cite the id if the id is useful: "the exception registry (FR-15)".
This holds hardest in text written for someone who is not reading the
specification at the time — pull request descriptions, comments, findings the
system emits, and anything addressed to a person rather than a file.

**VOICE-16. Padding.** "In order to" is "to". "Due to the fact that" is
"because". "At this point in time" is "now". "Has the ability to" is "can".
Do not restate a heading in the sentence beneath it.

**VOICE-17. Comment slop.** A comment that restates the code is deleted. A
docstring that begins "This function is responsible for" is rewritten to
start with the verb. Comments explain why, and record the constraint that is
not visible from the code. No commented-out code; git holds it.

**VOICE-18. Forward promises.** Documentation describes what is, in the
present tense. Not "will eventually support Forgejo". Intent belongs where
the project tracks it, under milestones or open questions.

**VOICE-19. Narrating yourself.** Pull request descriptions and commit
messages describe the change, not the process of arriving at it. No "I first
tried X, then realised Y". No apologies. No "as requested".

**VOICE-20. Rhetorical triples.** Three parallel items where the meaning
needs one or two. "It is faster, cleaner, and more maintainable" says
"faster" with two decorations. Count the items, then count the facts.

**VOICE-21. Em dashes.** Use a colon, a comma, a semicolon, or a full stop.
An em dash is a tell, not a choice, and the sentence it appears in is
almost always two sentences wearing one coat.

**VOICE-22. Telling the reader what they think.** No "and that is what you
really want", no "you might be wondering", no "the astute reader will
notice". State the thing; the reader's mind is theirs.

**VOICE-24. Slop vocabulary.** Words that arrive instead of thought:
"leverage" for "use", "utilise" for "use", "delve", "unpack", "landscape",
"realm", "tapestry", "testament to", "journey", "seamlessly", "robustly",
"holistic", "synergy", "paradigm", "game-changing", "best-in-class",
"cutting-edge", "elevate", "empower", "unlock", "supercharge". The list
grows as new ones appear; each entry is a word that would not survive being
asked what it adds.

**VOICE-25. Because we can.** A change justified by its own availability is
not justified. No "because we can", no "why not", no "it seemed like a good
idea". Say what the change is for.

**VOICE-26. Coy teasers.** A list whose items are withheld, ranked or
flavoured before they are given: "one of them matters", "and here is the
interesting part", "guess which one". Say which item matters and why in the
same breath as the item, or say nothing about the ranking.

**VOICE-27. Manufactured antithesis.** "X, not Y", "X, rather than Y", "not
only Y but X", where Y is not a live alternative anyone proposed. "Make the
round trip a command, not only a test" is four faults in one line:

- The negative half is dead weight. The sentence's job is to name the change;
  half of it describes the state being left behind, which the reader can see.
- It argues with an imagined objection. "not only a test" implies someone
  thought a test was enough, and casts the writer as the one who noticed.
- The contrast is empty. A command is not a test, so saying so adds nothing.
  The shape promises a distinction and delivers a restatement, which is how
  an aphorism is built: the cadence of significance with none of the content.
- It hides the deliverable and blurs the scope. The change is "add a
  command"; the frame defers the noun, and "not only" leaves it unsaid
  whether the test survived.

"Add the round trip command" is the same change in fewer words.

The test is deletion. Strike the negated half. If every fact survives, the
half was rhetoric and the clause is broken. If a fact goes with it, the
contrast was carrying information and the sentence is fine: what the code did
before, which of two options was rejected and why, a measurement that only
means something beside another one. "Nine of ten cases pass, not the eleven
claimed" loses a number when struck. "A command, not only a test" loses
nothing.

**VOICE-28. Garden paths.** A sentence the reader must parse twice. "Correct
references the doctrine cannot resolve" reads first as "correct references",
then as "references the doctrine", and only then as intended. Give the noun
its article and put its modifiers before it: "Correct the unresolvable
doctrine references". If a clause must follow the noun, keep its "that".

The test is the opening words. If they form a phrase the sentence does not
mean, rewrite it.
