# LP xuanlang zhao kxs806

## Linear Problem

Maximize or minimize a linear problem under some constraints.

## Standard form

Convert to standard form:

1. Change minimize problem to maximize problem
2. Replace variable without non-negative constraints with $x_i' - x_i''$
3. Change greater-or-equal and equal constraint
4. Rename variables

## slack form

Convert to slack form:

1. Add slack variable to change inequity to equity.
1. Take new variables to the left side.

The left side variables are basic; the right side is none basic.

Set all none basic variables to 0 to get the basic solution

## simplex

1. find the variable which has the maximum positive coefficient, and increase it to find a bind
2. update z value and current solution
3. Repeat until no variable can be bigger

## Auxiliary LP

Optimal value of auxiliary LP will indicate if the original LP is feasible. If original LP is feasible, then the slack form of the auxiliary LP will yield a feasible basic solution to the original LP

## Dual

Dual is an upper bound of the original lp problem.

Get lp dual:

1. Multiply yi to both sides of ith constrain and add them to form an inequality
2. combine terms and make n new constraints with xn's coefficient

