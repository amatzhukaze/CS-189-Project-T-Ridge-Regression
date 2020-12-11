# CS-189-Project-T-Ridge-Regression

## Updates (12/10)
* Added quiz questions in separate document
* Restructured notebook assignments:
  * Original notebook was very long, and had multiple large sections that depended on each other. We split the original notebook into 5 separate notebooks that can be run independently.
* Improved integration of sklearn
  * Added an sklearn implementation side-by-side with numpy implementation of ridge to allow students to verify their solution
  * Moved the sklearn application section to after the bias-variance tradeoff section, because this is when students are most prepared to tune lambda
* Added a section to the notes clarifying how we would use the Ridge solution to make predictions
* Added content to the Fake Data/Fake Features section
  * Added a section in the notes on how to use the weight vectors learned from both perspectives to make predictions, specifically explained how to use the full (n+d) dimension weight vector from the fake feature perspective for predictions
  * Added quiz questions in notebook asking about how we would use the learned w’s to make predictions

## Navigating the Repo
* [All Assignments](Ridge_Assignment) | [All Solutions](Ridge_Solution)
* Problem 1: OLS, Polynomial Toy Model, and Motivation for Ridge
  * [ipynb Assignment](Ridge_Assignment/prob1.ipynb) | [ipynb Solution](Ridge_Solutions/prob1-sol.ipynb)
* Problem 2: Ridge Regression
  * [ipynb Assignment](Ridge_Assignment/prob2.ipynb) | [ipynb Solution](Ridge_Solutions/prob2-sol.ipynb)
* Problem 3: Sklearn
  * [ipynb Assignment](Ridge_Assignment/prob3.ipynb) | [ipynb Solution](Ridge_Solutions/prob3-sol.ipynb)
* Problem 4: Eigenvalue Perspective of Ridge Regression
  * [ipynb Assignment](Ridge_Assignment/prob4.ipynb) | [ipynb Solution](Ridge_Solutions/prob4-sol.ipynb)
* Problem 5: Alternative Solution to Ridge Regression
  * [ipynb Assignment](Ridge_Assignment/prob5.ipynb) | [ipynb Solution](Ridge_Solutions/prob5-sol.ipynb)
* Slides: [PDF](Ridge_Slides.pdf) | [Google](https://docs.google.com/presentation/d/1LYJdIy-f_f5NRS41nCvi7KfB5YRRByuTvddpJPkE5zQ/edit?usp=sharing)
* Notes: [PDF](Ridge_Notes.pdf) | [Overleaf](https://www.overleaf.com/read/gcgvnyjyxrst)
* Quiz: [PDF](Ridge_Quiz.pdf)

## Learning Objectives
### Overall
Our assignment is broken down into 6 problems:
1. OLS, Polynomial Toy Model, and Motivation for Ridge
2. Ridge Regression
3. Sklearn
4. Eigenvalue Perspective of Ridge Regression
5. Alternative Solution to Ridge Regression

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
  * Understand bias-variance trade-off in the context of ridge regression
  * Understand how the lambda parameter affects bias and variance
  * Code simulation of bias and variance as lambda varies
  * Understand that the lambda that minimizes (bias)^2 + variance also minimizes test error 
#### 3. Sklearn

  * Learn to use Sklearn’s Ridge class to perform Ridge Regression on the same Polynomial Toy Model as before
  * Practice applying Sklearn package to other datasets
  * Practice writing code from scratch
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
