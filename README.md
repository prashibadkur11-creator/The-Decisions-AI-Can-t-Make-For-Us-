# The Decisions AI Can't Make for Us

AI slop is real. Most of us have brushed up against it by now — an email that went out before anyone approved it, a meeting that landed on a calendar while the organizer heard about it from an attendee. And now agents are starting to take calls on our behalf. Speaking as us. Committing us to things.

A year ago, the story was that AI could do everything. And honestly? The capability is mostly there. That's not where the story broke down.

It broke down at a quieter question: *just because an agent can act, should it?*

Here's what I keep coming back to. The model was never going to answer that question. It can't. Whether an agent drafts an email or sends it, whether it proposes a meeting or books it, whether it answers your phone or takes a message — those were never AI decisions.

MCP now standardizes how agents use tools. A2A standardizes how agents talk to each other. But no protocol will ever standardize when an agent should stop and ask a human. That question doesn't have a technical answer — it's a product decision, made by people.

It starts with a simple distinction: trust attaches to actions, not to agents. The same assistant can be fully autonomous when reading your inbox and need sign-off before replying to a customer. Reading is not writing. Drafting is not sending. Internal is not external. Reversible is not irreversible. Classify each action, and most of the hard conversations get easier.

And then the question nobody enjoys but everyone needs: what does the agent do when it's *not sure*? When an approval times out, when an instruction is ambiguous. If we don't decide, the software decides for us — and software defaults to proceeding. The better default is the opposite: stop, escalate, ask. Silence is not consent.

None of this makes AI less capable. It makes it trustworthy — and trust, not capability, is what's actually scarce right now.

After all, humans build AI, not the other way around. Every agent shipping today behaves the way someone chose — or the way nobody chose, which is its own kind of choice. The opportunity in front of PMs isn't to slow this technology down. It's to give it judgment.

So here's the question worth sitting with: for the agents in your product, could you say — for every action they can take — whether a human is in the loop, and why?

If you can — you're already building the future the right way. If you can't yet, start today: pick one agent, list every action it can take, and decide where the human belongs in each. That's all it takes to turn an agent people tolerate into one they trust.

Because the teams that win this era won't be the ones who shipped agents first. They'll be the ones who gave them judgment.

---

## The framework

I turned my answer to that question into a framework — four oversight tiers, a 10-second decision ladder, and a failure rule.

**[View the carousel (PDF)](.agent-oversight-tiers-carousel_1.pdf)**

| Tier | Name | Behavior |
|------|------|----------|
| 🟢 T0 | Go | Full autonomy. Read-only, reversible actions. |
| 🟡 T1 | Do, Then Tell | Act freely, report after. Undoable, internal writes. |
| 🟠 T2 | Ask, Then Act | Human approves first. Irreversible, external, or spends money. |
| 🔴 T3 | Hands Off | Agent never does it. Credentials, permissions, legal. |

**The decision ladder** — check in order, first match wins:
1. Touches credentials, permissions, or legal? → **T3**
2. Moves money, irreversible, or leaves the org? → **T2**
3. Writes or changes anything — undoable, internal? → **T1**
4. Read-only? → **T0**

**The failure rule**: when the agent is unsure — approval times out, instruction is ambiguous, request denied — it stops and escalates. It never guesses. Silence is not consent.

---

*Part of my [AI Product Toolkit](https://github.com/prashibadkur11-creator)
