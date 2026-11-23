# Learning Log — Exercise 05: Context engineering

**Issue 5 of 30 · Working with the models** · [Read the issue](https://barrosbuilds.com/log) · [All exercises](https://github.com/andrebarros6/learning-log)

**Kind:** inside Claude · **Needs:** a Claude account, git · **Cost:** free

Decide what goes in front of the model, and be able to say why you left the rest out.

---

## The theory

Every message you send carries its context with it: the instructions, the documents, the history. The model reads all of it, every time. So context is a budget you spend, not a bucket you fill.

The easy move is to paste everything. The whole policy folder, the whole spreadsheet, the whole email archive, because choosing takes effort and leaving something out feels risky. Sometimes that's fine. Often it isn't:

- **It costs.** Every token you send is paid for, on every call, in money or in usage limits.
- **It confuses smaller models.** Give a small model three versions of the same policy and it may stall between them instead of choosing.
- **It hides what matters.** The one line that decides the answer sits somewhere in the middle of thousands of lines that don't.

Context engineering is the habit of choosing. Three moves:

- **Selection.** What does this task actually need? Keep that. Drop the rest.
- **Ordering.** Stable material first, the question last. That's the layout Anthropic's documentation recommends for long inputs, and it's what lets an API cache the stable part and not pay for it again (issue 27 covers the cost side).
- **Eviction.** What can go now that it has done its job? Old versions, settled threads, last month's notes.

The skill isn't cutting. It's being able to defend the cut.

## What you'll do

This one happens in the Claude chat window. No code, no API key.

1. **Read the task** in [TASK.md](TASK.md): three emails to answer for a small coffee roaster.
2. **Answer them with the whole drive** pasted in: about 9,700 words of everything the business has.
3. **Select** what each email actually needs, and write down what you left out and why.
4. **Answer them again** with only your selection.
5. **Compare** the size, the answers, and what your cut couldn't see.

## When this is not the right tool

**When the material fits and all of it is relevant, don't engineer it.** A long document the task really needs belongs in the context whole. Cutting it to save tokens can cost you the answer.

**And watch what the cut loses.** A selection answers the question you asked. The whole drive sometimes answers a question you didn't think to ask. Step 5 is there to find out whether that happened to you.

---

## Setup

```bash
git clone https://github.com/andrebarros6/learning-log-05-context-engineering
cd learning-log-05-context-engineering
```

Open [claude.ai](https://claude.ai) in a browser or the desktop app. **Write down which model you're using** at the top of [LOG.md](LOG.md), and use the same one throughout.

What's in the repo:

| Path | What it is |
|---|---|
| [`prompt.md`](prompt.md) | The task prompt. Paste it as it is, every time. **Don't edit it.** Only the context changes in this exercise |
| [`emails/`](emails/) | The three emails to answer |
| [`drive/`](drive/) | Torrefação Lume's shared drive: eleven files, some current, some not |
| [`whole-drive.md`](whole-drive.md) | Every file in `drive/` joined into one, for step 1 |
| [`selected/`](selected/) | Where your selections go |

## Run it

### 1. The whole drive

For each email in `emails/`:

1. **Open a fresh chat.**
2. Attach or paste [`whole-drive.md`](whole-drive.md) first. Then, in the same message, paste `prompt.md` and the email.
3. Score the reply against the checks in [TASK.md](TASK.md). Fill in the **Whole drive** column of the scoreboard in LOG.md.
4. Copy anything the reply says *beyond* the answer (a note to Inês, a warning, a question) into table 4 of LOG.md.

Three chats. These are long messages. If your plan hits a usage limit, wait and carry on later; the exercise doesn't need them in one sitting.

### 2. Select

For each email, open the files in [`drive/`](drive/) and decide what the email actually needs. Copy only that into `selected/01-cafe-ponte.md`, `02-return.md` and `03-ponte-nova.md`. You can take a whole file, a section, or a few rows of a CSV.

Fill in table 3 of LOG.md as you go: every file in the drive, kept or dropped, and **why**. "Not relevant" isn't a reason. "Superseded by the October terms" is.

Then fill in table 1 with the word counts. In VS Code, select the text and the status bar shows the count. Or in a terminal: `wc -w whole-drive.md selected/*.md` (PowerShell: `Get-Content selected\01-cafe-ponte.md | Measure-Object -Word`).

### 3. The selection

Same as step 1, three fresh chats, but attach your `selected/` file instead of the whole drive. Same `prompt.md`, same email. Fill in the **Selected** column.

### 4. Compare

Fill in the rest of LOG.md:

- **Size:** how much smaller was what you sent?
- **Answers:** did any check change between the two columns, in either direction?
- **What the cut couldn't see:** go back to table 4. Is there anything there that the selected replies couldn't have said, because the evidence for it was in a file you dropped? Was it worth knowing?

**If your plan lets you pick a model**, run step 1 again on the smallest one available. That's where the whole drive tends to hurt.

## Checking your work

There's no `pytest` here. The check is your log against the solution branch:

```bash
git checkout solution
```

`ANSWER-KEY.md` has the right answer to each email and the trap in it, which drive files each one needs, and the selections that are defensible either way. `selected/` has mine. `SOLUTION.md` has my runs on three models.

**Look hardest at table 3.** Two selections can both get every answer right, and one of them can still have dropped the file that would have warned Inês about something.

## Bring your own context

Inês's drive is scaffolding. **The exercise is the largest prompt in your own work**: the one where you paste a whole document, a whole thread or a whole folder because it's easier than choosing.

Do it after the solution, because your own material has no answer key:

1. Run it as you do now, and keep the reply.
2. Cut it by half. Write down what you dropped and why.
3. Run the cut version. Compare the replies, and read the first one again for anything the second couldn't have said.

Put your own material in a `mine/` folder. It's gitignored. Don't commit real documents to a public repo.

---

## Questions, corrections, things that broke

[Discussions on the hub repo](https://github.com/andrebarros6/learning-log/discussions) are one place for all exercises.

Found a step that's gone stale because a tool changed? Open an issue here. Corrections are genuinely welcome; things breaking in public is the format.

## Licence

MIT. See [LICENSE](LICENSE). The exercise is yours to keep.
