`Fahim Muntasir`
# Calculus and Analytic Geometry - I

## Content
- [[#Week 1 Part 1]]
- [[#Week 1 Part 2]]
## Week 1 Part 1
### Functions
##### Definition of a function
A **Function** *f* is a rule that connects a unique output with each unique input 
If the input is labelled *x* ,then the output is denoted by *f*(x)
The input of a function (which is *x* in this case) is always the **independent** variable as it is free to change. Similarly, the output of a function is always the **dependent** variable as it is dependent on the input value

Functions can have one input for one output
                 OR
Functions can have two inputs for one output
				BUT
Functions can NOT have one input with two outputs 
##### Representing functions
Common methods for representing a function are:
- Using a table with inputs and corresponding outputs
- Algebraic notation
- Geometric visualization



##### Absolute functions
$|-a|$  = $|a|$
$|ab|$ = $|a|$ $|b|$ 
|$\frac{a}{b}$| = $\frac{|a|}{|b|}$ , $b$ $\neq$ 0
|$a$ + $b$| $\leq$ |$a$| + |$b$|
##### Domain and Range
The set of all allowable inputs is called the ***domain*** of the function
The set of all allowable outputs is called the ***co-domain*** of the function
	Not all elements of a co-domain have a corresponding input , this means that the number of elements in the range of a function is ***always*** less than or equal to the number of elements in the co-domain of a function
The set of all outputs with a corresponding input is called the ***range*** of the function

## Week 1 Part 2
#### Combining functions
You can perform any arithmetic operation on a function and get a new function
##### Addition
$(f+g)(x) = f(x) + g(x)$
##### Subtraction
$(f-g)(x) = f(x) - g(x)$
##### Multiplication
$(fg)(x) = f(x)g(x)$
##### Division
$(\frac{f}{g})(x) = \frac{f(x)}{g(x)}$
##### Domains of functions
- $f(x)$ is a function with a domain $D_f$ 
- $g(x)$ is a function with a domain $D_g$
If $h(x) = (f+g)(x) = f(x) + g(x)$  OR  $h(x) = (f - g)(x) = f(x) - g(x)$
- $D = D_f \cup D_g$
Example,
let,
$f(x) = 1 + \sqrt{x - 2}$
$g(x) = x - 3$
therefore,
$(f + g)(x) = f(x) + g(x) = x - 2 + \sqrt{x - 2}$ 
$(f - g)(x) = f(x) - g(x) = 4 - x + \sqrt{x - 2}$ 
$(fg)(x) = f(x)g(x) = (1 + \sqrt{x - 2})(x - 3)$
$(\frac{f}{g})(x) = \frac{f(x)}{g(x)} = \frac{(1 + \sqrt{x - 2})}{(x - 3)}$

The method for finding the domains of $(f+g),(f-g),(fg)$ is the same : Find the intersection of the domains of $f(x)$ and $g(x)$ .
$D = D_f \cap D_g$
so,
$D_f = [2,+\infty)$
$D_g = (-\infty,+\infty)$
$D = [2, +\infty) \cup (-\infty,+\infty) = [2, +\infty)$

To find the domain of $(\frac{f}{g})$ , first find the intersection of the domains of $f(x)$ and $g(x)$ and then exclude the values of $x$ where $g(x) = 0$ .
first step : $D = [2, +\infty)$
second step : $g(x) = 0$ when $x = 3$ , so exclude $3$
$D = [2,3) \cup (3,+\infty)$
##### Composite functions
Composite functions are functions with other functions nested inside of them
let,
$f(x) = x^2$
$g(x) = x + 1$
therefore,
$f(g(x)) = (x + 1)^2$
> The domain of $f(g(x))$ consists of all values of x that is in the domain of g(x) for which g(x) is in the domain of f(x)
##### Translation of a function
| Operation on function $f(x)$ | Geometric effect on $f(x)$ |
| ---- | ---- |
| $f(x)+c$ | Shift graph up by $c$ units |
| $f(x)-c$ | Shift graph down by $c$ units |
| $f(x+c)$ | Shift graph left by $c$ units |
| $f(x-c)$ | Shift graph right by $c$ units |
#####  Reflection of a function
| Operation on function $f(x)$ | Geometric effect on $f(x)$ |
| ---- | ---- |
| $f(x \cdot -1)$ | Reflection with respect to y axis |
| $f(x)\cdot-1$ | Reflection with respect to x axis |
##### Transformation of a function
| Operation on function $f(x)$ | Geometric effect on $f(x)$ |
| ---- | ---- |
| Multiply $f(x)$ by $c$ , $(c>1)$ | Vertically stretches by a factor of $c$ |
| Multiply $f(x)$ by $c$ , $(1>c>0)$ | Vertically compresses by a factor of $\frac{1}{c}$ |
| Multiply $x$ by $c$, $(1>c>0)$ | Horizontally stretches by a factor of $c$ |
| Multiply $x$ by $c$, $(c<1)$ | Horizontally compresses b a factor of $\frac{1}{c}$ |
##### Even and odd functions
A function is even when ;
- $f(x) = f(-x)$
- Or in other words, when a graph is symmetrical about the y axis
A function is odd when ;
- $f(x) = -f(x)$
- Or in other words, when a graph has a $180\degree$ clockwise rotational symmetry
