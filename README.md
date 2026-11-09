# Role Fit — AI-Powered Job Application Copilot

> I believe that a personalized AI job application copilot, powered by a structured professional history, can help job seekers evaluate opportunities more accurately and create tailored applications faster than existing general-purpose tools.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:** Role Fit — AI-Powered Job Application Copilot
- **AI Value Archetype:** Copilot
- **Vulnerability Scores:** Moat 2/5 · Data 2/5 · Platform 1/5
- **Top Risk:** Our biggest strategic risk is that established platforms like LinkedIn could replicate our core AI capabilities and leverage their existing user base, making it difficult for us to differentiate and attract users.
- **Confidence:** Medium
- **Prototype:** https://rolefit.lovable.app/
- **Kill Criteria:** We will evaluate these kill criteria after a 90-day pilot with a representative group of target users. If the criteria are not met after reasonable corrective iterations, we will reconsider the product strategy, scope or continued investment.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 8/20
- **Weakest Loop:** Network
- **Top Encroachment Threat:** LinkedIn (Microsoft)
- **Encroachment Defense:** Build a deeper, evidence-based Career Knowledge Base that captures detailed professional experience beyond LinkedIn profiles. Strengthen correction and preference loops to improve personalization with continued use.
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** 95.3%
- **Gross Margin (AI-adjusted):** 72.8%
- **Pricing Model:** Hybrid — monthly subscription plus usage-based add-ons.
- **Pricing Today → Tomorrow:** Free prototype; no monetization implemented. → $14.99/month, including 40 job-fit assessments, 10 tailored CV generations and 5 CV regenerations. Additional usage pack: $4.99 for 10 assessments and 3 CV generations/regenerations.
- **Total AI COGS / unit:** $4.08
- **Cascading Strategy:** Triage: Claude Sonnet; frontier: Claude Opus; ratio 73% Sonnet / 27% Opus (based on 40 assessments and 15 CV operations per month).
- **Net Margin Shift:** **−22.5 percentage points** in gross margin and **−$3.38** in gross profit per user/month at the same subscription price, due to AI inference.…

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** ≥92%
- **Golden Dataset:** 11 test cases, including 4 adversarial cases
- **Confidence UX:** Tiered confidence + visible uncertainty + human in the loop trigger
- **HITL Architecture:** End-user review when confidence is below 70% or career evidence is missing or contradictory. Users approve changes to their Career Profile.
- **Failure Mode Coverage:** Prompt injection, fabricated qualifications, insufficient evidence and contradictory career records. Unsupported claims are flagged rather than invented.


→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** Individual-level learning through user corrections and cross-workflow reuse of career evidence. Network Intelligence remains a future capability.
- **Governance Posture:** Human oversight, evidence-based AI outputs, privacy-by-design, transparent assessments and controlled changes to the Career Profile.
- **Autonomy Boundaries:** AI can analyze job descriptions and prepare drafts. Changes to verified Career Profile information require user approval. Applications and recruiter communications are never submitted autonomously.
- **Escalation Triggers:** Confidence below 70%, conflicting or missing evidence, unsupported claims, unauthorized data sharing, and potentially discriminatory assessments.
- **Audit Cadence:** Real-time incident monitoring, weekly correction reviews, monthly reliability assessments and quarterly governance reviews.
- **Shadow AI Audit (user-side):** 5 potential workarounds · 4 Build candidates · 1 Partner candidate · $75/month illustrative adjacent spend.
- **Agent Boundaries:** Proposed Career Profile, Job Fit Analysis, Tailored CV and Learning & Quality agents, with defined human approval requirements.
- **Regulatory Exposure:** GDPR, Swiss FADP and EU AI Act (subject to applicability assessment).

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):** Complete core workflows, improve Career Profile import, and implement AI quality, cost, and privacy controls (0–4 weeks).
- **Horizon 2 (Next):** Run the 90-day pilot to validate usefulness, accuracy, willingness to pay, and the Career Knowledge Base's value (1–3 months).
- **Horizon 3 (Bet):** Explore job discovery integrations and opt-in Network Intelligence, subject to pilot results (3–6 months).
- **Board Narrative:** Validate Rolefit's personalized, evidence-based job application copilot before scaling. The key challenge is proving meaningful differentiation against LinkedIn and general-purpose AI tools.
- **Ask:** Hypothetical $10,000 budget, one existing Product Lead and part-time engineering support for a 90-day pilot, followed by a go/no-go decision.
- **Key Strategic Change:** From a product hypothesis in M1 to an investment strategy with measurable validation criteria, reliability targets, unit economics, governance, and a prioritized roadmap.

→ Details: [`06-the-pitch/`](06-the-pitch/)

