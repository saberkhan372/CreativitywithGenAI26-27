# Lesson 3 — BookBot + the Toy language model

**Working with Gen AI · Unit 1 · 70 minutes (planning allocation)**

## Ready for class

- [Slides](lesson-3-bookbot-slides.html)
- [Student activity: two printable pages and copyable corpus](lesson-3-bookbot-activity.html)
- [Robot Garden corpus](bookbot-corpus.txt)
- The Day 3 pages of [the combined booklet](handouts.html) contain the same student activity.

## Learning question

How can the same collection of words produce different writing—and what makes an output worth keeping?

Students count next-word occurrences, follow a greedy selection rule, compare repeated generations while changing temperature, and explain a creative decision using the output as evidence.

## Before class

Use a laptop per pair, paper and pencils.

**Decide the access route tonight, on a student device if possible.** Two options on [Machine Learning for Kids](https://machinelearningforkids.co.uk):

- **Try it now** (Get started → Try without registering). No accounts; the site says these projects are deleted after at least four hours. On 2026-09-14 this button stayed greyed out in Claude's embedded browser, so test it in the browser students will use.
- **Class login** through your teacher account, if student logins already exist. Do not schedule account creation inside this lesson.

Then rehearse: **generating text** project → **Toy** → paste Robot Garden → smallest context → top-p at the high end → starting text `the robot`. Keep the duplicate line. Confirm it generates. No Small/Large model downloads.

If the tool says the prompt needs more words, return to the smallest context and restore the start. If it stays blocked, use a teacher demonstration or the paper route below.

**How students reach the corpus:** the Copy button on the activity page needs the page served over the web. If students open it from a Drive or Classroom preview and Copy does nothing, they open [bookbot-corpus.txt](bookbot-corpus.txt), select all and copy.

**Expect loops.** In Robot Garden, `silver` and `paper` each follow `a` six times. A most-common-word walk from `the robot` loops: *the robot paints a silver moon above the robot paints a silver moon above…* (hand count by word; the Toy may split text slightly differently). Tell students before the experiment that a loop is evidence, not a broken tool.

Prepare one teacher example with the six-line book if useful for the transition. Then switch explicitly to Robot Garden for the shared experiment. The longer corpus is fictional text authored for this activity with AI assistance. No private details or student writing are needed.

## Timing

| Minutes | Activity |
|---|---|
| 5 | Warm-up: tally the room's completions |
| 12 | Six-line book, one tally and greedy walk |
| 5 | Why did the same sentence repeat? |
| 8 | Toy model setup and shared corpus |
| 20 | Temperature comparison and evidence capture |
| 8 | Artwork title: keep, edit or replace |
| 7 | Reflection and Classroom submission |
| 5 | Setup and transition buffer |

Total: 70 minutes. These are proposed allocations, not measured classroom runtimes. The final preview fits inside the closing block.

## 1. BookBot: count and walk

Warm-up: complete **the robot paints a ____**, then tally the actual class answers.

Our whole book:

```
the robot paints a moon .
the robot paints a star .
the robot folds  a map .
the fox   paints a moon .
the fox   folds  a map .
the robot paints a moon .
```

Count repeats, treat the period as a token, and never count across line breaks. Count what follows `a`: **moon 3, map 2, star 1**. Use the matching lists on the student activity to walk from `the`, always choosing the most common next word. Stop at the period.

**Answer:** `the robot paints a moon .`

With this book, starting word and greedy rule, the result repeats. This does not mean every model can produce only one sentence, or that greedy selection always finds the most probable whole sentence. The unused `fox` row has a tie; our specified start avoids it.

Transition: **We always picked the most common next word. What happens if other words get a chance? The computer will do the counting; we will investigate the choices.**

## 2. Shared setup

Use Robot Garden in the Toy model. A corpus is the source text. The smallest context uses a short preceding sequence; begin there. The start is **the robot**, without quotes or a final period. This is text continuation, not a chatbot instruction.

Keep top-p at the high end throughout the required experiment. Explain briefly that it limits candidate choices; investigating it is for another day. The Toy model counts word sequences. Modern neural language models use learned parameters. This activity illustrates a related prediction-and-selection process, not their exact implementation.

## 3. Temperature experiment

Pairs predict first. Keep corpus, starting text, context and top-p unchanged.

- **A:** temperature toward low; three runs at that setting.
- **B:** temperature toward high; three runs at that setting.

No numbers on the slider? About a quarter of the way for A, three-quarters for B. Screenshot both settings. Restore `the robot` before every generation.

**Screenshot every run.** For A1 and B1 only, students also copy the first **10 generated words** by hand, excluding the starting text. Other runs get the screenshot name in the table. This keeps the 20 minutes on comparing rather than copying. Keep repeats and label errors as errors.

Look for repetition, surprising combinations, and phrases that could serve a purpose. Lower temperature generally favors common candidates more strongly; higher temperature gives less-common candidates more chance. It does not guarantee better creativity, factual accuracy, or a different output on each run. Three runs per condition support a small initial comparison, not a general claim about all models.

## 4. Creative decision

Imagine an artwork: **a robot's nighttime garden**. Choose one generated phrase as its title. **Keep, edit, or replace** it. Retain the original phrase, record the final title, and explain how the choice serves the artwork. Every student makes their own decision, including when observing a partner or demonstration.

## 5. Reflection and submission

> I changed ____ and kept ____ fixed. I observed ____. My evidence is ____. This does not establish ____.

Ask: **What did you decide that the model did not?** People supplied the corpus and procedure; the student chose settings and selected or revised a title. Do not call the process authorless.

**Classroom:** a photo of both activity pages, the A/B settings screenshots and run screenshots; type the final title and claim in the submission. Filename `Lastname-U1D3`. Use the existing assignment; nothing is posted by these materials.

## Paper route if access fails

Use the six entries after `a`: moon, star, map, moon, map, moon. Make six equal-sized slips. Condition A selects the most common word three times; condition B draws a slip without looking, replaces it, mixes, and repeats three times. Record each word in A1–B3 and label the route **paper selection comparison**. Use one result to make a title and complete the same reflection.

This compares greedy selection with sampling. It does **not** test the website's temperature control, and six choices cannot establish the distribution. No slips available: record a partner or teacher demonstration. An unchanged output is a valid result.

## Optional extension

After the required log, change context alone while holding temperature, top-p and corpus fixed. Use the same sufficiently long source phrase in both conditions, for example `the robot paints a silver moon`. Record separately. More exact context can lead to more direct copying with a small corpus; it does not guarantee better original writing.

## Next lesson

Today: one model with different settings. Next: the same task with different models. Bring a task and describe what a useful result would look like.

## Teacher references

- [Dale Lane: Toy model walkthrough](https://dalelane.co.uk/blog/?p=5538)
- [Dale Lane: classroom sequence and device considerations](https://dalelane.co.uk/blog/?p=5847)

Current access, generation and clipboard behavior need checking in the classroom browser.
