minimize or maximize $f(x, y)$ subject to the constraint $g(x, y) = k$ 

**ex** find the right triangle with hypotenuse 10 with the largest possible area 
constraint:
$$x^2 + y^2 = 100$$
$$\frac{1}{2}(xy) = A$$ simplest approach to maximize a: use the constraint to eliminate a variable
$$y = \sqrt{100 - x^2}$$
$$g(x) = \frac{x\sqrt{100 - x^2}}{2}$$
where $0 \leq x \leq 10$

$$g'(x) = \frac{\sqrt{100 - x^2}}{2} + \frac{x}{2}\frac{1}{2\sqrt{100 - x^2}}$$
$$ = \frac{\sqrt{100 - x^2}}{2} - \frac{x^2}{2\sqrt{100 - x^2}}$$

$$= \frac{100 - x^2}{2\sqrt{100 - x^2}} - \frac{x^2}{2\sqrt{100 - x^2}}$$
$$ = \frac{100 - 2x^2}{2\sqrt{100 - x^2}}$$

when $g'(0) = 0 <==> 100 - 2x^2 = 0$
	$x^2 = 50$
	$x = \sqrt{50}$

thus, the maximum is $f(\sqrt{50}, \sqrt{50})$
