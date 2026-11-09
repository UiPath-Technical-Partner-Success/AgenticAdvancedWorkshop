# Participant's Handbook

**Thank you for joining the UiPath Advanced Agentic Automation Course!**

This handbook is your practical guide for the hands-on exercises. It walks you through each step,
explains what's happening and why, and helps you build something real by the end of the session.

---

!!! tip "Training Environment"
    - **Platform:** [**cloud.uipath.com/tpenlabs**](https://cloud.uipath.com/tpenlabs/AgenticAdvancedWorkshop/)
    - **Tenant:** ***AgenticAdvancedWorkshop***

Work inside your workshop VM, and make sure the **AgenticAdvancedWorkshop** tenant is selected in the top right
corner before you start. If you can't reach the environment, raise a hand.

## What You'll Build

This course has two exercises. Each one starts with its own setup lesson, so you can begin with
either.

### 1. First Notice of Loss Agent

An insurer receives a **First Notice of Loss (FNOL)** claim together with the homeowner's policy it
refers to. You'll have Codex build a low-code agent in **Studio Web** that reads both PDFs, runs
five eligibility checks, and returns a decision, an escalation flag and a summary.

Then you'll turn a set of test documents into an evaluation set and let Codex run the loop: run the
evaluations, find what fails, fix the prompt, and run again until the scores hold.

[Start First Notice of Loss Agent →](getting-started/index.md)

### 2. Support Ticket Triage

You'll build a support-ticket triage automation for HomeFix in **Maestro Flow**, with **Codex**
doing the building. An inline agent classifies each ticket and drafts a reply grounded in the
HomeFix knowledge base, and a human reviews the draft in **Action Center**.

Then you'll do the part that matters: feed your review decisions and trace feedback back to Codex,
and let it build a second and third version that route urgent tickets, drop noise, and finally
auto-resolve the safe cases. Six prompts, three versions, one scoreboard.

[Start Support Ticket Triage →](support-ticket-triage/index.md)

**Use the navigation at the top to access the lessons!**

---

!!! info "Something worth holding onto as you work through the exercises"
    The workshop is not "build a flow". It's an improvement cycle: run real examples, collect human
    review decisions, leave trace feedback, revise, and add automation only where the evidence
    supports it.
