# Step 8 – Clean up (and troubleshooting)

[⬅ Previous: Copilot](07-m365-copilot-known-limitation.md) | [Next: Problems log ➡](09-problems-log.md)

## Cleanup: from the outside in
I deleted things in the reverse order people reach them: the user's entry point first, the cloud resources next, billing last. That way nothing is left pointing at something that no longer exists, and nothing keeps costing money.

> **Analogy:** closing a shop. Take down the sign on the street first (Teams app), then let the staff go (agents), then empty and return the building (resource group), then cancel the lease (subscription and trial billing).

| # | What | How | Done |
|---|---|---|---|
| 1 | Teams app | Teams → **Apps** → **Manage your apps** → ntcorp-policy-agent → **Uninstall** | ✅ |
| 2 | Both agents | Foundry → **Agents** → `ntcorp-policy-agent` and `my-first-agent` → **Delete** | ✅ |
| 3 | Resource group `rg-nash-4219` | Azure portal → **Resource groups** → `rg-nash-4219` → checked it holds the Foundry resource, the project and the **Azure Bot** → **Delete resource group** → typed the name to confirm | ✅ |
| 4 | Subscription `nash-lab-sub` | Azure portal → **Subscriptions** → `nash-lab-sub` → **Cancel subscription** | ✅ |
| 5 | Microsoft 365 trial billing | https://admin.microsoft.com → **Billing** → **Your products** → the Business trial → **Recurring billing: Off** (otherwise it renews at $89.55/year) | ✅ |

All done on **25 November 2026**.

## Troubleshooting
Short fixes for what can go wrong. My own issues and their fixes are in the [problems log](09-problems-log.md).

| Symptom | Likely cause | Fix |
|---|---|---|
| "Personal account not supported" | Outlook/Hotmail account | Use a work account; create a lab org ([step 1](01-accounts-subscription-and-budget.md)) |
| Can't find Pay-As-You-Go | Renamed | Choose **Microsoft Azure Plan** |
| Publishing fails, mentions Microsoft.BotService | Provider not registered | Register it ([step 5.1](05-publish-to-teams.md)) and publish again |
| Agent not in Teams | Still propagating, or wrong account | Wait ~10 min; same account as Foundry; search Apps for the name |
| Generic answers, no citations | File search missing, or old chat | Check File search lists both files, **Save**, start a **new chat** |
| Answers from the internet | Web search still attached | Remove the Web search tool and Save |
| Made-up answer to parental leave | Instructions changed | Re-paste [`agent/instructions.txt`](../agent/instructions.txt) and Save |
| Teams works but answers are old | Changed the agent after publishing | Publish again with a new version (e.g. `1.0.1`) |

[⬅ Previous: Copilot](07-m365-copilot-known-limitation.md) | [Next: Problems log ➡](09-problems-log.md)
