MFDNN - Multi-Fidelity Bayesian Optimization via Deep Neural Networks

ASHA - Asynchronous Successive Halving

HB - HyperBand

SH - Successive Halving

**Baseline setup:**

**MFDNN:**

We used the official implementation of MFDNN [1] by the authors which can be found at the following link: https://github.com/shib0li/DNN-MFBO

Initially we tried to use multiple incremental fidelity levels like for DyHPO, however, the method runtime was too high and it could not achieve competitive results. 
Because of that, we use only a few fidelity levels like the authors do in their work [1]. We use the same fidelity levels as for Hyperband, DEHB and BOHB to have a fair comparison 
between the baselines and the same number of initial points to have the same maximal resource allocated for each fidelity level.

As a sanity check, we also ran on the synthetic benchmark offered by the authors to evaluate the convergence of the implementation. In particular, we used the Levy synthetic Benchmark and we provide the regret over time of our run at the following plot:

https://github.com/ConferencePaperSubmission/DYHPO/blob/main/plots/mfdnn_levy_regret.pdf

**ASHA-HB:**

For the suggested comparison against ASHA [2], we decided to incorporate ASHA-HB into our experiments, since, it is an enhancement of ASHA for different initial brackets, like HB is for SH.
For the ASHA-HB implementation we use the implementation from the well known optuna library (version 2.10.0). We used the same eta, minimum and maximal budget as for HB, DEHB and BOHB in our experiments to have a fair comparison between the baselines.

**For all baselines we use the same seeds to have comparable results.**

[1] Multi-Fidelity Bayesian Optimization via Deep Neural Networks
    Li, Shibo and Xing, Wei and Kirby, Robert and Zhe, Shandian
    Advances in Neural Information Processing Systems 2020
[2] A System for Massively Parallel Hyperparameter Tuning
    Liam Li, Kevin Jamieson, Afshin Rostamizadeh, Ekaterina Gonina, Moritz Hardt, Benjamin Recht, Ameet Talwalkar
    Conference on Machine Learning and Systems 2020



