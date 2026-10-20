# Statistical and Machine Learning — Homework

Homework for the course **Statistical and Machine Learning** (M2 IM / IMDS / MIAGE, Université de Haute-Alsace).

Author: Amina MENACER

## Contents

| Folder | Topic | Notebook |
|---|---|---|
| [`HW1/`](HW1/) | Introduction and learnability: PAC vs. Agnostic PAC | [`HW1 PAC vs Agnostic PAC.ipynb`](HW1/HW1%20PAC%20vs%20Agnostic%20PAC.ipynb) |
| [`HW2/`](HW2/) | Uniform convergence and the limits of learning | [`HW2_Uniform_Convergence_NFL.ipynb`](HW2/HW2_Uniform_Convergence_NFL.ipynb) |

## HW1 — PAC vs. Agnostic PAC

Experimental comparison of the PAC (realizable) and Agnostic PAC learning frameworks, using an Empirical Risk Minimization (ERM) learner over threshold classifiers on $\mathcal{X} = [0,1]$:

0. Setup and experimental parameters
1. Data generation (realizable and noisy labels)
2. Implementation of ERM
3. Performance evaluation (empirical vs. true error)
4. Experimental verification of PAC learning: Monte Carlo vs. exact failure probability, comparison with the finite-class bound $\log(|\mathcal H|/\delta)/\varepsilon$, influence of $\varepsilon$, $\delta$, $\theta$, choice of ERM rule
5. From PAC to Agnostic PAC with label noise (effect of the noise level $\eta$)
6. Agnostic PAC with a target outside the class (approximation vs. estimation error)
7. Conclusion

## HW2 — Uniform convergence and the limits of learning

Repeated probabilistic simulations of the theoretical results, every Monte Carlo estimate being checked against the exact binomial value:

- **Part I — Uniform convergence.** Empirical risk as a random variable, deviation probability vs. Hoeffding's bound, the maximum deviation $\Delta_S$ over a finite class vs. $2|\mathcal H|e^{-2m\varepsilon^2}$, effect of $|\mathcal H|$ (linear in $\ln|\mathcal H|$), experimental vs. theoretical sample complexity.
- **Part II — No-Free-Lunch.** Fraction of unseen inputs $(1-1/N)^m$, risk $\frac12(1-1/N)^m$ of a memorization learner on random targets, no rule for unseen inputs wins on average.
- **Part III — Prior knowledge.** ERM over threshold classifiers on threshold targets, and a 2×2 comparison (random/structured targets × memorizer/threshold learner) showing that generalization needs a matching inductive bias.

Every experiment uses its own seeded random generator, so the notebooks give the same results whatever the order the cells are run in.

## Requirements

Only `numpy` and `matplotlib`; the learning algorithms are implemented from scratch.

```bash
pip install numpy matplotlib jupyter
jupyter notebook HW2/HW2_Uniform_Convergence_NFL.ipynb
```
