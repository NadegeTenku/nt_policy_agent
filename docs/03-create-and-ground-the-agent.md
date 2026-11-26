# Step 3 – Create and ground the agent

[⬅ Previous: Foundry project](02-create-the-foundry-project.md) | [Next: Test in the playground ➡](04-test-in-the-playground.md)

## 3.1 Create the agent
1. In project `nash-1323` → **Agents** → **Create agent**.
2. **Name:** `ntcorp-policy-agent` (lowercase, hyphens: it becomes part of the endpoint URL).
3. **Interaction mode:** Text. **Copilot harness:** left **unchecked** (not needed; I publish to Teams).
4. **Model:** gpt-5-mini.

## 3.2 Instructions (the agent's job description)
I replaced the default text with my own, from [`agent/instructions.txt`](../agent/instructions.txt):

```
You are the NTCorp Policy Assistant for NTCorp.

Your role:
- Answer questions about company policies and procedures
- Provide accurate information from uploaded documents
- Be professional, helpful, and concise
- If you don't know the answer, say so and suggest who to contact

Always cite your sources when referencing specific policies.
```

**Why each part:** *role* keeps it on topic; *from uploaded documents* pushes it to use the files, not general knowledge; *say so and suggest who to contact* prevents made-up answers (hallucinations); *cite your sources* lets employees check the answer.

## 3.3 Ground it in the policy documents (File search)
1. Under **Tools** → **File search** → **Upload files**.
2. Uploaded both files from [`data/sample_documents/`](../data/sample_documents/):
   - `it_security_policy.txt`
   - `remote_work_policy.txt`
3. Waited until both were ready (Foundry splits them into chunks and indexes them in a **vector store**, a search index that finds passages by meaning, not just exact words), then attached them.

> **Grounding** = tying the agent's answers to real sources. Like giving a new hire the employee handbook and telling them "only answer from this".

## 3.4 Remove the Web search tool
Foundry **adds a Web search tool by default**. I removed it because:
- answers must come **only from company documents**, not the internet;
- with web search, question text **leaves Azure** to an outside search service;
- it is an **extra cost**;
- if it can search the web, I **can't prove** an answer came from our policies.

## 3.5 Save (versions)
Every **Save** creates a new **version** of the agent, like a Git commit. My final configuration is **Version 4** (instructions + File search with 2 documents, no Web search).

## Check before continuing
- [x] Instructions show "NTCorp Policy Assistant".
- [x] File search lists both documents.
- [x] Web search removed.
- [x] Saved (Version 4).

[⬅ Previous: Foundry project](02-create-the-foundry-project.md) | [Next: Test in the playground ➡](04-test-in-the-playground.md)
