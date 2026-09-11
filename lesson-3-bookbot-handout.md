# Lesson 3 — BookBot

**Working with Gen AI · Unit 1 · 70 minutes**
**Materials: this book, paper, a pencil. Nothing else.**

> **Reference sheet.** The lesson runs on the board and on your own paper. This is
> here to look things up — not to fill in.

---

## Today's question

**If nobody writes a single rule about what to say — only a record of which words
actually followed which — what can a machine produce?**

---

## Our whole book

Six lines. That is the entire library.

```
1.  the robot paints a moon .
2.  the robot paints a star .
3.  the robot folds  a map .
4.  the fox   paints a moon .
5.  the fox   folds  a map .
6.  the robot paints a moon .
```

**Rule 1 — Count every time, including repeats.** Line 6 repeats line 1. That repeat
is not a mistake to tidy up. It *is* the pattern.

**Rule 2 — The period counts as a word.** It is how you know when to stop.

**Never count across a line break.** Line 1 does not hand anything to line 2.

### Matching lists — every next word, repeats kept

Built from the six lines above. Repeats are left in on purpose: they *are* the counts.

| Current word | Every word that follows it, in book order |
|---|---|
| `the` | robot, robot, robot, fox, fox, robot |
| `robot` | paints, paints, folds, paints |
| `fox` | paints, folds |
| `paints` | a, a, a, a |
| `folds` | a, a |
| `a` | **moon, star, map, moon, map, moon** |
| `moon` | . , . , . |
| `star` | . |
| `map` | . , . |

Check the `a` row against your own table in Step 2. They should match.

---

## Step 1 — Warm-up

On the board: **"the robot paints a ______"** — one word each, no conferring.

That tally is a **distribution.** Nobody wrote a rule. You counted what people
actually said.

---

## Step 2 — Count one table

Find every `a` in the book. Tally the word that comes next.

| Word after `a` | Tally | Count |
|---|---|---|
| | | |
| | | |
| | | |

**This is all the counting you do today.**

---

## Step 3 — Walk the sentence

**The only rule: always take the word that appears most often.**

Start at `the`. Find its row in the matching lists. Whichever word appears most times
in that row — write it down. Then jump to *that* word's row and do it again. Stop when
you write the period.

`the` → `________` → `________` → `________` → `________` → `.`

No dice. No choosing. The counts decide every word.

---

## Step 4 — The catch

Everyone in the room wrote the same sentence.

It is **line 1** of the book. It is also line 6 — the sentence the book repeats. The
most likely sentence turned out to be the most repeated sentence.

Run it again and you get the same sentence. And again.

**It can only ever make one.**

**What would it need in order to write a different one?**

`_________________________________________________________________________`

Look at the `a` row again: **moon, star, map, moon, map, moon**. Greedy takes `moon`
every time. But `star` and `map` are sitting right there, in proportion.

*(Hold that thought. Choosing among them instead of always taking the top one is where
Unit 2 starts.)*

### If you finish early

Tear the six words of the `a` row into six slips. Draw one without looking, then put
it back. Do that ten times and tally what you get. How close is it to 3 / 2 / 1?

---

## Where the skew came from

Why does `moon` win? Not because it is a better word — because it is in the book
**three times out of six.** That is the whole reason.

In week 1 some of you said you would train a cat detector on *"the same cat a million
times"*, and others said *"keep the cat in the middle"* of every photo.

| That choice | What it actually learns |
|---|---|
| The same cat, a million times | **That cat.** Not cats. |
| Every cat centred | Cats are in the middle. A cat at the edge? Unknown. |

**What goes in decides what comes out.**

---

## The sentence to carry out of this room

> **Fluency is not accuracy.**

BookBot can easily produce a false sentence. What it cannot do is *check* — it has no
way to compare anything against the world. It counts and picks, and it sounds like
language because the counts came from language.

Everything you meet from here is doing a version of this with more data than any
person could count — and it will sound far more confident.

---

## Reflection — before you leave

**Circle one in each row.**

| Prompt | | | | |
|---|---|---|---|---|
| My sentence read as… | fluent and sensible | fluent but hollow | not fluent |
| The words were chosen by… | me | the counts | both |
| A bigger book would make the output… | more fluent | more accurate | both | neither |

**One bounded claim.** Your table and your sentence are the evidence.

> I observed `______________________________________________________`
>
> My evidence is `____________________________________________________`
>
> This suggests `_____________________________________________________`
>
> but it does not establish `___________________________________________`

**Authorship line.** BookBot has no author and no intent. When your sentence sounded
meaningful, **who supplied the meaning?**

`_________________________________________________________________________`

### Classroom — transfer, attach, turn in

**Thinking:** copy your three circles and your claim into the Classroom response box.

**Evidence:** attach one photo of **your own paper** showing your table, your sentence,
and your claim together.

Filename `Lastname-U1D3`. **Open the attachment to check it is readable, then turn in.**

---

## Next time — Explore LLMs

You built the toy by hand. Next: the real thing, several of them, given the same task.

**Bring:** a laptop and a task you actually care about getting done.
