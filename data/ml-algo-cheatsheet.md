# linear methods for regression
If you have a dataset of the form $$y_i;\vec{x}_i$$ where $$\vec{x}_i$$ is a feature vector and $$y_i$$ is the
label, then you have to find the $$\vec{\beta}$$ vector that minimizes
## linear regression

$$error = \frac{1}{N} \sum_{i}^{N}{\big(y_i - (\beta_0 + \sum_{j=1}^{M}{\beta_i x_{ij}})}\big)^2$$

## lasso regression

$$error + \lambda regularization$$

$$error = \frac{1}{N} \sum_{i}^{N}{\big(y_i - (\beta_0 + \sum_{j=1}^{M}{\beta_i x_{ij}})}\big)^2$$

$$regularization = \sum_{i}^{M}{\lvert \beta_i \rvert}$$

## ridge regression

$$error + \lambda regularization$$

$$error = \frac{1}{N} \sum_{i}^{N}{\big(y_i - (\beta_0 + \sum_{j=1}^{M}{\beta_i x_{ij}})}\big)^2$$

$$regularization = \sum_{j=0}^{M}{\big( \beta_j \big)^2}$$


# linear methods for classification
If you have a dataset of the form $$y_i;\vec{x}_i$$ where $$\vec{x}_i$$ is a feature vector and $$y_i \in \{0, 1\} $$ is the
label, then you have to find the $$\vec{\beta}$$ vector that minimizes
## linear discriminant analysis

$$ \phi = \frac{1}{N} \sum_{i}^{N}{y_i} $$

$$ \vec{\mu}_0 =  { {\sum_{i}^{N}{y_i\vec{x}_i}}\over{\sum_{i}^{N}{y_i} } } $$

$$ \vec{\mu}_1 =  { {\sum_{i}^{N}{(1-y_i)\vec{x}_i}}\over{\sum_{i}^{N}{(1-y_i)}}} $$

$$ \Sigma = \frac{1}{N} \sum_{i}^{N}{\Big( \vec{x}_i - (1-y_i)\vec{\mu}_0 - y_i \vec{\mu}_1 \Big) \Big( \vec{x}_i - (1-y_i) \vec{\mu}_0 - y_i \vec{\mu}_1 \Big)^T } $$


for a new point $$ \vec{w} $$ whe choose the greatest
among $$ P(y=0 | \vec{w}) $$ and  $$ P(y=0 | \vec{w}) $$

where

$$ P(y=0 | \vec{w}) = { { P(\vec{w} | y=0) P(y=0)} \over {P(\vec{w})}} $$

$$ P(y=1 | \vec{w}) = { { P(\vec{w} | y=1) P(y=1)} \over {P(\vec{w})}} $$

$$ P(\vec{w} | y=1) = { {1} \over {\big( 2 \pi \big)^{\frac{1}{2}} \lvert \Sigma \rvert ^{\frac{1}{2} }  } } \exp \Big( - \frac{1}{2} (\vec{w} - \vec{\mu}_1) ^T \Sigma^{-1} (\vec{x} - \vec{\mu}_1) \Big) $$

$$ P(\vec{w} | y=0) = { {1} \over {\big( 2 \pi \big)^{\frac{1}{2}} \lvert \Sigma \rvert ^{\frac{1}{2} }  } } \exp \Big( - \frac{1}{2} (\vec{w} - \vec{\mu}_0) ^T \Sigma^{-1} (\vec{x} - \vec{\mu}_0) \Big) $$

$$ P(\vec{w}) = P(\vec{w} | y=1) P(y=1) + P(\vec{w} | y=0) P(y=0) $$

$$ P(y=1) = \phi $$

$$ P(y=0) = 1 - \phi $$

## logistic regression
## perceptron
## maximal margin classifier

# tree based methods
## regression trees
## classification trees
## random forest

# ensembles
## boosting
## bagging

# support vector machines
## support vector classifier
## support vector machines

# model assessment and selection
## bias, variance and model complexity
## cross validation
## confussion matrix
## accuracy, precision, recall/sensitivity, specificity
## roc and auc

# unsupervised learning
## clustering
## principal components
## non-negative matrix factorization
## independent component analysis
