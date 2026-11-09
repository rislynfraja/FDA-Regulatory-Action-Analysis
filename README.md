# FDA-Regulatory-Action-Analysis
### Final Project for BA780 - Team A06
---

## Team

Malak Taoujni, Filip Handjiski, David Chiu, Rislyn Raja, Aryan Bajaj

---

## What It Does

1. **Data Cleaning & Linking** - loads the FDA Recalls (2012-2026) and FDA Compliance Actions (2008-2026) data, fixes hidden missing values (`-`), converts dates, and counts each recall **event** once (not each product row). The two datasets are then joined by facility ID (**FEI Number**) into one facility-level table.
2. **Part 1: Team Assignment (Q1-Q5)** - recall trends over time, and recalls vs. FDA actions by product type, state and facility, plus which products get the harshest actions.
3. **Part 2: Final Project Expansion (Q6-Q15)** - recall severity and causes, enforcement trends, facility-level risk (including recalls before and after a first action), and state-level enforcement gaps.
4. **Recommendations** - four actionable suggestions for better targeting FDA oversight, based on the findings.

---

## Files

| File | Description |
|---|---|
| `A06-FDA-Regulatory-Action-Analysis.ipynb` | Full analysis notebook: cleaning, 15 questions with charts, conclusions |
| FDA-Regulatory-Action-Analysis-Presentation (slideshow) | Slides summarizing the project and findings |

---

## Requirements

```
numpy
pandas
matplotlib
```

Install with:
```bash
pip install numpy pandas matplotlib
```

---

## How to Run

**Step 1: Open the notebook** in Google Colab.
**Step 2: Run all cells from top to bottom.** The notebook loads both datasets from shared Google Drive links, so no manual download is needed. This will:
- Clean both datasets and print before/after checks
- Build the facility-level table joined on FEI Number
- Produce charts and display "So what" / "Caveat" takeaways for Q1-Q15
- Display the final conclusion and recommendations

---

## Dataset

Two public datasets from the **U.S. Food and Drug Administration (FDA) Data Dashboard** (public domain):

| Dataset | Coverage | Size after cleaning |
|---|---|---|
| [Recalls](https://datadashboard.fda.gov/oii/cd/recalls.htm) | 2012-2026 | 104,083 product rows (37,623 recall events) |
| [Compliance Actions](https://datadashboard.fda.gov/oii/cd/complianceactions.htm) | 2008-2026 | 177,252 actions (warning letters, seizures, injunctions) |

1,724 facilities appear in both datasets. To re-download, use the Export (CSV) option on each dashboard page (~69 MB and ~17 MB).

---
