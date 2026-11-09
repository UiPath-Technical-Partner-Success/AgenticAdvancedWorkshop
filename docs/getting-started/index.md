# First Notice of Loss Agent

**Use Codex to build an agent that checks an insurance claim against its policy, then prove it works with an evaluation set.**

## Overview

When a homeowner reports damage, the insurer receives a **First Notice of Loss (FNOL)**: the claim form that opens the case. Before anyone assesses the damage, someone has to check the basics:

- Is the policy paid up?
- Is the claimant the policyholder?
- Did the loss happen while the policy was in force?

It's careful, repetitive work, and a mistake here sends the wrong claims forward.

In this exercise you build a low-code agent in **Studio Web** that does those checks, working with **Codex**, a coding agent. You describe what the agent should do and Codex writes it. Then you test it, review the results and decide what to change. The finished agent takes the claim and the homeowner's policy as two PDFs and decides whether the claim is eligible for assessment.

### The five checks

| Check | The question it answers |
| :--- | :--- |
| **Policy status** | Is the policy Current or Paid, rather than Lapsed, Cancelled or Expired? |
| **Identity** | Is the claimant the person named on the policy? |
| **Address** | Do the claim and the policy describe the same property? |
| **Coverage period** | Did the loss happen while the policy was in force? |
| **Filing deadline** | Was the claim filed within 60 days of the loss, or does it explain why not? |

### What the agent returns

- A **yes** or **no** on eligibility.
- A **flag** for claims a person should look at, for example a late claim that explains the delay.
- A short **summary** of the decision in plain language.
- The result of each check as **JSON**. Other apps and agents could read it, so the field names and structure are fixed.

### Why the exercise doesn't stop at a working agent

An LLM doesn't always give the same answer twice. A prompt that works on one sample claim can still trip on a date written day first, or on an explanation hidden in the middle of a paragraph. So once the agent works, you'll give it an **evaluation set**: seven test cases with known answers, one clean claim, one for each check that can fail, and one late claim that a person should review.

Codex then runs the loop on its own: run the evaluations, find what fails, fix the prompt, and run again. It stops when every decision is right, the summary scores 95 or more and the JSON similarity 80 or more, on two clean runs in a row.

### What you will touch today

- A solution called `EligibilityCheck` followed by your first or last name, with an agent called `EligibilityCheckAgent`.
- A sample claim and its policy, plus an offline kit of seven claim and policy pairs for the evaluations.
- An evaluation set called **Eligibility Scenarios**, scored by exact match, JSON similarity, and an LLM judge.

| Step | Focus |
| ---: | :--- |
| [**Connecting to Your Workshop Environment**](1-connect-to-your-environment.md) | Log into the VM and Automation Cloud, and confirm the workshop tenant in Studio Web |
| [**Build, Test and Improve Your First Agent**](2-build-your-first-agent.md) | Start Codex in your working folder, build the agent, create the evaluation set, and run the test-and-fix loop |

!!! tip "Training Environment"
    Log in at **[cloud.uipath.com/tpenlabs](https://cloud.uipath.com/tpenlabs/AgenticAdvancedWorkshop/)** inside your workshop VM and confirm the tenant picker shows **AgenticAdvancedWorkshop** before you start.
