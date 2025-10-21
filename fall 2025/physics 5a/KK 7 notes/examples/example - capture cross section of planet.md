goal: aim spacecraft onto a planet.

the planet has the shape of a disk with area $\pi R^2$.
since gravity attracts the spacecraft towards the planet, the effective area to land a hit, $A_e$, is geometric than the geometric area of the planet.

we could calculate the energy, OR we could examine possible trajectories of the spacecraft.
![[Pasted image 20251013200131.png]]
distance $b$ between initial trajectory and line $aa$ is known as the *impact parameter* of the trajectory.
$b'$ is the largest impact parameter for which the trajectory hits the planet.
thus, the area through which the trajectory must pass is $A_e = \pi(b')^2$.
so, how do we find $b'$? first of all, we note that the energy of the spacecraft and it's angular momentum around the center of the planet are conserved.
	linear momentum is not conserved.
$K = \frac{1}{2}mv^2$ and $U = -mMG/r$. 
$$ E = \frac{1}{2}mv^2 - \frac{mMG}{r}$$
at first, $r\rightarrow\infty$, so
$$L_i = -mb'v_0$$ $$E_i = \frac{1}{2}mv_0^2$$de
when the distance of closest approach = $R$, $\mathbf{r}$ and $\mathbf{v}$ are perpendicular.
So:
$$L_c = -mRv(r)$$
$$E_c = \frac{1}{2}mv(R)^2 - \frac{mMG}{R}$$
$L$ and $E$ are conserved, so:
$$-mb'v_0 = -mRv(R)$$
$$\frac{1}{2}mv_0^2 = \frac{1}{2}mv(R)^2 - \frac{mMG}{R}$$
by substitution, we obtain:
$$(b')^2 = R^2(1 + \frac{mMG/R}{mv_0^2/2})$$
since $A_e = \pi(b')^2$,
$$A_e = \pi R^2(1 + \frac{mMG/R}{mv_0^2/2})$$
