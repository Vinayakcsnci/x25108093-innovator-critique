# Innovator Critique: From Pipeline to Position
## Briefing Document

**Module:** Customer Engagement and Artificial Intelligence (H9CEAI)  
**Assessment:** Innovator Critique: From Pipeline to Position  
**Student ID:** x25108093  
**Programme:** MSCAIBUS1 / MSCAI  
**Lecturer:** Victor del Rosal  
**Date:** 14 April 2026  
**Venture:** MangoMind — AI-Powered Employee Burnout Risk Intelligence for Irish SMBs

---

## Pipeline Parameters

*Note on parameter selection: The AI Innovator interface at https://victordelrosal.com/ai-innovator/ requires interactive JavaScript rendering to reveal the pipeline prompt text. The static HTML was not machine-readable. I resolved this ambiguity by selecting my own parameters, as the brief permits: "If any instruction in this brief is unclear, state the doubt explicitly and make your own reasoned decision." I selected parameters that would generate a coherent, researchable, and commercially credible venture.*

| Parameter | Value |
|-----------|-------|
| Country | Ireland |
| Fruit | Mango |
| Animal | Dolphin |
| Action | Track |
| Wild Card (5th) | Burnout |

**Venture Name:** MangoMind  
**Venture Description:** AI-powered, privacy-preserving burnout risk intelligence platform for Irish SMBs. Anonymously tracks team-level behavioural signals from Slack, Teams, and Calendar metadata to surface a Burnout Risk Index (BRI) for HR managers — with no individual employee identification.

---

## Repository & URLs

| Item | Value |
|------|-------|
| **GitHub Repository** | https://github.com/Vinayakcsnci/x25108093-innovator-critique |
| **GitHub Pages – Landing Page** | https://vinayakcsnci.github.io/x25108093-innovator-critique/index.html |
| **GitHub Pages – Pitch Deck** | https://vinayakcsnci.github.io/x25108093-innovator-critique/pitch.html |
| **GitHub Pages – Prototype** | https://vinayakcsnci.github.io/x25108093-innovator-critique/prototype.html |
| **Initial Commit Hash** | *(recorded after push — see repository)* |
| **Prototype Commit Hash** | *(recorded after push — see repository)* |

---

## Part A: Regulatory Audit of Own Artefacts

*(Full table in `Part-A/regulatory-audit.md`)*

| Artefact | Issue | Severity | Quoted Offending Text | Regulatory Basis | Recommended Fix |
|----------|-------|----------|-----------------------|-----------------|-----------------|
| `index.html` | Unsubstantiated "3 weeks before" claim — no clinical trial | **High** | "Know your team is burning out 3 weeks before they do" | EU AI Act Art. 13; CPA 2007 s.43 | Qualify with pilot data caveat and UCD study reference |
| `pitch.html` | €11B figure overstates employer-specific cost by ~3x | **High** | "€11B — Annual cost of workplace mental health to Irish businesses" | EU AI Act Art. 13; CPA 2007 s.43 | Change to €3.7B (Mental Health Reform, Counting the Cost, 2022) |
| `pitch.html` | 78% IBEC statistic is unverifiable — hallucinated source | **High** | "78% of burnout-related departures… (IBEC 2023)" | CPA 2007 s.43; GDPR Art. 5(1)(d) accuracy | Replace with verifiable IBEC 2023 figure (54% reactive-only) |
| `index.html` | DPIA asserted without published summary or DPC reference | **High** | "fully GDPR-compliant and operates under a completed DPIA" | GDPR Art. 13, 35; Irish DPC Guidance | Publish DPIA summary; name DPO; state DPC consultation status |
| `index.html` | EU AI Act self-classification as limited-risk — not legally verified | **High** | "MangoMind is classified as a limited-risk AI system" | EU AI Act Annex III (4)(a); Art. 6 | Obtain legal opinion; add qualification pending formal review |
| `pitch.html` | 94% retention from n=5 is arithmetically incoherent | **Medium** | "94% Beta customer retention at 90 days" | Irish CPA 2007 s.42; CCPC testimonial guidance | Change to "80% retention (4/5), n=5 beta cohort — early signal" |
| `index.html` | "ISO 27001 certification in progress" implies near-completion | **Medium** | "ISO 27001 certification in progress" | CPA 2007 s.43 (misleading omission) | Restate as "pursuing certification; expected Q4 2026" |
| `index.html` | No accessibility statement for a health-adjacent product | **Low** | Landing page — no WCAG notice | SI 358/2020 (Web Accessibility); Irish Disability Act 2005 | Add WCAG 2.1 AA conformance statement |

**Regulatory Risk Posture (≤100 words):**  
MangoMind's artefacts carry material legal exposure across three vectors. The EU AI Act self-classification as limited-risk is the most urgent: if Annex III (4)(a) applies to workplace wellbeing monitoring in an employment context — which legal counsel must determine before launch — deployment without a conformity assessment constitutes non-compliance as of August 2024. Separately, three statistics in the artefacts are unverifiable or arithmetically incoherent, creating Irish consumer law exposure. The GDPR DPIA assertion without any supporting disclosure fails Article 13 obligations. None of these issues are fatal, but none should survive into a commercial launch without correction.

---

## Part B: Trust Transfer Audit

*(Full analysis in `Part-B/trust-transfer-audit.md`)*

**Auditor persona:** CIPD-qualified HR Manager, 65-person Irish tech startup, personally affected by burnout-related team departure in 2024.

**Moment 1 — Precision without evidence:**  
*"Know your team is burning out 3 weeks before they do"* (`index.html`, hero)  
An HR manager with clinical literacy knows burnout onset is a process, not a discrete event. The claim of 3-week advance detection without a single cited study, trial, or methodology reads as hallucinated precision. The specific number signals either unpublished evidence or pipeline output that no one pushed back on — neither of which builds trust.

**Moment 2 — Arithmetic failure in traction data:**  
*"94% Beta customer retention at 90 days"* (`pitch.html`, Slide 8 — Traction)  
This statistic is computed on n=5 customers. 94% of 5 is 4.7 customers — a non-integer retention rate. Any HR manager who has reviewed SaaS tool proposals knows what a 5-customer beta looks like. A percentage that cannot be calculated from the stated cohort size destroys the credibility of every other number in the deck.

**Moment 3 — Compliance assertion without substance:**  
*"Our system is fully GDPR-compliant and operates under a completed Data Protection Impact Assessment (DPIA)."* (`index.html`, Privacy section)  
Before deploying any data monitoring tool to 65 employees, the HR manager's legal team will ask for the DPIA summary. There is no link, no DPO contact, no DPC consultation reference. Claiming compliance without any supporting documentation for a tool that monitors worker behaviour is not reassurance — it is a red flag.

---

## Part C: Research and Correct

*(Full report and corrections in `Part-C/research-and-correct.md`)*

**Changes made to `index.html` and `pitch.html`:**

| Error | Original | Corrected | Severity |
|-------|----------|-----------|---------|
| €11B employer cost figure | "€11B annual cost to Irish businesses" | "€3.7B annual cost to Irish employers (Mental Health Reform, 2022)" | High |
| IBEC 78% hallucinated statistic | "78% of departures, warning signs unacted (IBEC 2023)" | "54% of HR managers use reactive-only approach (IBEC Workplace Wellbeing Survey, 2023)" | High |
| €14K CIPD attribution | "€14K average cost (CIPD Ireland 2024)" | "€10K–€14K estimated, based on CIPD UK benchmarks adjusted for Irish market, 2024" | Medium |
| "3 weeks before" unqualified | "Know your team is burning out 3 weeks before" | Added: "based on beta pilot data, n=5 teams. Clinical validation with UCD in progress Q3 2026" | High |
| EU AI Act self-declaration | "classified as a limited-risk AI system" | "designed to qualify as limited-risk; formal classification review in progress with legal counsel" | High |
| 94% retention metric | "94% Beta customer retention at 90 days" | "80% retention (4 of 5 beta customers, n=5 cohort — early signal only)" | Medium |

**Do these errors significantly alter the project?** The core proposition is intact. The statistical hallucinations inflate the market case but do not fabricate it — workplace mental health costs are real and significant. The EU AI Act issue is the most material: a high-risk determination would add 6–12 months to the compliance roadmap, reshape the capital allocation in Part F, and require a conformity assessment before any customer deployment. The product is viable; the artefacts were overconfident.

---

## Part D: Prototype

**File:** `prototype.html` (repository root, served via GitHub Pages)

MangoMind's alpha prototype demonstrates the core value proposition: an HR manager sees a team-level Burnout Risk Index (BRI) computed in real time from four signal-category sliders, colour-coded from green (healthy) to red (critical), compared against a 4-week rolling baseline. The prototype includes:

- Live BRI gauge (SVG, real-time weighted formula: after-hours 35%, meetings 25%, sentiment 25%, latency 15%)
- Risk category labels and plain-language recommendations
- Trend vs. baseline indicator (improving/stable/worsening)
- Actionable HR buttons at elevated BRI
- 4-week historical sparkline
- Full transparency panel documenting what the system tracks and explicitly does not track (including "✗ Message content — never read" and "✗ Individual employee scores — never shown")

No backend required. Runs entirely in-browser. Zero external dependencies.

*(Full prototype notes in `Part-D/prototype-notes.md`)*

---

## Part E: Business Modelling

**Position: Ship with Named Conditions (Option b)**

*(Full analysis in `Part-E/business-modelling.md`)*

MangoMind should not ship in 90 days in its current state, but the venture is viable and the €2M offer should be taken. Three non-negotiable conditions must be met before launch:

**Condition 1: EU AI Act conformity assessment completed**  
Without a formal legal opinion confirming limited-risk status, shipping constitutes regulatory non-compliance. A DPC complaint would destroy the trust capital the product depends on. Timeline: 90 days. Cost: €25K.

**Condition 2: IBEC/ICTU joint engagement completed; model union clause agreed**  
Irish employment law context requires engagement with employee representatives before deploying behavioural monitoring. Without this, MangoMind cannot enter any unionised workplace, which constrains the addressable market significantly. Timeline: 60–90 days. Cost: €10K.

**Condition 3: All artefact statistics independently verified and corrected**  
Three claims are currently unverifiable or wrong (see Part C). An investor who detects fabricated statistics during diligence will withdraw. This is a 2-week desk research exercise. Cost: zero.

**Advisory stress-test dissent (key):** Four advisors challenged the pitch. Legal counsel flagged EU AI Act exposure. A CFO flagged the n=5 retention metric. A clinical psychologist flagged the detection claim. A trade union official flagged union engagement absence. All four dissenting voices pointed to the same root failure: the pipeline generated a polished-sounding product that skipped the hard work of validation.

**Pre-mortem failure modes:** (1) EU AI Act misclassification triggers DPC investigation; (2) customer misuses BRI data in an employment decision — MangoMind faces negligence exposure; (3) clinical detection claim is challenged in media, destroying brand trust.

**Scenario analysis:**

| Scenario | Year 1 ARR | Year 3 ARR | Key Variable |
|----------|-----------|-----------|-------------|
| Best case | €720K | €9.2M | IBEC endorsement + EAP partnership |
| Base case | €450K | €6.3M | Organic growth, 25→280 customers |
| Worst case | €180K | €2.1M | AI Act high-risk classification delays 6 months |

---

## Part F: The Plan

*(Full line-item budgets in `Part-F/the-plan.md`)*

### 90-Day Plan Summary (€274K deployed of €1M first tranche)

**Critical path: regulatory compliance before customer acquisition.**

| Priority | Activity | Budget |
|----------|----------|--------|
| 1 | Legal: EU AI Act conformity assessment | €25K |
| 2 | DPO (fractional) + GDPR DPIA | €21K |
| 3 | Hire Senior ML Engineer (Week 4) | €21K (3mo) |
| 4 | Hire Head of Product/Design (Week 6) | €14K (1.5mo) |
| 5 | Fix all artefact statistics (Week 2) | €0 |
| 6 | IBEC/ICTU engagement | €10K |
| 7 | Sales & marketing (IBEC pipeline, CIPD presence) | €48K |
| 8 | Infrastructure, operations, advisors | €135K |
| **Total** | | **€274K** |

**Key milestones:** DPIA filed (Week 8); AI Act opinion received (Week 10); Teams integration live (Week 12); IBEC engagement complete (Week 10).

### 180-Day Plan Summary (additional €543K deployed; €183K held as reserve)

| Priority | Activity | Budget |
|----------|----------|--------|
| New hires | AE, CSM, Senior Backend Engineer | €245K (6mo) |
| UCD clinical validation study | €40K |
| Sales & marketing (EAP partnership, PR launch, content) | €103K |
| ISO 27001 audit commencement | €20K |
| Ongoing legal + compliance | €25K |
| Infrastructure + operations | €60K |
| **Total Days 91–180** | | **€543K** |

**Key milestones:** 10 paying customers (Week 16); 20 customers / €200K+ ARR (Week 24); Laya Healthcare EAP partnership signed (Week 22); Series A data room complete (Week 24).

### What We Are Deliberately NOT Doing

- **UK expansion before Day 180:** Ireland is proof-of-concept. UK entry is a Series A objective.
- **Enterprise (250+ employees) sales:** SMB wedge first; enterprise procurement cycles are too long at this stage.
- **Custom AI model from scratch:** Fine-tuned BERT + federated learning is sufficient; proprietary training data is Year 2.
- **Acquisitions:** No M&A before Series A.
- **PR agency retainer:** Direct outreach; freelance PR at €3–5K/campaign vs. €8–12K/month agency.

### Full 180-Day Capital Summary

| Category | Total Spend | % of €2M |
|----------|-------------|----------|
| Salaries (8 FTE + fractionals) | €410K | 20.5% |
| Legal & Compliance | €80K | 4% |
| Sales & Marketing | €151K | 7.55% |
| Clinical Research (UCD) | €40K | 2% |
| Infrastructure | €45K | 2.25% |
| Product & Engineering (tools) | €45K | 2.25% |
| Operations, Admin, Advisors | €56K | 2.8% |
| **Total deployed** | **€827K** | **41.35%** |
| **Reserve (runway + strategic)** | **€1,173K** | **58.65%** |

The reserve provides 14+ months of runway beyond Day 180 at the projected burn rate of ~€82K/month, targeting Series A at ≥€2M ARR (projected Q2 2027).

---

## Reflection on AI Use

This assessment was completed with the AI Innovator pipeline (for pipeline content generation) and Claude Code (for file structure, critique drafting, code, and research verification). The pipeline generated a coherent venture concept rapidly. The critique work — identifying hallucinations, verifying statistics, conducting legal analysis, and taking a defensible position — was human-led and AI-assisted rather than AI-generated. The 78% IBEC statistic and the 94% retention metric were hallucinations that the pipeline produced without flagging; only independent research surfaced them. This is the trust transfer problem in practice: the artefacts looked professional enough that a non-critical reader would not question them. Critical thinking, not tooling, determined whether the output was fit for purpose.

---

*Innovator Critique Briefing Document — x25108093 — NCI MSCAI 2026*
