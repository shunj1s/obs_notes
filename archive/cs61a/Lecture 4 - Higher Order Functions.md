### Evaluating Boolean Expressions
False values in python: False, 0, '', None
True values: anything that isn't a false value!

Evaluating expression \<left\> and \<right>
1. If left is false, expression evaluates to left
2. Otherwise, evaluate to right

Evaluate \<left> or \<right>:
1. If left is true, evaluate to left
2. Otherwise, evaluate to right

Evaluate *not* \<exp>
1. Returns true of \<exp> yields a false value

```python
first_name = "Dylan"
first_name and True
# >>> True
first_name or True
# >>> "Dylan"
First_name and False
# >>> False

def get_name(first_name, last_name):
	if first_name:
		return first_name
	else:
		return last_name
		
get_name("", "Chang")
# >>> "Chang"

def get_name(first_name, last_name):
	return first_name or last_name
	
# also works due to nature of or expressions
# if first_name does not exist, it will return last_name
# otherwise, returns first_name

```

Ultimately, Python will **stop evaluating** when it knows the answer and return the most recently evaluated subexpression.

### Guide to Designing Functions
Give each function exactly one job, but make it apply to multiple related situations.
	**Don't repeat yourself (DRY)** - implement something once, and use it many times!

Calling user defined frames:
1. Add a local frame (new environment)
2. Bind that frame's formal parameters to its arguments
3. Execute the function in that new environment
