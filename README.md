# Principal Component Analysis
Principal Component Analysis (PCA) is a statistical technique to convert a set of observations of possibly correlated variables into a set of values of linearly uncorrelated variables called principal components. It captures the maximum variability in the data in decreasing order of significance.

Given a data matrix X of dimension N x M, where N is the number of samples and M is the number of features, PCA aims to find a few orthogonal linear combinations of the M features that capture most of the variability.

We first center the data by subtracting the mean:

$$X_{centered} = X - \overline{X}$$

Where $\overline{X}$ is the mean of each feature.

We then calculate the covariance matrix:

$$S = \frac{1}{N} X_{centered}^T X_{centered}$$

The eigen decomposition of S gives us:

$$S = PΛP^{-1}$$

Where $P$ is a M x M matrix with eigenvectors as columns and $Λ$ has eigenvalues λ1 ≥ λ2 ≥...≥ 0 along the diagonal.

We rank eigenvalues from largest to smallest significance. The K principal axes defined by eigenvectors corresponding to the top K eigenvalues represent the directions of maximum variability in the data.

To project a point x onto the new K dimensional space:

$$x_{PCA} = P_K^Tx$$

Where $P_K$ contains eigenvectors in P corresponding to the largest eigenvalues λ1 to λK.

The projected data xPCA has a lower dimension while preserving most information about the variability in X. We have reduced the dimensionality from M to K principal components.

The proportion of total variance captured by selecting K components is given by:

$$\frac{\sum_{i=1}^{K} \lambda_{i}}{\sum_{i=1}^{M}\lambda_{i}}$$
