# Problem 1 [40 pts] — Testing Linear Asset Pricing Models

In this question, you will test the performance of linear factor models using real return data. 
Your task is to evaluate how well common factors explain the cross-section of returns for industry 
portfolios using a two-pass regression framework.

You will use monthly data from **Ken French’s Data Library**:

- **F-F Research Data 5 Factors 2x3** — the standard 5-factor model from Fama and French  
- **F-F Momentum Factor (UMD)** — the momentum factor  
- **17 Industry Portfolios** — value-weighted excess returns by industry  

Retrieve all series for the sample period **1980–2021**.  
Ensure that all returns are in **excess form**.

---

## (a) Data Retrieval and Summary Statistics

Retrieve and merge the six-factor dataset and the 17 industry portfolios from Ken French’s website.  
Ensure the data is properly aligned and cleaned.

You must:

- Report basic summary statistics for all series  
- Provide time-series plots for at least **three industries** and **two factors**  
- Briefly discuss notable differences across series  

**[10 pts]**

---

## (b) First-Pass Time-Series Regression (OLS)

Estimate the linear factor model:

\[
R_{it} = lpha_i + eta_i^{\top} f_t + arepsilon_{it}
\]

Where:

- \(R_{it}\): excess return of industry *i* at time *t*  
- \(f_t\): six-factor vector (including momentum)  
- \(eta_i\): factor loadings  
- \(lpha_i\): pricing error  
- \(arepsilon_{it}\): residual  

You must report:

- Average \(R^2\)  
- Estimated betas (\(eta_i\))  
- Robust t-statistics  

Also comment on patterns or anomalies across industries and factors.  
**[10 pts]**

---

## (c) Second-Pass Cross-Sectional Regression

Estimate the factor risk prices from:

\[
ar{R}_i = \lambda^{\top} eta_i + \eta_i
\]

Where:

- \(ar{R}_i\): average excess return of industry *i*  
- \(eta_i\): estimated loadings from Part (b)  
- \(\lambda\): vector of factor risk prices  
- \(\eta_i\): pricing error  

You must:

- Estimate \(\lambda\) (prices of risk)  
- Report **robust t-stats**  
- Conduct the **J-test** for pricing performance  
- Discuss:  
  - Are pricing errors fully explained?  
  - Which factors are significantly priced?  

**[10 pts]**

---

## (d) Non‑Traded Factor Specification

Repeat part (c) assuming the factors are **non‑traded**.

Then:

- Compare the two J-tests  
- Discuss which specification is more appropriate and explain why  

**[5 pts]**

---

## (e) Reflection

Answer each question in **1–2 sentences**:

1. Do any portfolios earn a return unexplained by the factors?  
2. Do your conclusions depend on whether the factors are traded?  

**[5 pts]**

---

## Improved Mathematical Writing for Functions

### First-Pass Regression Function (from Part b)

\[
R_{it} = lpha_i + eta_i^{\top} f_t + arepsilon_{it}
\]

Where:

- Input: time-series of excess returns \(R_{it}\) and factor matrix \(F_t\)  
- Output: \(lpha_i\), \(eta_i\), robust t-statistics, \(R^2\)

### Second-Pass Cross-Sectional Regression Function (from Part c)

\[
ar{R}_i = \lambda^{\top} eta_i + \eta_i
\]

Where:

- Input: vector of average excess returns \(ar{R}_i\) and estimated betas \(eta_i\)  
- Output: estimated \(\lambda\), its robust t-statistics, J-test value

