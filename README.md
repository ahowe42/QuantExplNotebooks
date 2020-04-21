# Quantitative Modeling Exploration

This is a repository for various quantitative modeling explorations I perform. Most of the explorations stored here will (or have) come from modeling topics I read about or hear somewhere, and want to explore in more detail.

The current explorations are listed below.

## Holt-Winters Time Series Modeling

Holt-winters time series modeling is basically triple exponential smoothing, where smoothing is applied to *levels*, *trends*, and *seasons*. In [this notebook](src/HoltWinters_TripleExponentialSmoothing.ipynb), I explore single-, double-, and triple- exponential smoothing of some data, with smoothing coefficients set via nonlinear optimization (such as *Nelder-Mead*).

## Fast Non-dominated Sorting for Multiobjective Optimization

I've been interested in optimization and multi-objective optimization for quite a while. I read [this paper](docs/2002Debetal_NSGAIIMultiobjectiveGA.pdf) and thought the *Pareto Frontier*-based approach for multi-objective optimization to be very interesting. I coded up the algorithm and evaluated it in [this notebook](src/fastnondominatedsort.ipynb).


## Game Theoretic Dynamic Weighted Feature Evaluation

I read [this paper](docs/2019Chowdhuryetal_AntimicrobResitGameTheory.pdf), in which the authors propose a dynamically-weighted feature selection method based on game theory. Specifically, their approach is based on *mutual information* and *conditional mutual information* - fundamental concepts of information theory. They have code in [this GitHub repository](https://github.com/abu034004/GTDWFE/blob/master/code/GT_Feature_Selection.R), but it's all in `R`, and relies on some `R` packages :-( (*friends don't let friends use `R`!*). So I coded it all up - including the mutual informations - in [this notebook](src/GTDWFE.ipynb).
