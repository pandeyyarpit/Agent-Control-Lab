Jev Controller Hypothesis — v0.1

Hypothesis: The performance of an AI coding agent is determined not only by the capability of its underlying LLM, but substantially by the quality of the control system surrounding that model.

A lower-cost or weaker LLM operating inside a strong coding harness can potentially close a meaningful portion of the performance gap with frontier coding agents when an external controller — Jev — governs how the agent works.

Rather than asking the LLM to autonomously plan, execute, evaluate, and decide when it is finished, Jev separates execution from judgment.

The coding model remains responsible for generating code, investigating the repository, and proposing actions. Jev acts as a supervisory decision layer that continuously evaluates:

Goal → Plan → Execute → Observe → Verify → Decide → Continue / Retry / Replan / Escalate / Stop

Jev's purpose is to prevent common sources of agent inefficiency: unnecessary exploration, repeated reasoning, context pollution, premature completion, unproductive loops, incorrect assumptions, and excessive token consumption.

The central prediction is therefore:

Model capability × Harness quality × Control quality → Agent capability

rather than:

Model capability → Agent capability

If this hypothesis is correct, improving the controller may sometimes produce a larger improvement in real-world coding-agent performance per dollar than simply moving to a more capable and expensive model.

We will test this by running identical software-engineering tasks under controlled conditions and comparing:

DeepSeek + Harness

versus

DeepSeek + Harness + Jev

and, where useful, established coding agents such as Codex and Claude Code as external baselines.

Measurements will include task completion, tests passed, regressions introduced, unnecessary actions, retries, tokens consumed, cost, elapsed time, and human intervention.

The goal is not to prove that the underlying LLM is irrelevant. The goal is to determine how much of coding-agent performance can be shifted from raw model intelligence into a reusable, model-independent control layer.
