# Part D: Prototype Notes

**Student ID:** x25108093  
**Prototype file:** `prototype.html` (repository root, served via GitHub Pages)

---

## What Was Built

`prototype.html` is a fully working, browser-native alpha prototype of the MangoMind HR dashboard. It requires no backend, no API keys, and no external dependencies — it runs entirely in-browser with vanilla HTML, CSS, and JavaScript.

### Core Interactions Demonstrated

1. **Signal Input Panel** — Four range sliders simulate the four core signal types MangoMind would collect from workplace tools (after-hours messages, meeting density, sentiment, response latency). Each slider represents a team-level aggregate on a 0–100 scale.

2. **Live Burnout Risk Index** — A circular SVG gauge updates in real time as sliders change. The BRI (0–100) is computed by a weighted formula: `BRI = (s1 × 0.35) + (s2 × 0.25) + (s3 × 0.25) + (s4 × 0.15)`, reflecting the relative predictive weight assigned to each signal category.

3. **Risk Classification & Colour Coding** — Five BRI bands (Healthy, Mild, Moderate, High, Critical) map to colours (green → red), category labels, and plain-language descriptions, simulating what an HR manager sees.

4. **Trend vs. Baseline** — The prototype computes a delta against a hard-coded 4-week baseline of 42, displaying trend direction (improving/stable/worsening) — the core product differentiator (team-vs-own-baseline, not cross-company comparison).

5. **Recommendation Cards** — At BRI > 50, actionable HR intervention buttons appear (simulated: "View EAP Resources", "Log HR Intervention", "Schedule Team Check-in"), with realistic button-click feedback.

6. **4-Week Sparkline** — A visual trend bar chart shows a simulated team history plus the current BRI, providing the temporal context that is central to the product's value.

7. **Transparency Panel** — Documents exactly what MangoMind tracks (✓) and does not track (✗), fulfilling EU AI Act Article 50 transparency obligations in the product UI itself.

---

## Prototype Limitations (Alpha)

- BRI formula is a weighted arithmetic average — production system uses an ML model calibrated against MBI
- Signals are manually input via sliders — production system is fully automated via API integrations
- No authentication, no real data storage, no multi-team comparison
- Historical data is hard-coded (not persisted between sessions)
- Accessibility: basic but not WCAG 2.1 AA certified

---

## How to Access

GitHub Pages URL: `[repo-root]/prototype.html`  
Navigation links from `index.html` and `pitch.html` link directly to this file.

---

*Part D: Prototype — MangoMind Innovator Critique, x25108093*
