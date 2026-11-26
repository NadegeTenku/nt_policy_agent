# Step 9 – Problems log / lessons learned

[⬅ Previous: Clean up](08-cleanup-and-troubleshooting.md) | [Next: Portfolio and LinkedIn ➡](10-portfolio-and-linkedin.md)

Every issue I hit while building this project: what happened, how I fixed it, and why it matters.

| # | Lesson | Cause / what happened | Fix | Why it matters |
|---|---|---|---|---|
| 1 | Lesson learned: Personal Microsoft accounts can't use Teams agents | My only account was a personal Outlook account; Teams agents and Copilot need a work or school account | Created a lab organization with a Microsoft 365 Business trial (Nash Lab, `nash@ntailab.onmicrosoft.com`) and used it in a private window | Identity and tenant setup come first in any Microsoft cloud project; Azure and Teams must be in the same organization |
| 2 | Lesson learned: Azure free credit expires after 30 days | My personal Azure $200 credit had expired before this project | Created a pay-as-you-go subscription `nash-lab-sub` in the lab organization, with a $5 budget alert | Free credit is time-limited; plan labs around it and always set a budget alert before spending |
| 3 | Lesson learned: Pay-As-You-Go is now called "Microsoft Azure Plan" | The guide said Pay-As-You-Go, but **+ Add** only showed Microsoft Azure Plan | Picked Microsoft Azure Plan (same pay-as-you-go billing, newer name) | Cloud portals rename things often; match options by meaning, not exact words |
| 4 | Lesson learned: Agents can't be renamed | Foundry auto-created a demo agent `my-first-agent`, and there is no rename option | Created a new agent `ntcorp-policy-agent` and deleted the demo one at cleanup | Choose names carefully up front (hyphens, since the name goes into the endpoint URL) |
| 5 | Lesson learned: Web search is added by default | New agents come with a Web search tool attached | Removed it, kept only File search, saved (Version 4) | A policy assistant must answer only from company documents; web search sends data outside Azure, adds cost and breaks proof of grounding |
| 6 | Lesson learned: Register Microsoft.BotService before publishing | Publishing creates an Azure Bot Service, which the subscription must be allowed to create | Registered Microsoft.BotService under the subscription's Resource providers, waited for Registered | Prevents a publishing error; like enabling an API before you use it |
| 7 | Lesson learned: The Azure bot services field is locked | The publish form's bot name field could not be edited | Left it; Foundry auto-named it `ntcorp-policy-agent35943` | Not an error: the platform makes the bot name unique; knowing its name helps find it at cleanup |
| 8 | Lesson learned: A published agent takes ~10 minutes to appear in Teams | Right after publishing, the app wasn't in Teams yet | Waited about 10 minutes, then searched Teams Apps for "ntcorp" | Publishing propagates across Microsoft 365; waiting is part of the process, not a failure |
| 9 | Lesson learned: A computer restart doesn't lose cloud work | My computer restarted mid-project and closed my browser windows | Signed back in (private window, lab account); project, agent and settings were all still there | Cloud resources live in Azure, not in the browser; only unsaved changes in the page are at risk, so Save often |
| 10 | Lesson learned: Copilot needs its own licence | The Microsoft 365 Business trial includes Teams but not Microsoft 365 Copilot | Skipped the Copilot test and documented it as a known limitation | Know which features need extra licences before promising them |
| 11 | Lesson learned: Clean up from the outside in | Resources depend on each other, and the trial would auto-renew at $89.55/year | Uninstalled the Teams app → deleted agents → deleted rg-nash-4219 → cancelled nash-lab-sub → turned off M365 recurring billing | Nothing left behind that still shows up, breaks, or costs money |

[⬅ Previous: Clean up](08-cleanup-and-troubleshooting.md) | [Next: Portfolio and LinkedIn ➡](10-portfolio-and-linkedin.md)
