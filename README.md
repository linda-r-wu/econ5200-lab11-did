[README.md](https://github.com/user-attachments/files/34341862/README.md)
# Difference-in-Differences: Parallel Trends, Staggered Adoption and the Forbidden Comparison

## Objective

I examined when difference-in-differences estimates become misleading because of different trends, treatment timing or incorrect standard errors.

## Methodology

- Reproduced Card and Krueger’s minimum-wage analysis using the original data and compared it with their published **+2.76 full-time-equivalent employees**.
- Simulated different treatment and control trends and ran a pre-trend test.
- Broke a staggered-adoption TWFE estimate into its two-by-two comparisons and weights.
- Compared ordinary standard errors with errors clustered by state.
- Checked an AI-generated Goodman-Bacon decomposition against my calculations and revised its missing-data handling.

## Key Findings

**Parallel trends:** DiD estimated **1.148** when the true effect was zero because the treated group was already growing faster. The pre-trend test found a slope difference of **0.194**.

**Staggered adoption:** TWFE returned **−0.99**, despite a true mean effect of **6.71**. The clean comparison was **5.043**, while the comparison using already-treated controls was **−4.012** and received **66.7%** of the weight.

**Standard errors:** Clustering by state made the standard error **8.6 times larger**, showing how ignoring shared, persistent shocks can create misleading significance.

**AI verification:** The decomposition matched my balanced-panel calculations and reproduced TWFE at **−0.9939**. After revision, it handled missing outcomes explicitly but still stopped when the remaining panel was unbalanced. I documented that limitation rather than reporting an unsupported result.

