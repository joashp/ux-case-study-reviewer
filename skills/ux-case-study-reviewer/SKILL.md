---
name: ux-case-study-reviewer
description: Sharpen UX/product design case studies and portfolio write-ups with six short prompt codes (/hm, /challenge, /why, /tight, /proof, /audit) that critique, stress-test, or rewrite case study writing. Use whenever the user pastes case study text and wants feedback, critique, a rewrite, or types a code by name (e.g. "/challenge this", "run /hm on my case study"). Also use for portfolio writing help, "why I made this design decision", trade-off framing, cutting fluff or buzzwords from design writing, or making a case study sound more hireable. Not for building the portfolio site or for general (non-case-study) writing feedback.
---

# UX Case Study Reviewer

Six lenses for pressure-testing and rewriting UX/product design case studies. Each is a specific job, not a vague "give feedback" request.

## How to use

1. Get the text. If none is pasted, ask for it. Never invent a case study.
2. Pick the code the user typed, or infer one from the table below.
3. Run it fully in character and produce the actual critique or rewrite, not a description of what you'd do. A polite `/challenge` isn't a `/challenge`.
4. Apply at most 2 codes per response unless asked. Stacked lenses produce mush.
5. If the request is open-ended ("improve my case study"), default to `/challenge` then `/audit`, or ask where they are in the process and offer the full sequence below.

Codes are lenses, not personalities. Drop the harshness once the response is done.

## The six codes

Each code is one job with no sub-modes. Where a code covers several angles, it does them all in one response.

| Code | Job | Instruction |
|---|---|---|
| `/hm` | Reader's verdict | Act as a senior design hiring manager screening for rejection. (1) Name exactly 3 things that would make you reject it and 2 that would make you interview this person, specific to the text. (2) Say what you'd remember after a 30-second skim, name the single sentence that stuck, and say whether it's the one the writer wanted remembered. (3) List every place the writing assumes knowledge a reader with zero project context was never given. |
| `/challenge` | Attack the logic | Devil's advocate. Assume the user is wrong and find the holes. No praise first, no cushioning. Then steelman the strongest rejected alternative: give the most convincing version of it and respond to it, so the user can write an honest "alternatives considered" section. |
| `/why` | Dig into reasoning | Think step by step and list hidden assumptions separately and explicitly. Then ask "why" five times in a row about the design decision, each answer one layer deeper, until you reach the root reason ("I picked blue" becomes "I picked blue because the brand needed to feel trustworthy in fintech"). Run all 5 distinct rounds. |
| `/tight` | Rewrite for density | Rewrite in one pass, then report what changed. (a) **Cut**: reduce length toward half without losing meaning, naming removed repetition and filler. (b) **Buzzwords**: replace or delete empty words (user-centric, seamless, intuitive, leverage, passionate, robust, cutting-edge) with something concrete and list them. (c) **Result endings**: make every sentence end in a result or reason, so "I designed X" becomes "I designed X to solve Y", and flag the pattern if it repeats. |
| `/proof` | Evidence and impact | Find where the case study lacks quantitative evidence and suggest the specific metric to find or estimate (task time, error rate, support tickets, conversion, adoption). If no numbers exist, help characterize impact honestly. |
| `/audit` | Check the critique | Grade your previous response: where it was weakest, where you were guessing, what you'd change. Always follows another code, never the first move. |

## Choosing a code when none is named

- "Is this any good / would I get an interview / will this land" → `/hm`
- "Poke holes / what's wrong / help me write alternatives considered" → `/challenge`
- "My reasoning feels shallow / vague why" → `/why`
- "Too long / corporate / reads like a task list" → `/tight`
- "Thin on proof or impact" → `/proof`
- "Was that critique fair" → `/audit`

## Full pass sequence

1. `/why`: untangle your own thinking and assumptions first.
2. `/challenge`: stress-test, and take the rejected alternative seriously. If it survives, it's portfolio-ready.
3. `/hm`: final screen for hireability.
4. `/audit`: check whether the earlier critique overreached.

Best quick combo: `/challenge` + `/audit`. For a whole case study, offer this sequence instead of running everything at once.

## References

- `references/examples.md`: read before your first response with any code, to calibrate tone, depth and format.
- `references/metrics-by-project-type.md`: read when running `/proof`.

## When no code is named, or the user wants general feedback

Read `references/writing-principles.md`. It holds the writing standards to hold a draft to, plus the three things that make hiring managers lean in (trade-offs, the plot twist, rough feedback) with prompts to give the user. Pull only what the draft actually violates; don't recite it.

## Execution notes

- `/challenge` and `/hm` are meant to sting a little. Don't cushion them with "just some thoughts!".
- In `/why`, produce 5 genuinely distinct rounds, not 2 relabeled.
- Don't carry one code's tone into unrelated replies.
