<!-- Source: coding-agents-workshop-building-a-continuous-improvement-loo-steps.pdf, rebuilt from the PDF content streams. <<IMG:n>> = staging/pdf-images/NN.jpg. -->

## 2. Start Codex and confirm status

Connect to your VM. We recommend using "Connect via Azure Bastion" and using the username and password to log into the VM:

<<IMG:1>>

<<IMG:2>>

You should see a notification asking you whether you want to allow clipboard access. Please accept.

You should see the VM load in that browser tab:

<<IMG:3>>

Perform the rest of the steps in this guide inside the VM:

Open the chrome browser and open a tab to https://staging.uipath.com/uipathlabsworkshop/Coding_Agents_Work_20260921_p7dm/

Optional: If you can't paste into the VM using CTRL+V then visit chrome://settings/content/clipboard in the browser and make sure Bastion isn't blocked from using the Clipboard.

<<IMG:4>>

Choose "Continue with Microsoft" to log in.

<<IMG:5>>

<<IMG:6>>

Use your provided username and password in the "Your Workshop Account" area for login.

<<IMG:7>>

<<IMG:8>>

<<IMG:9>>

Once in Automation Cloud, navigate to Studio Web and confirm the tenant picker shows the workshop tenant Coding_Agents_Work_20260921_p7dm in the upper right corner.

<<IMG:10>>

1. Open the terminal on your VM

<<IMG:11>>

2. Start Codex in it by typing codex and pressing enter. Codex should start in a few moments.

<<IMG:12>>

<<IMG:13>>

3. Type /status and confirm the model reads gpt-5.3-codex and reasoning effort reads medium. If not, use /model to pick GPT-5.3-codex and medium effort.

<<IMG:14>>

<<IMG:15>>

4. In the terminal type ! uip login --authority "https://staging.uipath.com/identity_" --organization uipathlabsworkshop --tenant Coding_Agents_Work_20260921_p7dm You should see a "Ready to automate" browser tab appear and a successful authentication message in the terminal.

<<IMG:16>>

<<IMG:17>>

Checkpoint: /status shows GPT-5.5 at xhigh, and Studio Web is open on the workshop tenant.

Why: the VM already has Codex CLI, the UiPath CLI, the UiPath skills, and both logins in place. You run nothing else in the shell today. Codex runs every command, including the login check in the next step. Keep this one Codex session for the whole workshop so it remembers your solution IDs and run manifest.
