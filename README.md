<h1 align="center">Emmanuel Abugauch</h1>

<p align="center">
  <b>Senior Backend Engineer @ Yuno</b> — payments infrastructure<br>
  Córdoba, Argentina
</p>

<p align="center">
  <em>I build systems that stay correct when the interesting part fails:<br>
  payments that recover from declines, agents that don't lose the plot,<br>
  bots that reason about the cards they can't see.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/event--sourcing-NATS%20%2F%20JetStream-27AAE1?style=flat-square" alt="Event sourcing">
  <img src="https://img.shields.io/badge/domain-payments%20%C2%B7%20AI%20agents-6E56CF?style=flat-square" alt="Domains">
</p>

---

### What I'm building

- **[rey-del-truco-motor](https://github.com/ekamuna/rey-del-truco-motor)** — `Python` · a 1v1 Argentine *truco* engine and a family of bots that walks the whole spectrum of game AI: `if/else` → tabular Q-learning → deep RL → **PIMC** (Perfect Information Monte Carlo). The result that made the project worth writing: a neural net trained on 770k self-play games landed **below** the rule-based bot, while PIMC — which trains on nothing and simply **infers the hidden cards** — wins the panel at **78%** over 300-game matchups. In imperfect information you don't win by training more, you win by guessing better at what you can't see. 125 tests, `mypy --strict`, `ruff`.

- **split** — `Go` *(private, in progress)* · a self-hosted, multi-persona AI assistant: many personas with real domain expertise and **their own judgment**, sharing **one mind**. Event-sourced on NATS/JetStream, N personas per instance via per-call impersonation, and a distributed agent loop that runs for hours and **survives `kill -9`** by replaying its own log.

- **keel** — `Go` *(pre-alpha, design-first)* · the black box + circuit breaker for long-running coding agents. It records every tool call to a durable ordered log, scores **live** whether the trajectory still matches the spec's intent, and rolls back to the last coherent git checkpoint before a drifting run corrupts the repo. Most agent failures at hour six started at hour two — nobody measures that while it's happening.

- **ai-translate** — `Go` · `macOS` · a local English coach disguised as a translator. Two global hotkeys: one translates EN↔ES, the other reads your English *as if a Spanish speaker wrote it* and turns every mistake into a categorized micro-lesson. Weekly digests, spaced repetition built from your own past corrections, everything in local SQLite.

- **[zenithpay-retry](https://github.com/eabugauch/zenithpay-retry)** — payment retry orchestration: classifies soft vs. hard declines, schedules retries on that classification instead of a blind fixed backoff, tracks the full transaction lifecycle and reports recovery analytics. The everyday shape of the work — the money that gets lost between "declined" and "actually unrecoverable."

---

### How I work

**I measure instead of assuming.** Every claim above came from a scoreboard, not a hunch — and the headline finding of my own AI project is that the sophisticated approach *lost*. I'd rather publish the experiment that killed my hypothesis than the demo that flatters it.

**Design-first on the hard parts.** `keel` and `split` started as a PRD and an architecture doc with numbered, stable anchors, because the expensive mistakes in event-sourced systems are made before the first line of code.

**Strict by default.** `mypy --strict`, `ruff`, real test suites, CI. Tooling that says "no" early is cheaper than a code review that says "no" late.

**Documentation is part of the deliverable.** Every repo carries the *why*: a PRD, a roadmap, and an honest log of what was tried and discarded.

---

### Elsewhere

[![GitHub](https://img.shields.io/badge/legacy%20account-eabugauch-181717?style=flat-square&logo=github)](https://github.com/eabugauch)
