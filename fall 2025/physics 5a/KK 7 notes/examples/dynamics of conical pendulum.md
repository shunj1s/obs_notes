in [[7.2 Angular Momentum of a Particle]] we used a similar example to look at angular momentum. now, we use the same pendulum to show $\tau = d\mathbf{L}/dt$. 

UCM has no circular motion, so:
$$T\cos\alpha - Mg = 0$$the net force of the pendulum is radially inward, so:
$$\tau_A = \mathbf{r}_A \times \mathbf{F}$$
$$ = 0$$
so, $\frac{d\mathbf{L}_a}{dt} = 0$.

However, if we take the origin at $B$,
$\tau_b = \mathbf{r}_b\times\mathbf{F}$
and $|\mathbf{\tau}_B| = lF\cos{\alpha} = lT\cos\alpha\sin\alpha$.
$$|\tau_B| = Mgl\sin{\alpha}$$
since the direction of $\tau_b$ is tangential to the line of motion $M$:
$$\tau_B = Mgl\sin{\alpha\hat{\mathbf{\theta}}}$$
We know $|\mathbf{L}_B| = Mlr\omega$. $L_B$ has a component $L_z$ and a radial component $L_r$.
$$\mathbf{L_B} = \mathbf{L_z} + \mathbf{L_r}$$
and $\mathbf{L}_z$ is constant because $\tau_B$ has no vertical component.
$\mathbf{L_r}$ has a constant magnitude but  not a constant direction, so $\mathbf{L_B}$ must also be rotating.
$\Delta\mathbf{L}_r = \mathbf{L}_r(t + \Delta t) - L_r(t) \rightarrow |\Delta\mathbf{L}_r|\approx L_r\Delta\theta$.
as $\Delta t \rightarrow 0$, 
$$\frac{dL_r}{dt} = L_r\frac{d\theta}{dt}$$
and since we know $L_r = Mlr\omega\cos\alpha$:
$$\frac{dL_r}{dt} = Mlr\omega^2\cos\alpha$$
since $T\sin\alpha$ so that $Mlr\omega^2\cos\alpha = Tl\sin\alpha\cos\alpha$:
$$\frac{dL_r}{dt} = Mgl\sin\alpha$$
so, by differentiating $\mathbf{L}_B$, we get:
$$\frac{d\mathbf{L}_b}{dt} = Mlr\omega\cos\alpha\frac{d\mathbf{\hat{r}}}{dt}$$
$$ = Mlr\omega^2\cos\alpha\hat{\mathbf{\theta}}$$
