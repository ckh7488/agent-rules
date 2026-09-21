# agent-rules

Personal operating rules for AI agents.

This repository exists to reduce recurring LLM failure modes during technical analysis, document review, comparison, and verification.

## Current rule set

### Passive
- **문서우선** — prefer provided primary sources over prior model knowledge, with evidence-linked conclusions.
- **가설중립** — do not privilege the user's hypothesis; derive explanations from observations first.
- **근거압축** — extract a compact evidence set before reasoning over long or multi-document context.
- **독립비교** — evaluate candidates independently under fixed criteria before direct comparison.
- **도구검증** — use deterministic tools for exact tasks whenever available.

### Active
- **재검토** — re-read the source material and solve from scratch before comparing with the previous answer.

## Usage

Use `AGENTS.md` as the instruction file for compatible agents such as Codex.

The passive rules should be applied automatically when relevant.
The active command is invoked explicitly by the user.

## Design principle

Only add a rule when:
1. the failure mode is reproducible or well-supported,
2. the mitigation is actionable,
3. the rule is not already covered by an existing one.

The goal is a small, high-value rule set rather than a large prompt checklist.
