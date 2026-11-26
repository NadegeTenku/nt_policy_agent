# Step 5 – Publish to Microsoft Teams

[⬅ Previous: Playground](04-test-in-the-playground.md) | [Next: Test in Teams ➡](06-test-in-teams.md)

Publishing turns the agent into a **Teams app**. Behind the scenes Foundry creates an **Azure Bot Service** (the "phone line" between Teams and the agent) and an app package for Teams.

## 5.1 Register the Microsoft.BotService provider first
An Azure subscription has to "switch on" each kind of service before it can create it. Publishing creates a Bot Service, so I registered it first to avoid a publishing error:

1. https://portal.azure.com → **Subscriptions** → **`nash-lab-sub`** → **Resource providers**.
2. Filtered for **`Microsoft.BotService`** → selected it → **Register**.
3. Refreshed until the status showed **Registered**. (Registering is free.)

## 5.2 Start publishing
In Foundry → `ntcorp-policy-agent` → **Publish** → **Publish to Teams and Microsoft 365**.

## 5.3 App details I entered

| Field | My value |
|---|---|
| App name | `ntcorp-policy-agent` |
| Version | `1.0.0` (dots, no spaces) |
| Short description | `NTCorp assistant for company policies` |
| Full description | `AI assistant that answers NTCorp employee questions about IT security and remote work policies, with citations from company documents` |
| Developer name | `Nadege Tenku` |
| Website / Terms / Privacy | `https://contoso.com`, `https://contoso.com/terms`, `https://contoso.com/privacy` (placeholders: the form requires URLs and NTCorp has no real website) |
| Azure bot services | **Locked**, filled in automatically: `ntcorp-policy-agent35943` (Foundry adds a number to make it unique) |

## 5.4 Publish options
- **Publish method:** Direct publish.
- **Scope:** **Just you**. No admin approval is needed. (*Organization* scope would make it visible to everyone, but an admin must approve it first.)
- Clicked **Publish** and got the success message.

## 5.5 Wait
A newly published agent takes **about 10 minutes** to appear in Teams. Waiting is normal; it's not an error.

## Check before continuing
- [x] Microsoft.BotService registered.
- [x] Publish succeeded with version 1.0.0, scope Just you.

[⬅ Previous: Playground](04-test-in-the-playground.md) | [Next: Test in Teams ➡](06-test-in-teams.md)
