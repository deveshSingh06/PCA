# Principal-Component-Analysis-PCA-on-MNIST-dataset
Using PCA I've tried to reduce the dimensions of the MNIST dataset. I've tried to visualize the MNIST dataset in 2-d by reducing the dimensionality of the dataset from 784-d to 2-d.
# About MNIST
MNIST dataset consist of 60k handwritten images of numbers from 0-9 and is commonly used for training various image processing systems.
- It can be downloaded from: https://www.kaggle.com/c/digit-recognizer/data
- For more information on MNIST dataset, visit: https://en.wikipedia.org/wiki/MNIST_database
# Interpretation Of Eigen Values And Eigen Vectors
Any two eigen vectors, say V<sub>i</sub> and V_{j}, of a covariance matrix S_dxd are perpendicular to each other.

Eigen vectors tell the direction of the variance. V_{1} is the direction where the variance is largest, V_{2} the second largest, so on.

Eigen values tell how is the data spread, is it spread only in one axis or amongst many axes. 

Example 1: If Lambda_1 = 3 and Lambda_2 = 0, it means the data is spread only in one dimension.
Example 2: If Lambda_1 = 3 and Lambda_2 = 1, it means the data is spread in two dimensions and it is spread more in the direction of V_1 than V_2.

(Lambda_i/Summation of Lambda_i over i=1 to d) tells what %age of variance is explained in the direction  of V_i when the data is converted from d-dimensions to one dimension(in the direction of V_i only).

Example 1: If Lambda_1 = 3 and Lambda_2 = 0. Since (Lambda_1/Lambda_1 +                  Lambda_2) = 1. It means 100% of variance is explained in the                  direction of V_1 when the data is converted from 2-d to 1-d(in the            direction of V_1)
Example 2: If Lambda_1 = 3 and Lambda_2 = 1. Since (Lambda_1/Lambda_1 +                  Lambda_2) = 0.75. It means only 75% of variance is explained in               the direction of V_1 when the data is converted from 2-d to 1-d(in            the direction of V_1)
