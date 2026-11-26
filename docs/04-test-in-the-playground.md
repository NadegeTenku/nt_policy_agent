# Step 4 – Test in the playground

[⬅ Previous: Create the agent](03-create-and-ground-the-agent.md) | [Next: Publish to Teams ➡](05-publish-to-teams.md)

The **playground** is the chat window inside Foundry where I can test the agent before anyone else sees it. Like a dress rehearsal before opening night.

## 4.1 Tests I ran
Full table with expected answers: [`agent/test-questions.md`](../agent/test-questions.md).

| # | Question | Result |
|---|---|---|
| 1 | Password requirements | ✅ 12 characters, change every 90 days, can't reuse last 5, cited |
| 2 | Core hours for remote employees | ✅ Mon–Fri 9 AM–3 PM local time, cited |
| 3 | Laptop encryption | ✅ BitLocker, cited |
| 4 | Parental leave policy | ✅ Said it doesn't have that information, suggested HR (**hallucination test**) |
| 5 | *My own:* Can I work from a coffee shop on public Wi-Fi? | ✅ Only with the Cisco AnyConnect VPN, cited |
| 6 | *My own:* Which password manager does the company provide? | ✅ 1Password, cited |

## 4.2 Why I added my own tests
The standard questions check headline facts. My two extra questions check that the agent:
- understands a question asked the way a **real employee** would ask it (coffee shop → VPN rule), and
- finds a **small detail** buried in a long document (1Password).

## Check before continuing
- [x] All answers use the documents' exact facts and show citations.
- [x] The parental leave question gets "I don't know", not an invented policy.

[⬅ Previous: Create the agent](03-create-and-ground-the-agent.md) | [Next: Publish to Teams ➡](05-publish-to-teams.md)
