# The task

Torrefação Lume is a two-person coffee roaster in Porto. Inês runs the shop and the cafés it supplies; Rui roasts. Three emails came in this week, and Inês wants Claude to draft the replies.

| Email | From | About |
|---|---|---|
| [01-cafe-ponte.md](emails/01-cafe-ponte.md) | João, who runs a café they supply | A payment reminder he thinks came too early |
| [02-return.md](emails/02-return.md) | Diogo, a shop customer | Sending back two unopened bags |
| [03-ponte-nova.md](emails/03-ponte-nova.md) | Sofia, who runs another café | A bag that split in the delivery |

Everything needed to answer them is somewhere in [`drive/`](drive/), the business's shared drive. So is a lot that isn't needed, and some that is out of date. Like most shared drives, nobody has tidied it: old versions sit next to new ones, and a file called FINAL isn't necessarily the latest.

The business is invented. Every name, café and number is fictional. "Today" is the date on each email.

## The prompt

[prompt.md](prompt.md) is the same for every chat, and you don't change it:

> You answer emails for Inês at Torrefação Lume, a small coffee roaster in Porto. Draft her reply to the email. Use only facts from the material provided. If the material doesn't settle something, say Inês will check rather than guessing. British English, no exclamation marks. Sign off as Inês.

The only thing that changes between your runs is the material that goes with it.

## What a good reply looks like

Score every reply against five checks. Pass or fail, no half marks. If you're unsure, it's a fail.

| # | Check | Fails when… |
|---|---|---|
| 1 | **Current rule** | The reply applies a policy, term or price that has since been replaced, or offers it as a possibility ("I'll check whether we can do what we did last time") |
| 2 | **Right numbers** | A date, amount, deadline or quantity is wrong, or one the email needs is missing |
| 3 | **Commits** | The material settles the question but the reply doesn't answer it: it says Inês will check something the drive already answers |
| 4 | **Nothing invented** | A policy, date, amount or promise that isn't in the material |
| 5 | **Voice** | American spelling, an exclamation mark, or not signed Inês |

Check 3 is the one people skip. A reply that hedges looks careful. If the answer is in the drive and the reply says "I'll look into it", the reply has failed. Saying "I'll check" is right only when the material really doesn't settle the point.

## Notes worth scoring separately

Sometimes a reply adds something beyond the answer: a note to Inês before she sends it, a warning, a question. Don't score these. Copy them into table 4 of [LOG.md](LOG.md). They're what step 4 is about.
