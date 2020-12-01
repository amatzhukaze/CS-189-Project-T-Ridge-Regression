# CS-189-Project-T-Ridge-Regression

## Navigating the Repo
* Assignment: [ipynb](Ridge_Assignment.ipynb)
* Solution: [ipynb](Ridge_Solution.ipynb)
* Slides: [PDF](RidgeRegressionSlides.pdf) [Google](https://docs.google.com/presentation/d/1LYJdIy-f_f5NRS41nCvi7KfB5YRRByuTvddpJPkE5zQ/edit?usp=sharing)
* Notes: [PDF](RidgeRegressionNotes.pdf) [Overleaf](https://www.overleaf.com/read/gcgvnyjyxrst)
* Quiz questions weaved into the coding assignment

## Learning Objectives
### Overall
Our assignment is broken down into 6 problems:
1. OLS, Polynomial Toy Model, and Motivation for Ridge
2. Ridge Regression
3. Bias-Variance Trade Off
4. Eigenvalue Perspective of Ridge Regression
5. Alternative Solution to Ridge Regression
6. Sklearn

The first problem reviews OLS and sets up a polynomial toy model where OLS overfits the training data to show our motivation for Ridge Regression. This transitions into the second problem where we introduce Ridge Regression and have students practice implementing code. The third, fourth, and fifth problems are designed to offer other perspectives on Ridge Regression. Finally, the sixth and last problem on the assignment introduces the Sklearn library to the students and has them training various models using Ridge Regression.

### Broken Down by Section
#### 1. OLS, Polynomial Toy Model, and Motivation for Ridge

  * Review of OLS
  * Review of featurization and understand the Polynomial Toy Model that will be used in this problem and the next
  * Understand how OLS could overfit noisy training data
  * Understand the difference of train error vs test error and how we could identify overfitting from error plots
#### 2. Ridge Regression

  * Implement Ridge Regression
  * Understand how regularization makes us more resistant to noise
  * Notice how tuning the hyper-parameters affects the degree of regularization
#### 3. Bias-Variance Trade-Off

  * Understand bias-variance trade-off in the context of ridge regression
  * Understand how the lambda parameter affects bias and variance
  * Code simulation of bias and variance as lambda varies
  * Understand that the lambda that minimizes (bias)^2 + variance also minimizes test error 
#### 4. Eigenvalue Perspective of Ridge Regression

  * Show the “hacky” perspective of ridge regression
  * Understand how OLS suffers from an ill-conditioned XtX, making the inverse unstable
  * Understand how this instability allows small perturbations from observation noise to drastically change the calculated weight vector
  * Develop intuition that Ridge lower bounds the eigenvalues of XtX, making the matrix more well-conditioned
  * Visually compare the eigenvalues of OLS and Ridge to solidify this intuition
  * Understand how this lower bound prevents the inverse from becoming unstable
  * Understand how this extra stability makes Ridge more robust against small perturbations from observation noise
  * Compare the behavior of eigenvalues in Ridge with a high-pass filter to associate ridge with something more concrete
#### 5. Alternative Solution to Ridge Regression

  * See the parallel between the alternative ridge regression and the minimum-norm solution
  * Exposure to the fake data and fake feature perspectives of Ridge Regression and how we can derive the two closed-form solutions to Ridge this way
#### 6. Sklearn

  * Learn to use Sklearn’s Ridge class to perform Ridge Regression on the same Polynomial Toy Model as before
  * Practice applying Sklearn package to other datasets
  * Practice writing code from scratch
