<!-- Source: coding-agents-workshop-building-a-continuous-improvement-loo-steps.pdf, rebuilt from the PDF content streams. <<IMG:n>> = staging/pdf-images/NN.jpg. -->

## 7. Prompt 3: run batch A

Return to the terminal for the next step. For this step, Codex will work for 7-8 minutes.

Paste the run prompt:

```text
Run every ticket in the shared TicketsV1 entity through my deployed V1 flow, one job each. Flows start with uip maestro flow process run <processKey> <folderKey> --release-key <releaseKey>, not with jobs start. Check the deployed process key and folder key first; the deployment folder is inside my personal workspace. If you don't see the deployment folder in my personal workspace, stop and tell me I forgot to deploy the solution from Studio Web to my personal workspace. The batch is settled when every instance is either Completed or has an open Action Center task. Check that instead of waiting on job state, and report after a bounded two-minute window.
```

<<IMG:28>>

Once finished, codex should provide a summary of the runs and pending Action Center tasks.

<<IMG:29>>

Checkpoint: 8 review tasks in Action Center about a minute after the first job started, each already under "My tasks", not "Unassigned". Codex reports instance IDs and the task count. The error "Couldn't find any user with unattended robot permissions" should not happen. If it does, raise a hand.

## 8. Review batch A with Codex

For this step, Codex will work for 5 minutes.

Batch A is where you learn what V1 gets wrong. You read, your agent completes.

1. Ask your agent to show you the review queue and clear it:

```text
Show me the 8 open review tasks as a table: ticket ID, subject, the agent's category, and the first line of its draft. Then complete every task on my behalf and tell me which drafts you approved as-is, which you rewrote before sending, and why.
```

<<IMG:30>>

Once finished, review the summary Codex provided on the completed tasks.

<<IMG:31>>

2. While it works, read the table. Notice what V1 cannot see: the outage is not marked urgent, the out-of-office auto-reply got a task like a real ticket, and the question the knowledge base does not cover still got an answer.

Checkpoint: 8 tasks completed, 0 open. Your score so far: 8 human touches for 8 tickets.
