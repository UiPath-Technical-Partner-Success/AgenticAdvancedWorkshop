# Running Batch C and Comparing Versions

!!! tip "Here is our plan for this lesson:"

    1. Run the TicketsV3 tickets through V3 and look at the routing.
    2. Release the final batch with `go` so **Codex** completes the tasks.
    3. Read the V1/V2/V3 scoreboard.

## Goal

By the end of this lesson you'll have a report that compares V1, V2, and V3 from the run manifest: tickets processed, review tasks created, human touches, delegated reviews, auto-resolutions, faults, and what changed between versions.

## What to expect from V3

Auto-resolved tickets finish in 6 to 16 seconds. Review tasks appear in about 15 seconds. Codex pauses once so you can see the routing before it clears the tasks.

## Steps

### 1. Prompt 6: run batch C, finish the tasks, build the scoreboard

!!! info "For this step, Codex works 15 minutes in three stages."

Return to your terminal and paste the final prompt:

```text
V3 is deployed. Check the V3 release's index folderPath and patch it to "Shared" if needed, then run every ticket in TicketsV3 through V3 and tell me when every instance is Completed or has an open task. Show me which tickets auto-resolved (with the knowledge article each one cited), which escalated as urgent, which closed as noise, and which landed in review, then wait for my go before completing the tasks. After I say go, complete the open tasks from this batch on my behalf the same way as before, then create a report that compares V1, V2, and V3 from the run manifest: tickets processed, review tasks created, human touches, delegated reviews, auto-resolutions, faults, and what changed between versions.
```

![Codex terminal with the final prompt pasted below the V3 build summary](7-run-batch-c-and-compare.images/1-paste-prompt-6-W.jpg){ .screenshot width="900" }

### 2. Check the routing, then say go

Look at the routing Codex shows you and glance at the review tasks in **Action Center**. When satisfied, type `go`.

```text
go
```

!!! tip "Checkpoint"
    3 to 4 tickets auto-resolve with a cited knowledge article, noise auto-closes, 2 urgent tickets escalate, and 1 to 2 land in review, always including the question the knowledge base doesn't cover. If the uncovered ticket was auto-sent instead, your gate trusts confidence alone. Ask Codex how it knows the knowledge base actually covered the answer. Final scoreboard: 8, then 7, then 3 or 4 review tasks.
