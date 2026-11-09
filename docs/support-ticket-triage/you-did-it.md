# You did it!

!!! tip "Congratulations!"

    You've run a full improvement loop: three versions of a support-ticket triage flow, each one built by Codex from the evidence the previous one produced.

---

## What you built

You started with a flow that sent every ticket to a human, and finished with one that auto-resolves the safe cases, closes noise, escalates urgent tickets, and still sends anything the knowledge base doesn't cover to review. Final scoreboard: 8, then 7, then 3 or 4 review tasks.

| Component | Role |
|-----------|------|
| **Codex** | Built, validated, uploaded, ran, and reviewed every version from the terminal |
| **Maestro Flow** (V1, V2, V3) | Orchestrated the inline agent, the knowledge index, and the review task |
| **Inline agent** | Classified each ticket and drafted a reply |
| **SupportKB** (Context Grounding) | Grounded every draft in the HomeFix help articles |
| **Action Center** | Review tasks with Approve, Modify & Send, and Reject outcomes |
| **Trace feedback** | Recorded what was weak in individual V1 runs, as evidence for V2 |
| **Run manifest** | Kept every run's ticket, job, task, and outcome for the final comparison |

---

## Next steps

### 1. Compare scoreboards

Compare scoreboards with the people around you.

### 2. Remember what the falling count means

The workshop is not "build a flow". It demonstrates an improvement cycle: run real examples, collect human review decisions, leave trace feedback, revise the agent and the orchestration logic, then add automation only where the evidence supports it. The three batches contain different tickets, so the falling count shows routing behavior, not a controlled accuracy benchmark.

---

## Keep iterating

**Question the gate**

- Ask Codex how it knows the knowledge base actually covered an answer. If the uncovered ticket was auto-sent, your gate trusts confidence alone.

**Run the same tickets twice**

- The batches differ by design. To measure accuracy rather than routing, run one ticket set through every version.

**Feed back more evidence**

- Leave trace feedback on the V3 runs that went to review, and ask Codex what a V4 should change.

---

## Learn more

| Resource | Description |
|----------|-------------|
| [Using UiPath CLI with Coding Agents](https://docs.uipath.com/uipath-cli/standalone/latest/user-guide/coding-agents) | Per-agent setup walkthroughs |
| [uip skills reference](https://docs.uipath.com/uipath-cli/standalone/latest/user-guide/uip-skills) | Full command and flag reference |
| [Context Grounding](https://docs.uipath.com/automation-cloud/automation-cloud/latest/admin-guide/about-context-grounding) | Anchoring an agent's answers to your own data |
| [UiPath/skills (GitHub)](https://github.com/uipath/skills) | The source of the UiPath skills |
