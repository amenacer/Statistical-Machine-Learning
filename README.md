# Statistical and Machine Learning — Homework

Homework for the course **Statistical and Machine Learning** (M2 IM / IMDS / MIAGE, Université de Haute-Alsace).

Author: Amina MENACER

## Contents

| Folder | Topic | Notebook |
|---|---|---|
| [`HW1/`](HW1/) | Introduction and learnability: PAC vs. Agnostic PAC | [`HW1_PAC_vs_Agnostic_PAC.ipynb`](HW1/HW1_PAC_vs_Agnostic_PAC.ipynb) |

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

Every experiment uses its own seeded random generator, so the notebook gives the same results whatever the order the cells are run in.

## Requirements

Only `numpy` and `matplotlib`; the learning algorithm is implemented from scratch.

```bash
pip install numpy matplotlib jupyter
jupyter notebook HW1/HW1_PAC_vs_Agnostic_PAC.ipynb
```
