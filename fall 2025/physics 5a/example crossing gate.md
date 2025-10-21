railroad gate consists of long narrow plank w/ mass $M$ and length $2L$ pivoted at one end. 

where should the support rod be placed to minimize wear and tear ont he pivot?
![[Pasted image 20251015150651.png]]
$F_{sv}$ is due to the support
$F_{pv}$ is due to the pivot/weight force
$F_{pv}$ can be made to vanish, thus minimizing the force on the pivot
$$\tau = MgL - F_{sv}l$$
$$= I_p\ddot{\theta}$$
where $I_p$ is the moment of inertia around the pivot and $L$ is the distance from the pivot to the center of mass (also visualized in diagram)
$$I_p\dot{\theta} \approx (MgL - F_{sv}l)\Delta t$$
$$\approx -F_{sv}l\Delta t$$
Thus, applying Newton's second law:
$$M\frac{dV}{dt} = -(F_{sv} + F_{pv}) + Mg$$
and then integrating:
$$MV = ML\dot{\theta} = -(F_{sv} + F_{pv})$$
Where the impulse can be neglected.
Thus, from these equations:
$$F_{pv}\Delta t = (I_p/l - ML)\dot{\theta}$$
Thus, the support rod should be palced at:
$$l = \frac{I_p}{ML}$$
