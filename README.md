# Marketing A/B Testing — Advertising Conversion Optimization

## Project Overview

This project analyzes an A/B test involving 588,101 users to determine whether displaying commercial advertisements increases conversion rates compared to public service announcements (PSAs). The goal is to evaluate the effectiveness of the advertising campaign and provide a data-driven rollout recommendation.

## Business Questions

- Do advertisements significantly improve conversion rates?
- How large is the improvement in conversion?
- How does advertisement frequency relate to conversion rates?
- Should the company roll out the advertising campaign?

## Dataset

The [Marketing A/B Testing dataset](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing) contains 588,101 user records, including experiment assignments, conversion outcomes, advertisement frequency, and exposure times.

- **Control Group:** Users shown public service announcements.
- **Treatment Group:** Users shown commercial advertisements.
- **Primary Metric:** Conversion rate.

## Methodology

- Performed data cleaning and validation to identify missing values, duplicate users, and invalid experiment assignments.
- Compared conversion rates between the control and treatment groups.
- Conducted a two-proportion Z-test at a 5% significance level.
- Calculated absolute lift, relative lift, and a 95% confidence interval.
- Analyzed the relationship between advertisement frequency and conversion rates.
- Estimated incremental conversions and break-even advertising costs.

## Key Findings

| Metric | Result |
|---|---:|
| Total Users | 588,101 |
| Control Conversion Rate | 1.79% |
| Treatment Conversion Rate | 2.55% |
| Absolute Conversion Lift | +0.769 percentage points |
| Relative Conversion Lift | +43.09% |
| P-value | 1.705 × 10⁻¹³ |
| 95% Confidence Interval | [0.587, 0.936] pp |
| Estimated Incremental Conversions | 4,343 |

The hypothesis test revealed a statistically significant improvement in conversion rates for users who received advertisements.

### Advertisement Frequency

Conversion rates increased as users received more advertisements, ranging from 0.25% among users who received five or fewer ads to 17.14% among users who received more than 100 ads.

However, this relationship is observational and does not establish that increasing advertisement frequency directly causes higher conversions.

## Business Impact

- Estimated 769 additional conversions per 100,000 users exposed to the advertising treatment.
- Using an assumed contribution margin of $50 per conversion, the estimated break-even incremental advertising cost is approximately $0.38 per user.

## Conclusion and Recommendation

Based on the statistically significant 43.09% relative improvement in conversion rates, I recommend a phased rollout of the advertising campaign, provided that experiment assignment is valid and incremental contribution exceeds advertising costs.

I also recommend maintaining a randomized control group to monitor campaign performance and conducting a follow-up A/B test to determine the optimal advertisement frequency.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Statsmodels
- Jupyter Notebook

## Running the Project

1. Clone the repository.
2. Download `marketing_AB.csv` from Kaggle.
3. Place the dataset in the same directory as the notebook.
4. Install the required Python libraries.
5. Open and run the Jupyter notebook.
