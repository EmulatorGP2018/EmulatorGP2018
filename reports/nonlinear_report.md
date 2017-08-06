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
Good estimate for initial approximations<br/><br/>Usually converge even for poor initial approximations | **Linear** convergence rate 

## Inverse quadratic interpolation

Pros | Cons 
--- | --- 
converge fast to the root once they get close | performance is often quite poor if you do not start very close to the actual root <br/><br/>rarely used as a stand-alone algorithm

## Muller method

Pros | Cons 
--- | --- 
Gets imaginary roots | Slower than Newton method<br/><br/>It is much harder to determine the roots of a polynomial of degree 3 or higher





## Solvers

Lots of numerical math packages use *Modified* Newton algorithms  

Solver | Method(s) | Code availability
--- | --- | ---
[Netlib `minpack` package](http://www.netlib.org/minpack/) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Open source
[Extreme Optimization `.NET`](http://www.extremeoptimization.com/Documentation/Mathematics/Solving-Equations/Solving-Systems-of-Non-Linear-Equations.aspx) | **Newton method** <br/><br/>Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Subscription required 
[Nelib `hompack` package](http://www.netlib.org/hompack/) | **Homotopy methods** | Open source
[IMSL `C` Numerical Library](http://docs.roguewave.com/imsl/c/8.6/pdf/CNL86FC.pdf) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Subscription required 
[NAG library](https://www.nag.com/numeric/cl/nagdoc_latest/html/c05/c05qbc.html) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Subscription required 
[Matlab `fsolve`](https://www.mathworks.com/help/optim/ug/equation-solving-algorithms.html) | Levenberg-Marquardt method<br/><br/>Trust-region method<br/><br/> Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Subscription required 
[GNU scientific library `GSL`](https://www.gnu.org/software/gsl/doc/html/multiroots.html) | **Newton method** <br/><br/>Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Open source
[Python `Scipy`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.fsolve.html) | Combination of the **Broyden method** and **Steepest Descent method** known as *Powell hybrid algorithm* | Open source

## References
[https://www.math.utah.edu/software/minpack/minpack/hybrd.html](https://www.math.utah.edu/software/minpack/minpack/hybrd.html)

[http://www.nag.co.uk/numeric/FL/manual/pdf/C05/c05pdf.pdf](http://www.nag.co.uk/numeric/FL/manual/pdf/C05/c05pdf.pdf)

[http://www.ibspan.waw.pl/~paprzyck/mp/cvr/research/varia_papers/CAMES_2000.pdf](http://www.ibspan.waw.pl/~paprzyck/mp/cvr/research/varia_papers/CAMES_2000.pdf)

[Burden Numerical Analysis. Numerical Solutions of Nonlinear Systems of Equations 9th Ed.](ins.sjtu.edu.cn/people/mtang/textbook.pdf)

[https://www.lakeheadu.ca/sites/default/files/uploads/77/docs/RemaniFinal.pdf](https://www.lakeheadu.ca/sites/default/files/uploads/77/docs/RemaniFinal.pdf)

[https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.fsolve.html](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.fsolve.html)

[https://www.gnu.org/software/gsl/doc/html/multiroots.html](https://www.gnu.org/software/gsl/doc/html/multiroots.html)

[https://www.mathworks.com/help/optim/ug/equation-solving-algorithms.html](https://www.mathworks.com/help/optim/ug/equation-solving-algorithms.html)

[http://docs.roguewave.com/imsl/c/8.6/pdf/CNL86FC.pdf](http://docs.roguewave.com/imsl/c/8.6/pdf/CNL86FC.pdf)

[http://www.netlib.org/minpack/](http://www.netlib.org/minpack/)