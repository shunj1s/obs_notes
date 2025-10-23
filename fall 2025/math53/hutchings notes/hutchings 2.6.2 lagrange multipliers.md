to minimize or maximize $f(x, y)$ with the constraint $g(x, y) = k$, you want to solve the equations:
$$\nabla f = \lambda \nabla g$$
where $\lambda$ is a scalar called the **lagrange multiplier**
$$ g = k$$ so, $\nabla f$ is some scalar multiplier of $\nabla g$. also need to check where $\nabla g  = 0$.

**claim**: suppose $(x, y)$ minimizes or maximizes $f$ subject to the constraint $g(x, y ) = k$. suppose $\nabla g(x, y) \neq 0$. Then $\nabla f(x, y) = \lambda \nabla g(x, y)$.

let $\gamma$ be a parameterized curve on the level set $g = k$ with $\gamma (0) = (x, y)$. 
since $(x, y)$ is optimal:
$$\frac{d}{dt}|_{t=0}f(\gamma(t)) = 0$$
where left side is equal to $\nabla f(x, y) * \gamma '(0)$.
also, $g(\gamma(t)) = k$ for all $t$. So, 
$$\frac{d}{dt}|_{t=0}d(\gamma(t)) = 0$$
thus, $\nabla g$ will be parallel to $\nabla f$ and perpendicular to $\gamma ' (0)$ (all tangent vectors to the level set).

**example**: maximize $f(x, y) = \frac{xy}{2}$ with the constraint $g(x, y) = x^2 + y^2 = 100$. 

$$\nabla f = <\frac{y}{2}, \frac{x}{2}>$$
$$ \nabla g = <2x, 2y$$
thus:
$$<\frac{y}{2}, \frac{x}{2}> = \lambda<2x, 2y>$$
so, $\lambda = 0$ or $\lambda = \pm \frac{1}{4}$. 
so, solving $\nabla f = \lambda \nabla g$, $x = y$. 


what about solving $g = 100$?
$$2x^2 = 100$$
$$x = \pm \sqrt{50}$$
$$x = \sqrt{50}, y=\sqrt{50}$$
