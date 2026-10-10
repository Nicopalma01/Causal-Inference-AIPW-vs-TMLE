# Causal ATE estimation: AIPW vs TMLE

This project compares two doubly robust estimators of the Average Treatment Effect, AIPW and TMLE (with machine-learning and deep-learning outcome models), on the National Supported Work (LaLonde) experimental sample combined with PSID/CPS controls. It evaluates accuracy against the experimental benchmark, efficiency (standard error) and behavior under poor overlap.

## Repository structure
- `notebooks/` – AIPW and TMLE notebooks
- `data/` – NSW sample, CPS/PSID controls and matched/raw datasets
- `docs/` – full project report (English and Italian)

## Methods
- Doubly robust estimation: AIPW and TMLE
- Propensity score via class-conditional Gaussian Mixture Models and Bayes' theorem
- Coarsened Exact Matching on the combined dataset
- Outcome models: Random Forest, Gradient Boosting, fully-connected neural network

## Results
| Method | Estimate | SE | 95% CI |
|---|---|---|---|
| AIPW (ATE) | 384.63 | 367.88 | [-336.41, 1105.66] |
| TMLE (ML) | 194.30 | 356 | [-503, 892] |
| TMLE (Deep Learning) | 1773.69 | 190 | [1401, 2147] |
| Experimental benchmark | 1794.34 | - | - |

## Libraries
numpy, pandas, scikit-learn, keras, cem, PyALE

## Report
See `docs/report_en.pdf`.

## References
LaLonde, R. (1986). Evaluating the econometric evaluations of training programs with experimental data. American Economic Review.

## Author
Nicola Palmieri
