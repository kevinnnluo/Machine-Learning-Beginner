### Regression
* Finding the best-fit line to a set of points

### Gradient ascent
* Definition
  * If we want to find the maximum point on a function, then the best way to move is in the direction of the gradient. In other words, gradient ascent algorithm helps us minimize the error between actual and predicted values. (Linear Algebra: Best-fit line)
* Terminology
  * Weights: Coefficients of our function
* Formula
  * $\nabla f(x, y) = \begin{matrix} \frac{\partial f(x, y)}{\partial x} \\\ \frac{\partial f(x, y)}{\partial y} \end{matrix}$
* Gradient ascent algorithm
  * $\mathbf{w} := \mathbf{w} + \alpha \nabla \mathbf{w}f(\mathbf{w})$

### Using gradient ascent to find the best parameters
* Pseudocode
  * ```
    Start with the weights all set to 1
    Repeat R number of times:
       Calculate the gradient of the entire dataset
       Update the weights vector by alpha * gradient
       Return the weights vector
    ```


### Stochastic gradient ascent
* Definition
  * Because previous optimization algorithm needs too many calculations, we need a better algorithm. Stochastic gradient ascent algorithm updates the weights using only one instance at a time. This is because stochastic gradient ascent is an example of online laerning algorithm, i.e. we can incrementally update the classifier as new data comes in rather than all at once.
* Pseudocode
  * ```
    Start with the weights all set to 1
    For each piece of data in the dataset:
        Calculate the gradient of one piece of data
        Update the weights vector by alpha * gradient
        Return the weights vector
     ```
* Optimization
  * Changes alpha on each iteration, which will improve the oscillations that occur in the dataset or high-frequency oscillations
  * Randomly selecting each instance to use in updating the weights. This will reduce the periodic vatiations


