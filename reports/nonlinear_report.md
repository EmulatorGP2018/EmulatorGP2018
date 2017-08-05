# Methods for solving systems of nonlinear equations

## Newton Method

Pros | Cons 
--- | --- 
**Quadratic** convergence rate<br/><br/>Not too complicated| Lots of operations to do per iteration. Jacobian matrix and its inverse has to be calculated **each iteration**  `O(N^3)` per iteration<br/><br/>The initial approximations **must be** close to the solution of the system to ensure convergence

## Broyden Method

A modified Newton method

Pros | Cons 
--- | --- 
Less computations than Newton method `O(N^2)` per iteration | **Superlinear** convergence rate which is a bit slower than newton method

## Steepest Descent method

Used with any Newton based method to find accurate starting points to ensure convergence

Pros | Cons 
--- | --- 
Good estimate for initial approximations<br/><br/>Converge **independent** of the initial approximations | **Linear** convergence rate |


## Solvers

Lots of numerical math packages use *Modified* Newton algorithms  

Solver | Method(s)
--- | ---
[Netlib `minpack` package](http://www.netlib.org/minpack/) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm*
[Extreme Optimization .NET](http://www.extremeoptimization.com/Documentation/Mathematics/Solving-Equations/Solving-Systems-of-Non-Linear-Equations.aspx) | **Newton method** <br/><br/>Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm*
[Nelib `hompack` package](http://www.netlib.org/hompack/) | **Homotopy methods** //No idea
[IMSL `C` Numerical Library](http://docs.roguewave.com/imsl/c/8.6/pdf/CNL86FC.pdf) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm*
[NAG library](https://www.nag.com/numeric/cl/nagdoc_latest/html/c05/c05qbc.html) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* 
[Matlab `fsolve`](https://www.mathworks.com/help/optim/ug/equation-solving-algorithms.html) | Levenberg-Marquardt method<br/><br/>Trust-region method<br/><br/> Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* 