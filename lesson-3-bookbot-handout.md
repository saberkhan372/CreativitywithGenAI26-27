# Lesson 3 — BookBot: Generating From Counts

**Working with Gen AI · Unit 1 · 70 minutes · unplugged, no computers**

Name: `______________________________`  Book / passage: `____________________`  Date: `__________`

---

## Today's question

**If a machine has no rules at all — only a record of which words actually followed
which — what can it produce?**

By the end of today you can: build a probability distribution from counts; generate
text by sampling from it; and explain why fluent output is not accurate output.

---

## Part A — Warm-up (8 min) · no writing implements down yet

On the board: **"The cat sat on the ________"**

Everyone writes **one** word. No conferring.

My word: `________________`

Now the tally goes on the board.

| Word | Tally | Count |
|---|---|---|
| mat | | |
| floor | | |
| couch | | |
| | | |
| | | |

**Two questions before we move on:**

Which word won, and did anyone pick something nobody else did? `_____________`

Where did your word come from — a rule you followed, or things you have read
before? `_________________________________________________________________`

> **That tally is a probability distribution.** You just built one out of a room.
> BookBot builds one out of a book.

---

## Part B — Build the table (20 min)

Take your assigned passage. Pick a **starting word** that appears at least four times.

**For every place your word appears, write down the word that comes next.** One tally
mark each. Do not skip repeats — repeats are the entire point.

**Current word:** `________________`

| Word that followed | Tally | Count |
|---|---|---|
| | | |
| | | |
| | | |
| | | |
| | | |
| | | |

**Total tally marks (N):** `______`

---

## Part C — Generate (18 min)

### The sampling rule — read this carefully

You must pick a next word **in proportion to its count.** A word tallied 5 times must
be five times likelier than one tallied once. Anything else throws away the
distribution you just built.

**Method 1 — The word jar (exact, use this first).**
Write **one slip per tally mark.** A word tallied 5 times gets 5 slips. Fold them,
put them in the cup, draw one without looking, then **put it back.**

**Method 2 — d20 with re-roll (faster once you trust it).**
Number your tally marks 1 to N. Roll the d20. If it lands above N, **roll again** —
do not adjust, do not round. Re-rolling is what keeps the proportions honest.

> ⚠ Never "give the top word two numbers and everyone else one." That replaces your
> counted distribution with an invented one, and the counting was the whole exercise.

### The Rolling Rule

The word you just drew becomes your **new current word.** Go back to the passage,
build a **new** table for *that* word, and draw again.

Yes — a new table every single word. Notice how much work one word costs.

**Generate 8–12 words. Write the sentence exactly as it comes out.**

`_________________________________________________________________________`

`_________________________________________________________________________`

**How many tables did you build?** `______`  **Roughly how long did that take?** `______`

---

## Part D — Reflection and submission (12 min) · before you leave

**Circle one in each row.**

| Prompt | | | |
|---|---|---|---|
| My sentence read as… | fluent and sensible | fluent but wrong | not fluent |
| The words came from… | my judgment | the counts | the counts, but I nudged it |
| A longer passage would make output… | more fluent | more accurate | both | neither |

**One bounded claim.** Your table and your generated sentence are the evidence.

> I observed `______________________________________________________`
>
> My evidence is `____________________________________________________`
>
> This suggests `_____________________________________________________`
>
> but it does not establish `___________________________________________`

**Authorship line.** BookBot has no author and no intent. When your sentence sounded
meaningful, who supplied the meaning?

`_________________________________________________________________________`

### Submit to Google Classroom

1. Photo showing your **Part B table** and your **generated sentence**
2. Filename: `Lastname-Lesson3.jpg`

---

## The sentence to carry out of this room

> **Fluency is not accuracy.**

BookBot cannot be right or wrong, because it is not making claims. It is drawing
slips out of a cup. It produces sentence-shaped output because the counts came from
sentence-shaped input.

Hold on to that. Everything you meet from here on is doing a version of this with
more data than any person could count — and it will sound far more confident.

---

## Next time — Explore LLMs

You have now built the toy version by hand. Next: the real thing, several of them,
given the **same task**.

Same prompt. Different models. You log every output verbatim and find out which
differences are real and which you are imagining.

**Bring:** this handout, a laptop, and a task you actually care about getting done.
