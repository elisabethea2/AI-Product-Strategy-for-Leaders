# Cost Curve & Pricing Strategy

## Packaging Decision
| Leader | Filler | Killer | Killer Usage % | Bundle or Add-on |
|---|---|---|---|---|
| AI Job Fit Assessment + Tailored CV Generation | Application Tracker & Career Dashboard | Unlimited CV Regeneration | 20–30% (estimated) | Add-on |

**Decision:** Include 40 job-fit assessments, 10 tailored CV generations and 5 CV regenerations in the monthly subscription. Charge separately for additional usage.

### AI Usage Assumptions
The following estimates represent one active Role Fit user per month. They are planning assumptions, not measured production usage.

| AI Feature | Requests / Month | Model Tier | Proposed Model |
|---|---:|---|---|
| Job Fit Assessment | 40 | Mid | Claude Sonnet |
| Tailored CV Generation | 10 | Frontier | Claude Opus |
| CV Regeneration | 5 | Frontier | Claude Opus |
| **Total** | **55** | | |

**Model distribution:** 40 Mid requests (73%) and 15 Frontier requests (27%).

### Token Consumption Assumptions
| AI Operation | Input Tokens / Request | Output Tokens / Request |
|---|---:|---:|
| Job Fit Assessment (Sonnet) | 5,000 | 1,500 |
| CV Generation / Regeneration (Opus) | 10,000 | 3,000 |

These are hypothetical token estimates. Actual usage must be measured and validated.

### Estimated Monthly Inference Costs
| AI Operation | Requests / Month | Estimated Cost / Request | Monthly Cost |
|---|---:|---:|---:|
| Job Fit Assessment (Sonnet) | 40 | $0.0375 | $1.50 |
| Tailored CV Generation (Opus) | 10 | $0.125 | $1.25 |
| CV Regeneration (Opus) | 5 | $0.125 | $0.625 |
| **Total inference** | **55** | **$0.0614 blended** | **$3.375 (~$3.38)** |

**Calculation:** (40 × $0.0375) + (10 × $0.125) + (5 × $0.125) = $3.375. Blended inference cost per request = $3.375 / 55 = $0.06136.

This estimate excludes infrastructure, storage, human-in-the-loop costs, caching benefits, and additional model calls. Model selection is a proposed architecture, not a verified description of the current implementation.

## Cost Model
| Cost Category | Per-User/Month | Notes |
|---|---:|---|
| Inference (primary model) | $1.88 | Claude Opus: 10 CV generations + 5 regenerations |
| Inference (cascading/triage) | $1.50 | Claude Sonnet: 40 job-fit assessments |
| Infrastructure | $0.50 | Estimated hosting and backend costs |
| Data/storage | $0.20 | Estimated Career Knowledge Base and CV storage |
| Human-in-the-loop | $0.00 | Users review their own outputs; no paid human review |
| **Total AI COGS** | **$4.08** | **Estimated cost per active user/month** |

## Cascading Strategy
**Triage model:** Claude Sonnet
**Frontier model:** Claude Opus
**Routing rule:** Route job-fit assessments to Sonnet. Route tailored CV generation and regeneration to Opus, where deeper reasoning and accurate use of professional evidence are critical.
**Expected cascade ratio:** 73% Sonnet / 27% Opus (based on 40 assessments and 15 CV operations per month).

## Pricing Model
**Pricing strategy:** Penetrate — accessible pricing to encourage adoption among job seekers.  
**Unit of work:** AI-assisted job application (job-fit assessment plus a tailored CV). Additional usage is sold in packs rather than charged for every individual model call.  
**Current pricing:** Free prototype; no monetization implemented.  
**Proposed AI pricing:** $14.99/month, including 40 job-fit assessments, 10 tailored CV generations and 5 CV regenerations. Additional usage pack: $4.99 for 10 assessments and 3 CV generations/regenerations.  
**Model:** Hybrid — monthly subscription plus usage-based add-ons.

The subscription and add-on prices are hypotheses, not validated customer willingness to pay. Add-on revenue is excluded from the base margin calculation.

# Margin Calculator
| Input | Base Scenario | Stress (Inference 3x) |
|---|---:|---:|
| Avg requests/user/month | 55 | 55 |
| Cost per request (blended inference only) | $0.0614 | $0.1841 |
| Monthly COGS per user | $4.08 | $10.83 |
| Revenue per user/month | $14.99 | $14.99 |
| Gross margin per user | $10.92 | $4.16 |
| **Gross margin %** | **72.8%** | **27.8%** |

**Calculation:** Base COGS = $3.375 inference + $0.70 other costs = $4.075. Stress COGS = (3 × $3.375) + $0.70 = $10.825. Gross margin = revenue − COGS; gross margin % = gross margin / revenue.

**Key finding:** The proposed price produces an estimated 72.8% gross margin in the base case, but only 27.8% if inference costs triple—below the course's 40% stress threshold. Cost optimization, usage limits, or pricing changes would be needed. These figures exclude payment processing fees, customer acquisition, support overhead and taxes.

## Stress Tests
| Scenario | Impact on Margin | Response |
|---|---|---|
| Inference costs 3x | COGS $10.83; gross margin **27.8%** (down 45.0 percentage points) | Optimize routing and prompts, evaluate caching, enforce included usage limits, and revisit pricing if the increase persists. |
| Heavy-user workload doubles | **Illustrative heavy-user case:** if requests and inference costs double to 110 requests while price remains $14.99, COGS $7.45 and gross margin **50.3%**. This is a per-heavy-user scenario, not a forecast of the overall customer mix. | Monitor usage by cohort; cap included CV generations and offer paid usage packs to protect margins. |
| Model provider raises prices 50% | If all inference prices rise 50%, COGS $5.76 and gross margin **61.6%** (down 11.3 percentage points). | Test alternate providers, compare quality/cost, and retain the ability to switch model routing. |

**Stress-test assumptions:** Revenue remains $14.99/month; non-inference costs remain $0.70/user/month; no additional usage packs are purchased in the stress cases. The heavy-user scenario assumes double the base workload, not double the number of heavy users in the customer population.

**Scale decision**: The 3× inference-cost scenario reduces gross margin to 27.8%, below the 40% stress threshold. Before scaling paid acquisition, Role fit must demonstrate a credible mitigation path through model routing, usage controls, cost optimization or revised pricing.

## Board One-Pager

> **Illustrative before/after comparison, not historical financial performance.** Role Fit has no previous paid SaaS offering. To make the course comparison meaningful, both scenarios use the same hypothetical $14.99 subscription price and 1 active paying user. The "before" scenario assumes only $0.70 in non-AI delivery costs; it is a simplified non-AI benchmark, not an actual prior product.

| Metric (per user/month) | Before: Hypothetical Non-AI SaaS | After: Proposed AI-Enabled Product |
|---|---:|---:|
| Revenue | $14.99 | $14.99 |
| COGS | $0.70 | $4.08 |
| Gross profit | $14.29 | $10.92 |
| Gross margin | 95.3% | 72.8% |

**Before (traditional SaaS):** Hypothetical $14.99/month subscription with $0.70 of infrastructure and storage costs; $14.29 gross profit and 95.3% gross margin. This benchmark assumes no AI inference or human review costs.

**After (AI-enabled):** Proposed hybrid subscription of $14.99/month plus optional usage packs, with $4.075 estimated base COGS; $10.915 gross profit and 72.8% gross margin before add-on sales.

**Net margin shift:** **−22.5 percentage points** in gross margin and **−$3.38** in gross profit per user/month at the same subscription price, due to AI inference. This is a modeled cost of adding AI, not an observed decline in Role Fit margins.

**Board narrative:** AI-assisted fit assessment and CV tailoring create the core user value, but add variable inference costs. The proposed $14.99 hybrid plan preserves a positive base gross margin while usage caps and add-on packs help manage intensive use. Under a 3× inference-cost shock, margin falls below 40%, so provider portability, routing optimization, and disciplined usage limits are key economic safeguards. Higher revenue or retention from AI has not yet been validated.