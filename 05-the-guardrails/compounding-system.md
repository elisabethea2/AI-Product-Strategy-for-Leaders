# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | User corrections to Fit Analysis, including additional evidence of skills and experience | Updated Career Profile used to improve future job-fit assessments and reduce repeated mismatches. | Y | active |
| Cross-Domain Transfer | Skills, experience and evidence added to the Career Profile through Fit Analysis and other product workflows | Shared profile knowledge improves both future Fit Analysis results and Tailored CV generation. | Y | active |
| Network Intelligence | Potential future input: anonymized and aggregated patterns from user corrections, skill gaps and job-fit assessments. | Potential future output: improved matching criteria and identification of recurring assessment errors across users, without exposing personal data. | N | missing |

*Learning scope*: Recursive Learning currently operates at the individual user level. Corrections enrich the Career Profile and improve future AI outputs through reusable context, without retraining the underlying model. Cross-user learning remains a future capability.

**Broken loop identified by partner:** Network Intelligence is missing. User corrections improve individual profiles but do not contribute to product-wide learning.
**Fix plan:** Introduce an opt-in, privacy-preserving feedback pipeline that aggregates recurring corrections and matching errors across users. Review patterns regularly and use validated findings to improve Fit Analysis criteria, without exposing personal data.

## Context Connectivity

**How knowledge flows:** User corrections and edits from Fit Analysis and Tailored CV are saved to the central Career Profile. This shared knowledge is reused across product features, continuously improving personalized assessments and CV generation.

**Where it silos:** Knowledge remains isolated within individual user profiles. Corrections and recurring assessment errors are not aggregated across users, preventing product-wide learning and improvement of matching criteria.

## Governance Policy

**Scope:** AI-powered features within Role Fit, including CV parsing and profile extraction, job-fit assessments, skills matching, personalized recommendations, and tailored CV generation. Covers AI processing of user career data, automated assessments, user corrections, and human oversight. Excludes: Non-AI operations such as user authentication, manual application status updates, and document storage without AI processing. These functionalities remain subject to standard security and data protection policies. External recruitment platforms and employer hiring decisions are outside Role Fit's control.

**Autonomy boundaries:** Modify or replace existing Career Profile information, human approval required. Submit job applications or contact recruiters on behalf of users, never auto. Share personal career data with third parties without explicit authorization, never auto.

**Escalation triggers:** 
1. AI confidence falls below 70% when extracting or matching career information. 
2. AI-generated information conflicts with existing Career Profile data. 
3. The AI identifies missing or ambiguous evidence for an essential job requirement. 
4. Any AI-generated change to the Career Profile requires user confirmation before saving. 
5. Any action involving external sharing of personal data or submission of job applications requires explicit user authorization. 
6. Users report incorrect, misleading, or potentially discriminatory AI assessments.

**Audit cadence:** Real-time, Critical errors, unauthorized actions and personal data exposure. (System monitoring / Product Owner). Weekly, User corrections, incorrect job-fit assessments and AI extraction errors. (Product Owner). Monthly, AI accuracy, bias patterns, evaluation results and model performance drift. (Product Owner / AI Engineer). Quarterly, Governance policy, privacy controls, regulatory compliance and escalation procedures. (Product Owner / Security & Privacy Lead).

**Regulatory exposure (EU AI Act / other):** EU General Data Protection Regulation (GDPR), Swiss Federal Act on Data Protection (FADP), EU AI Act (subject to applicability assessment).. Controls: Privacy-by-design and data minimization; explicit user consent for data processing and sharing; encryption of personal data; role-based access controls; user approval for AI-generated profile changes; transparent AI assessments and explanations; audit logs; data retention and deletion policies; regular bias and accuracy testing; human oversight and incident response procedures..

## Agent Topology

Proposed agent architecture: The following agents represent the target operating design. Their responsibilities and approval boundaries do not imply that all agents are currently implemented as independent components.

1. Career Profile Agent
Can extract and structure career information from uploaded CVs and user inputs. Cannot modify or delete existing profile data without user confirmation. Approval: User.

2. Job Fit Analysis Agent
Can analyze job descriptions, match requirements against the Career Profile, calculate fit scores and identify skill gaps. Cannot invent qualifications or make final employment decisions. Approval: Product Owner for changes to assessment criteria.

3. Tailored CV Agent
Can generate personalized CV drafts and recommend relevant skills and experience. Cannot fabricate achievements, overwrite approved profile information or submit applications without explicit authorization. Approval: User.

4. Learning & Quality Agent
Can monitor AI performance, analyze anonymized feedback patterns and recommend improvements to matching criteria. Cannot access identifiable user data across accounts or deploy model changes autonomously. Approval: AI Engineering Lead and Product Owner.


## Shadow AI Audit

| Tool / Workaround | Owner / Signal Source | Risk Level | Decision |
|---|---|---|---|
| ChatGPT for interview preparation | User interviews | H | Build |
| Spreadsheets for application analytics | Support tickets | M | Build |
| External AI for cover letter generation | User interviews | H | Build |
| ChatGPT to verify Fit Analysis scores | User feedback | M | Build |
| External job alerts and automation tools | User interviews | H | Partner |

**Total tools found:** 5
**Tools after triage:** 4 Build candidates
**Estimated hidden spend:** $75/month (illustrative)

### Shadow AI Audit — Role Fit Roadmap Brief

**Audit findings**

Five user-side AI workarounds were identified, revealing capability, workflow and trust gaps in Role Fit's current offering.

- **Decisions:** 4 Build · 1 Partner · 0 Ignore
- **Estimated adjacent spend:** $75/month (illustrative, based on audit assumptions)
- **Dominant signal:** Capability gap (tied with Workflow gap in the five identified cases)

**Strategic recommendations**

Prioritize improvements based on user frequency, strategic relevance and their ability to strengthen Role Fit's core value proposition.

**Priority 1 — Strengthen the core product**
- Improve Fit Analysis explainability to increase user trust in AI-generated assessments.
- Introduce application analytics to identify rejection patterns and help users improve their job-search strategy.

**Priority 2 — Expand career support capabilities**
- Build AI-powered cover letter generation using Career Profile data.
- Introduce personalized interview preparation based on job requirements, identified gaps and user experience.

**Priority 3 — Expand through partnerships**
- Integrate external job discovery and alert providers through authorized APIs or partnerships, avoiding the cost of maintaining multiple independent job data sources.

**Next steps**

Validate the five workarounds through user research, assess technical feasibility and prioritize delivery based on expected impact and implementation effort. Monitor adoption and user satisfaction, and repeat the Shadow AI Audit quarterly to identify emerging needs and competitive threats.


## Responsible AI Maturity Scorer

**Total: 18/25, Proactive**
Solid foundation. Now make governance a competitive advantage.
Weakest: Compliance, Fairness

**Compliance: 3/5**
1 = no formal compliance, 5 = certified and audited

**Transparency: 4/5**
1 = black box, 5 = full explainability + audit trails

**Fairness: 3/5**
1 = no bias testing, 5 = continuous monitoring + remediation

**Privacy: 4/5**
1 = minimal consent, 5 = privacy-by-design + user controls

**Accountability: 4/5**
1 = no owner, 5 = RACI defined + incident playbooks
