# Problem 2 — MLE with Student-t Errors

In this question, you will explore maximum likelihood estimation in the presence of heavy-tailed errors. When financial returns exhibit fat tails or outliers, the normal likelihood can lead to misleading inference.

To address this, we model regression residuals using a Student-t distribution, which nests the Gaussian as a special case (when degrees of freedom → ∞).

You will use a flexible likelihood function that assumes t-distributed errors, compare nested models via likelihood ratio tests, and examine the profile likelihood for the degrees of freedom parameter.

Use any dataset of your choice (for example, one industry portfolio regressed on Fama-French factors), as long as it fits the structure of a dependent variable with a set of predictors. Let’s assume your DataFrame is organized such that:

- The first column is the dependent variable (e.g., portfolio return)
- All other columns are regressors (e.g., factors)

## (a)
Write a function that accepts:

- a DataFrame `df` (with first column as the dependent variable),
- an integer `dof` (degrees of freedom > 0),

and returns the log-likelihood of a linear regression model assuming Student‑t errors:

- Fit an OLS regression of the first column on a constant and the other columns.
- Calculate the standardized residuals.
- Evaluate and return the log-likelihood assuming the residuals follow a t-distribution with `dof` degrees of freedom.

Interpret what the log‑likelihood represents in this context.

## (b)
Write a function that uses your log‑likelihood function to compute a Likelihood Ratio (LR) test comparing:

- the full model (with all predictors),
- a restricted model (with only a constant).

Return the LR statistic and its p-value under the χ² distribution. What does the LR test tell you about the joint significance of the predictors under heavy‑tailed errors?

## (c)
Create a profile likelihood plot for the degrees of freedom parameter of the t‑distribution:

- Evaluate the log‑likelihood for `dof = e^{j/12}`, for `j = 0, …, 50`.
- Plot the log‑likelihood as a function of `dof`.

Discuss what the shape of the curve reveals about tail thickness. Where does the MLE for `dof` appear to be located?

## (d)
Based on your profile likelihood plot above, which of the following best describes the implied value of `dof` that maximizes the likelihood? (Choose one, and justify your choice.)

- A very small value (≈ 1)
- A moderate value (≈ 15)
- A large value (> 60)
- A strange value like −1370 (note: this is invalid)

Why does this matter in financial modeling?
