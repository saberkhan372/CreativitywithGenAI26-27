# Unit 1 — How Machines Handle Language

**Working with Gen AI · 2026–27 · Saber Khan**
Five 70-minute blocks. Rebuilt 2026-09-09.

---

## The arc

Each lesson hands the next one its question.

> **Lessons 1 and 2 are written from what actually happened** (first taught
> 2026-09-09). Lesson 1: the cat problem, Bletchley Park and Turing, a first look at
> ELIZA, then Teachable Machine — no worksheet used or needed.
>
> **Lesson 2 was rewritten after reading the cohort's ELIZA responses.** The original
> asked students to record replies that "felt human." Not one of eight reported
> feeling understood — they diagnosed the mechanism and several called it pointless.
> The lesson now asks the better question: why did it fool people in 1966 when it
> plainly does not fool you? That leads straight to sycophancy in modern systems,
> which is where the caution actually bites.

| # | Lesson | Mechanism on the table | The question it leaves open |
|---|---|---|---|
| 1 | **Who writes the rules?** | Cat problem · Bletchley Park · ELIZA · Teachable Machine | If rules can look like understanding, what counts as evidence? |
| 2 | **Why did ELIZA ever work?** | Reply rules a person wrote | If rules fool people but not you, what fools *you*? |
| 3 | **BookBot** | Counted continuations + one rule for choosing | It can only make one sentence. What is missing? |
| 4 | **Explore LLMs** | Learned prediction at scale | Which differences are real, and how would we know? |
| 5 | **Project + Poster** | Student-designed investigation | — |

The spine, stated precisely: **hand-written reply rules → counted continuations plus a
selection rule → predictions from learned parameters.** Each step removes a little more
hand-written instruction about what to say — none of them removes rules altogether.
*Fluency is not accuracy* runs across all five.

---

## Every lesson has the same four parts

1. **Warm-up** — a question or discussion, 8 min. Nothing technical. Journals open, laptops closed.
2. **Lesson / activity** — 40 min.
3. **Reflection + Classroom submission** — 12 min, *in class, before anyone leaves.*
4. **Preview** — 5 min. Name the question the next lesson answers.

Remaining 5 min is transition slack.

---

## Four design rules, and why

These come from an analysis of the full 2025–26 student corpus (kept private — it
contains student work). The finding that drove this rebuild: across five
investigation labs, every student filled in 0–2 of 5 worksheets while completing
every making activity. The capture failed, not the activities.

**1. The analysis lives inside the artifact.** No separate worksheet to abandon.
The poster carries the claim and its evidence; the submission photo carries the tally.

**2. Three forced choices plus one written claim.** Not twelve open questions.
Circling takes 15 seconds and is still analyzable. Exactly one question needs prose.

**3. Capture during, not after.** Submission happens in the room while the surprise
is fresh — never as homework.

**4. Authorship gets named out loud, every time.** Last year only 25% of students
articulated that they directed the model. Every lesson ends with an authorship line,
and Lesson 4 makes it a judged decision — **keep, change or reject** against a goal the
student writes down first. All three count as authorship if they can defend the call.

---

## The one sentence stem, used all five days

> I observed ______. My evidence is ______. This suggests ______,
> but it does not establish ______.

Students should be sick of it by Lesson 5. That is the point — the fourth clause is
the one that makes a claim honest, and it is the one that does not come naturally.

---

## Files

| Lesson | Reference handout (Markdown) | Deck |
|---|---|---|
| 1 | `lesson-1-conventions-handout.md` | `lesson-1-conventions-slides.html` |
| 2 | `lesson-2-eliza-handout.md` | `lesson-2-eliza-slides.html` |
| 3 | `lesson-3-bookbot-handout.md` | `lesson-3-bookbot-slides.html` |
| 4 | `lesson-4-explore-llms-handout.md` | `lesson-4-explore-llms-slides.html` |
| 5 | `lesson-5-project-poster-handout.md` | `lesson-5-project-poster-slides.html` |

**Printable worksheets** live in `handouts.html` — all five lessons, **two pages each,
ten pages total.** Fixed 8.5×11in page boxes, so pagination is deterministic rather than
renderer-dependent. Print at 100%, double-sided, no scaling. Measured in a browser:
every sheet's content fits inside its box, the tightest with about 30px to spare.

The per-lesson `*-handout.md` files are the **fuller reference version** — the same
material with the surrounding explanation, readable on GitHub. Students do not need
either one to take part; nothing in any submission requires a handout.

**Poster templates** (`poster-templates.html`) hold the blank six-zone layout and the
two worked examples used in Lesson 5's warm-up.

**Decks** are self-contained HTML — one file each, no build step, no server.
Double-click to open. Each is a fixed 1920×1080 canvas scaled to the projector,
matching the canonical deck's visual language (cream `#f5ead8`, clay `#c67139`,
olive `#7a8a5e`, Fraunces + Figtree).

**Deck controls:** `→` / `←` or click to advance · `N` toggles facilitator notes ·
`F` fullscreen · `Home` / `End` jump to first / last.

Fonts load from Google Fonts when online and fall back to Georgia / system sans
offline. Nothing else is fetched; no analytics, no storage, no student data.

**Images** live in `img/` and are bundled rather than hot-linked, so the decks work
with no network in a classroom. All are Wikimedia Commons, public domain or CC BY-SA,
attributed on the slide that uses them and again on a credits slide at the end of each
deck. Terms and source links: [`img/CREDITS.md`](img/CREDITS.md).

---

## Source material this rebuild draws on

The 2025–26 course handouts were the starting point, not discarded:

- `ELIZA Investigation Handout (Unplugged + Web).docx` — Parts A/B/C structure and
  the "ELIZA moves" vocabulary carried over nearly intact; it was already good.
- `Bookbot2.0 student-facing.docx` — activity retained, **sampling method changed**
  (see Lesson 3 note below).
- `Gen AI - First Project - Explore LLMs (Day 1).docx`
- `Gen AI Project 1 — Local LLM Lab Poster (Day 2/Day 3).docx`

### One deliberate fix

`FINDINGS-2026-08-12.md` §4.3 flagged that BookBot's dice rule — *"give the most
common option 2–3 numbers … adjust so it still totals 6"* — substitutes an arbitrary
distribution for the counted one, quietly destroying the concept the activity exists
to teach. Lesson 3 now avoids the problem differently: there is **no randomiser at all.** The rule
is "always take the word that appears most often," which needs nothing but paper and a
pencil and is deterministic — every student gets `the robot paints a moon .`, so it is
checkable in ten seconds. Sampling returns in Unit 2 as temperature, set up by Lesson 3's
closing question: the machine can produce exactly one sentence, so what is missing?

An optional slips exercise for early finishers turns the `a` row into a real sampling
demo without adding a required step.

### One caution that must be said aloud, not just known

Lessons 1 and 2 both put ELIZA next to a modern chatbot. A camp participant flagged
that this comparison can imply an LLM would make a better therapist or confidant. The
anthropomorphism and sycophancy caution is written onto the slide and into the handout
in **both** lessons. Do not skip it, and name real people at school when you say it.

---

## Relationship to the existing semester plan

The prior 2026–27 semester plan scheduled these dates as Human as Model → Tokens →
Temperature → Same Task Different Models → AI for Real Work → Mini-Case Study.
**This unit replaces that sequence.** That plan has not been edited; reconcile the
two before publishing a calendar to students.

Concepts from the old sequence that are preserved here: next-token prediction
(Lesson 3), controlled comparison (Lessons 4–5), the seven-step investigation cycle
(Lesson 5), and the lightweight reflection stem (all five).

Concepts deferred: tokenization and temperature as a formal one-variable
investigation. Both now land in Unit 2 with more grounding behind them.
