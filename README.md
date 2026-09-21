# Agent Control Lab

Experiments in control systems for AI coding agents.

## Core Question

How much of an AI coding agent's capability comes from the underlying language model, and how much can be moved into the system surrounding the model?

This repository explores whether stronger harnesses, controllers, verification loops, context management, and decision layers can make lower-cost models substantially more capable, reliable, and token-efficient.

The broader idea is to treat **model intelligence** and **agent intelligence** as related but distinct things.

A useful working model is:

> **Model Capability × Harness Quality × Control Quality → Agent Capability**

## Current Experiment: Jev

Jev is an experimental supervisory controller designed to separate **execution from judgment**.

The coding model performs the work: exploring repositories, generating code, using tools, and proposing actions.

Jev supervises that process:

**Goal → Plan → Execute → Observe → Verify → Decide**

It can then choose to:

**Continue / Retry / Replan / Escalate / Stop**

The objective is to investigate whether this architecture can reduce wasted exploration, repeated reasoning, context pollution, premature completion, unproductive loops, and unnecessary token consumption.

## Hypothesis

The initial hypothesis and proposed evaluation methodology are documented here:

[`docs/hypothesis.md`](docs/hypothesis.md)

## Status

Early-stage research and experimentation.

The claims in this repository are hypotheses unless supported by published experimental results.

As experiments are completed, results, failures, architecture changes, and benchmarks will be documented here.
