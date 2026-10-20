# Hypothesis Testing — Is Job Training Worth It?

## Objective
This lab tests whether the NSW job training program increased 1978 earnings, looking at both whether the effect was statistically significant and how large it was.

## Methodology
- Loaded the LaLonde NSW job training experiment, which has 445 people: 185 trainees and 260 controls.
- Ran a one-sample t-test and a two-sample Welch's t-test on 1978 earnings.
- Wrote Welch's t-statistic as a function, welch_t(), and checked it against scipy on the full sample and on five subgroups.
- Computed Cohen's d to judge the size of the effect, not only whether it is significant.
- Ran a power analysis to find the power of this study and the sample size needed to detect d = 0.3.
- Tested the treatment effect in 5 overlapping demographic subgroups, then applied Bonferroni and Benjamini-Hochberg corrections.
- Simulated p-value distributions when the null is true and when it is false.

## Key Findings
- Trainees earned $1,794.34 more in 1978 than controls, with a Welch's t of 2.6741 and a p-value of 0.0079, so the difference is statistically significant.
- The Cohen's d was 0.2727, which is a small effect, so the difference is real but not large relative to the spread in earnings.
- 2 of the 5 subgroup effects were significant before correction, but only 1 remained significant after Bonferroni, which shows how running many tests can make results look stronger than they are.
