# MangoMind – Solution Design

**Pipeline Step 4**

---

## Solution Overview

MangoMind is a **team-level burnout risk intelligence platform** for Irish SMBs. It passively aggregates anonymised behavioural signals from workplace tools (Slack, Microsoft Teams, Google Calendar, email metadata), processes them through an on-device AI model, and surfaces a **team burnout risk index** to HR managers — without ever exposing individual employee data.

---

## Core Architecture

### 1. Signal Collection Layer
MangoMind integrates via OAuth with:
- **Slack / Microsoft Teams:** Message frequency, response latency, reaction usage, after-hours message timestamps (content is never read — only metadata)
- **Google Calendar / Outlook:** Meeting density, meeting-free time, back-to-back meeting frequency, declined meetings
- **Email (metadata only):** Send/receive frequency, after-hours patterns
- **Optional weekly pulse check-in:** A single-question anonymous 5-point scale ("How full is your tank this week?") delivered via Slack bot or email

### 2. On-Device Processing
All raw data is processed at source (employee device or company workspace tenant) using a lightweight on-device ML model. **No individual-level raw data leaves the processing boundary.** The model computes a **personal signal vector** which is immediately aggregated with the team cohort before transmission.

### 3. Anonymised Aggregation Layer
Personal signal vectors are aggregated using **k-anonymity with k≥5**: a team member's signal can only be included in a report if at least 5 members are in the cohort. This ensures no single individual can be inferred from the output. Aggregated team-level scores are transmitted to MangoMind's servers over TLS.

### 4. Burnout Risk Index Engine
The team-level aggregated score feeds a **Burnout Risk Index (BRI)**, a composite score (0–100) derived from:
- Signal deviation from that team's own rolling 12-week baseline (not a cross-company comparison)
- Trend velocity (rate of change, not just absolute level)
- Validated instrument mapping: BRI is calibrated against the Maslach Burnout Inventory (MBI) dimensions: Exhaustion, Cynicism, Efficacy

### 5. HR Dashboard
A clean, mobile-first dashboard displays:
- **Team BRI trend** (7-day, 30-day, 90-day)
- **Alert cards** when BRI crosses configurable thresholds
- **Recommended HR actions** (plain-language, not clinical): e.g., "Your team's after-hours messaging has increased 40% this month. Consider a team working-hours agreement."
- **Resource links:** EAP information, HSE mental health resources, MangoMind's curated intervention library

### 6. No Individual Identification — by Design
MangoMind never shows HR managers individual-level scores. The system cannot be used to identify, rank, or evaluate individual employees. This is a design constraint, not a feature toggle. It is enforced at the aggregation layer and documented in the data processing agreement.

---

## Technology Stack

| Component | Technology |
|-----------|-----------|
| Signal processing | Python, on-device (WebAssembly for web clients) |
| ML model | Fine-tuned BERT variant for metadata patterns; calibrated against MBI |
| Aggregation | Privacy-preserving federated computation (Flower FL framework) |
| Backend | Node.js + PostgreSQL (encrypted at rest, hosted on AWS eu-west-1 Dublin) |
| Dashboard | React, mobile-first PWA |
| Integrations | Slack API, Microsoft Graph API, Google Workspace API |
| Auth | OAuth 2.0; SSO via Okta/Microsoft Entra |

---

## Privacy & Compliance Design

- **GDPR legal basis:** Legitimate interests (Article 6(1)(f)) + explicit informed consent for optional check-ins; DPIA completed before deployment
- **EU AI Act classification:** Limited-risk system (emotion inference in workplace context may trigger Article 50 transparency requirements); transparency notice deployed to all employees
- **Data minimisation:** Only metadata processed; message content never accessed
- **Right to erasure:** Employee can request removal of their signal contribution; system automatically excludes on deletion request
- **Data retention:** Aggregated team scores retained 36 months; no individual-level data retained beyond 24 hours of processing

---

## Pricing

| Plan | Price | Features |
|------|-------|----------|
| Starter | €12/employee/month | Up to 25 employees, Slack/Teams integration, weekly BRI report |
| Growth | €22/employee/month | Up to 100 employees, all integrations, daily BRI, intervention library |
| Scale | €35/employee/month | 100+ employees, custom thresholds, API access, dedicated CSM |

---

*Generated as Step 4 of the AI Innovator pipeline.*
