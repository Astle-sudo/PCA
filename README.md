# Principal Component Analysis (PCA)
PCA is a dimensionality reduction technique that transforms a high-dimensional dataset into a smaller set of independent variables that contain most of the information from the original data.

It projects the data onto a new coordinate system such that the projected data has the largest possible variance. This is done by finding the eigenvectors and eigenvalues of the covariance matrix of the data.

Mathematically, if our data matrix is represented by X with dimensions NxM where N is the number of observations and M is the number of features, then the covariance matrix is calculated as:

$$S = \frac{1}{N}(X - \bar{X})(X - \bar{X})^T$$

The eigenvectors (P) and eigenvalues (λ) of S are found and ordered decreasingly by eigenvalue size.

The K principal components are the eigenvectors corresponding to the K largest eigenvalues that can approximate our original dataset. The transformed and dimensionality-reduced dataset X' can then be obtained by:

$$X′ = XP$$

By reducing data to its principal components, PCA minimizes redundancy and reveals hidden structures while still explaining as much variance as possible.
