# Step 0 – Plan the project

[⬅ README](../README.md) | [Next: Accounts, subscription and budget ➡](01-accounts-subscription-and-budget.md)

## 0.1 The problem
Employees can't quickly find answers in long policy documents, so they guess or ask IT/HR the same questions repeatedly. I want an assistant that answers **from the company's own documents**, **inside Microsoft Teams**, **with citations**, and that **admits when it doesn't know**.

## 0.2 Design decisions

| Decision | My choice | Why |
|---|---|---|
| Company name | **NTCorp** (fictional) | My own branding. The sample documents still say *Contoso*; I left their text unchanged so the expected answers stay the same |
| Agent name | **`ntcorp-policy-agent`** | Lowercase with **hyphens**: the name becomes part of the agent's web address (endpoint URL), where spaces and underscores cause problems. Agents **can't be renamed** later, so I picked it carefully |
| Repo name | **`nt_policy_agent`** | Matches my other repo `nt_chatbot` |
| Platform | **Microsoft Foundry**, low-code | Builds, grounds and publishes the agent to Teams in one place |
| Knowledge | **2 policy documents** via File search | Small, clear documents make it easy to prove each answer is grounded |
| Delivery | **Microsoft Teams** | Where employees already work |

## 0.3 Plan of the steps
Accounts → Azure subscription + budget → Foundry project → agent (instructions + documents) → playground tests → publish → Teams test → clean up → write-up.

> **Analogy:** like setting up a new help desk. First you need a building and a badge (accounts), a budget, then you hire the assistant (agent), hand them the handbook (documents), quiz them (tests), open the front desk (Teams), and when the pilot ends you lock up and hand back the keys (cleanup).

[⬅ README](../README.md) | [Next: Accounts, subscription and budget ➡](01-accounts-subscription-and-budget.md)
