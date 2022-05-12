# PU_Training_tests
Testing effects of positive and unlabelled training variables

[1] Semi-Supervised Classification of Unlabeled Data (PU Learning) https://towardsdatascience.com/semi-supervised-classification-of-unlabeled-data-pu-learning-81f96e96f7cb

[2] Paper Elkan et al 2008: Learning classifiers from only positive and unlabeled data https://dl.acm.org/doi/10.1145/1401890.1401920

Elkan et al claims and proves the probability that a sample is positive is dependent on the probability that a sample is labelled times a constant factor. Labelled means known positive, while unlabelled means could be a positive or negative.

<img src="https://github.com/Magnushhoie/PU_Training_tests/blob/main/figures/formula.png">

In practice, we start with an imbalanced dataset with few positive samples. Then we take a subset of the positive, e.g. 70 %, and sample equally as many of the remaining positive and negative sambles, setting all labels to negative/unlabelled. Then train our probabilistic classifier. We repeat this process n times to build an ensemble. We then use the ensemble to predict on our test set.

<img src="https://github.com/Magnushhoie/PU_Training_tests/blob/main/figures/example_paper.png">

Nb: Since the constant factor above does not affect our AUC calculation, it can be disregarded if the threshold to set is known. Otherwise it can be set as c/2.



