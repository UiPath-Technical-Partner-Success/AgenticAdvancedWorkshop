# Connecting to Your Workshop Environment

!!! tip "Here is our plan for this lesson:"

    1. Connect to your VM and sign in to **Automation Cloud**.
    2. Confirm you're on the workshop tenant in **Studio Web**.

## Goal

By the end of this lesson you'll have a VM open in your browser and **Studio Web** open on the workshop tenant. You'll start **Codex** in the next lesson, from inside your working folder.

## What's already on the VM

The VM already has Codex CLI, the UiPath CLI, the UiPath skills, and both logins in place. Apart from creating your working folder in the next lesson, Codex runs every command for you.


## Steps

### 1. Connect to your VM

On your workshop page, find the **Sandbox** row. We recommend "**Connect in browser**": it opens your VM through **Azure Bastion**, right in a browser tab. Use the username and password shown under **Sandbox sign-in** to log into the VM.

![Workshop page with the Sandbox row showing Ready, the Connect in browser button highlighted, and the Sandbox sign-in and UiPath sign-in details below](1-connect-to-your-environment.images/1-workshop-portal-connect-in-browser-W.png){ .screenshot width="900" }

The Bastion login asks for the same username and password:

[[[
![VM credentials panel with username, masked password, Download RDP File and Connect via Azure Bastion buttons](1-connect-to-your-environment.images/2-vm-credentials.jpg){ .screenshot }
|50|
![Azure Bastion login form with protocol RDP, port 3389, username, password and keyboard language](1-connect-to-your-environment.images/3-azure-bastion-login.jpg){ .screenshot }
]]]

**You should see a notification asking you whether you want to allow clipboard access. Please accept.**

You should see the VM load in that browser tab:

![Windows VM desktop loaded inside a browser tab through Azure Bastion](1-connect-to-your-environment.images/4-vm-desktop-in-browser-W.jpg){ .screenshot width="900" }

### 2. Open the workshop tenant

Perform the rest of the steps in this guide ***inside the VM***.

Open the Chrome browser and open a tab to:

```text
https://cloud.uipath.com/tpenlabs/AgenticAdvancedWorkshop/
```

!!! tip "Can't paste into the VM?"
    If you can't paste into the VM using **CTRL+V**, visit `chrome://settings/content/clipboard` in the browser and make sure Bastion isn't blocked from using the Clipboard.

![Chrome clipboard settings with the Bastion site in the allowed list](1-connect-to-your-environment.images/5-chrome-clipboard-settings-W.jpg){ .screenshot width="900" }

### 3. Sign in to Automation Cloud

[[[
Choose "**Continue with Microsoft**" to log in.
|30|
![UiPath sign-in page with Continue with Microsoft highlighted among the Google, LinkedIn and Email options](1-connect-to-your-environment.images/6-uipath-sign-in-options.png){ .screenshot }
]]]

[[[
Use your provided username and password in the "**Your Workshop Account**" area for login.

![Your Workshop Account panel with the workshop username and a masked password](1-connect-to-your-environment.images/8-workshop-account-credentials.jpg){ .screenshot }
|50|
![Empty Microsoft sign-in form](1-connect-to-your-environment.images/7-microsoft-sign-in.jpg){ .screenshot }

![Microsoft sign-in form with the workshop username entered](1-connect-to-your-environment.images/9-microsoft-sign-in-username.jpg){ .screenshot }

![Enter password screen for the workshop account](1-connect-to-your-environment.images/10-enter-password.jpg){ .screenshot }
]]]

### 4. Confirm the tenant in Studio Web

Once in Automation Cloud, navigate to [**Studio Web**](https://cloud.uipath.com/tpenlabs/studio_/projects) and confirm the tenant picker shows the workshop tenant **AgenticAdvancedWorkshop** in the upper right corner.

![Studio Web Cloud Workspace with Tenant: AgenticAdvancedWorkshop shown in the tenant picker](1-connect-to-your-environment.images/11-studio-web-tenant-picker-W.png){ .screenshot width="900" }

!!! tip "Checkpoint"
    Studio Web is open on the workshop tenant.
