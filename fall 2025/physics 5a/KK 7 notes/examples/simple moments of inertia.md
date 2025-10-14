### uniform thin ring of mass M and radius R
The ring is thin, so $dm = \lambda ds$ where $\lambda = M/2\pi R$ (mass per unit length of ring)
$\rho = R$ for all points, so:

$$I_{ring} = \int^{2\pi R}_0 R^2\lambda ds$$
$$ = R^2(\frac{M}{2\pi R}s|^{2\pi R}_0)$$
$$ = MR^2$$

### uniform thin disk of mass M and radius R
divide into a series of rings with radius $\rho$ and width $d\rho$ and moment of inertia $dI$
$$I = \int dI$$
$dA = 2\pi\rho d\rho$, so:
$$dm = M\frac{dA}{A} = \frac{M2\pi\rho d\rho}{\pi R^2}$$
$$ = \frac{2M\rho d\rho}{R^2}$$
$$dI = \rho^2 dm = \frac{2M\rho^3 d\rho}{R^2}$$
$$I = \int^R_0\frac{2M\rho^3 d\rho}{R^2}$$
$$ = \frac{1}{2}MR^2$$
alternatively, we can double integrate this.

### uniform thin stick of mass M and length L around perpendicular axis through midpoint
![[Pasted image 20251013180005.png]]
$$I_{\sigma, rod} = \int^{L/2}_{-L_2}x^2 dm$$
$$ = \frac{M}{L}\int^{L/2}_{-L/2}x^2dx$$
$$= \frac{M}{L}\frac{1}{3}x^3|^{L/2}_{-L/2}$$
$$ = \frac{1}{12}ML^2$$
## uniform thin stick around perpendicular axis at its end

$$I_{rod} = \frac{M}{L}\int^L_0x^2dx$$
$$ = \frac{1}{3}ML^2$$
### uniform sphere of mass M and radius R, axis through center
$$I_{sphere} = \frac{2}{5}MLR^2$$
