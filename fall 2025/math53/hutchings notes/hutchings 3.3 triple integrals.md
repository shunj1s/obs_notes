## 3.3.1 definition of triple integrals
Rectangular box $R = [a, b]\times[c,d]\times[r,s]$
Then, suppose we have a function $f: R\rightarrow\mathbb{R}$
	thus, we divide the intervals into parts:
	$$a=x_0 < x_1 < ...<x_n =b$$
	 $$c = y_0 < y_1 < ... < y_n =d$$ $$r = z_0 < z_1 < ... < z_n = s$$
	such that $$x_i - x_{i - 1} = \Delta x = \frac{b- a}{n}$$
now, define$$\iiint_RfdV = \lim_{n\rightarrow\inf}f(x_{ijk}^*, y_{ijk}^*, z_{ijk}^*)\Delta x\Delta y\Delta z$$
where $$(x_{ijk}^*, y_{ijk}^*, z_{ijk}^*)\epsilon[x_{i-1}, x_i]\times[y_{j-1}, y_j]\times[z_{k-1},z_k]$$
**fact**: $\iiint_RfdV$ is well defined if $f$  is continuous

Analog of fubini's theorem for triple integrals:
$$\iiint fdV = \int_a^b\int_c^d\int_f^sf(x, y, z)dzdydx$$
and there are also 5 other orders to arrange this.

Analogue of a "Type 1 region":
	Region over some region $D$ in the $x-y$ plane, where $phi_1, \phi_2:D\rightarrow\mathbb{R}$.
$$R = \{(x, y, z)|(x, y)\epsilon D, \phi_1(x, y)\leq z \leq\phi_2(x, y)\}$$
thus:
$$\iiint_RfdV = \iint_D\int^{\phi_2(x, y)}_{\phi_1(x, y)}f(x, y, z)dzdA$$

if D itself is a "Type 1 region":
$$D = \{(x, y)|a\leq x\leq b, g_1(x)\leq y\leq g_2(x)\}$$
thus:
$$\iiint_R fdV = \int_a^b\int_{g_1(x)}^{g_2(x)}\int^{\phi_2(x, y)}_{\phi_1(x, y)}f(x, y, z)dzdydx$$

Example: let E be the solid bounded by the surfaces $x^2 + z^2 = 4$, $y=0$, $y=4$.
Write $\iiint_EfdV$ as an integrated integral. 
![[Pasted image 20251022103526.png]]
look at possible ranges of each variable
$-2\leq x\leq 2$
$-\sqrt{4-x^2}\leq z\leq \sqrt{4-x^2}$
$0\leq y \leq 4$

thus
$$\int_{-2}^2\int_0^4\int_{-\sqrt{4-x^2}}^{\sqrt{4-x^2}}fdzdydx$$
what about shifting it to $\iiint fdxdydz$?
x and z fulfill the same role, so we can just switch x and z

## 3.3.2
compute $\iiint_ExdV$ where E is the region bound by the paraboloid $x = 4y^2 + 4z^2$ and the plane $x=4$. 
$$\int^4_0\iint_{y^2 + z^2 \leq \frac{x}{4}}xdAdx$$
so, we have to write $xdA$ as an integral over y and z.
since x is a constant in the integral:
$$ = \int^4_0xArea(y^2+z^2\leq\frac{x}{4})dx$$
so, how do we find the area?
	disk of radius $\sqrt{x/4}$
$$=\int_0^4x\pi(\frac{x}{4})dx = \frac{\pi x^3}{12}|^4_0 = \frac{16\pi}{3}$$
we can also do this in different orders, but it won't be as neat
$$\iiint xdxdydz = ?$$
using $x=4$ and $x = 4y^2 + 4z^2$ we get that $1=y^2+z^2$
$$\int_{-1}^1\int_{-\sqrt{1-z^2}}^{\sqrt{1-z^2}}\int x dxdydz$$
but then what about the inner ones? we need x as a range of functions of y and z
lower limit = $4y^2 + 4z^2$
upper limit = 4
integrating this is far messier, but produces the same result ^^

## 3.4.4 triple integrals in spherical coordinates
$$(x, y, z) \rightarrow(\rho, \theta,\phi)$$
![[Pasted image 20251024093857.png]]
$\rho$ fulfills the same role as $r$
$\theta$ is the same
$\phi$ represents the angle the point creates with the $z$ axis

$$z=\rho\cos\phi$$
$$r=\rho\sin\phi$$
from what we know about $r$:
$$x=\rho\sin\phi\cos\theta$$
$$y=\rho\sin\phi\sin\theta$$
$$\rho=\sqrt{x^2+y^2+z^2}$$
bounds of the coordinates:
$$0\leq\phi\leq\pi$$
$$\rho\geq0$$
$\phi=0$ is a positive z axis, whereas $\phi = \pi$ is the negative z axis.
if $\rho > 0$ is fixed, a sphere is created, where $\theta$ is longitude and $\phi$ is magnitude

analogue of a box in spherical coordinates:

$$E = { (\rho, \theta,\phi)| a\leq\rho\leq b; \alpha\leq\theta\leq\beta; c\leq\phi\leq d}\}$$
thus:
$$\iiint_EfdV = \int_c^d\int_\alpha^\beta\int_a^b=f\rho^2\sin\phi dpd\theta d\phi$$
where $\rho^2\sin\phi$ is the magnification factor. 
