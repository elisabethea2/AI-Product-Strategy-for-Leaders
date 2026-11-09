# Kill Switch Audit

## Vendor Dependency Assessment
| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | Claude (Anthropic) is our primary AI provider | H | Identify an alternative model (e.g., OpenAI) and test the main AI workflows. |
| **Abstraction** | AI integration exists, but provider-independent architecture has not been verified. | M | Review AI integration points and isolate provider-specific logic. |
| **Routing** | No confirmed automatic fallback to another provider | H | Implement a configurable provider switch and test a manual failover.|
| **Eval** | Outputs are reviewed manually; no automated evaluation framework has been confirmed. | H | Use the Golden Dataset defined to evaluate alternative models against job-fit accuracy, unsupported claims and CV tailoring quality before enabling failover.|

## Portability Score
Partial

## If Anthropic doubles pricing tomorrow:
Assess the cost impact on our AI workflows, prioritize critical features (job-fit assessment and CV tailoring), and test an alternative provider such as OpenAI. Temporarily limit non-essential AI usage if necessary.

Before switching providers, validate the alternative against the Reliability Contract. If no provider meets the minimum quality requirements, retain the current provider for critical workflows while applying usage limits and cost optimizations.

## If Anthropic ships a competing product:
Differentiate through our structured Career Knowledge Base, which captures detailed professional experience, achievements, and supporting evidence. Strengthen personalization by learning from user corrections and preferences, making Role Fit increasingly valuable with continued use.
