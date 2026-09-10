# Lesson 3 — BookBot: Generating From Counts

**Working with Gen AI · Unit 1 · 70 minutes · unplugged, no computers**

Name: `______________________________`  Partner(s): `__________________`  Date: `__________`

---

## Today's question

**If a machine has no rules at all — only a record of which words actually followed
which — what can it produce?**

By the end of today you can: build a probability distribution from counts; generate
text by sampling from it; and explain why fluent output is not accurate output.

---

## Part A — Warm-up (8 min) · no writing implements down yet

On the board: **"the robot paints a ________"**

Everyone writes **one** word. No conferring.

My word: `________________`

Now the tally goes on the board.

| Word | Tally | Count |
|---|---|---|
| moon | | |
| star | | |
| map | | |
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

### Our tiny book

The whole class uses these six lines. That way every table can be checked.

```
1.  the robot paints a moon .
2.  the robot paints a star .
3.  the robot folds a map .
4.  the fox   paints a moon .
5.  the fox   folds  a map .
6.  the robot paints a moon .
```

**Three rules for counting:**

1. **Count only inside a line.** Never join the end of one line to the start of the
   next. Line 1 does not hand anything to line 2.
2. **The period is its own word.** It can be counted and it can be drawn.
3. **Do not skip repeats.** Line 6 repeats line 1. That repeat is not a mistake to
   tidy up — it is the whole distribution.

### Table 1 — one word of context

**Current word: `a`** — find every `a` and tally what comes next.

| Word that followed `a` | Tally | Count |
|---|---|---|
| | | |
| | | |
| | | |

**Total (N):** `______`

### Table 2 — two words of context

Now do it again, but the current *phrase* is **`paints a`**.

| Word that followed `paints a` | Tally | Count |
|---|---|---|
| | | |
| | | |

**Total (N):** `______`

**Compare the two tables.** What happened to `moon`'s share when you gave the machine
one more word of context?

`_________________________________________________________________________`

> That is what "context" buys. More context, sharper prediction — and it costs you
> a whole new table every time.

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

The word you just drew becomes your **new current word.** Go back to the tiny book,
build a **new** table for *that* word, and draw again.

Yes — a new table every single word. Notice how much work one word costs.

**Start at `the` and generate until you draw a period.** Write the line exactly as
it comes out — including any repeat that looks like it "should" have been different.

`_________________________________________________________________________`

`_________________________________________________________________________`

**How many tables did you build?** `______`  **Roughly how long did that take?** `______`

> **If your line came out identical to line 1 of the tiny book — you did it right.**
> The most likely word wins most of the time, so a sampled run often matches the
> greedy run. Sameness is a real result, not a mistake. Run it a second time.

---

## Part D — Reflection and submission (12 min) · before you leave

**Circle one in each row.**

| Prompt | | | |
|---|---|---|---|
| My sentence read as… | fluent and sensible | fluent but wrong | not fluent |
| The words came from… | my judgment | the counts | the counts, but I nudged it |
| A bigger tiny book would make output… | more fluent | more accurate | both | neither |

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

## Back to the cat question

Why does `moon` win? Not because it is a better word — because it appears **three
times out of six.** That is the whole reason.

In week 1 some of you said you would train a cat detector on *"the same cat a million
times with different backgrounds"*, and others said *"keep the cat in the middle"* of
every photo.

| That choice | What the machine actually learns |
|---|---|
| The same cat, a million times | **That cat.** Not cats. |
| Every cat centred in frame | Cats are in the middle. A cat at the edge? Unknown. |

Your six-line book is the same problem, small enough to see all of it.
**What goes in decides what comes out.**

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
