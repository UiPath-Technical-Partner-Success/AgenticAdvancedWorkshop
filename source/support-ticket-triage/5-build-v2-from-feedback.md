<!-- Source: coding-agents-workshop-building-a-continuous-improvement-loo-steps.pdf, rebuilt from the PDF content streams. <<IMG:n>> = staging/pdf-images/NN.jpg. -->

## 9. Prompt 4: leave trace feedback and build V2

For this step, Codex will work for 5 minutes.

Paste the feedback-and-build prompt:

```text
First leave trace feedback on three of the V1 runs (uip traces feedback create needs --positive or --negative plus --comment): the outage ticket should have been treated as urgent, the auto-reply is noise that never needed review, and every draft should come with a recommended approach for the reviewer. Then look at my review decisions in the completed tasks together with that feedback, figure out what's weak in V1, and build a second flow in the same solution, named my team code followed by v2 (for example triage-user24v2), that fixes it. Validate and upload it; I'll deploy from the designer and tell you when it's done.
```

Once finished, review the summary Codex provided.

<<IMG:32>>

Return to Studio Web and open your project again.

<<IMG:33>>

Click on v2 of your Flow project.

<<IMG:34>>

Finish connecting the outcomes from the Action Center task to your end node.

<<IMG:35>>

Checkpoint: 3 feedback entries readable via uip traces feedback list. Codex names the weaknesses from your evidence (no urgency path, noise reviewed for nothing, no reviewer guidance) and reports a second flow with a needsReview flag, a recommendedApproach field, urgent routing to a High-priority task, and review suppressed for non-actionable noise. Both review tasks are still assigned to you. Upload needs --force this time; that is expected.

## 10. Deploy V2

1. In the designer, click Pack and upgrade, bump the version, and deploy.

<<IMG:36>>

2. Wait for "Deployment successful" before the next prompt.

<<IMG:37>>

Checkpoint: "Deployment successful" with the new version. If you prompt Codex too early it finds no V2 release and stops.
