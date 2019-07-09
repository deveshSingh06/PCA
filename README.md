# Principal-Component-Analysis-PCA-on-MNIST-dataset
Using PCA, the dimensions of the MNIST dataset have been reduced. The MNIST dataset has been visualized in 2-d by reducing its dimensionality from 784-d to 2-d.
# About MNIST
MNIST dataset consist of 60k handwritten images of numbers from 0-9 and is commonly used for training various image processing systems.
- It can be downloaded from [here](https://www.kaggle.com/c/digit-recognizer/data).
- For more information on MNIST dataset, click [here](https://en.wikipedia.org/wiki/MNIST_database).
# Steps involved in PCA
Let X<sub>nxd</sub> be the given matrix. To reduce the dimentionality of X<sub>nxd</sub>, we apply the following steps:
1. Column standardise X<sub>nxd</sub>.
2. Find the covariance matrix of X<sub>nxd</sub> as:<b>S<sub>dxd</sub> = X<sup>T</sup>X</b>
3. Find the eigen values and eigen vectors of the covariance matrix S<sub>dxd</sub>
4. Select the principal component.

> **Note**: PCA works on the mathematical concept of **maximizing the variance of the projected points**.

## Interpretation Of Eigen Values And Eigen Vectors
- Eigen vectors tell the direction of the variance. V<sub>1</sub> is the direction where the variance is largest, V<sub>2</sub> the second largest, so on.
- Eigen values tell how is the data spread, is it spread only in one axis or amongst many axes.
- Any two eigen vectors, say V<sub>i</sub> and V<sub>j</sub>, of a covariance matrix S<sub>dxd</sub> are perpendicular to each other.
- Example 1: If &#955;<sub>1</sub> = 3 and &#955;<sub>2</sub> = 0, it means the data is spread only in one dimension.
- Example 2: If &#955;<sub>1</sub> = 3 and &#955;<sub>2</sub> = 1, it means the data is spread in two dimensions and it is spread more in the direction of V<sub>1</sub> than V<sub>2</sub>.

- The formula

   ![](https://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Clambda_i%7D%7B%5Csum%5Climits_%7Bi%3D1%7D%5E%7Bn%7D%5Clambda_i%7D100)

tells what percentage of variance is explained in the direction  of V<sub>i</sub> when the data is converted from d-dimensions to one dimension(in the direction of V<sub>i</sub> only).

- Example 1: If &#955;<sub>1</sub> = 3 and &#955;<sub>2</sub> = 0. Since (&#955;<sub>1</sub>/&#955;<sub>1</sub> + &#955;<sub>2</sub>) = 1, it means 100% of variance is explained in the direction of V<sub>1</sub> when the data is converted from 2-d to 1-d(in the direction of V<sub>1</sub>)
- Example 2: If &#955;<sub>1</sub> = 3 and &#955;<sub>2</sub> = 1. Since (&#955;<sub>1</sub>/&#955;<sub>1</sub> + &#955;<sub>2</sub>) = 0.75. It means only 75% of variance is explained in the direction of V<sub>1</sub> when the data is converted from 2-d to 1-d(in the direction of V<sub>1</sub>)
- Eigen values have a property as:
  - &#955;<sub>1</sub>>&#955;<sub>2</sub>>&#955;<sub>3</sub>>&#955;<sub>4</sub>>&#955;<sub>5</sub>>&#955;<sub>6</sub> so on..
  
## Limitations of PCA
- There are chances that we might loose some information when we reduce the dimensionality of a dataset which has very symmetrically spread(such as circular or spherical).
