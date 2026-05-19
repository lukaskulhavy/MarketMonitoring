# Workflow: Research Report
# Purpose: Produce a structured market research report on any given topic
# Trigger: User provides a topic or question to research

---

## PHASE 1 — Pre-Research Interview

Before doing any research, ask the following 4 questions in a single message.
Wait for answers before proceeding.

Tell the user: "Before I start researching, I need a few quick answers to scope
this correctly."

1. What is the topic or question? (State it in one sentence.)
2. What depth do you need?
   - BRIEF: 1-2 page summary, top findings, quick turnaround
   - STANDARD: 3-4 page report, full findings, key players, implications
   - DEEP-DIVE: comprehensive analysis, multiple angles, full source list
3. Who will read this, and what decision or action does it need to enable?
4. Any geographies, companies, regulations, or angles to include or exclude?
   (Default: USA, Canada, Germany with a financial services lens.)

Then offer: "Need a more thorough scoping? I can ask 7 additional questions for
high-stakes reports — just say 'full scoping'."

### Full Scoping (only if user requests it)

Ask these 7 additional questions in a single follow-up message:

5. What time horizon matters most — right now, past 6-12 months, or a 3-5 year
   trend view?
6. Any specific companies, vendors, or regulatory standards that must be covered?
7. What does the audience already know? (Expert / business-literate / beginner)
8. Any sub-topics or angles to explicitly exclude?
9. Preferred source types? (Analyst reports, regulator publications, financial
   press, vendor whitepapers, academic papers — or a mix?)
10. Is a specific report structure required, or should the agent decide?
11. What is the deadline or urgency?

---

## PHASE 2 — Research Plan

Before searching, show the user:

1. One-sentence research objective (restated from Phase 1 answers)
2. A numbered list of 4-6 search angles that together cover the topic fully —
   label this "Research Plan"
3. The source types most likely to yield relevant results for this topic
4. The selected depth tier and what it means:
   - BRIEF: 4-6 searches, 5-8 sources minimum
   - STANDARD: 8-12 searches, 10-15 sources minimum
   - DEEP-DIVE: 15-20 searches, 20+ sources minimum

Ask: "Does this plan look right? Any adjustments before I start?"
Wait for a go-ahead (or adjustments) before proceeding to Phase 3.

---

## PHASE 3 — Research Execution

Conduct web searches systematically, following the research plan from Phase 2.

### Search Rules

- Run searches in the order of the research plan angles.
- Follow the source minimums for the selected depth tier.
- Always include at least one search specifically for each confirmed geography.
- Always include at least one search for recent regulatory or compliance
  developments relevant to the topic in a financial services context.
- Prioritize primary sources (regulator sites, official publications, company
  investor relations pages) over secondary sources (news). Use both.
- Flag any source older than 18 months as potentially outdated.
- Note contradictions between sources with "CONFLICT:" and coverage gaps with
  "GAP:". These are analytically valuable and must appear in the final report.

### Save Research Notes File

When all searches are complete, save a working notes file BEFORE writing the
report.

File path: `output/YYYY-MM-DD_[topic-slug]_notes.md`

Notes file contents:
- Research objective (one sentence)
- Date of research
- All sources consulted: [number] | Title | URL | Date published
- Raw findings organized by research angle (bullet points)
- Any CONFLICT: or GAP: flags

Do NOT polish this file. It is a working document, not a deliverable.

---

## PHASE 4 — Report Writing

Write the final report using the template below exactly.

---

### REPORT TEMPLATE

```
# [Topic Title]

**Report type:** [BRIEF / STANDARD / DEEP-DIVE]
**Prepared for:** [Audience from Phase 1]
**Geography focus:** [Geographies confirmed in Phase 1]
**Date:** YYYY-MM-DD
**Research conducted by:** Claude (AI research agent)

---

## Executive Summary

3-5 bullets. Each bullet is one key finding or conclusion, one line maximum.
This section alone should tell the reader what they need to know.

---

## Context and Background

(Omit this section for BRIEF reports.)
3-6 bullets covering what this topic is, why it matters now, and essential
background for a business-literate reader.

---

## Key Findings

### [Category 1 — name based on topic, e.g., Market Trends]
- Finding [1]
- Finding [2]

### [Category 2 — e.g., Regulatory Landscape]
- Finding [3]

### [Category 3 — e.g., Technology / Competitive Landscape]
- Finding [4]

Cite sources inline throughout: "Finding text [1]."
Add or remove categories as the topic requires. Typical categories for
financial services market research: Market Trends, Regulatory Landscape,
Competitive Landscape, Technology Landscape, Geographic Specifics.

---

## Implications for Financial Services Consulting

So-what bullets framed for a consultant whose clients are banks.
- What should a bank or financial services firm be paying attention to?
- What opportunities or risks does this topic create for consulting engagements?
- Any urgent items (regulatory deadlines, competitive moves, expectation shifts)?

BRIEF: 3-5 bullets. STANDARD: 5-8 bullets. DEEP-DIVE: 8-12 bullets.

---

## Geographic Highlights

(Skip this section if there is no meaningful geographic variation — note
"No significant geographic variation found.")

### United States
- Key points specific to USA

### Canada
- Key points specific to Canada

### Germany
- Key points specific to Germany

---

## Key Takeaways and Recommended Next Steps

**Key Takeaways**
3-5 bullets distilling the most important conclusions from the report.

**Recommended Next Steps**
3-5 action-oriented bullets framed for a consultant:
- Assess client exposure to X
- Monitor regulation Y — deadline: [date]
- Explore offering in area W
- Brief client on Z before [event or date]

BRIEF: 2-3 takeaways + 2-3 steps. STANDARD/DEEP-DIVE: 3-5 each.

---

## Gaps and Limitations

2-4 bullets maximum.
- What was not found or not well-covered in available sources?
- What assumptions were made?
- What would require additional research to confirm?

---

## Sources

Numbered list matching inline citations used throughout the report.

[1] Title of source — Publisher — URL — Date accessed: YYYY-MM-DD
[2] ...

Minimum source counts: BRIEF: 5. STANDARD: 10. DEEP-DIVE: 20.
```

---

### Report Filename Convention

Format: `output/YYYY-MM-DD_[topic-slug]_[depth].md`

- `YYYY-MM-DD` — today's date
- `[topic-slug]` — 2-4 words from the topic, lowercase, hyphenated, no special
  characters (e.g., `ai-in-trade-finance`, `open-banking-germany`,
  `kyc-automation-trends`)
- `[depth]` — one of: `brief` | `standard` | `deep-dive`

Examples:
- `output/2026-05-19_ai-in-trade-finance_deep-dive.md`
- `output/2026-05-19_open-banking-germany_brief.md`
- `output/2026-05-19_kyc-automation-trends_standard.md`

---

## PHASE 5 — Delivery

1. Save the completed report to the correct output/ path using the filename
   convention above.
2. Tell the user:
   - Report filename
   - Notes filename
   - Number of sources used
   - Geographies covered
3. Offer three follow-up options:
   a. "Drill deeper into any section"
   b. "Produce a one-page executive brief" (if report was STANDARD or DEEP-DIVE)
   c. "Research a related topic"

Do NOT ask the user to review the notes file unless they specifically request
to see working documents.

---

## AGENT BEHAVIOR RULES (apply throughout all phases)

- Never start researching before Phase 1 and Phase 2 are complete and confirmed.
- Never write the report without saving the notes file first (end of Phase 3).
- Never use vague citations like "according to industry reports" — always cite
  specific sources with numbers.
- Never assume geographic scope — always confirm it explicitly in Phase 1.
- If a search returns no useful results, log it as a GAP and disclose it in
  the Gaps and Limitations section. Do not fill gaps with speculation.
- If the topic falls outside banking and financial services, flag this and ask
  whether to proceed with a general-market framing before continuing.
- Keep all bullet points to one line where possible. Expand to two lines only
  if cutting to one line loses essential meaning.
