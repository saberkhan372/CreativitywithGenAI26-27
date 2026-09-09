# Unit 1 — How Machines Handle Language

**Working with Gen AI · 2026–27 · Saber Khan**
Five 70-minute blocks. Rebuilt 2026-09-09.

---

## The arc

Each lesson hands the next one its question.

| # | Lesson | Mechanism on the table | The question it leaves open |
|---|---|---|---|
| 1 | **Conventions: CS vs ML** | Humans write rules | What if the rules were *all* there was? |
| 2 | **ELIZA** | Rules only — no learning | Rules feel like understanding. What would counts do instead? |
| 3 | **BookBot** | Counts → probability, sampled | This is tiny. What happens at scale? |
| 4 | **Explore LLMs** | Learned prediction at scale | Which differences are real, and how would we know? |
| 5 | **Project + Poster** | Student-designed investigation | — |

The spine: **rules → counts → learned prediction**, with *fluency is not accuracy*
carried across all five.

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
articulated that they directed the model. Each lesson ends with a version of
*"name one thing the machine chose that you overrode."*

---

## The one sentence stem, used all five days

> I observed ______. My evidence is ______. This suggests ______,
> but it does not establish ______.

Students should be sick of it by Lesson 5. That is the point — the fourth clause is
the one that makes a claim honest, and it is the one that does not come naturally.

---

## Files

| Lesson | Handout | Deck |
|---|---|---|
| 1 | `lesson-1-conventions-handout.md` | `lesson-1-conventions-slides.html` |
| 2 | `lesson-2-eliza-handout.md` | `lesson-2-eliza-slides.html` |
| 3 | `lesson-3-bookbot-handout.md` | `lesson-3-bookbot-slides.html` |
| 4 | `lesson-4-explore-llms-handout.md` | `lesson-4-explore-llms-slides.html` |
| 5 | `lesson-5-project-poster-handout.md` | `lesson-5-project-poster-slides.html` |

**Handouts** are Markdown sized to two printed pages. Print at 100%, double-sided.

**Decks** are self-contained HTML — one file each, no build step, no server.
Double-click to open. Each is a fixed 1920×1080 canvas scaled to the projector,
matching the canonical deck's visual language (cream `#f5ead8`, clay `#c67139`,
olive `#7a8a5e`, Fraunces + Figtree).

**Deck controls:** `→` / `←` or click to advance · `N` toggles facilitator notes ·
`F` fullscreen · `Home` / `End` jump to first / last.

Fonts load from Google Fonts when online and fall back to Georgia / system sans
offline. Nothing else is fetched; no analytics, no storage, no student data.

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
to teach. Lesson 3 replaces it with two methods that preserve the counted weights
exactly: a **word jar** (one paper slip per tally mark, drawn and replaced) and a
**d20 with re-roll** (number the marks 1–N; if the roll exceeds N, roll again — never
adjust or round). Temperature is introduced later as a deliberate distortion of a
distribution students have already built honestly.

### One caution that must be said aloud, not just known

Lesson 2 compares ELIZA to a modern LLM. A camp participant flagged that this
comparison can imply an LLM would make a better therapist or confidant. The
anthropomorphism and sycophancy caution is written onto the slide and into the
handout. Do not skip it.

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
