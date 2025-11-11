---
theme: default
title: MCP Reality Check
info: A presentation giving a critical review of MCP servers.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# MCP Reality Check

Sorry, this presentation isn't going to go with all the hype.

<div class="abs-br m-6 text-xl">
  <!-- <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button> -->
  <a href="https://github.com/andrewgremlich/mcp-hype" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<style>
  .qr-bottom-left {
    position: absolute;
    left: 30px;
    bottom: 30px;
  }
</style>

<!--
- I am not in favor of the hype surrounding MCP technology.
- I do think it may be useful in some cases.
- Traditional still will work.
-->

---
transition: slide-up
---

<v-clicks>

- Disillusioned.
- Usability includes what problem it solves.
- Hype mostly just inflates value.

</v-clicks>

<style>
  li {
    font-size: 40px;
  }
</style>

<!--
- There is so much push to use AI.
- There is so much money.
- Not all AI is profitable.
- The ROI doesn't have much to say.
-->

---
transition: slide-left
---

<v-clicks>

- Normal Person
- My own life experience
- I see a certain way
- We may disagree, and that's okay
- No contempt
- Appreciate all life experiences
- Work together.

</v-clicks>

<style>
  li {
    font-size: 34px;
  }
</style>

<!--
Try to practice listening skills.
-->

---
src: ./pages/hype-technology.md
hide: false
---

---
tranistion: slide-left
layout: statement
---

These things can be useful!

<style>
  p {
    font-size: 40px;
  }
</style>

<!--
- Somethings can be useful!
- Blockchain helps privacy
- Quantum computers speed up computation.
-->

---
transition: slide-up
---

# MCP Technology

<v-clicks>

- MCP extend LLM capability.
- MCP will probably not be for a normal user.

</v-clicks>

<style>
  li {
    font-size: 32px;
  }
</style>

<!--
- Impressive MCP yes!
- Still seems like normal REST API.
- Why are chatbots being made for normal user?
- MCP enabled chatbots are more for power users.
- MCP depends on LLM.
-->


---
transition: slide-up
layout: statement
---

This seems like a fancy way to talk to an LLM...

<style>
  p {
    font-size: 40px;
  }
</style>

<!--
- Chat should be complementary, not primary
- Too many features = poor UX
- AI winners have focused solutions
-->


---
src: ./pages/dont-make-me-think.md
hide: false
---

---
transition: slide-left
---

# Not So User Friendly

<v-clicks>

- Chatbot as primary interface = guessing game
- Frustrated users = divested users
- Traditional interfaces provide clear cues
- Why replace what already works?

</v-clicks>

<style>
  li {
    font-size: 32px;
  }
</style>

<!--
- Software engineers think chatbots replace traditional UI
- Shows limited UX knowledge
- Users need obvious features, not hidden ones
- Chatbots make users guess what's possible
-->

---
transition: slide-left
---

# The Interface Paradox

<v-clicks>

- Chatbot needs to cue users about features
- This defeats the purpose of "no traditional UI"
- If you need traditional cues... why not traditional UI?
- Conduct UX research first!

</v-clicks>

<style>
  li {
    font-size: 30px;
  }
</style>

<!--
- Chatbots still need to explain their capabilities
- Ends up being more work than traditional interface
- Research should drive design decisions
-->

---
transition: slide-left
---

# Power Users vs Everyone Else

<v-clicks>

- As a power user, I don't use many features
- Microsoft Word: hundreds of features, most widely unused
- Google Docs wins with essential feature set
- Usability > Feature count

</v-clicks>

<style>
  li {
    font-size: 30px;
  }
</style>

<!--
- Personal anecdotes about feature usage
- More features doesn't mean better experience
- Simplicity and reliability matter more
-->

---
transition: slide-up
---

# LLM Reality Check

<v-clicks>

- Productivity boost is context dependent
- Non-deterministic results
- Too many demos require negotiating with the chatbot
- Demos should encourage use, not caution

</v-clicks>

<style>
  li {
    font-size: 32px;
  }
</style>

<!--
- Presented at UtahJS about LLM limitations
- Context matters for effectiveness
- Bad demos create expectation mismatch
-->

---
transition: slide-left
---

# The Context Engineering Shift

<v-clicks>

- Anthropic: "Prompt engineering isn't that useful"
- Now we need "context engineering"
- Sounds familiar... like rubber duck programming?
- Give AI context = talk to rubber duck?

</v-clicks>

<style>
  li {
    font-size: 30px;
  }
</style>

<!--
- Industry pivoting on advice
- Context engineering = explaining problem thoroughly
- Good engineers might solve it themselves with that context
-->

---
transition: slide-down
---

# Context Problem

- Use MCPs too much, then context bloat risk.
- Use LLMs for a secure system, risk prompt injection.

<!--
- Current events should show that non-deterministic results of an LLM __are risky__.
-->

---
transition: slide-left
---

# The Duck Programming Problem

<v-clicks>

- At sufficient context, couldn't you solve it yourself?
- LLMs still hallucinate (non-deterministic)
- Can't reliably trust output
- Need smaller bursts, not sweeping changes

</v-clicks>

<style>
  li {
    font-size: 30px;
  }
</style>

<!--
- If you explain the problem fully, you're halfway there
- Hallucination risk remains
- Trust issues require careful, incremental use
-->

---
transition: slide-up
---

# Tooling Issues

<v-clicks>

- Configuration speed
- Tool Reliability.

<!--
- I really don't see how one can argue that MCP setup is any faster tooling setup.
- Take the whole context together.
- At best, they shouldn't even be compared.
- MCPs still rely on LLMs and that is not 100% reliable.
- If you had a TV or a phone that worked 90% of the time, wouldn't you get frustrated?
- Traditional tools have a higher usability rate.
-->

</v-clicks>

---
transition: slide-left
---

<!-- This is a weather script. -->

---
transition: slide-up
---

# A Different Path Forward

<v-clicks>

- MCPs without chatbot interface?
- Simple ML program accessing MCP servers
- Competes with GraphQL and REST APIs
- Why not just use a button? 😱

</v-clicks>

<style>
  li {
    font-size: 32px;
  }
</style>

<!--
- Maybe the interface is the problem
- Traditional APIs already exist
- Sometimes simple solutions are better
-->

---
transition: slide-left
---

# The Integration Problem

<div v-click>

> "AI doesn't have a capabilities problem—it has an integration problem."

<div class="text-center mt-8">
  <p class="text-2xl">— Fabric Project</p>
</div>

</div>


<v-clicks>

- AI works best in simple automation tasks
- Integration into daily life is the challenge
- Boil down to simple, easy tasks

</v-clicks>

<style>
  blockquote {
    font-size: 28px;
    margin: 20px 0;
  }
  li {
    font-size: 28px;
  }
</style>

<!--
- Fabric project gets it right
- The problem isn't capability
- It's making AI actually useful in practice
-->

---
transition: slide-left
layout: statement
---

Work together, not against each other.

<style>
  p {
    font-size: 40px;
  }
</style>

<!--
- Technology should serve users
- Not force users to adapt to technology
- Collaboration over hype
-->

---

<div class="text-center">

# Read my blog for references and notes!

<QRCode urlToEncode="https://www.gremlich.me/software-engineering/2025/mcp-reality-check/" />

</div>

<style>
  .text-center {
    height: 100%;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>
