# EARNINGS ESTIMATES

# *Estimating profitability decomposition frameworks via machine learning: Implications for earnings forecasting and financial statement analysis*

[Article PDF](Estimating_Profitability_Decompostion_ML.pdf)

Binz, O., Schipper, K., & Standridge, K. R. (2023). *Estimating profitability decomposition frameworks via machine learning: Implications for earnings forecasting and financial statement analysis*. Journal of Accounting and Economics.

---

## Overview
This paper studies whether **nonlinear machine learning (ML) estimation** of classic **profitability decomposition frameworks** improves the accuracy of profitability forecasts and whether those forecasts are useful for **predicting stock returns**. The authors focus on the well-known **Nissim and Penman (2001, 2003)** hierarchical decomposition of profitability and evaluate how ML methods enhance traditional fundamental analysis.

---

## Key Methodology

### Profitability Framework
- The paper builds on **Nissim–Penman profitability decomposition**, which breaks return on equity into economically meaningful components (e.g., operating vs. financing activities, margins, turnover).
- The framework is **hierarchical and nonlinear by construction**, making it a natural candidate for ML estimation.

### Estimation Approach
- The authors apply **machine learning techniques** to estimate the nonlinear relationships within the decomposition framework.
- Forecasts are generated **out of sample**, with performance compared against:
  - A **random walk** benchmark.
  - **Linear regression** versions of the same decomposition.

### Design Choices Examined
The study systematically evaluates three core financial statement analysis choices:
1. **Depth of decomposition** (more granular breakdowns of profitability).
2. **Focus on core operating items** versus total profitability.
3. **Length of historical information** (up to three years of past data).

---

## Data Sources
- **Financial statement data:** Compustat.
- **Stock returns:** CRSP.
- **Analyst forecasts:** I/B/E/S (used for comparison and controls).
- Sample consists of U.S. publicly traded firms over multiple decades (exact period varies by test).

---

## Main Empirical Findings

### Forecast Accuracy
- **Nonlinear ML estimation significantly outperforms** both random walk and linear models in forecasting future profitability.
- Gains come from:
  - Nonlinear estimation itself.
  - **Synergies between ML and the decomposition structure**, rather than ML alone.

### Role of Financial Statement Design
- Forecast accuracy improves when:
  - Profitability is **more deeply decomposed**.
  - Analysis focuses on **core operating profitability**.
  - **Up to three years** of historical accounting data are used.

### Asset Pricing Results
- ML-based profitability forecasts:
  - **Predict future stock returns**.
  - Predict **changes in profitability**.
- These relations hold **after controlling for**:
  - Analyst earnings forecasts.
  - Standard asset pricing factors (e.g., size, value, momentum).

---

## Relevance for Forecasting Stock Returns

- The paper provides strong evidence that **fundamental signals extracted via ML-enhanced accounting models contain priced information**.
- Unlike many “black-box” ML return predictors, the approach:
  - Retains **economic interpretability**.
  - Is directly linked to **valuation-relevant fundamentals**.
- For quantitative finance and asset management, the results suggest:
  - Combining **structured accounting models with ML** is a promising path for return forecasting.
  - Profitability-based signals remain incremental even in the presence of analyst forecasts and factor models.

---

# *Analyst Forecast Bias: The Interaction of Earnings Skewness and Information Environment*

[Article PDF](Analyst_Forecast_Bias_Skewness.pdf)

Brightbill, K., Gleason, C. A., & Penno, M. (2024). *Analyst Forecast Bias: The Interaction of Earnings Skewness and Information Environment*. Working paper, Utah State University and University of Iowa.

---

## Overview
This paper examines **systematic bias in analysts’ earnings forecasts** arising from the interaction between **earnings skewness** and **constraints in the information environment**. The authors develop a rational, forward-looking framework in which analysts understand the skewness of earnings distributions but face limits on their ability to fully incorporate that information due to external constraints. These limits generate predictable optimism or pessimism in forecasts.

---

## Key Methodology

### Conceptual Framework
- Earnings distributions are **asymmetric (skewed)**, and this skewness affects optimal forecasting.
- Analysts are assumed to be **rational but constrained**, meaning forecast bias arises not from irrationality but from frictions such as:
  - Deterioration in the firm’s information environment.
  - Analyst **busyness** (attention constraints).
- Forward-looking earnings skewness interacts with these constraints to produce **directional forecast bias**.

### Empirical Design
- Tests directional predictions linking:
  - **Right-skewed earnings** → analyst optimism under tighter constraints.
  - **Left-skewed earnings** → analyst pessimism under tighter constraints.
- Uses **multiple proxies** for:
  - Earnings skewness.
  - Information environment quality.
  - Analyst constraints (including workload and coverage breadth).
- Includes **simulation analysis** to show that the proposed forecasting mechanism reproduces empirical patterns documented in prior research.

---

## Data Sources
- **Analyst forecasts:** I/B/E/S.
- **Earnings and accounting data:** Compustat.
- **Market and firm characteristics:** CRSP and related databases.
- Sample spans multiple time periods and institutional settings to demonstrate robustness.

---

## Main Empirical Findings

### Forecast Bias
- Analysts are:
  - **More optimistic** for firms with **right-skewed earnings** when the information environment worsens or analysts are busier.
  - **More pessimistic** for firms with **left-skewed earnings** under the same conditions.
- These effects are:
  - Statistically and economically significant.
  - Robust across alternative measures of skewness and information environment.

### Role of Information Environment
- Improvements in disclosure quality and information availability:
  - Reduce analyst forecast bias.
  - Improve forecast accuracy.
- Bias is not confined to a single market regime or time period.

### Validation via Simulation
- Simulated analyst forecasts based on the model:
  - Match observed empirical regularities in analyst optimism and pessimism.
  - Support the interpretation that analysts are skewness-aware but constrained.

---

## Relevance for Forecasting Stock Returns

- Analyst forecast bias linked to **earnings skewness** implies **predictable forecast errors**, which can translate into:
  - Earnings surprises.
  - Post-announcement return predictability.
- For quantitative finance:
  - Skewness-informed adjustments to analyst forecasts may improve **earnings and return forecasts**.
  - Results suggest that analyst-based signals are **state-dependent**, becoming less reliable when information frictions are high.
- More broadly, the findings help explain **when and why analyst forecasts embed mispricing**, offering guidance for:
  - Signal timing.
  - Cross-sectional return strategies exploiting forecast bias.

---

# *Good-Bye I/B/E/S (or Not?)*

[Article PDF](Good-Bye_IBES_or_Not.pdf)

Law, K. K. F. (2023). *Good-Bye I/B/E/S (or Not?)* Journal of Financial Reporting, Nanyang Technological University.

---

## Overview
This paper investigates whether **I/B/E/S analyst and broker identifier (ID) anonymization and reshuffling**, announced in October 2018, materially compromise empirical research using post-2018 I/B/E/S Detail History Files. Given the central role of stable analyst identifiers in the analyst literature, the paper addresses widespread concern that a large fraction of analyst-level research may be invalidated.

---

## Key Methodology

### Identification Tests
The author conducts a **forensic data audit** of I/B/E/S files to assess two distinct issues:

1. **ID anonymization**  
   - An analyst ID is considered anonymized when `ANALYS = 0`.
   - The paper tracks the frequency of anonymized IDs over time and across forecast types.

2. **ID reshuffling**  
   - Reshuffling is tested by comparing **multiple vintages** of I/B/E/S data (2015–2021).
   - The author examines whether forecasts originally associated with anonymized IDs are later reassigned to different analysts.

### File-Level Comparison
- Analysis distinguishes between:
  - **Unadjusted Detail History Files** (primary concern for researchers).
  - **Recommendations Detail Files**, which retain largely stable analyst identifiers.
- Cross-file consistency is exploited to validate analyst identity continuity.

---

## Data Sources
- **I/B/E/S Unadjusted Detail History Files** (earnings forecasts).
- **I/B/E/S Recommendations Detail Files**.
- Multiple **historical vintages** of I/B/E/S downloads (2015–2021) via WRDS.
- Sample includes both **U.S. and non-U.S. firms**, allowing for geographic comparison.

---

## Main Empirical Findings

### ID Anonymization
- **No evidence of large-scale anonymization** for:
  - Annual and quarterly EPS forecasts for **U.S. firms**.
- Anonymization:
  - Primarily affects **non-U.S. firms**.
  - Begins as early as **January 2017**, earlier than I/B/E/S’s stated October 2018 change.
- A substantial fraction of non-U.S. forecasts have anonymized analyst IDs post-2017.

### ID Reshuffling
- **No evidence of large-scale reshuffling** of analyst or broker IDs in:
  - U.S. earnings forecasts.
  - Recommendations data.
- Alleged reshuffling rates cited by WRDS appear to overstate the severity of the issue for commonly used research samples.

### Recommendations File Stability
- The Recommendations Detail File is **largely unaffected** by anonymization.
- This stability enables the author to provide **practical steps to reverse-engineer anonymized analyst IDs** in the earnings forecast files.

---

## Relevance for Forecasting Stock Returns

- Analyst-based signals (forecast errors, revisions, dispersion, analyst characteristics) remain:
  - **Largely valid for U.S. equity return prediction** post-2018.
- The paper reassures quantitative researchers that:
  - Most **cross-sectional return predictability studies using analyst data are not mechanically invalidated**.
- However:
  - Caution is warranted for **international samples** and studies relying heavily on analyst-level identifiers outside the U.S.
- The provided reverse-engineering approach helps preserve:
  - Analyst fixed effects.
  - Analyst reputation and skill measures.
  - Forecast-based return predictors.

---

# *Expected EPS × Trailing PE: Pricing Without Discounting*

[Article PDF](Expected_EPS_Times_Trailing_PE.pdf)

Ben-David, I., & Chinco, A. (2025). *Expected EPS × Trailing PE: Pricing Without Discounting*. Working paper.

---

## Overview
This paper studies **how sell-side equity analysts actually set price targets** and documents a striking departure from standard present-value valuation theory. By directly reading analyst reports and validating findings in large-sample data, the authors show that most analysts rely on a **simple pricing heuristic**—multiplying expected earnings per share (EPS) by a trailing price–earnings (PE) ratio—rather than discounting future cash flows.

---

## Key Methodology

### Hand-Collected Evidence
- The authors manually read **513 sell-side analyst reports**.
- They extract analysts’ **explicit descriptions of valuation methods** used to justify price targets.
- This qualitative approach establishes how analysts *say* they value stocks, rather than inferring methods indirectly.

### Large-Sample Validation
- Using the full **I/B/E/S price target database**, the authors test whether the pricing rule:
  
  \[
  \text{Price Target} \approx \text{Expected EPS} \times \text{Trailing PE}
  \]

  explains observed price targets.
- Regression and decomposition analyses assess how much of price target variation is explained by this rule relative to more complex valuation models.

### Event-Response Tests
- The paper examines how:
  - Analyst price targets
  - Market prices  
  respond to earnings news, testing whether responses are consistent with the trailing-PE pricing model.

---

## Data Sources
- **Analyst price targets and earnings forecasts:** I/B/E/S.
- **Firm financial data:** Compustat.
- **Stock returns and prices:** CRSP.
- **Hand-collected analyst reports** from major sell-side institutions.

---

## Main Empirical Findings

### Analyst Valuation Practices
- A **majority of analysts explicitly state** that they value stocks by:
  - Forecasting near-term EPS.
  - Applying a **historical (trailing) PE multiple**.
- Few analysts describe using discounted cash flow (DCF) or other present-value logic in practice.

### Explanatory Power of the Heuristic
- The **Expected EPS × Trailing PE** rule explains:
  - The bulk of cross-sectional and time-series variation in analyst price targets.
- After accounting for selection effects, trailing-PE-based price targets are:
  - **Approximately unbiased on average**.

### Market and Price Target Responses
- A simple trailing PE model:
  - Accurately predicts how **price targets adjust to earnings news**.
  - Helps explain observed **stock price reactions** around forecast revisions.
- Market prices appear to co-move with the same simple inputs used by analysts.

---

## Relevance for Forecasting Stock Returns

- The paper implies that **near-term earnings expectations and valuation multiples**, rather than long-horizon discounting, play a dominant role in:
  - Analyst behavior.
  - Market pricing dynamics.
- For quantitative return forecasting:
  - Changes in **expected EPS** and **trailing valuation multiples** are key state variables.
  - Models exploiting **earnings news × valuation context** may capture predictable return responses.
- More broadly, the findings help explain why:
  - Simple earnings-based signals often outperform theoretically richer valuation models.
  - Analyst price targets and market prices can react strongly to short-term fundamentals.

---

# *Man versus Machine Learning: The Term Structure of Earnings Expectations and Conditional Biases*

[Article PDF](Man_vs_ML_Term_Structure_Earnings_Expectations.pdf)

[Appendix PDF](hhac085_supplementary_data.pdf)

van Binsbergen, J. H., Han, X., & Lopez-Lira, A. (2023). *Man versus Machine Learning: The Term Structure of Earnings Expectations and Conditional Biases*. *Review of Financial Studies*, 36(6), 2361–2396.

---

## Overview
This paper compares **human (sell-side analyst)** and **machine learning–based earnings forecasts** through the lens of a newly introduced concept: the **term structure of earnings expectations**. The authors develop a real-time measure of **conditional forecast bias** that varies across forecast horizons and states of the world. The central question is whether analysts’ biases are systematic and state-dependent, and whether machine learning forecasts can discipline or outperform human judgment.

---

## Key Methodology

### Term Structure of Earnings Expectations
- The authors construct a **term structure** by examining forecasts of earnings at multiple horizons (short-term vs. long-term).
- They define a **conditional bias measure** as the difference between forecasted earnings growth and subsequently realized earnings growth, conditional on information available at the forecast date.

### Human vs. Machine Forecasts
- Analyst forecasts are compared with:
  - **Machine learning forecasts** trained on historical earnings, prices, and firm characteristics.
- ML models are explicitly designed to:
  - Be **out-of-sample** and real-time.
  - Avoid look-ahead bias.
- The comparison focuses on:
  - Forecast accuracy.
  - Systematic conditional biases across horizons and firm states.

### State Dependence
- Biases are examined conditional on:
  - Firm growth characteristics.
  - Valuation levels.
  - Recent performance and macro conditions.
- This allows the authors to distinguish **unconditional optimism** from **state-dependent forecasting errors**.

---

## Data Sources
- **Analyst earnings forecasts:** I/B/E/S.
- **Firm fundamentals:** Compustat.
- **Stock prices and returns:** CRSP.
- Sample spans several decades of U.S. publicly traded firms, enabling horizon-by-horizon analysis.

---

## Main Empirical Findings

### Analyst Forecast Biases
- Analyst earnings forecasts exhibit **strong conditional biases**:
  - **Over-optimism at longer horizons**, especially for growth firms.
  - Less bias at short horizons.
- Biases vary systematically with firm characteristics and economic conditions, forming a **non-flat term structure of bias**.

### Machine Learning Performance
- ML forecasts:
  - Are **significantly less biased** across horizons.
  - Outperform analysts in terms of **forecast accuracy**, particularly at longer horizons.
- ML models adapt better to nonlinearities and regime changes.

### Market Pricing Implications
- The market appears to **partially incorporate** analyst bias:
  - Prices reflect some correction for long-horizon optimism, but not fully.
- Conditional bias measures predict:
  - Subsequent earnings surprises.
  - Post-forecast stock returns.

---

## Relevance for Forecasting Stock Returns

- The paper shows that **state-dependent earnings forecast bias** is a powerful predictor of returns.
- Stocks with:
  - **More optimistic long-horizon analyst forecasts** earn predictably lower future returns.
  - Less biased or pessimistically biased forecasts earn higher future returns.
- For quantitative asset pricing:
  - ML-based earnings expectations provide cleaner fundamental signals.
  - The *difference* between human and machine forecasts is itself a **priced signal**.
- More broadly, the framework bridges:
  - Behavioral finance (conditional optimism).
  - Machine learning–based forecasting.
  - Return predictability tied to fundamentals.

---
# *I/B/E/S: Introduction and Research Guide*

[Article pdf](./1S_zm7Fqc2ZTKo-sTDETh4hgWrXQTsuVH)

Dai, R. *I/B/E/S @ WRDS 101: Introduction and Research Guide*. Slides accessed from WRDS.

### 1. Purpose and Scope of I/B/E/S

The slides introduce **I/B/E/S (Institutional Brokers’ Estimate System)** via WRDS as a core database for **sell-side analyst forecasts**. The dataset covers:

* Earnings per share (EPS) forecasts
* Long-term growth forecasts
* Target prices
* Recommendation levels (buy/hold/sell)

The focus is on **research usage**, data structure, and common pitfalls.

---

### 2. Data Structure and Key Files

The presentation explains the distinction between:

* **Detail files**: Individual analyst forecasts with timestamps
* **Summary files**: Consensus statistics (mean, median, dispersion, number of analysts)

Key variables highlighted include:

* Forecast period indicators (FY1, FY2, LTG)
* Forecast issue date vs. fiscal period end
* Actual earnings and adjustment factors

⚠️ Emphasis is placed on **proper alignment of forecast timing with returns**, a frequent source of bias in empirical asset pricing.

---

### 3. Forecast Revisions and Analyst Behavior

The slides discuss how forecasts evolve through time:

* Analysts update estimates in response to earnings announcements and firm news
* Revisions are **clustered** and often exhibit **underreaction**

This section implicitly motivates using:

* Forecast revisions
* Changes in consensus
* Analyst disagreement

as economically meaningful signals.

---

### 4. Common Research Pitfalls

Several warnings are stressed:

* **Look-ahead bias** when using post-announcement data
* **Survivorship bias** if delisted firms are dropped
* Confusion between announcement dates, forecast dates, and fiscal period labels

These issues are directly relevant for return predictability tests.

---

### 5. Typical Research Applications

Examples mentioned or implied include:

* Earnings surprise studies
* Analyst optimism/pessimism
* Market reaction to forecast changes
* Cross-sectional asset pricing tests

---

## Relevant Points for Forecasting Stock Returns

From a return-prediction standpoint, the slides reinforce several well-established but practically important ideas:

### 1. Earnings Forecast Revisions as Predictors

Changes in analyst forecasts (not just levels) are key predictors of:

* Short-horizon abnormal returns
* Post-earnings-announcement drift

Properly timestamped revisions can be used as **signals of slow information diffusion**.

---

### 2. Analyst Disagreement and Uncertainty

Dispersion in forecasts proxies for:

* Information uncertainty
* Limits to arbitrage

Higher dispersion is often associated with:

* Higher expected returns
* Greater volatility around earnings events

---

### 3. Bias and Optimism Effects

Systematic analyst optimism (especially for growth firms) implies:

* Overly positive forecasts
* Subsequent negative return predictability when expectations are revised downward

This is relevant for **contrarian strategies** based on forecast errors.

---

### 4. Timing Is Everything

The slides strongly imply that:

> Forecasts must be aligned with **what was known at the portfolio formation date**.

This is crucial for:

* Avoiding spurious predictability
* Constructing tradable forecasting signals

---

### 5. Complementarity with Other Signals

I/B/E/S data is best used alongside:

* Price momentum
* Accounting fundamentals (e.g., accruals)
* Event indicators (earnings announcements, guidance)

Analyst data often improves forecasts when combined with **fundamental and market-based predictors**.

---

# *Post-Earnings Announcement Drift (PEAD)*

[Article PDF](Post_Earnings_Announcement_Drift_WRDS.pdf)

Wharton Research Data Services (WRDS). *Post-Earnings Announcement Drift Research Application*. Based on Livnat, J. and Mendenhall, R. (2006), *Journal of Accounting Research*.

---

## Overview

The slides present a **WRDS research application** illustrating how to construct and test **Post-Earnings Announcement Drift (PEAD)** portfolios using **Compustat, CRSP, and I/B/E/S** data. PEAD refers to the empirical regularity that **stock returns continue to drift in the direction of an earnings surprise for weeks after the earnings announcement date (EAD)**.

The methodology closely follows **Livnat and Mendenhall (2006, JAR)** and emphasizes careful data linking and timing alignment.

---

## Earnings Surprise Measures

Three standardized unexpected earnings (SUE) measures are described:

### 1. **SUE1 (Compustat-based, seasonal random walk)**
- Assumes quarterly EPS follows a seasonal random walk.
- Surprise is computed as the difference between current EPS and EPS from the same quarter last year, scaled by price.
- Uses primary or diluted EPS depending on analyst convention.
- Requires split adjustments using Compustat adjustment factors.

### 2. **SUE2 (Compustat excluding special items)**
- Adjusts reported EPS by removing special items (SPIQ × 65%).
- Better aligns Compustat “GAAP” earnings with I/B/E/S “street” earnings.
- Motivated by evidence that special items distort measured surprises.

### 3. **SUE3 (I/B/E/S analyst-based)**
- Uses the **median of analyst forecasts issued within 90 days before EAD**.
- Compares analyst expectations to I/B/E/S reported actuals.
- Constructed from **I/B/E/S unadjusted detail data** to avoid rounding bias.
- Forecasts and actuals are split-adjusted using CRSP factors.

---

## Portfolio Construction and Returns

- Earnings announcement dates are adjusted to trading days using the CRSP calendar.
- Portfolios are formed based on SUE quintiles.
- Performance is evaluated using **abnormal returns (EXRET)** relative to the CRSP value-weighted market index.
- Drift is examined from **day 0 to day +50** after EAD.

---

## Key Empirical Findings

1. **Robust PEAD Effect**  
   - Returns continue to drift in the direction of the earnings surprise after the announcement.
   - PEAD is confirmed for both large-cap (S&P 500) and small-cap (S&P 600) firms.

2. **Asymmetry Between Long and Short Sides**  
   - The **long leg (positive surprises)** tends to be more profitable than the short leg.
   - For S&P 500 firms, CARs over [+2, +50] are approximately:
     - +0.72% for top SUE quintile
     - −0.67% for bottom SUE quintile

3. **Stronger Effects in Small-Cap Stocks**  
   - PEAD is larger among smaller, lower-priced firms.
   - Zero-cost PEAD portfolios earn roughly:
     - 1.4% for large caps
     - 1.9% for small caps over [+2, +50]

4. **Declining Drift in Recent Years**  
   - In more recent subsamples (post-2006), most price adjustment occurs within the first day or two.
   - Suggests **increased arbitrage and faster information incorporation**, especially in small stocks.

---

## Implications for Forecasting Stock Returns

- **Analyst-based earnings surprises (SUE3)** are particularly powerful predictors of short-horizon returns.
- PEAD supports models of **underreaction to public information**.
- Forecast revisions and analyst expectations contain incremental information beyond historical earnings.
- Predictability is **state-dependent**:
  - Stronger in small, illiquid, or low-attention stocks.
  - Weaker in more recent, highly arbitraged markets.
- Careful handling of:
  - Timing (forecast date vs. EAD)
  - Split adjustments
  - Special items  
  is essential to avoid biased return forecasts.

---


# Summary: Analysts’ Annual Earnings Forecasts and Changes to the I/B/E/S Database

[Article PDF](Analysts_Changes_IBES.pdf)

Call, A. C., Hewitt, M., Watkins, J., & Yohn, T. L. (2020). *Analysts’ annual earnings forecasts and changes to the I/B/E/S database*. Review of Accounting Studies, Springer Nature.

---

## Overview

This article examines **material changes over time in the I/B/E/S analyst earnings forecast database** and evaluates how those changes affect empirical research. Using two historical “vintages” of the I/B/E/S **detail file** (one distributed in 2009 and another in 2015), the authors show that analyst forecasts for the *same firms and periods* differ meaningfully across database versions.

The paper’s core message is methodological: **I/B/E/S data are not time-invariant**, and database revisions can materially affect conclusions about analyst behavior, earnings surprises, and return predictability.

---

## Data Sources

- **I/B/E/S Detail Files**
  - 2009 vintage vs. 2015 vintage
  - Annual EPS forecasts
  - Individual analyst-level observations
- **I/B/E/S Actuals**
  - Used to compute forecast errors and bias
- **Compustat**
  - Firm fundamentals
- **CRSP**
  - Stock returns (used indirectly to motivate capital market implications)

The analysis focuses on a **common firm–year sample** so that any differences arise solely from database revisions rather than sample selection.

---

## Key Methodology

1. **Vintage Comparison Approach**
   - The authors compare two archived versions of I/B/E/S covering the *same historical forecast periods*.
   - This isolates the effect of database cleaning, restatement, and vendor-side corrections.

2. **Forecast Attribute Analysis**
   - Forecast accuracy (absolute forecast error)
   - Forecast bias (optimism/pessimism)
   - Distribution of forecast errors around zero

3. **Benchmark Beating Classification**
   - Firms are classified as:
     - Missing expectations
     - Meeting expectations
     - Just beating expectations  
   - The paper examines how classifications change across vintages.

4. **Replication Sensitivity**
   - The authors assess how common research designs (e.g., earnings surprise tests) are affected by the data version used.

---

## Main Empirical Findings

### 1. Substantial Differences Across I/B/E/S Vintages
- Many analyst forecasts appear in one vintage but not the other.
- Forecast values for the same analyst–firm–year frequently differ.
- Differences are **not random**.

---

### 2. Improved Accuracy in Later Versions
- Forecasts in the **2015 vintage** are:
  - More accurate
  - Less optimistic
  - Less dispersed around zero error  

This suggests vendor-side improvements in:
- Analyst attribution
- Split adjustments
- Data cleaning procedures

---

### 3. Earnings Surprise Classification Is Not Stable
- A non-trivial fraction of firms classified as “meeting or just beating” expectations in the 2009 vintage are **reclassified** in the 2015 vintage.
- This directly affects:
  - Earnings management studies
  - PEAD research
  - Tests of investor fixation on benchmarks

---

### 4. Implications for Replicability
- Results in prior studies may **not replicate** when using newer I/B/E/S vintages—even if the sample period is unchanged.
- Differences are economically meaningful, not just statistically detectable.

---

## Relevance for Forecasting Stock Returns

### 1. Analyst-Based Signals Are Vintage-Sensitive
Forecast errors, surprises, and revisions—commonly used predictors of stock returns—depend critically on:
- Which I/B/E/S vintage is used
- Whether forecasts are “as originally issued” or retrospectively cleaned

This matters for:
- PEAD strategies
- Earnings surprise portfolios
- Analyst optimism/contrarian signals

---

### 2. Backtesting Risk
Using modern I/B/E/S data to test historical trading strategies may introduce **look-ahead bias** if the data implicitly reflects later corrections.

> Apparent return predictability may partly reflect data revisions rather than true market inefficiencies.

---

### 3. Benchmark Effects and Drift
Because “meet/beat” classifications change across vintages:
- Measured post-earnings announcement drift
- Market reactions to small surprises  
may be overstated or understated depending on data version.

---

### 4. Best Practices for Return Prediction Research
The paper implicitly recommends:
- Archiving data vintages when possible
- Reporting I/B/E/S extraction dates
- Stress-testing results across alternative forecast constructions

---

# *You Have a Point – But a Point Is Not Enough: The Case for Distributional Forecasts of Earnings*

[Article PDF](Point_Not_Enough_Distributional.pdf)

Dichev, I. D., Huang, X., Lee, D. K. K., & Zhao, J. (2025). *You have a point – but a point is not enough: The case for distributional forecasts of earnings*. Working paper, Goizueta Business School, Emory University.

---

## Overview

This article argues that **traditional point forecasts of earnings (e.g., consensus EPS)** are fundamentally incomplete and potentially misleading. Instead, the authors advocate for **distributional earnings forecasts**, which characterize not only the expected value of earnings but also the **shape, dispersion, and tail risks** of possible outcomes.

The paper is both conceptual and empirical, demonstrating that **information contained in the full distribution of earnings expectations is economically meaningful** and has implications for how investors price risk and forecast stock returns.

---

## Data Sources

The study combines multiple large-scale datasets:

- **I/B/E/S analyst earnings forecasts**
  - Individual analyst point forecasts
  - Used to infer implied forecast distributions
- **Compustat**
  - Realized earnings and accounting fundamentals
- **CRSP**
  - Stock returns and market data
- **Option-implied information (conceptual benchmark)**
  - Used as a comparison point for distribution-based expectations

The analysis spans a broad cross-section of U.S. publicly traded firms over multiple decades.

---

## Key Methodology

### 1. Constructing Earnings Forecast Distributions
Rather than relying on the consensus mean or median, the authors:
- Aggregate **individual analyst forecasts** into a **firm-level distribution**
- Extract moments such as:
  - Variance (uncertainty)
  - Skewness (downside vs. upside risk)
  - Tail thickness (extreme outcomes)

This approach treats disagreement among analysts as **information**, not noise.

---

### 2. Evaluating Forecast Quality
The paper compares:
- Point forecasts vs. distributional forecasts
- Ability to predict:
  - Realized earnings
  - Extreme earnings outcomes
  - Forecast errors and revisions

The authors show that **distributional forecasts dominate point forecasts**, especially in identifying downside risk.

---

### 3. Asset Pricing Tests
The study examines whether distributional properties of earnings expectations predict:
- Cross-sectional stock returns
- Earnings-announcement returns
- Measures of risk premia

Portfolio sorts and regression-based asset pricing tests are used to link forecast distributions to subsequent returns.

---

## Main Empirical Findings

### 1. Analyst Disagreement Is Informative
Dispersion and skewness in analyst forecasts:
- Predict the **magnitude and direction of future earnings surprises**
- Contain information beyond the consensus estimate

Higher downside skewness is associated with:
- Negative future surprises
- Lower subsequent stock returns

---

### 2. Point Forecasts Mask Risk
Two firms with identical consensus EPS forecasts can have:
- Very different forecast distributions
- Very different risk profiles  

Markets appear to price these differences, even though they are invisible in standard consensus measures.

---

### 3. Distributional Measures Predict Returns
Firms with:
- Greater downside tail risk
- Higher forecast uncertainty  

earn **higher average returns**, consistent with compensation for earnings risk that is not captured by point forecasts.

---

### 4. Implications for Earnings Announcements
Distributional forecasts:
- Better explain announcement-day returns
- Help predict post-earnings announcement drift, especially when downside risk is elevated

---

## Relevance for Forecasting Stock Returns

### 1. Beyond Earnings Surprises
Traditional signals such as:
- Earnings surprises
- Forecast revisions  

are **one-dimensional**. Distributional forecasts provide **multi-dimensional predictors** that improve return forecasts.

---

### 2. Risk-Based Return Predictability
The results suggest that some return predictability traditionally attributed to mispricing may instead reflect:
- Compensation for asymmetric earnings risk
- Downside tail exposure

This has direct implications for:
- Factor construction
- Risk-adjusted portfolio strategies

---

### 3. Practical Implications for Quantitative Models
For return forecasting and portfolio construction:
- Incorporating analyst forecast dispersion and skewness improves signal quality
- Distributional measures help identify firms vulnerable to negative shocks
- These variables are particularly useful around earnings events

---

# *Rankings of Financial Analysts and I/B/E/S Earnings Consensus*

[Article PDF](Rankings_Financial_Analysts_Consensus.pdf)

Shoorvazi, Z., Bozdog, D., & Karbhari, Y. D. (2024). *Rankings of financial analysts and I/B/E/S earnings consensus*. Stevens Institute of Technology, Working Paper.

---

## Overview

This article develops a **dynamic ranking system for financial analysts** based on the **accuracy of their earnings-per-share (EPS) forecasts** using data from the I/B/E/S database. Rather than treating analyst forecasts as homogeneous inputs to a consensus, the study evaluates **heterogeneity in analyst skill** and examines how analyst performance evolves over time.

The paper contributes to the literature by showing that **analyst identity and past accuracy matter**, and that the I/B/E/S consensus can be improved by conditioning on analyst rankings.

---

## Data Sources

The analysis relies primarily on:

- **I/B/E/S Detail Files**
  - Individual analyst quarterly EPS forecasts
  - Firm-level consensus forecasts
  - Historical realized earnings
- **Firm Coverage**
  - Publicly traded U.S. firms
  - Multiple quarters per firm
- (Indirect relevance)
  - Market data are not directly modeled, but the implications are framed in terms of information quality relevant for investors

The dataset spans multiple firms and years, allowing the authors to track analyst performance longitudinally.

---

## Key Methodology

### 1. Analyst Accuracy Measurement
- Forecast accuracy is measured using **forecast errors** between analyst EPS forecasts and realized EPS.
- Errors are evaluated at the **quarterly horizon**, which is most relevant for short-term market reactions.

---

### 2. Dynamic Analyst Ranking System
- Analysts are ranked **relative to peers** based on historical forecasting accuracy.
- Rankings are:
  - Company-specific (performance on a given firm)
  - Aggregate (performance across multiple firms)
- Rankings are updated through time, allowing analyst skill to evolve.

---

### 3. Stability and Persistence Analysis
- The study examines:
  - Whether high-performing analysts remain highly ranked
  - Whether poor performance persists
- Analyst “longevity” (continued forecasting activity) is linked to ranking stability.

---

### 4. Comparison to Consensus Forecasts
- The paper compares:
  - Simple I/B/E/S consensus forecasts
  - Forecasts constructed using **rank-weighted analysts**
- This highlights whether treating analysts symmetrically is suboptimal.

---

## Main Empirical Findings

### 1. Analyst Skill Is Heterogeneous
- Analysts differ substantially in forecasting accuracy.
- A small subset of analysts consistently outperforms the consensus and their peers.

---

### 2. Persistence in Analyst Performance
- High-ranked analysts are more likely to remain accurate in subsequent periods.
- Low-ranked analysts tend to exhibit persistently poor performance or exit coverage.

This contradicts the view that analyst accuracy is mostly noise.

---

### 3. Consensus Forecasts Can Be Improved
- Consensus forecasts constructed from **top-ranked analysts** are:
  - More accurate
  - Less biased  
than equal-weighted consensus forecasts.

---

### 4. Analyst Attrition and Survival
- Analysts with poor rankings are less likely to continue issuing forecasts.
- This selection effect partially explains improvements in consensus accuracy over time.

---

## Relevance for Forecasting Stock Returns

### 1. Analyst-Based Return Predictors
Since earnings surprises and forecast revisions are key predictors of returns:
- Conditioning on **analyst quality** improves the measurement of true expectations.
- Rank-weighted surprises may better predict:
  - Earnings announcement returns
  - Post-earnings announcement drift (PEAD)

---

### 2. Signal-to-Noise Improvement
Using all analysts equally dilutes information:
- High-skill analysts contain more predictive content
- Low-skill analysts add noise

This is directly relevant for:
- Quantitative earnings surprise construction
- Alpha signals based on analyst expectations

---

### 3. Implications for Market Efficiency
The persistence of analyst skill suggests:
- Markets may underweight superior analysts’ information
- There is scope for **return predictability driven by differential information processing**

---

### 4. Practical Applications
For systematic investors:
- Filter or weight I/B/E/S forecasts by analyst rank
- Combine analyst-quality measures with:
  - Forecast revisions
  - Disagreement
  - Distributional forecast metrics  

to enhance return forecasts.

---



# *Consensus? An Examination of Differences in Earnings Information Across Forecast Data Providers*  

[Article PDF](Consensus_Differences_Forecast_Providers.pdf)

Larocque, S., Watkins, J., & Weisbrod, E. (2025). *Consensus? An Examination of Differences in Earnings Information Across Forecast Data Providers*. Working paper, University of Notre Dame and University of Kansas.

---

### Key Methodology and Data Sources

- **Data Providers Studied:** The paper compares earnings information from the five largest forecast data providers (FDPs): **Bloomberg, Capital IQ, FactSet, I/B/E/S, and Zacks**.
- **Unit of Analysis:** Firm–quarter observations, focusing on **street earnings**, **consensus forecasts**, **actual earnings**, and the resulting **earnings surprise** as reported by each FDP.
- **Core Construct:** *FDP differences* — variation in the reported earnings surprise for the **same firm-quarter** across different FDPs.
- **Empirical Framework:**
  1. Measure the **prevalence and magnitude** of FDP differences.
  2. Examine **capital market consequences** of these differences (price response efficiency, liquidity, volatility).
  3. Test whether investors place greater weight on earnings information with **higher expected quality and salience**.
- **Market Outcomes Analyzed:** Abnormal returns, post-earnings-announcement drift, bid–ask spreads, trading volume, and return volatility around earnings announcements.

---
You are a quantitative finance researcher.  Please summarize the attached article; be sure to note its key methodology and data sources, its main empirical findings, and its relevance for forecasting stock returns.
Please output in markdown format; include a relative link to the filename and a reference line to cite the source.

### Main Empirical Findings

1. **Substantial Cross-Provider Disagreement:**  
   Even for the same firm and quarter, earnings forecasts, actuals, and earnings surprises differ meaningfully across FDPs.

2. **Market Efficiency Implications:**  
   Larger FDP differences are associated with **less efficient price responses** to earnings announcements, as well as **reduced liquidity** and **higher volatility**.

3. **Investor Selectivity Across FDPs:**  
   Investors do not treat all FDPs equally. When discrepancies arise, they rely more heavily on earnings information perceived to have:
   - Higher **data quality** (e.g., cleaner aggregation, fewer errors), and
   - Greater **salience** (more widely used or visible).

4. **Dominant Role of I/B/E/S:**  
   On average, **I/B/E/S ranks highest** in measures of quality and salience, and market reactions align more closely with I/B/E/S-based earnings surprises. This provides validation for its widespread use in academic asset-pricYou are a quantitative finance researcher.  Please summarize the attached article; be sure to note its key methodology and data sources, its main empirical findings, and its relevance for forecasting stock returns.
Please output in markdown format; include a relative link to the filename and a reference line to cite the source.
ing and accounting research.

5. **Strategic Differentiation by Data Providers:**  
   Results are consistent with FDPs pursuing **differentiated information production strategies**, which can unintentionally introduce frictions into capital markets.

---

### Relevance for Forecasting Stock Returns

- **Measurement Matters:**  
  Earnings surprise—one of the most important predictors of short-horizon returns—is **not uniquely defined**. Return predictability can vary depending on the FDP used.
- **Implications for Empirical Asset Pricing:**  
  Studies of post-earnings-announcement drift, anomaly replication, or factor construction may be sensitive to the choice of earnings data provider.
- **Practical Forecasting Insight:**  
  Trading strategies and signals based on earnings surprises may perform differently depending on **which FDP investors collectively attend to**, especially during periods of large cross-provider disagreement.
- **Data Quality as a State Variable:**  
  FDP disagreement itself may proxy for **information frictions**, offering an additional conditioning variable for return predictability and risk assessment.

---

# *The Value of Analyst Forecast Revisions: Evidence from Earnings Announcements*

[Article PDF](Value_Analyst_Forecast_Revision_Announcements.pdf)  

Huang, Kanyuan (2022). *The Value of Analyst Forecast Revisions: Evidence from Earnings Announcements*. PhD Dissertation, University of California, Los Angeles.

---

## Overview

This article studies how **analyst earnings forecast revisions following earnings announcements** contribute to stock return predictability. Rather than focusing solely on traditional earnings surprises, the paper emphasizes analysts’ role as information intermediaries who interpret earnings news for investors.

---

## Key Methodology

- **Event-study framework** centered on **earnings announcements**.
- Firms are **sorted by aggregated analyst forecast revisions** made *after* earnings announcements.
- The predictive power of these revisions is compared against standard measures of **earnings surprises**.
- Cross-sectional tests examine heterogeneity across:
  - Magnitude of earnings surprises  
  - Information opacity  
  - Accrual levels  
  - Investor attention  
  - Analyst disagreement  

The core empirical design evaluates **post–earnings-announcement drift (PEAD)** under different information signals.

---

## Data Sources

- **Analyst earnings forecasts and revisions:** I/B/E/S-style analyst forecast data.
- **Earnings announcement data:** Firm-reported quarterly earnings.
- **Stock returns:** CRSP-style daily and monthly return data.
- **Firm characteristics:** Accounting variables (e.g., accruals) from Compustat-type sources.
- **Attention and information environment proxies:** Trading activity, analyst coverage, and disagreement measures.

---

## Main Empirical Findings

1. **Forecast revisions dominate earnings surprises**  
   Sorting firms on aggregated analyst forecast revisions produces a **much stronger post–earnings-announcement drift** than sorting on earnings surprises alone.

2. **Effects are strongest for large earnings surprises**  
   The predictive power of forecast revisions is concentrated among firms with **large-magnitude earnings surprises**, consistent with analysts helping investors interpret complex or extreme news.

3. **Contradictory signals matter most**  
   Mispricing is largest when **analyst revisions contradict the sign of earnings surprises**, suggesting investors struggle to process conflicting information.

4. **Information environment amplifies predictability**  
   Forecast revisions are more informative when:
   - The earnings environment is more opaque  
   - Firms have high accruals  
   - Investor attention is low  

5. **Analyst disagreement weakens signals**  
   When analysts disagree more, aggregated forecast revisions are **less informative**, consistent with noisier interpretation.

---

## Relevance for Forecasting Stock Returns

- The paper shows that **analyst forecast revisions are a powerful return-predictive signal**, particularly in the earnings-announcement window.
- It provides a refined view of PEAD:  
  > PEAD reflects not just delayed reaction to earnings, but delayed reaction to *analysts’ interpretation* of earnings.
- For quantitative return forecasting:
  - Aggregated post-announcement forecast revisions can improve earnings-based trading strategies.
  - Conditioning on **signal conflicts**, **information opacity**, and **attention proxies** enhances predictability.
- The results support models of **limited attention and signal processing frictions** in asset pricing.

---










