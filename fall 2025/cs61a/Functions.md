```python
area, circ = pi * radius * radius, 2 * pi * radius
```
- Assignment statements disregard the earlier assignment statement
```python
f = max
# f --> <built-in function max>
max = 7
# f(1, 2, 3) will still return 3
# max will return 7
max = f
# max(1, 2, 3) will now return 3
```
* If a function is assigned to a variable, it will return the function's value even if the variable is changed (for built-in functions)
```python
from operator import add, mul
# add --> <built-in function add>
# mul --> <built-in-function mul>
def square(x):
	return mul(x, x)
# square --> <function square at [memory spot]>

```
Functions can be called within functions as long as they are defined prior.

**Primitive expressions**:
- number/numeral
- name of a function or variable
- String

**Call expressions**
operator(operand)

## Environment Diagrams
Within a frame, each name is bound to a single value
	A name cannot be repeated.
**Assignment statements** change the relation between names and values within frames.

Execution rule for assignment statements:
1. Evaluate expressions to the right of =, from left to right.
2. Bind names of the left of = to the resulting values in the current frame.
*Right of = is evaluated before the left of =.*

```python
f = min
f = max
g, h = min, max
max = g
max(f(2, g(h(1, 5), 3)), 4)
```
So, what corresponds to what in this execution?
```python
f = max
g = min
h = max
max = min
max(f(2, g(h(1, 5), 3)), 4) = 3
```
For the final line, the operators are evaluated before the operands, which results in the final function called being **h**.

## Defining Functions

Assignment binds names to values. 
Function definition binds names to expressions.

```python
def <name>(<formal parameters>): #signature indicating arguments
	return <return expression>
```
Execution process of def statements:
1. Create a function with signature name(formal parameters)
2. Set the body of that function to be everything *after that first line*
3. Bind name to that function in the first line

Procedure for applying user-defined function:
1. add a local frame, **forming a new environment**
2. bind function's parameters to arguments in that frame
3. execute the body of the function in that environment
So, the signature contains all the information necessary to construct the new, local frame.

Local frame takes priority over global frame when it comes to evaluating name expressions.

Overall:
- An environment is a sequence of frames.
- A name evaluates to the value bound to that name in the earliest frame of the current environment in which that name is found.

```python
def square(square):
	return mul(square, square)
square(-2)
```
While this code seems weird (and appears to be calling itself from the body) the formal parameter square is more recent, and thus overrides the function name "square". Square in this environment means -2, not the function.

## Print and None
What is the difference between "printing" and "evaluating"?
```python
None # --> nothing will return
print(None) # --> the word None will appear
print(print(1), print(2)) # --> will return:
# 1
# 2
# None None
```
Why is this? "None" indicates that nothing has returned.
```python
def does_not_square(x):
	x * x
does_not_square(4) # --> will return None
sixteen = does_not_square(4)
sixteen + 4 # will result in an error
# unsupported operand type for NoneType + int
```

**Pure Functions** strictly return values. For example, the function abs(-2) will return 2 and nothing else.
 
**Non-Pure Functions** also have side effects. print() is a good example--the return value is None, but the side effect causes the output to be displayed.


