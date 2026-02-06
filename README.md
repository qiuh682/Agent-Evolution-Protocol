# Agent Evolution Protocol v2.1

A production-ready protocol for building self-evolving AI agents with metacognitive analysis capabilities. Designed for adaptive execution — pursuing high accuracy on complex tasks and high efficiency on simple ones.

## Overview

This protocol defines a structured framework for AI agent behavior, covering task assessment, execution workflows, verification standards, and safety mechanisms. It introduces three key innovations:

- **Feature-Based Complexity Scoring** — 5-dimension objective scoring model (file scope, dependencies, reversibility, security, requirement clarity) replacing subjective time estimates
- **Verification Ladder** — 4-level auditable verification system (L1 Self-check → L2 Reproducible → L3 External Evidence → L4 Test/Simulation) replacing vague confidence percentages
- **LLM-Specific Safety** — Dedicated modules for hallucination prevention, credential protection, prompt injection defense, and tool call security

## Documents

| File | Language | Description |
|------|----------|-------------|
| [agent-protocol-core.md](agent-protocol-core.md) | English | Concise core protocol reference |
| [Agent 进化协议：递归与逻辑增强架构.md](<Agent 进化协议：递归与逻辑增强架构.md>) | 中文 | Full protocol with detailed examples, version history, and implementation guidance |

## Core Architecture

### Adaptive P.I.T.R. Loop

**Plan → Implement → Test → Refine** — scales with task complexity:

| Score | Complexity | Execution Mode | Verification |
|-------|------------|----------------|--------------|
| 0-2 | Simple | Silent execution | L1 Self-check |
| 3-5 | Medium | Simplified P.I.T.R. | L2 Reproducible |
| 6-8 | Complex | Full P.I.T.R. | L3 External Evidence |
| 9-10 | Critical | Full P.I.T.R. + Human Confirmation | L4 Test/Simulation |

### 5-Dimension Complexity Scoring

| Dimension | 0 | 1 | 2 |
|-----------|---|---|---|
| File Scope | Single file | 2-5 files | >5 files / cross-module |
| Dependencies | No new deps | New usage of existing | New library/service |
| Reversibility | Fully reversible | Manual restore | Delete/reset/publish |
| Security | No sensitive ops | User data | Auth/payment/PII |
| Requirement Clarity | Clear & specific | Partial inference | Ambiguous |

### Cognitive Modes

| Mode | Trigger | Action |
|------|---------|--------|
| Tree of Thoughts | Score 6+ or multiple viable approaches | Present 2-3 options with trade-offs |
| Devil's Advocate | Score 3+ or security/data integrity | Identify and optimize weaknesses |
| Backtracking | Any test failure or logic error | Revert to logic fork point, no patching |

### Safety Protocol

- **Failure Circuit Breaker** — Auto-stop on repeated errors (same error x2, module errors x3, coverage drop >5%, security vulnerability)
- **Anti-Hallucination** — Mandatory source verification for external references; fabricating doc links is forbidden
- **Credential Protection** — Regex-based detection for API keys, tokens; enforced environment variable patterns
- **Prompt Injection Defense** — Keyword detection with graceful degradation to clarification mode

## Usage

These documents can be used as:

- **System prompts** for Claude Code or other AI coding assistants
- **Agent workflow specifications** for team standardization
- **CI/CD integration** — embed the scoring model and verification ladder into automated pipelines

## Version History

| Version | Key Features |
|---------|-------------|
| v2.1 | Feature scoring + Verification ladder + LLM-specific safety |
| v2.0 | Adaptive P.I.T.R. + Tool integration + Task classification |
| v1.0 | Base P.I.T.R. loop + Metacognitive analysis |

## License

MIT
