we've found the angular momentum from the [[torque on the rotating skew rod]], but now lets use $\mathbf{L} = \mathbf{\widetilde{I}}\omega$
- massless rod
- length $2l$
- two equal masses $m$ 
- skewed at angle $\alpha$ with the vertical
- rotates around z axis with angular velocity $\omega$

using the parameters $\rho = l\cos\alpha$ and $h = l\sin\alpha$ , the coordinates can be known at any time:
	$x_1 = \rho\cos\omega t$, $y_1 = \rho\sin\omega t$, $z_1 = -h$
	$x_2 = -\rho\cos\omega t$, $y_2 = -\rho\sin\omega t$, $z_2 = h$

from this, we can calculate the components of $\mathbf{\widetilde{I}}$:
$$I_{zz} = m_1(y_1^2 + z_1^2) + m_2(y_2^2 + z_2^2)$$
$$ = 2m(\rho^2\sin^2\omega t + h^2)$$
and $I_{zy} = 2m\rho h\sin\omega t$.
evaluating the remaining terms:
$$\mathbf{\widetilde{I}} = 2m\left(\begin{array}{ccc}\rho^2\sin^2\omega t + h^2 & -\rho^2\sin\omega t \cos\omega t & \rho h \cos\omega t \\ -\rho^2\sin\omega t\cos\omega t & \rho^2\cos^2\omega t + h^2 & \rho h \sin\omega t \\ \rho h \cos\omega t & \rho h \sin\omega t & \rho^2\end{array}\right)$$
and since $\omega = (0, 0, \omega)$:
$L_x = 2m\rho h\omega\cos\omega t$
$L_y = 2m\rho h\omega\sin\omega t$
$L_z = 2m\rho^2\omega$
We can then find the torque:
$$\tau_x = -2m\rho h\omega^2\sin\omega t$$
$$\tau_y = 2m\rho h\omega^2\cos\omega t$$
$$\tau_z = 0$$
if we make the substitution $\rho h = l^2\cos\alpha\sin\alpha$, then we get the answer of [[torque on the rotating skew rod]] exactly.

