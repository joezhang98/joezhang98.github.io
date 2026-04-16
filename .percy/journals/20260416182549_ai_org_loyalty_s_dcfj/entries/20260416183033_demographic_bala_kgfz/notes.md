**Balance Checks:** All demographic variables were balanced across Human vs. AI conditions. Age: t(58)=0.06, p=.956. Gender: χ²(2)=1.15, p=.562. Ethnicity: χ²(4)=3.20, p=.526. Education showed a marginal difference: χ²(5)=9.91, p=.078, though still non-significant at α=.05.

**Moderation Analyses:** OLS models tested whether Age, Gender (binary), and Education (ordinal) moderated the effect of Condition on each loyalty DV. All Condition × Moderator interactions were non-significant (all p > .60), suggesting no meaningful moderation by any demographic variable.

**Publication Tables (added):** Three publication-quality matplotlib tables were generated in the notebook:
- *Table 1 — Main Effects:* Per-item Welch's t-tests and composite scores for LOYALTY_3RD and LOYALTY_1ST, with Human M(SD), AI M(SD), t(58), p, and Cohen's d [95% CI].
- *Table 2 — Demographics Balance:* Counts and percentages by condition for Age, Gender, Education, and Ethnicity, with test statistics and p-values.
- *Table 3 — Moderation:* OLS regression coefficients for Condition, Condition × Moderator interactions, R², and adjusted R² for each DV.

**Bug fixed:** The `render_table()` helper used `ax.axhline(..., transform=ax.transAxes)` which raises a `ValueError` in newer matplotlib. Fixed by replacing with `ax.plot([0,1], [y,y], ..., transform=ax.transAxes)`.