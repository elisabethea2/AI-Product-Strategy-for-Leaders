# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops
| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Do users fix AI outputs? Is that signal captured and reused? | No capture | Automated retraining | 2/5 |
| **Preference** | Does the product learn individual / team preferences over time? | Stateless | Deep personalization | 2/5 |
| **Domain Context** | Does usage in one area improve quality in adjacent areas? | Siloed | Cross-domain transfer | 3/5 |
| **Network** | Does each new user / team make the product better for everyone? | Isolated | Strong network effects | 1/5 |

### Correction Loop - 2/5
**What you capture today:**
User edits to AI-generated CV content, manual evidence additions and revised job-fit assessments.
**How it compounds:**
Corrections enrich the Career Knowledge Base and can improve future assessments when saved as reusable evidence. No automated learning from edits yet.


### Preference Loop - 2/5
**What you capture today:**
Persistent career profile, selected CV content, job-specific guidance and application decisions.
**How it compounds:**
Reusable profile context supports personalization across applications, but preferences are not yet systematically learned from user behavior.

### Domain Context Loop - 3/5
**What you capture today:**
Structured work history, project details, skills, supporting evidence and job requirements.
**How it compounds:**
Evidence captured for one application can support fit assessments and tailored CVs for other roles and industries within the same user's Career Knowledge Base. This creates individual-level compounding value, but does not yet enable cross-user learning or model retraining.

### Network Loop - 1/5
**What you capture today:**
Private, user-specific career data and application records.
**How it compounds:**
No cross-user learning or network effects currently exist. Each user's data benefits only their own experience.

**Total Flywheel Score: 8/20**
**Weakest Loop:**
Network
**Fix for weakest loop:**
Introduce privacy-preserving, opt-in aggregation of anonymized feedback and job requirement patterns to improve recommendations across users.
---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:**
LinkedIn (Microsoft)
**Vector:**
LinkedIn could integrate AI-powered job-fit assessments, tailored CV generation and application tracking directly into its existing job-search platform, leveraging its professional profiles, job listings and established user base.
**Time-to-threat:**
12–24 months
**% of value at risk:**
70%

### 2. Vertical Competitor
**Attacker:**
Teal
**Vector:**
Teal already offers job tracking and AI-assisted resume tailoring. It could deepen its personalization capabilities by building a structured Career Knowledge Base, connecting professional evidence to job requirements and generating more context-aware applications.
**Time-to-threat:**
3-6 Months
**% of value at risk:**
80%

### 3. Adjacent Expansion
**Attacker:**
Anthropic (Claude Code)
**Vector:**
General-purpose AI coding agents could enable users to build their own personalized job-search workflows, including career profiles, job-fit assessments, application tracking and tailored CV generation, reducing the need for a dedicated product like Role Fit.
**Time-to-threat:**
Already possible for technical users; 6–12 months for broader adoption (estimate).
**% of value at risk:**
60%

---

## 90-Day Encroachment Plan
**Attacker:** 
LinkedIn (Microsoft)
**Attack vector (target the weakest loop):**
Role Fit has no network effects (1/5). Each user's data benefits only that individual, while LinkedIn already has an established professional network, job listings and a large user base.
**Weeks 1-4 - what they ship:**
Launch an AI Job Application Assistant that evaluates job fit and generates tailored CVs using existing LinkedIn profiles and job descriptions.
**Weeks 5-8 - how they poach users:**
Promote the assistant directly within LinkedIn's job-search experience. Offer easy access with no separate registration or career profile setup.
**Weeks 9-12 - why users don't come back:**
Users can discover jobs, assess their fit and prepare applications within one platform. Switching to Role Fit requires additional effort without an immediately obvious benefit.

**Your defense:**
Build a deeper, evidence-based Career Knowledge Base that captures detailed projects, achievements and professional experience beyond LinkedIn profiles. Strengthen the Correction and Preference loops so the product becomes increasingly personalized and accurate with use.