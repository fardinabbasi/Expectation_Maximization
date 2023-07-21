# Expected Maximization
The **EM** algorithm will be implemented, and **GMM** estimation will be performed on an [image dataset](https://github.com/fardinabbasi/Expectation_Maximization/tree/main/Images) containing images of Manchester United and Chelsea football clubs in order to classify them.
## Preprocessing
1. All the labels have been replaced with '**m**' for Manchester United and '**c**' for Chelsea. The dataset consists of 64 images with the label 'c' and 58 images with the label 'm'.
2. Only the **blue** and **red** channels have been extracted as features. 
3. The dataset is divided into a **training set** and a **test set**.
## Data Exploration
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
