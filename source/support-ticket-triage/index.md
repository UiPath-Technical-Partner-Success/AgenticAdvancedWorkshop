<!-- Source: coding-agents-workshop-building-a-continuous-improvement-loo-steps.pdf, rebuilt from the PDF content streams. <<IMG:n>> = staging/pdf-images/NN.jpg. -->

## 1. What you'll build (read first)

In this workshop you build a support-ticket triage automation in UiPath Maestro Flow, with Codex doing the building. A ticket arrives as flow input. An inline agent classifies it and drafts a reply grounded in the HomeFix knowledge base. A human reviews the draft in Action Center and approves, edits, or rejects it. You then feed your review decisions and trace feedback back to Codex, and it builds a second and third version that route urgent tickets, drop noise, and finally auto-resolve the safe cases. Three things work together

- Codex as the agent running the terminal: it reads files, edits flow definitions, runs the UiPath CLI, queries the tenant, and reports results.

- Maestro Flow orchestrating an inline agent, a knowledge index, and a human task side by side.

- An improvement loop driven by evidence: run real tickets, collect human decisions, leave trace feedback, revise, and add automation only where the evidence supports it. What you will touch today

- A Maestro Flow solution named triage- plus your username, for example triage-user24, with three flows: triage-user24v1, triage-user24v2, and triage-user24v3.

- The shared SupportKB knowledge index in the Shared folder.

- Action Center review tasks assigned to you, with outcomes Approve, Modify & Send, and Reject.

- Trace feedback on weak runs, and a final V1/V2/V3 scoreboard. How the prompts work Every prompt in this workshop is typed exactly as written. There are six of them, plus one word to release the final batch. Codex looks up your username, email, and tenant itself, so the same text works for everyone in the room. Your team code is triage- plus your username, the part of your email before the first underscore. A login of user24_internaltestfusion20ymux5i@uipathstaging.onmicrosoft.com gives triage-user24. Codex derives it for you in the next prompt, so you never type it. Expect a loop, not a single prompt: build V1, run test tickets, review tasks, leave feedback, ask Codex to infer weaknesses, build V2, run a second ticket set, complete tasks, build V3 with safe automation, run final tickets, compare results.
