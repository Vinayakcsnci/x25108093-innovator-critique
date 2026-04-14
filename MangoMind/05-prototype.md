# MangoMind – Prototype Specification

**Pipeline Step 5**

---

## Prototype Goal

Build an **alpha prototype** that demonstrates the core value proposition: an HR manager enters a simulated week of team behavioural signal data and receives a MangoMind Burnout Risk Index (BRI) score with a plain-language recommendation.

This prototype is a **browser-based single-file demo** (`prototype.html`) — no backend required, no API keys needed. It simulates the signal ingestion, scoring, and recommendation engine using hard-coded logic and in-browser JavaScript.

---

## Prototype Scope (Alpha)

### What the prototype does:
1. Presents the HR manager with a **simulated team signal dashboard** for a fictional 8-person team
2. Shows adjustable sliders for 4 signal categories: After-Hours Messages, Meeting Density, Check-in Sentiment, Response Latency
3. Calculates a real-time **Burnout Risk Index (0–100)** from the slider inputs
4. Displays a **trend indicator** (improving/stable/worsening) based on BRI vs. a simulated 4-week baseline
5. Shows a **plain-language recommendation card** matched to the BRI range
6. Presents a **"What MangoMind tracks" explainer** panel demonstrating transparency

### What the prototype does NOT do:
- No real data integration (Slack, Teams, Calendar)
- No actual ML model — scoring is a weighted formula
- No real employee data — all signals are simulated
- No backend persistence

---

## Prototype UX Flow

```
[Landing state]
  MangoMind logo + "Team Burnout Risk Dashboard"
  Team name: "Product Team – Dublin" (simulated)
  Week: "Week of 14 April 2026"
  
[Signal Input Panel]
  Slider: After-hours messages this week    [0-100, default 45]
  Slider: Meeting density (% of day)        [0-100, default 60]
  Slider: Check-in sentiment score          [0-100, default 55]
  Slider: Avg. response latency change (%)  [0-100, default 40]

[Live BRI Display]
  Large circular gauge: BRI = [calculated]
  Colour: Green (0-30), Amber (31-60), Red (61-100)
  Trend arrow: ↑ Worsening / → Stable / ↓ Improving
  Baseline: "4-week team average: 42"

[Recommendation Card]
  BRI 0-30:  "Your team signals are healthy. Continue regular check-ins."
  BRI 31-50: "Mild elevation detected. Consider a team working-hours check-in."
  BRI 51-70: "Moderate risk. Recommend scheduling a 1:1 wellness conversation."
  BRI 71-85: "High risk. Consider activating your EAP and reducing workload this sprint."
  BRI 86+:   "Critical. Immediate HR intervention recommended. Contact EAP provider."

[Transparency Panel]
  "MangoMind only analyses: message timing, calendar patterns, and optional check-ins.
   MangoMind never reads message content. Individual scores are never shown."
```

---

## Prototype File

Output file: `prototype.html`
Location: repository root (served via GitHub Pages)

---

*Generated as Step 5 of the AI Innovator pipeline.*
