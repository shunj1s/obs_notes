building off of [[example - the driving force of the tides]]

pretend that two wells of water run from the surface of earth to the center, where they join.
- one is along the earth-sun axis
- one is $\perp$
- to reach equilibrium, the pressures on the bottom of the wells must be identical.

pressure at height $dr$ = $\rho g(r)dr$ where $\rho$ is the density of water and $g(r)$ is the effective gravitational field at $r$. 
thus, the condition for equilibrium:
$$\int_0^{h_1}\rho g_1(r)dr = \int_0^{h_2}\rho g_2(r)dr$$
where $h_1$ and $h_2$ are the distances from the center of the earth to the surface. ![[Pasted image 20251026170503.png]]
if we assume water is incompressible, $\rho$ is constant. thus:
$$\int_0^{h_1}g_1(r)dr = \int_0^{h_2}g_2(r)dr$$
now, we want to calculate $h_1 - h_2 = \Delta h$, the height of the tide due to the sun.
so, we have to find $g_1(r)$ and $g_2(r)$.
since they are the effective gravitational fields, $g_1(r) = g(r) - G_1(r)$ where $G_1(r)$ is the effective field of the sun along column 1.
Thus, substituting $r$ for $R_e$:
$$G'_1(r) = \frac{2GM_sr}{r_s^3}$$
$$ = 2Cr$$
where $C = GM_s/r_s^3$.
Thus, $g_2(r) = g(r)+ Cr$ and therefore
$$\int^{h_1}_0g(r)dr - \int^{h_2}_0g(r)dr = \int^{h_1}_02Crdr + \int_0^{h_2}Crdr$$
combining the integrals:
$$g\Delta h_s = \frac{3}{2}CR_e^2$$
