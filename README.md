# Expected Maximization
The **EM** algorithm will be implemented, and **GMM** estimation will be performed on an [image dataset](https://github.com/fardinabbasi/Expectation_Maximization/tree/main/Images) containing images of Manchester United and Chelsea football clubs in order to classify them.
```ruby
from sklearn.mixture import GaussianMixture
```
## Preprocessing
1. All the labels have been replaced with '**m**' for Manchester United and '**c**' for Chelsea. The dataset consists of 64 images with the label 'c' and 58 images with the label 'm'.
2. Only the **blue** and **red** channels have been extracted as features. 
3. The dataset is divided into a **training set** and a **test set**.
## Data Exploration
Please find the scatter plot depicting the data points below.

<img src="/readme_images/scatter.png">
The table below provides an analytical description of these features.

| Metric | Red Feature | Blue Feature |
| --- | --- | --- |
| count | 122 | 122 |
| mean | 91.975741 | 78.674581 |
| std | 29.686593 | 30.071529 |
| min | 36.829846 | 23.841212 |
| 25% | 70.142986 | 55.459667 |
| 50% | 90.938226 | 72.883534 |
| 75% | 109.730649 | 96.326040 |
| max | 171.014902 | 188.230243 |
## n_components = 2
Selecting the right number of Gaussian models is essential for achieving the best results. In this study, the focus is on examining the case where n_components = 2.

| Parameter | First Gaussian Model     | Second Gaussian Model       |
| ---       | ---                     | ---                         |
| Mean      | [62.90, 55.94726292] | [104.27, 86.41]  |
| Covariance| [[209.36, 42.49], [ 42.49, 214.85]] | [[716.86, 177.62], [177.62, 792.93]] |

The **contour plot** is shown below.

<img src="/readme_images/contour.png">

## Best n_components
**AIC (Akaike Information Criterion)** and **BIC (Bayesian Information Criterion)** are statistical measures commonly used for model selection and evaluation in the context of Gaussian Mixture Models (GMMs) and other statistical models.

Both AIC and BIC are based on the principle of parsimony, which favors simpler models that explain the data well. The goal is to strike a **balance** between model complexity and goodness of fit. Lower values of AIC or BIC indicate better model performance. The model with the **lowest** AIC or BIC score is considered the **best choice**.

Here are the AIC and BIC scores for n_components ranging from 1 to 10. Based on these scores, the best n_components for this classification problem, considering the aforementioned features, is 1.

<img src="/readme_images/aic.png">
