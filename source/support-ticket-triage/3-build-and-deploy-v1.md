<!-- Source: coding-agents-workshop-building-a-continuous-improvement-loo-steps.pdf, rebuilt from the PDF content streams. <<IMG:n>> = staging/pdf-images/NN.jpg. -->

## 5. Prompt 2: build V1

For this step, Codex will work for 10-12 minutes.

Paste the build prompt:

```text
Build a Maestro Flow solution named after my team code from AGENTS.md (for example triage-user24), with a flow named my team code followed by v1 (for example triage-user24v1). It takes a support ticket (ticketId, subject, body, customerName) as inputs. An agent classifies it and drafts a reply grounded in the existing SupportKB index in the Shared folder, then an Action Center task assigned to me lets me Approve, Modify & Send, or Reject. Keep ticketId on the task and the final output, and route all three action center outcomes to a terminal result. Validate it, refresh the solution resources so the index links up, upload it to Studio Web, and give me the designer URL.
```

When Codex finishes, refresh the Studio Web view and open the project created "triage-user[number]".

<<IMG:22>>

<<IMG:23>>

Take a look at the Flow codex created.

<<IMG:24>>

Attaching any missing outcome lines from the Action Center task to the end node.

<<IMG:25>>

Checkpoint: Codex reports a designer URL, flow validate passed, and solution resources refresh imported the index (it should say "Imported 1", not "Created"). In the designer you see trigger, agent (with a knowledge attachment), review task, end. In the task node's recipient, the assignee is type "user" with your email, not the default "group". Warnings about outcomes without downstream nodes are fine; they don't block deploy.

## 6. Deploy V1 from Studio Web

This is the one browser step you repeat three times today. The deploy log runs for about a minute.

1. In the designer, click Deploy.

2. Leave "Pack to" on Personal. This deploys into your own personal workspace.

<<IMG:26>>

3. Click Deploy in the wizard and watch the log for "All services activated successfully".

<<IMG:27>>

Checkpoint: "Deployment successful" with your version number, and a new folder named after your team code (for example triage-user24) exists inside your personal workspace (My Workspace) on the tenant. If publish fails with "version already exists", bump the Version field in the wizard and retry.
