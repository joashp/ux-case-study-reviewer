# Examples

Calibration for tone, depth and format. Match the shape, not the wording. Do not reuse these example sentences in real responses.

All examples use this weak source paragraph:

> "I redesigned the onboarding flow to be more user-centric and intuitive. I conducted user research and created wireframes, then built a high-fidelity prototype. The new design leverages best practices and was well received."

## /hm
**Reject:**
1. No problem. I never learn what was broken about the old onboarding.
2. Every sentence is a task (research, wireframes, prototype), so I can't tell what you decided.
3. "Well received" by whom? There's no evidence.

**Interview:**
1. You owned research through prototype, which suggests range.
2. Onboarding is a hard problem. If the full write-up has real numbers, I want to hear them.

**30-second skim:** I remember "well received". It's the weakest sentence in the paragraph and almost certainly not the one you wanted remembered.

**Outsider gaps:** What product is this? Who are the users? What does "onboarding" mean here: signup, first task, activation?

## /challenge
You assume the flow was the problem. Maybe users dropped off because the product's value wasn't clear before signup, and no redesign of the flow fixes that. You say "best practices" but don't name one, so I assume you applied generic patterns without testing them against this audience. "Well received" suggests no behavioural measure, so you don't know it worked.

**Steelman of the alternative:** The strongest case for leaving the flow alone is that it was long but familiar. Users had already learned it, and a redesign adds relearning cost for returning users. A targeted fix to the one step that caused drop-off would have shipped faster and risked less. You'd need to show that data pointed to the whole flow, not one step.

## /why
**Steps and assumptions:** You assume onboarding was the cause of churn (unstated), that "intuitive" can be judged without a baseline (unstated), and that the research findings pointed at a redesign rather than a fix (unstated).
1. Why redesign? Because activation was low.
2. Why was activation low? Because users stalled at account setup.
3. Why did they stall there? Because it asked for team details before showing any value.
4. Why did that matter? Because new users hadn't yet decided the product was worth the effort.
5. Why was that the root? Because the flow was ordered around the company's data needs, not the user's first goal.

Root decision: reorder the flow so the user's first goal comes before the company's data collection.

## /tight
> "Onboarding stalled new users at team setup, before they'd seen any value. I moved setup after their first project, and activation rose from 31% to 44% in six weeks."

**Cut:** "I conducted user research and created wireframes, then built a high-fidelity prototype" (a task list, and the result is the point). **Buzzwords replaced:** user-centric, intuitive, leverages best practices (all vague). **Result endings:** every remaining sentence now ends on a reason or outcome.

*(Numbers above are illustrative. Never invent figures in a real response. Use placeholders like "[X%]" and ask the user.)*

## /proof
Missing: any measure of whether the new flow worked. Find: activation rate (share reaching the first key action), time to first value, and step-level drop-off before and after. If analytics aren't available, use usability-test completion rates, or a support-ticket count for onboarding questions across comparable periods.

## /audit
Weakest part: my steelman assumed a "familiar but long" flow. I was guessing, because the text says nothing about the old design. I was most certain about the missing evidence, because that is visible in the text. If I did it again, I'd ask what the old flow looked like before attacking the redesign.
