let $f$ be a function on a domain $D \epsilon \mathbb{R}^2$, and let $(a, b) \epsilon D$ .
	$(a, b)$ is a global maximum of $f$ if $f(a, b) \geq f(x, y)$ for all $(x, y)\epsilon D$
		$(a, b)$ is a local maximum of f if $f(a, b) \geq f(x, y)$ for all $(x, y)$ in some disk centered at $(a, b)$
	$(a, b)$ is a global minimum of $f$ if $f(a, b) \leq f(x, y)$ for all $(x, y)\epsilon D$
		$(a, b)$ is a local minimum of $f$ if $f(a, b)\leq f(x,y)$ for all $(x, y)$ in some disk centered at $(x, y)$

**local extremum**: local minimum or local maximum

$(a, b)$ is a critical point of $f$ if $f_x(a, b) = f_y(a, b) = 0$

**theorem**: if $(a, b)$ is a local extremum, if $(a, b)$ is not on the boundary of $D$, and if $f_x(a, b)$ and $f_y(a, b)$ are defined, then $f_x(a, b) = f_y(a, b) = 0$.
	**proof**:
	$g(x) = f(x, b)$. (fixing y = b and varying only x)
	then $g$ has a local extremum at $a$.
	by the single variable version, $g'(a) = 0$. 
	but $g'(a) = f_x(a, b)$., 
	so $f_x(a, b) = 0$. 
	similarly, $f_y(a, b) = 0$. 
if $(a, b)$ is a local extremum, then at least one of the following holds:
	1. $(a, b)$ is a critical point of $f$
	2. $f_x(a, b)$ and $f_y(a, b)$ are both not defined.
	3. $(a, b)$ is on the boundary of the domain.
	4. 