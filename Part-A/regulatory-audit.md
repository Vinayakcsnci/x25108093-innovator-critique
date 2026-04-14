# Part A: Regulatory Audit of MangoMind Artefacts

**Student ID:** x25108093  
**Artefacts audited:** `MangoMind/index.html`, `MangoMind/pitch.html`  
**Regulatory frameworks:** EU AI Act, GDPR, Irish Consumer Law (CPA 2007 / CCPC), Health & Safety legislation

---

## Regulatory Audit Table

| Artefact | Issue | Severity | Quoted Offending Text | Regulatory Basis | Recommended Fix |
|----------|-------|----------|-----------------------|-----------------|-----------------|
| `index.html` | Unsubstantiated claim: "AI detects burnout 3 weeks before crisis" — no clinical trial evidence cited; makes it a misleading commercial practice | **High** | *"Know your team is burning out 3 weeks before they do"* (hero headline) | EU AI Act Art. 13 (transparency & documentation); GDPR Art. 22 (automated decision-making implications); Irish CPA 2007 s.43 (misleading commercial practices) | Replace with a qualified claim: "MangoMind surfaces team-level risk signals up to 2–3 weeks before self-reported burnout, based on our pilot cohort of n=5 teams." Add footnote linking to methodology. |
| `pitch.html` | Unverified statistic: "€11B annual cost" cited without primary source in the deck | **High** | *"€11B — Annual cost of workplace mental health to Irish businesses"* (Slide 2) | EU AI Act Art. 13 (accuracy of claims); Irish CPA 2007 s.43 | Add attribution: "Source: Mental Health Reform, Ireland 2024 economic analysis" — verify source is accurate before citing. If source cannot be verified, remove or qualify. |
| `pitch.html` | Unverified statistic: "78% of burnout-related departures where retrospective warning signs were visible" — attributed to IBEC 2023, not independently verifiable | **High** | *"78% of burnout-related departures where retrospective warning signs were identified but not acted upon (IBEC 2023)"* (Slide 2) | GDPR Recital 71 (accuracy principle); Irish CPA 2007 s.43; EU AI Act Art. 13 | Verify IBEC 2023 report and cite precisely. If the figure cannot be located, remove and replace with verified data from CIPD Ireland or HSA Ireland. |
| `index.html` | GDPR transparency obligation not fully met: landing page claims DPIA is "completed" but no summary or DPC consultation reference is provided to users | **High** | *"Our system is fully GDPR-compliant and operates under a completed Data Protection Impact Assessment (DPIA)."* | GDPR Art. 13(1)(e) (purpose limitation disclosure); Art. 35 (DPIA requirement); Irish DPC Guidance on DPIAs (2023) | Publish a DPIA summary or link to it. State clearly who the Data Controller is, the DPO contact, and whether the DPC was consulted under Art. 36. |
| `index.html` | Claim "MangoMind AI is classified as limited-risk under the EU AI Act" — this is a self-classification and is not independently verified; workplace emotion/wellbeing monitoring may trigger Annex III (high-risk) classification | **High** | *"MangoMind is classified as a limited-risk AI system. Transparency obligations under Article 50 are met via mandatory employee disclosure notices."* | EU AI Act Annex III para 4 (high-risk AI in employment context); Art. 6 (classification rules); Art. 50 (limited-risk obligations) | Obtain formal legal opinion on AI Act classification. Workplace monitoring systems that infer workers' emotional or health states may fall under Annex III (4)(a) — high-risk. Until confirmed, the landing page must not assert a risk classification without a legal basis. |
| `pitch.html` | Testimonials on landing page and beta customer claims on pitch Slide 8 are unverified; Irish Consumer Protection Act requires testimonials to be genuine | **Medium** | *"94% Beta customer retention at 90 days"* (Slide 8, Traction); testimonials in `index.html` attributing names to beta users | Irish CPA 2007 s.42 (misleading commercial practices); CCPC Guidance on Testimonials (2022) | All testimonials must be genuine and on file. Retention figures must be verifiable. If the product is pre-revenue/beta, add a clear disclaimer: "Beta results from n=5 customers; not indicative of commercial-scale performance." |
| `index.html` | "ISO 27001 certification in progress" may mislead users into believing certification already exists | **Medium** | *"ISO 27001 certification in progress."* | Irish CPA 2007 s.43 (misleading omission); GDPR Art. 32 (appropriate technical measures) | Rephrase: "We are pursuing ISO 27001 certification. Current security practices include [specifics]. Certification is expected Q4 2026." Do not use certification language until certified. |
| `index.html` | No accessibility statement; landing page lacks WCAG 2.1 AA compliance indicators — relevant for a health-adjacent product marketed to employers with potential disability obligations | **Low** | Landing page overall — no accessibility notice, no skip navigation | EU Web Accessibility Directive (2016/2102) as transposed in Ireland (SI 358/2020); Irish Disability Act 2005 s.26 | Add WCAG 2.1 AA conformance statement. Conduct automated and manual accessibility audit. |

---

## Regulatory Risk Posture

MangoMind's artefacts carry material regulatory exposure across three vectors. First, the AI Act classification risk is the most serious: self-declaring as limited-risk when the system monitors worker wellbeing indicators may be legally incorrect — an Annex III high-risk designation would impose conformity assessments, registration obligations, and potentially prohibit deployment before formal authorisation. Second, unverified statistics in both artefacts create Irish consumer law exposure under the CPA 2007 if claims cannot be evidenced. Third, the GDPR DPIA claim without a published summary or DPC consultation reference is non-compliant. Legal counsel must review both artefacts before any commercial launch.

---

*Part A: Regulatory Audit — MangoMind Innovator Critique, x25108093*
