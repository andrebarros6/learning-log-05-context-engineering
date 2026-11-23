# Solution — Exercise 05

## What's on this branch

- **[ANSWER-KEY.md](ANSWER-KEY.md):** the right answer to each email, the trap in it, which drive files it needs, and the selections that are defensible either way. Check your log against it before you read on.
- **[`selected/`](selected/):** my three selections.
- **[LOG.md](LOG.md):** my filled-in log, for the Sonnet runs.
- **[`runs/`](runs/):** every reply, by model. See [runs/README.md](runs/README.md) for the naming.

## How these runs were done

Claude Code ran every chat, on 23 November 2026, on three models: Haiku 5.5, Sonnet 5.5 and Opus 5.5. Each chat was a fresh subagent with no history. It read one file holding exactly what you'd paste: the material, the prompt and the email. That's close to a claude.ai chat, but it isn't one. Every cell is a single run. Your numbers will differ. Read the failures more than the counts.

Each email ran three ways:

- **A:** the whole drive, with the prompt and email *first*.
- **B:** the whole drive, with the prompt and email *last*. This is step 1 of the exercise.
- **C:** my selection, prompt and email last. This is step 3.

A is extra. I ran it to see whether ordering alone changed anything.

One honest wrinkle: I added a March email to the drive halfway through, after a first version of email 02 turned out too easy (every model got it right). The Haiku and Opus runs for emails 01 and 03 were done on the drive without that email. It's one short thread about returns, unrelated to either.

## What I found

### Size

| Email | Whole drive | Selected | Cut by |
|---|---|---|---|
| 01 Café Ponte | ~9,700 words | 307 | 97% |
| 02 Return | ~9,700 words | 190 | 98% |
| 03 Ponte Nova | ~9,700 words | 282 | 97% |

The CSVs are most of the drive by size, and the emails need two of their rows between them.

### Answers

Pass or fail on all five checks. In the fail cells, what went wrong.

| Email | Model | A: whole, question first | B: whole, question last | C: selected |
|---|---|---|---|---|
| 01 Café Ponte | Haiku | **Fail:** "I'm checking which terms the reminder was based on" | **Fail:** lays out 30 and 14 days side by side, won't choose | ✓ |
| | Sonnet | ✓ | ✓ | ✓ |
| | Opus | ✓ | ✓ | ✓ |
| 02 Return | Haiku | ✓ | ✓ | **Fail:** "the 14 days are counted from a date I don't have" |
| | Sonnet | ✓ | ✓ | ✓ |
| | Opus | ✓ | ✓ | ✓ |
| 03 Ponte Nova | Haiku | **Fail:** gets €110 right, then "last time we refunded you, I need to check" | **Fail:** says credit, then offers to check whether a refund is possible | ✓ |
| | Sonnet | ✓ | ✓ | ✓ |
| | Opus | ✓ | ✓ | ✓ |

**The whole drive only hurt the small model.** Sonnet and Opus got every email right with nearly 10,000 words of mostly irrelevant, partly contradictory material in front of them. I expected the dump to fail more than it did. That's the result, so it's the lesson: on a strong model, the case for selecting isn't that the dump breaks. It's the other two things below.

**Haiku didn't invent anything. It stalled.** It never quoted an old rule as current. It saw two versions, couldn't choose, and wrote "I'll check". That's check 3, and it's the failure most likely to get past you, because a reply that hedges looks careful.

**Selection fixed Haiku on two of three, and broke it on the third.** Given only the shop policy, Haiku decided it didn't know what the 14 days count from, and wouldn't say Diogo was late. With the whole drive it was fine. A smaller context isn't automatically an easier one.

**Ordering made no difference.** Question first or question last, every model scored the same on every email. Ordering still matters for cost, because an API can only reuse the cached part of a prompt if the stable material comes first. But I couldn't show it changing an answer here.

### What the cut couldn't see

This is the part I'd look at hardest. In **8 of the 12** whole-drive replies from Sonnet and Opus, the reply added something for Inês that no selected reply could have:

- **01 and 03:** "Nothing in the drive shows the October terms were sent to Café Ponte" (or to Ponte Nova). João's September email still assumes 30 days. If he never got the new terms, holding him to them is unfair. That's true, it matters, and it's in no single file. It comes from noticing what *isn't* in `emails-2026.md`.
- **02:** "The old FAQ and your March reply to Joana still say 30 days. If that wording is still out there, Diogo may have read it." Worth knowing before you refuse him.

My selections got every answer right on Sonnet and Opus. They also dropped `emails-2026.md` every time, because no email *needed* it, and with it went the one warning in this exercise that could save Inês a falling-out with a customer.

**That's the "when not to".** Selection answers the question you asked. The whole drive sometimes answers one you didn't think to ask. If I did this again, I'd keep a short version of the email history in the wholesale selections: the threads with that café, not the whole archive.

## What I'd tell someone starting this

- **Cut for the model you're actually using.** On a strong model the dump mostly costs you tokens. On a small one it costs you answers.
- **Read the whole-drive replies for what they add, not just whether they're right.** That's where the dropped evidence shows up.
- **Defend each cut in a sentence.** "Superseded by the October terms" holds up. "Not relevant" is how `emails-2026.md` got dropped.
