# Session 3 Teaching Guide

## Theme

Engineering data analysis with pandas through a counterflow heat-exchanger experiment.

## Duration

90 minutes.

## Learning objectives

Students will be able to import and inspect tabular measurements, identify data-quality problems, apply documented cleaning rules, calculate performance metrics, group repeated tests, visualize uncertainty, and support an engineering decision with evidence.

## Suggested flow

| Time | Activity |
|---:|---|
| 0–10 min | Connect arrays from Session 2 to labeled DataFrames |
| 10–25 min | Load the embedded experiment and inspect rows, columns, and types |
| 25–40 min | Diagnose missing values and physically impossible measurements |
| 40–55 min | Calculate hot- and cold-side heat rates and energy imbalance |
| 55–68 min | Calculate effectiveness and filter unreliable runs |
| 68–80 min | Group repeated runs and plot mean ± standard deviation |
| 80–90 min | Write an engineering recommendation and complete the exit ticket |

## Core equations

For water, use \(c_p=4180\ \mathrm{J/(kg\,K)}\):

\[
\dot Q_h=\dot m_h c_p(T_{h,in}-T_{h,out}),\qquad
\dot Q_c=\dot m_c c_p(T_{c,out}-T_{c,in}).
\]

\[
\dot Q_{avg}=\frac{\dot Q_h+\dot Q_c}{2},\qquad
C_{min}=\min(\dot m_hc_p,\dot m_cc_p),
\]

\[
\varepsilon=\frac{\dot Q_{avg}}{C_{min}(T_{h,in}-T_{c,in})}.
\]

## Teaching prompts

- Is a missing value automatically a bad experiment?
- Which checks come from physics rather than statistics?
- Why compare hot- and cold-side heat rates?
- Why should repeated runs be summarized with both a mean and variability?
- What evidence is sufficient for an operating recommendation?

## Common difficulties

- Confusing L/min with kg/s.
- Using outlet-minus-inlet on the hot side and obtaining a negative heat rate.
- Silently deleting rows without documenting the rule.
- Averaging runs before checking energy imbalance.
- Treating correlation as proof of causation.

## Assessment

The notebook should retain the raw data, create a separate cleaned table, show transparent filters, use units in every calculated column and plot label, and end with a recommendation tied to the grouped results.

## Extension

Ask advanced students to compare \(\dot Q_h\) and \(\dot Q_c\) with a parity plot or estimate measurement uncertainty using sensor specifications.
