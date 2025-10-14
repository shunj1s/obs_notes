Two identical weights hanging on drooping arms from a peg.
![[Pasted image 20251013153912.png]]

## oscillation period of the teeter toy
related to [[6.2 Small Oscillations in a Bound System]]
$$U(\theta) = mg[L\cos{\theta} - l\cos{(\alpha + \theta)}] + mg[L\cos{\theta} - l\cos{(\alpha - \theta)}]$$
using $cos{(\alpha \pm \theta)} = \cos{\alpha}\cos{\theta}\pm\sin{\alpha}\sin{\theta}$:
$$U(\theta) = 2mg\cos{\theta}(L - lcos\alpha) = -A\cos\theta$$
where $A = 2mg(l\cos\alpha - L)$.
Using small angle approximation ($\alpha \approx 0$)
$$U(\theta) = -A(1 - \frac{\theta^2}{2})$$
$$\approx -A + \frac{1}{2}A\theta^2$$
If s is the distance of each mass from the pivot:
$$K = \frac{1}{2}(2m)s^2\dot{\theta}^2$$
$$ = \frac{1}{2}B\dot{\theta}^2$$

where $B  = 2ms^2$.
Thus:
$$\omega = \sqrt{\frac{A}{B}} - \sqrt{\frac{g(l\cos\alpha - L)}{s^2}}$$

## stability of teeter toy
related to [[6.3 Stability]]
the toy is quite stable--to understand this, we can look at $U$!
when toy is at angle $\theta$:
$$U(\theta) = = 2mgcos\theta(L - l\cos{\alpha})$$
Equilibrium occurs when:
$$\frac{dU}{d\theta} = -2mg\sin{\theta}(L-l\cos{\alpha}) = 0$$
which occurs when $\theta = 0$ (as expected from symmetry)
but how stable is it? to do that, we look at $\frac{d^2 U}{d\theta ^2}$
$$\frac{d^2 U} {d\theta ^2} = -2mg\cos{\theta}(L-l\cos{\alpha})$$
so at equilibrium,
$$\frac{d^2 U}{d\theta^2}|_{r_0} = -2mg(L - l\cos\alpha)$$
stability requires the second derivative to be positive, so as long as the weights hang below the pivot, then the toy is stable!
![[Pasted image 20251013162321.png]]
