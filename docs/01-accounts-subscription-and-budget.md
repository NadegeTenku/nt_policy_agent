# Step 1 – Accounts, subscription and budget

[⬅ Previous: Plan](00-plan-the-project.md) | [Next: Create the Foundry project ➡](02-create-the-foundry-project.md)

## 1.1 Why I needed a new "lab organization"
Teams agents and Microsoft 365 Copilot **don't accept personal Microsoft accounts** (Outlook, Hotmail). They need a **work or school** account, and **Azure and Teams must be in the same organization** (tenant) so the published agent can reach Teams.

I only had a personal account, so I created my own small organization.

> **Analogy:** a tenant is like an office building. Azure (where the agent lives) and Teams (where people talk to it) must be in the same building, or the agent's badge won't open the Teams door.

## 1.2 Create the Microsoft 365 lab organization
1. Opened a **private (InPrivate/Incognito) browser window**, so my personal account wouldn't get mixed in.
2. Started a **Microsoft 365 Business free trial** (1 month, includes Teams).
3. Chose **Set up account** when it said I was using a personal email.
4. Company name: **Nash Lab**. Domain: **ntailab**. Username: **nash**.
   ➡ My work account: **`nash@ntailab.onmicrosoft.com`**. I am the admin of this organization.
5. Added a card for verification (no charge during the trial) and started the trial.
6. Checked that **Teams** opened with the new account.

> I used this account, in the private window, for **every** step of the project.

## 1.3 Azure subscription `nash-lab-sub`
My personal Azure account's **$200 free credit had expired** (it only lasts 30 days, which is normal and caused no charge). And an Azure free account can only be created once per person. So in the new organization I created a pay-as-you-go subscription:

1. Signed in to https://portal.azure.com as `nash@ntailab.onmicrosoft.com`.
2. Searched **Subscriptions** → **+ Add**.
3. The guide said *Pay-As-You-Go*, but the screen showed **Microsoft Azure Plan**. They are the same thing: *Microsoft Azure Plan* is the newer name.
4. Named the subscription **`nash-lab-sub`** and finished the steps.

## 1.4 $5 budget alert
On the subscription's **Budget** tab I added a **$5** budget with an email alert.

> A budget is a **smoke alarm, not a sprinkler**: it warns me if spending passes $5, it does **not** stop or cap anything. Cleanup (step 8) is what stops costs.

## Check before continuing
- [x] Work account `nash@ntailab.onmicrosoft.com` signs in to Teams.
- [x] Subscription `nash-lab-sub` exists in the same organization.
- [x] $5 budget alert set.

[⬅ Previous: Plan](00-plan-the-project.md) | [Next: Create the Foundry project ➡](02-create-the-foundry-project.md)
