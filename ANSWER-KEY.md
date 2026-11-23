# Answer key

For each email: the right answer, the trap, what it needs from the drive, and what's defensible either way. Check your scoreboard and table 3 against it before you read SOLUTION.md.

## The drive, file by file

| File | What it is | Current? |
|---|---|---|
| `wholesale-terms.md` | Terms for cafés, January 2026 | No. 30-day payment, cash refunds for damage, Monday roast |
| `wholesale-terms-FINAL.md` | Terms for cafés, June 2026. Called FINAL, and says "this is the one to send" | No. 30-day payment, replacement on next delivery |
| `wholesale-terms-oct.md` | Terms for cafés, October 2026 | **Yes.** 14-day payment, credit note for damage, no cash refunds |
| `shop-policies.md` | Shop rules, updated 2 September 2026 | **Yes.** 14-day returns of unopened bags |
| `website-faq.md` | The old site's FAQ, March 2025 | No. 30-day returns, €3.90 shipping, Monday roast |
| `emails-2026.md` | Threads Inês kept | Mixed. Her replies quote whichever rule applied at the time, including 30 days in March and September |
| `cafes.md` | Who the cafés are | Yes, but only needed to tell Café Ponte from Ponte Nova |
| `invoices.csv` | Every wholesale invoice this year | Yes. Two rows matter |
| `weekly-notes-2026.md` | Prices and stock, week by week | Yes. Only the latest week matters |
| `roast-log.csv` | Roast batches | Not needed for any email |
| `suppliers-and-equipment.md` | Green coffee, roaster, van | Not needed for any email |

The trap in every email is the same shape: **an old rule, stated confidently, by a file that looks authoritative**. The FINAL file, Inês's own past replies, a published FAQ.

## 01 — Café Ponte: "I thought we had 30 days?"

**Right answer.** Payment is 14 days from the invoice date (October terms). LUM-2026-0485 is dated 4 November, so it fell due on 18 November and is overdue. No late fee yet: the 2% applies only 30 days after the due date, which is 18 December. Paying by the end of November avoids it.

**The trap.** "30 days" is in the January and June terms, and in Inês's September replies to Miradouro and to João himself. There's also a 30 in the October terms, in the late-fee clause, which is probably what João half-remembers.

**Needs:** `wholesale-terms-oct.md`, and the invoice row for LUM-2026-0485.

**Defensible either way:**

- Including Café Ponte's other recent invoices. It lets the reply mention LUM-2026-0509 (18 November, due 2 December), which is useful to João. Not required.
- Including `emails-2026.md`. Not needed for the answer. But it's the only file that shows Inês told João "30 days" in September, and that nothing records the October terms being sent to him. A reply that knows that can apologise for the change instead of just stating it. **This is the best example in the exercise of the cut losing something.**

**Fails:** says 30 days, says it isn't due yet, threatens a fee now, or says Inês will check which terms apply (the drive settles that).

## 02 — Diogo: returning two sealed bags

**Right answer.** Unopened bags can be returned within 14 days for a refund, postage paid by the customer (shop policies, September 2026). His order arrived on 5 November; the email is from 23 November, 18 days later. Outside the window. Offering to check whether Inês will make an exception is fine, as long as it's clearly an exception and not the policy.

**The trap.** The 2025 FAQ says 30 days for a full refund. So does Inês's March reply to Joana Pires. Under either, he'd be in time.

**Needs:** `shop-policies.md`. That's all.

**Defensible either way:** including the FAQ and the March email, labelled as superseded, so the reply can warn Inês that old wording may still be out there. A selection that includes them unlabelled is worse than the whole drive: you've kept the trap and dropped most of the context that shows it's old.

**Fails:** offers a refund under 30 days, or doesn't say the 14 days have passed ("I'll check whether the window still covers your bags").

## 03 — Ponte Nova: "Last time you refunded us by transfer"

**Right answer.** Damage reported within 48 hours, with a photo, is credited at full value against the next invoice. No cash refunds on wholesale orders (October terms). She reported it the morning of delivery, so she's inside the window. The bag is 5 kg of Casa at €22/kg: **€110** ex VAT, invoice LUM-2026-0510.

**The trap.** In April Inês refunded Sofia €100 by transfer, under the January terms. Sofia asks for the same. The June terms offer a replacement on the next delivery instead. Three files, three different remedies.

**Needs:** `wholesale-terms-oct.md`, the current Casa price (latest week of `weekly-notes-2026.md`, or the invoice row), and the invoice row for LUM-2026-0510.

**Defensible either way:** including the April thread from `emails-2026.md`. It lets the reply explain why it's different this time, which is kinder. Without it, the reply can only say "I'll check what happened in the spring", which is honest but weaker.

**Fails:** promises a transfer, offers a replacement, quotes €100 or €105, says it's too late, or says Inês will check whether a refund is possible this time (the terms say no).

## Easy to get wrong when selecting

- **Taking the FINAL file because of its name.** It's June's. October's file is the current one.
- **Taking a whole CSV for one row.** `invoices.csv` is about half the drive by size. Each wholesale email needs one or two rows.
- **Dropping the date.** A selection that includes the October terms but not the invoice date can't say whether the invoice is overdue.
