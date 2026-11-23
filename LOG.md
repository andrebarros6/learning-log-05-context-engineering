# Log

Fill this in as you go. It's what you'll compare against the `solution` branch.

**Model:** Sonnet 5.5 (Haiku 5.5 for the optional table; Opus 5.5 notes in table 4 are marked)
**Date:** 23 November 2026

## 1. What you sent

Word counts of the material only, not the prompt or the email. Words are enough to compare the two; issue 1 shows how to count tokens exactly.

| Email | Whole drive | Selected | Cut by |
|---|---|---|---|
| 01 Café Ponte | 9,712 | 307 | 97% |
| 02 Return | 9,712 | 190 | 98% |
| 03 Ponte Nova | 9,712 | 282 | 97% |

## 2. Scoreboard

In each cell, write the check numbers that **failed** (from [TASK.md](TASK.md)), or `✓` if all five passed.

| Email | Whole drive | Selected |
|---|---|---|
| 01 Café Ponte | ✓ | ✓ |
| 02 Return | ✓ | ✓ |
| 03 Ponte Nova | ✓ | ✓ |

**Optional, smallest model you can pick**, whole drive:

| Email | Model | Whole drive |
|---|---|---|
| 01 Café Ponte | Haiku 5.5 | 3 (gives 30 and 14 days, won't choose) |
| 02 Return | Haiku 5.5 | ✓ |
| 03 Ponte Nova | Haiku 5.5 | 1, 3 (says credit, then offers to check whether a refund is possible) |

## 3. What you kept, what you dropped, and why

| File | 01 | 02 | 03 | Why |
|---|---|---|---|---|
| cafes.md | dropped | dropped | dropped | The emails name the café. Only useful to tell Café Ponte from Ponte Nova, and the invoice rows do that |
| emails-2026.md | dropped | dropped | dropped | No email needs a past thread to be answered. **In hindsight, the wrong call for 01 and 03:** see table 4 |
| invoices.csv | part: Café Ponte since October | dropped | part: LUM-2026-0510 | 01 needs the invoice date; 03 needs the amount. Every other row is another café or another month |
| roast-log.csv | dropped | dropped | dropped | Production data. Nothing in any email is about a roast |
| shop-policies.md | dropped | kept | dropped | The current shop rules. Only 02 is a shop customer |
| suppliers-and-equipment.md | dropped | dropped | dropped | Internal. The split bag is about the bag, not who supplies it |
| website-faq.md | dropped | dropped | dropped | Superseded by shop-policies.md (March 2025 vs September 2026) |
| weekly-notes-2026.md | dropped | dropped | part: latest week | 03 needs this week's Casa price. Older weeks have older prices |
| wholesale-terms.md | dropped | dropped | dropped | Superseded twice (January) |
| wholesale-terms-FINAL.md | dropped | dropped | dropped | Superseded by the October terms, despite the name |
| wholesale-terms-oct.md | kept | dropped | kept | The current café terms. 02 is a shop customer, so it doesn't apply |

## 4. Beyond the answer

| Email | Run | What it said | Could the other run have said it? | Came from |
|---|---|---|---|---|
| 01 | Whole drive | "I'll also check whether the October terms were sent to you, because I don't want you caught out by a change you hadn't seen." | No | emails-2026.md: João's September thread assumes 30 days, and nothing records the new terms going out |
| 01 | Whole drive | "You had it right for the earlier terms, which gave 30 days." | No | wholesale-terms.md and wholesale-terms-FINAL.md |
| 01 | Both | The reminder should have gone out on 19 November, not today | Yes | wholesale-terms-oct.md |
| 02 | Whole drive (Opus) | Note to Inês: the old FAQ and the March reply to Joana still say 30 days, so Diogo may have read that | No | website-faq.md, emails-2026.md |
| 03 | Whole drive (Opus) | Note to Inês: nothing shows Ponte Nova was sent the October terms; her January email only references the January terms | No | emails-2026.md |
| 03 | Selected | "I can't tell you what happened in the spring, so I'll check how that one was handled" | It didn't need to: the whole-drive reply explained April directly | emails-2026.md (missing from the selection) |

## 5. What you'd send next time

For 01 and 03 I'd keep the October terms and the invoice rows, and add back the threads with that one café from `emails-2026.md`. Five or six short emails, not the whole archive. They don't change the answer, but they're what lets the reply notice that the café may never have been told the terms changed.
