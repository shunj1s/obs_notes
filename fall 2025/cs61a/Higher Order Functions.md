### Iteration Example
Fibonacci sequence = 0, 1, 1, 2, 3, 5, 8, etc.
```python
def fib(n):
	'''compute the nth fibonacci number'''
	pred, curr = 0, 1 #0th and 1st fibonacci numbers
	k = 1
	while k < n:
		pred, curr = curr, pred + curr
		k = k + 1
	return curr
```
### Control
Writing a function that does the same thing as an if statement?
```python
if ____:
	_____
else: 
	_____
```
1. Evaluate the header's expression
2. If it is a true value, execute the suite and skip remaining clauses

![[Pasted image 20250905131936.png]]

```python
def if_(c, t, f):
	if c:
		return t
	else:
		return f
```
1. Evaluate the operator and then operand subexpressions
2. Apply the function that is the value of the operator to the arguments (operands)

```python
def real_sqrt(x):
	if x >= 0:
		return sqrt(x)
	else:
		return 0
```

But, we can replace real_sqrt:
```python
def real_sqrt(x):
	return if_(x>=0, sqrt(x), 0)
```
However, this is bad, so there's no point in using it!
### Control Expressions
Logical operators:
	To evaluate the expression \<left> and \<right>:
		1. Evaluate the subexpression \<left>
		2. If the result is a false value v, then the expression evaluates to v
		3. Otherwise, the expression evaluates to the value of the subexpression \<right>
	To evaluate the expression \<left> or \<right>
		4. Evaluate the subexpression \<left>
		5. If the result is a true value v, the expression evaluates to v
		6. Otherwise, the expression evaluates to the subexpression \<right>

```python
def has_big_sqrt(x):
	return x > 0 and sqrt(x) > 10
```
So, if x < 0, sqrt(x) will never be evaluated.

```python
def reasonable(n):
	return n == 0 or 1/n != 0
```
so, reasonable(10 ** 10000) will return false
furthermore, 1/n will never return an error because of n == 0 being evaluated first!

### Higher Order Functions

```python
from math import pi

def area_square(r):
	return r * r
	
def area_circle(r):
	return r * r * pi

def area_hexagon(r):
	return r * r * 3 * sqrt(3) / 2
```

we can use assert statements to create errors

```python
def area_square(r):
	assert r > 0, 'a length must be positive'
	return r * r
```
we could reuse this assert statement... but what about DRY?

```python
def area(r, shape_constant):
	assert r > 0 "A length must be positive"
	return r * r * shape_constant
```
therefore:
```python
def area_square(r):
	return area(r, 1)
	
def area_circle(r):
	return area(r, pi)
	
def area_hexagon(r):
	return area(r, 3 * sqrt(3) / 2)
```
Yay! Basic generalization!
```python
def sum_naturals(n):
	'''sum the first N natural numbers'''
	total, k = 0, 1
	while k <= n:
		total, k = total + k, k + 1
	return total
	
def sum_cubes(n):
	total, k = 0, 1
	while k <= n:
		total, k = total + pow(k, 3), k + 1
	return total
```

wait!!!! but we're repeating ourselves!!!!

```python
def identity(k):
	return k

def cube(k):
	return pow(k, 3)
	
def summation(n, term):
	'''sum the first N terms of a sequence.
	>>> summation (5, cube)
	225
	'''
	total, k = 0, 1
	while k <= n:
		total, k = total + term(k), k + 1
	return total
```
so:
```python
def sum_naturals(n):
	return summation(n, identity)
	
def sum_cubes(n):
	return summation(n, cube)
```

### Functions as Return Values

```python
def make_adder(n):
	""" return a function that takes argument k and returns k + n."""
	def adder(k):
		return k + n
	return adder
```

so, the operator evaluates to a function make_adder, and returns an adder where 1 is a constant

```python
make_adder(1)(2)
# 3
make_adder(2000)(13):
# 2013
f = make_adder(2000)
f
# function
f(13)
# 2013
```
Higher order functions - functions that take a function as an argument value or returns a function as a return value
	- Express general methods of computation
	- Remove repetition from programs



