# Step 10 – Portfolio card and LinkedIn post

[⬅ Previous: Problems log](09-problems-log.md) | [Back to README ➡](../README.md)

## Portfolio card

**Title:** NTCorp Policy Agent: AI Assistant in Microsoft Teams
**Status:** ✅ Completed (November 2026)
**Tech:** Microsoft Foundry · Azure OpenAI (gpt-5-mini) · File search (RAG) · Azure Bot Service · Microsoft Teams · Microsoft 365 · Azure Cost Management

**Short description (1–2 lines):**
An AI agent grounded in company policy documents that answers employee questions inside Microsoft Teams, with citations, and says "I don't know" when the documents don't cover it.

**Longer description:**
Built a low-code enterprise knowledge agent in Microsoft Foundry for a fictional company, NTCorp. Grounded it in IT security and remote work policies with File search (RAG), removed web search so answers come only from company documents, and validated it with six test questions, including a hallucination test and two of my own. Published it to Microsoft Teams through Azure Bot Service, set a $5 budget alert, and cleaned up every resource afterwards. Total cost: a few cents.

**Links:** GitHub: https://github.com/NadegeTenku/nt_policy_agent

## LinkedIn post (draft)

> 🤖 Just finished my second AI project: an **AI policy assistant inside Microsoft Teams**.
>
> The problem: employees waste time digging through policy documents for simple answers like password rules or remote-work hours.
>
> What I built: an agent in **Microsoft Foundry**, grounded in company policy documents with **File search (RAG)**, published to **Microsoft Teams**. It answers with **citations**, and when the answer isn't in the documents, it says so and points to HR instead of making something up.
>
> What I learned:
> ✅ Grounding matters more than a clever prompt. I removed web search so every answer comes from the company's own documents.
> ✅ Test what the agent should NOT answer. My "parental leave" question proved it doesn't hallucinate.
> ✅ Identity comes first: Azure and Teams must live in the same organization.
> ✅ Clean up from the outside in. Total cost: a few cents.
>
> Write-up, steps and lessons learned on GitHub 👉 https://github.com/NadegeTenku/nt_policy_agent
>
> #GenerativeAI #AgenticAI #MicrosoftFoundry #Azure #MicrosoftTeams #RAG #DevOps #AIEngineering

📸 Attach 1–2 screenshots: the Teams answer with a citation, and the parental leave "I don't know" answer.

[⬅ Previous: Problems log](09-problems-log.md) | [Back to README ➡](../README.md)
