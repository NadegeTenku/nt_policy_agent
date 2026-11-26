# Step 2 – Create the Microsoft Foundry project

[⬅ Previous: Accounts](01-accounts-subscription-and-budget.md) | [Next: Create and ground the agent ➡](03-create-and-ground-the-agent.md)

**Microsoft Foundry** is Microsoft's portal for building AI apps and agents. A **project** is the folder that holds the model, the agents and their files.

## 2.1 Open Foundry
1. Went to https://ai.azure.com, signed in as `nash@ntailab.onmicrosoft.com`.
2. Switched the **New Foundry** toggle **on** (the newer experience the steps are based on).

## 2.2 What Foundry created for me
Foundry set up a starter project automatically, so I kept it instead of creating a second one:

| Item | Value |
|---|---|
| Project | **`nash-1323`** |
| Resource group | **`rg-nash-4219`** (the "box" that holds every Azure resource for this project) |
| Region | **West US 3** |
| Model deployment | **gpt-5-mini** |
| Demo agent | `my-first-agent` (deleted during cleanup) |

> **Why keep the auto-created names?** They work fine, and everything sits in one resource group, which makes cleanup a single delete. My own naming goes where people see it: the agent and the Teams app.

> **Note:** agents **can't be renamed** after creation, so I couldn't turn `my-first-agent` into my agent. I created a new one instead (step 3).

## Check before continuing
- [x] Project `nash-1323` open in Foundry.
- [x] A model (gpt-5-mini) is deployed.

[⬅ Previous: Accounts](01-accounts-subscription-and-budget.md) | [Next: Create and ground the agent ➡](03-create-and-ground-the-agent.md)
