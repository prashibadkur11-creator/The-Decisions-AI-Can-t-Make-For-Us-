# The Decisions AI Can't Make for Us

AI slop is real. I've seen emails go out that nobody approved. I've seen meetings appear on calendars where the organizer found out from an attendee. Agents have started taking phone calls for people now, and they can commit you to things while you're busy in another room.

A year ago the story was that AI could do everything. On capability, that's mostly true. The problem sits somewhere else: just because an agent can act, should it?

The model can't answer that question. Whether an agent drafts an email or actually sends it, whether it proposes a meeting or books it, whether it answers your phone or just takes a message... none of that is the model's call. Someone building the product decides, or nobody does and the product decides badly.

MCP standardizes how agents use tools. A2A standardizes how agents talk to each other. There is no protocol for when an agent should stop and ask a human, and there never will be, because that's a product decision made by people.

The way I think about it: trust belongs to actions, not to agents. The same assistant can read my inbox all day without asking me anything, but I want to see the reply before it goes to a customer. Reading and writing are different actions. Drafting and sending are different actions. Once you classify each action on its own, most of the hard conversations get easier.

The other thing to decide is what the agent does when it isn't sure. An approval request times out. An instruction is ambiguous. If you don't spec this, engineering will pick a default for you, and the path of least resistance is to proceed. It should be the opposite. The agent stops and asks.

Humans build AI, not the other way around. Every agent shipping today behaves the way somebody chose, or the way nobody chose, which is also a choice.

If you work on an agent product, try this: pick one agent, list every action it can take, and write down where a human belongs in each. It's a short document, and it's the difference between an agent people tolerate and one they trust.

---

## The framework

I turned my answer into a framework: four oversight tiers, a decision ladder, and a failure rule.

**[View the carousel (PDF)](agent-oversight-tiers-carousel.pdf)**

| Tier | Name | Behavior |
|------|------|----------|
| 🟢 T0 | Go | Full autonomy. Read-only, reversible actions. |
| 🟡 T1 | Do, Then Tell | Act freely, report after. Undoable, internal writes. |
| 🟠 T2 | Ask, Then Act | Human approves first. Irreversible, external, or spends money. |
| 🔴 T3 | Hands Off | Agent never does it. Credentials, permissions, legal. |

**The decision ladder.** Check in order, first match wins:
1. Touches credentials, permissions, or legal? → **T3**
2. Moves money, irreversible, or leaves the org? → **T2**
3. Writes or changes anything, undoable and internal? → **T1**
4. Read-only? → **T0**

**The failure rule.** When the agent is unsure (approval times out, instruction is ambiguous, request denied), it stops and escalates. It never guesses.

---

*Part of my [AI Product Toolkit](https://github.com/prashibadkur11-creator)*
