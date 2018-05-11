# simplex-method
A python implementation for simplex method

The current implementation uses two phase method and is able to identify case for Infeasible solution, Unbounded solution,
Degeneracy and Alternate Solution.
In case of Infeasible solution and Unbounded solution it raises an ValueError and in case of Degeneracy and Alternate Solution
it gives a warning and returns a optimum solution.


The constraints right hand side should be positive and all variables should hold non-negativity conditions.

Rules for constraint representation:

- Each variable should have coefficient if it is in constraint i.e
  `x_1` is not allowed, instead use `1x_1`. Note that it is not necessary to represent each variable in a constraint, but if
  a variable is there then it should have a coefficient.
- Only single spaces should be used.
- For a variable `x_i` i should be an integer in `[1, num_vars]`, where `num_vars` is number of variables

Objective function should be a tuple with first element as objective ie to maximize ('max') or minimize ('min') and second
element should value that is to be optimized (see example).

Here is an example:
``` python
>>> from simplex import Simplex
>>> objective = ('min', '4x_1 + 1x_2')
>>> constraints = ['3x_1 + 1x_2 = 3', '4x_1 + 3x_2 >= 6', '1x_1 + 2x_2 <= 4']
>>> system = Simplex(num_vars=2, constraints=constraints, objective_function=objective)
>>> print(system.solution())
Alternative solution exists.
Solution:
x_1 = 3/5
x_2 = 6/5
min = 17/5
```
