<!-- Source: coding-agents-workshop-building-a-continuous-improvement-loo-steps.pdf, rebuilt from the PDF content streams. <<IMG:n>> = staging/pdf-images/NN.jpg. -->

## 15. If something breaks

Everything you build lives in your own personal workspace, so you can't break anyone else's run. Look up your symptom here before raising a hand.

- Codex has been "waiting for jobs" for more than 2 minutes. The jobs are almost certainly done. Flow jobs show Running while they wait on a human. Say: "stop polling job state, list open Action Center tasks and completed instances, and report".

- Prompt 1 reports the wrong organization or tenant. The VM login points somewhere else. Raise a hand; a TA re-runs uip login for the workshop tenant on your VM. Do not build on the wrong tenant.

- Codex reports a team code that is not triage- plus your username. Tell Codex: "my username is the part of my email before the first underscore; recompute the team code and update AGENTS.md". Do this before Prompt 2, since the solution name is fixed once created.

- uip commands fail with DNS or "fetch failed" errors inside Codex. The Codex sandbox has no network access. Restart Codex with codex -c sandbox_workspace_write.network_access=true and re-paste Prompt 1; AGENTS.md keeps your team code.

- Codex does not know the UiPath skills. Ask Codex to run uip skills install --agent codex --path . --repo https://github.com/UiPath/skills.git, then restart Codex from the same folder and re-paste Prompt 1.

- Codex is not on GPT-5.5 Extra High. Type /model and select GPT-5.5 with reasoning Extra High, then confirm with /status. Do not continue on a substitute model without telling a TA.

- Deploy button is greyed out. The index debug overwrite is missing. Ask Codex to run uip solution resources refresh again, then open the designer in a fresh tab.

- Deploy wizard says "Pack only, no deployment". "Pack to" was switched to Shared. Attendee accounts cannot create folders under Shared. Set "Pack to" back to Personal and deploy again.

- Review tasks arrive Unassigned instead of under "My tasks". The task node kept the default assignee type "group". Have Codex set the recipient assignee to type "user" with your email from uip or users current, re-upload with --force, and Pack and upgrade. Meanwhile, tasks can still be opened from the Unassigned list.

- Codex wants to run flow debug. Say no. Debug runs bypass the deployed release, so the Shared index mapping is not applied and the knowledge index doesn't resolve. Deployed runs only.

- Codex packs or publishes from the CLI. Stop it. CLI packaging silently drops the agent's knowledge attachment. Deploys go through the designer button only.

- Codex says there is no V2 or V3 release. The deploy hasn't finished, or you skipped it. Wait for "Deployment successful" in the designer, then say "try again".

- Publish fails: "version already exists". Bump the Version field in the deploy wizard and retry. Never delete and recreate your solution; the old package name keeps its versions.

- Jobs won't start (uip or jobs start returns 409). Flows use uip maestro flow process run with the process key, folder key, and release key. Codex knows this if you nudge it.

- V2 or V3 agent faults: "Context grounding index was not found". A flow added after the first deploy gets its release index mapping pointed at your deployment folder instead of Shared, and every redeploy resets it. Have Codex patch the release's ResourceOverwrites folderPath to "Shared", then retry the faulted instances with uip maestro flow instance retry. No need to start new jobs.

- Task completion returns HTTP 403 with a bare "error code: 1010". Not a permissions problem. The web application firewall rejects non-browser clients. Complete the task in the Action Center UI, or have Codex send a browser User-Agent header on the completion call.

- Agent faults: "Missing static query value". The knowledge attachment's query is set to static with no value. It must be dynamic so the agent supplies the query at runtime. Have Codex fix the resource settings and re-upload.

- Agent runs but answers nonsense or says it got no message. The node prompt or the agent's message templates reference variables that don't exist. Have Codex regenerate the prompts from the actual inputs. If it edits agent.json messages directly, it must rebuild contentTokens to match content.

- Job faults instantly: "no user with unattended robot permissions". Personal workspace deployments run on your workspace's own robot, so this should not happen. Raise a hand. A TA checks the robot and roles on your workspace folder.

- Agent answers questions the knowledge base shouldn't cover. The index isn't attached. Check the flow shows a knowledge attachment on the agent node, and that the Prompt 1 test search worked.

- Designer goes blank or shows a stale deploy screen. Known Studio Web quirk. Open a fresh tab and confirm the tenant picker shows the workshop tenant.

- You're behind the room. Raise a hand. TAs carry reference builds of V1, V2, and V3 and can drop you into the room's current step.
