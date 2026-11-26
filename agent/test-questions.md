# Test questions and results

These are the questions I asked `ntcorp-policy-agent`, what a grounded answer should contain, and what actually happened. A **grounded** answer uses the exact facts from the policy documents (and cites them) instead of general internet knowledge.

| # | Question | What it tests | Expected (from the documents) | Result |
|---|---|---|---|---|
| 1 | `What are the password requirements for my laptop?` | Fact lookup | At least **12 characters**, mixed character types, change every **90 days**, can't reuse the last **5** | ✅ Passed, with citation |
| 2 | `What are the core hours for remote employees?` | Fact lookup (second document) | **9:00 AM – 3:00 PM**, Monday–Friday, employee's local time | ✅ Passed, with citation (playground **and** Teams) |
| 3 | `What encryption is required on company laptops?` | Fact lookup | **BitLocker** full disk encryption | ✅ Passed, with citation |
| 4 | `What is the company's parental leave policy?` | **Hallucination test**: the answer is *not* in the documents | Says it doesn't have that information and suggests contacting HR | ✅ Passed: did not make anything up |
| 5 | `Can I work from a coffee shop on public Wi-Fi?` | **My own test: everyday wording.** An employee's real-life question; the agent has to connect it to the VPN rule | Only when connected through the **Cisco AnyConnect VPN** | ✅ Passed, with citation |
| 6 | `Which password manager does the company provide?` | **My own test:** a small detail buried in the document | **1Password** | ✅ Passed, with citation |

**Why tests 4–6 matter:** anyone can get a chatbot to repeat a headline fact. Test 4 proves the agent admits when it doesn't know (instead of inventing a policy), test 5 proves it understands a question asked the way a real employee would ask it, and test 6 proves the search finds small details, not just the obvious ones.

✅ **Good signs:** exact numbers and names from the documents, plus a citation marker pointing to the policy file.
❌ **Bad signs:** vague "typically…" answers, or a confident made-up parental leave policy. See the [problems log](../docs/09-problems-log.md) and [troubleshooting tips](../docs/08-cleanup-and-troubleshooting.md#troubleshooting).
