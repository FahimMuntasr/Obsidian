---
Relations:
  - "[[Discrete Mathematics]]"
  - "[[Calculus and Analytic Geometry]]"
Books:
  - "[[Elementary Linear Algebra with Applications.pdf]]"
  - "[[Elementary linear algebra with applications. Solutions.pdf]]"
Syllabus: "[[MAT125_content.pdf]]"
---

#### Linear Equations
A linear equation in $n$ variables $x_1$,$x_2$,$x_3$,...,$x_n$ is expressed in the form $$a_1x_1+a_2x_2+...+a_nx_n=b$$
where $a_1$,$a_2$,...,$a_n$  and $b$ are real constants

Solution of a linear equation
A solution of a linear equation is a sequence of numbers such that the equation is satisfied when we substitute the variables with the solution values.
A parameter is an arbitrary number which is assigned to a variable, the solution set is described in terms of this parameter.
#### Linear Systems
A finite set of linear equations in the variables $x_1$,$x_2$,$x_3$,....,$x_n$ is called a linear system. 
Every system of linear equations has no solutions, or has exactly one solution, or has infinitely many solutions.
#### Consistent Equations
If there is at least on solution to a linear system it is said to be consistent.
System of equations with no solutions are called inconsistent.
#### Augmented Matrices
An augmented matrix is used to show a linear system in a matrix form where the elements of the matrix are all the coefficients of the linear system of equations in their respective order. 
#### Elementary Row Operations
1. Multiplying an equation by a nonzero constant
2. Interchanging two equations
3. Add a multiple of one equation to another
#### Row - Echelon Form
1. If a row consists entirely of zeros, they are grouped together at the bottom of the matrix.
2. If a row does not consist entirely of zeros, the first non zero number should be a 1 (Leading 1).
3. If any two successive rows do not consist of entirely of zeros, the leading 1 in the lower row occurs farther right than the leading 1 in the higher row.

$$\begin{bmatrix}1&*&*&*\\0&1&*&*\\0&0&1&*\\0&0&0&0\end{bmatrix}$$
#### Reduced Row - Echelon Form
All qualities are same as a row echelon form except an extra point which states that;
1. Each column that contains a leading zero has zeros everywhere else in that column.
$$\begin{bmatrix}1&0&0&*\\0&1&0&*\\0&0&1&*\\0&0&0&0\end{bmatrix}$$
#### Homogenous Equations
An equation is homogenous if all the constant terms are zero.
An homogenous equation always have a solution where all the values are 0. This is called the trivial solution, other solutions are called nontrivial solutions.
Possibilities of a homogenous system;
- The system has only the trivial solutions
- The system has infinitely many solutions in addition to the trivial solution

A homogenous system of linear equations with more unknowns than equations has infinitely many solutions.