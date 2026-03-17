# Raise Ready – Fundraising Co‑Founder Agent for Women's Health Startups

Raise Ready is an agentic AI workflow that helps women's health founders sharpen their investor narrative and identify gaps in their pitch materials before they go out to raise.

It is designed as a **co‑founder‑style assistant**: it reads your deck text, diagnoses what today’s health/AI investors expect to see at your stage, and proposes a clearer, more compelling story. It does **not** invent metrics or outcomes.

---

## What This Agent Does

- Parses a pitch deck text dump into structured sections (Problem, Solution, Market, Traction, Team, AI story, GTM, Financials, Ask).
- Performs a stage‑aware gap analysis (e.g., pre‑seed vs seed) against a lightweight fundraising checklist.
- Highlights missing or weak sections with explanations tailored to **women’s health and digital health**.
- Optionally generates a revised narrative outline and investor‑profile‑specific talking points.

This repo is the **portfolio implementation** for The Faulkner Group’s “Raise Ready” service.

---

## Architecture

Raise Ready is implemented as a small LangGraph workflow:

1. **IngestionAgent**
   - Input: raw deck text (e.g., exported from slides or pasted).
   - Output: structured `deck_analysis` JSON (sections and raw text).

2. **GapAnalysisAgent**
   - Input: `deck_analysis` + stage checklist.
   - Output: `gap_analysis` JSON (section reviews, missing sections, risk flags, overall comment).

3. **(Optional) NarrativeAgent**
   - Input: `deck_analysis` + `gap_analysis`.
   - Output: `narrative_outline` JSON (revised slide sequence and bullets).

State is passed through a simple `FundraiseState` object:

```python
class FundraiseState(TypedDict):
    deck_text: str
    deck_analysis: Dict[str, Any]
    gap_analysis: Dict[str, Any]
    narrative_outline: Dict[str, Any]
