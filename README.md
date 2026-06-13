# EMSC2010 – Week 8 Lectorial 1: Correlation and Bayesian Inference

This repository contains the template Jupyter notebook for **Week 8 Lectorial 1** of *EMSC2010: Data Science for Earth System Scientists* at the Australian National University.

The session introduces **correlation** as a measure of the linear relationship between two variables, and extends this into a Bayesian framework for inferring the population correlation coefficient.

---

## Notebook

### Notebook 1 – Correlation and the Bivariate Normal Distribution (`NB1`)

**Dataset:** Downstream river grain size measurements (distance downstream vs. grain size, in φ units).

This notebook uses river grain size data to explore how grain size changes with distance downstream, and how this relationship can be quantified.

The notebook covers:

- Plotting the raw data and visually assessing the relationship between distance and grain size
- Calculating deviations of each variable from its mean, and plotting these deviations to build intuition for how the sign and magnitude of $xy$ relate to the strength and direction of a relationship
- Calculating the **sample correlation coefficient** $r$ from first principles:

$$r = \frac{\Sigma xy}{\sqrt{\Sigma x^2}\sqrt{\Sigma y^2}}$$

- Applying **Bayes' theorem** via `PyMC` to model the data as a **bivariate normal distribution**, with priors placed on the means, standard deviations, and the population correlation coefficient $\rho$
- Using `arviz` to summarise the posterior distribution of $\rho$ and calculate its 95% credible interval
- Interpreting whether the credible interval excludes zero (indicating a significant linear relationship) — and discussing why correlation alone does not establish *why* two variables are related

**Key concepts:** Sample correlation coefficient, deviations from the mean, bivariate normal distribution, Bayesian inference of a correlation coefficient, credible intervals, correlation vs. causation

**Libraries:** `numpy`, `matplotlib`, `pymc`, `arviz`

---

## Getting Started

This is a **template repository**. To begin working on the notebook:

1. Click **"Use this template"** at the top of this page to create a copy of the repository in your own GitHub account.
2. Open the notebook from your copy of the repository and click the **"Open in Colab"** badge at the top of the notebook to launch it in Google Colab.
3. Before submitting, replace the `uXXXXXXX` placeholder in the filename with your ANU student UID.

---

## Repository Structure

```
EMSC2010-W8-L1/
├── EMSC2010_W8_L1_NB1_uXXXXXXX.ipynb   # Correlation and Bayesian inference of rho
└── README.md
```

---

## Course Information

| | |
|---|---|
| **Course** | EMSC2010 – Data Science for Earth System Scientists |
| **Institution** | Australian National University (ANU) |
| **Week** | 8 |
| **Session** | Lectorial 1 |
| **Topic** | Correlation and Bayesian Inference |

---

## License

This repository is released under the [MIT License](LICENSE).
