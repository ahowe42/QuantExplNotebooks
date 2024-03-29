# Quantitative Modeling Exploration

This is a repository for various quantitative modeling explorations / demonstrations I perform. Most of the explorations stored here will (or have) come from modeling topics I read about or hear somewhere, and want to explore in more detail. In addition, there are few notebooks I created to demonstrate some topic. I have worked on these various topics over the course of a few years, just keeping the files on my computer, but decided to store them all in a single repository. The current explorations are listed below.

## Holt-Winters Time Series Modeling

Holt-winters time series modeling is basically triple exponential smoothing, where smoothing is applied to *levels*, *trends*, and *seasons*. In [this notebook](src/HoltWinters_TripleExponentialSmoothing.ipynb), I explore single-, double-, and triple- exponential smoothing of some data, with smoothing coefficients set via nonlinear optimization (such as *Nelder-Mead*).

## Fast Non-dominated Sorting for Multiobjective Optimization

I've been interested in optimization and multi-objective optimization for quite a while. I read [this paper](docs/2002Debetal_NSGAIIMultiobjectiveGA.pdf) and thought the *Pareto Frontier*-based approach for multi-objective optimization to be very interesting. I coded up the algorithm and evaluated it in [this notebook](src/fastnondominatedsort.ipynb).


## Game Theoretic Dynamic Weighted Feature Evaluation

I read [this paper](docs/2019Chowdhuryetal_AntimicrobResitGameTheory.pdf), in which the authors propose a dynamically-weighted feature selection method based on game theory. Specifically, their approach is based on *mutual information* and *conditional mutual information* - fundamental concepts of information theory. They have code in [this GitHub repository](https://github.com/abu034004/GTDWFE/blob/master/code/GT_Feature_Selection.R), but it's all in `R`, and relies on some `R` packages :-( (*friends don't let friends use `R`!*). So I coded it all up - including the mutual informations - in [this notebook](src/GTDWFE.ipynb).

## Neural Networks

While learning *PyTorch*, I built a simple binary classification neural network with PyTorch - [this notebook](src/my_neuralnetwork_pytorch.ipynb). Based on this, I also created a simple tutorial for creating neural networks with PyTorch - [here](src/Pytorch_Tutorial_BinaryClass.ipynb).

Having coded up neural networks with *TensorFlow*, *Keras*, and *PyTorch*, I decided to attempt building one from scratch by myself. [This notebook](src/my_neuralnetwork.ipynb) is the result. It is incomplete and will only work for modeling a continuous response, but a good exercise in coding a neural network - including forward & backward propagation - nonetheless.

## Outlier Detection with Jackknife Resampling

The [jackknife](https://en.wikipedia.org/wiki/Jackknife_resampling) is a statistical resampling procedure which operates by iterating over a dataset, leaving out each observation sequentially. Some statistic or modeling procedure is then performed over the resultant `n-1` resampled datasets. The jackknife is also called "leave-one-out". In [this notebook](src/jackknife_outlier_demo.ipynb), I demonstrate using jackknife resampling to identify outliers based on how the total sum of squared errors changes when observations are removed.

## Plotly Tutorial

I have written [this tutorial](src/Plotly_tutorial.ipynb) to introduce the plotly visualization software package. Plotly is a powerful tool for developing interactive data visualizations. In addition to being powerful, it is also extremely flexible - perhaps even more than matplotlib. The plotly API is simple, with a shallow learning curve. With it's power and flexibility, one might think that plotly is sub-optimal for rapidly creating "throw-away" plots during exploratory work, and that another package should be used. This is not true - developing publication-ready visualizations with plotly is easy and quick. I have put together this tutorial / reference using my knowledge of plotly. I am sure it is very incomplete and that there topics I've missed. It is, at least, a start to practical use of plotly.

## Automated Machine Learning with TPOT

The acronym "TPOT" stands for "Tree-based Pipeline Optimization Tool". TPOT was first introduced in [this paper](https://dl.acm.org/doi/10.1145/2908812.2908918). It uses [Genetic Programming](https://en.wikipedia.org/wiki/Genetic_programming), with a customizable objective function to identify an optimal pipeline of operations for machine learning modeling. [This notebook](src/TPOT_Demo.ipynb) demonstrates using TPOT.

## Identifying Nonlinear Correlations with Mutual Information

I developed [this notebook](src/MutualInformation_Corr.ipynb) to explore and demonstrate using the maximal information coefficient and total information coefficient to identify nonlinear correlations in a dataset, as a supplement to the usual linear correlation coefficient. It is based on [this paper](https://www.science.org/doi/10.1126/science.1205438\).
