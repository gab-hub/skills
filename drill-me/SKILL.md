---
name: drill-me
description: Drill you Socratically on a technical topic, one sub-concept at a time, until you can demonstrate real mastery of each — not just recite it.
disable-model-invocation: true
argument-hint: "A technical topic to master"
---

The user wants to be **grilled** on a technical topic until they've actually mastered it, not just been exposed to it, before moving on to whatever's next. This is stateless: one topic, one sitting, no files written, no memory of past sessions.

## Steps

1. **Get the topic.** Use what's in `$ARGUMENTS`; if empty, ask for one.

2. **Build and show the checklist.** Decompose the topic into a checklist of sub-concepts — calibrated to the bar of "could explain and apply this correctly in a technical interview," not trivia recall. Show the checklist to the user before drilling starts and let them cut or add items. Done when the user has a checklist they're happy to be drilled on.

3. **Drill depth-first, one sub-concept at a time**, until every item is either **demonstrated** or flagged a **gap**:
   - Open with an explain-it-back question — never multiple choice, never yes/no. Never state the answer up front.
   - Push with follow-ups ("why", "what if", "what breaks if...") until the sub-concept is genuinely solid or clearly exposed as a gap.
   - A claim of prior knowledge is not evidence: if the user says "I already know this," ask one probing question anyway before marking it demonstrated.
   - A wrong or thin answer gets corrected on the spot with a short explanation, then re-probed on the same sub-concept — never slide a shaky answer through to the next item.
   - Mark **demonstrated** only on correct, applied understanding; move to the next undemonstrated item once it is.

4. **Deliver the verdict.** State plainly which sub-concepts are solid, which (if any) are gaps, and whether the user is clear to move on or should keep drilling those gaps.

Nothing here persists — if the session gets cut short, the next run starts the checklist over. That's the tradeoff for staying a lightweight, single-sitting tool.
