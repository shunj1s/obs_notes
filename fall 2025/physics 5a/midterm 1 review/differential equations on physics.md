* often used to find behavior at all times or behavior of a whole system
* frame differential equation and solve differential equation

## whirling rope (circular motion)
a uniform rope of mass $M$ and length $L$ is pivoted at one end and whirls in a horizontal plane with angular speed $\omega$. What is the tension in the rope at distance $r$ from the pivot?
![[Pasted image 20251007002725.png]]
so, lets find motion for small section $\Delta r$ with mass $\Delta m = M\Delta r /L$. motion is circular, so section has net radial force. tension is written as $T(r)$ .

inward force at distance $r$ is $T(r)$. outward force = $T(r + \Delta r)$.
treat small section as particle of mass $\Delta m \rightarrow$ radial acceleration = $r\omega^2$.
so:
$$ T(r + \Delta r) - T(r) = -(\Delta m)r\omega^2$$
$$\Delta T = - \frac{Mr\omega^2\Delta r}{L}$$
$$\frac{dT}{dr} = \lim{{\Delta r}\to0}\frac{T(r+\Delta r) - T)r}{\Delta r}$$
$$\frac{dT}{dr} = -\frac{Mr\omega^2}{L}$$
Since this gives us how tension varies with position, we can integrate it as a **differential equation**

$$dT = -\frac{M\omega^2}{L}rdr$$
$$\int_{T_0}^{T(r)}dT = \int_0^r\frac{M\omega^2}{L}rdr$$
$$T(r) - T_0 = -\frac{M\omega^2}{L}\frac{r^2}{2}$$
$$T(r) = T_0 - \frac{M\omega^2}{L}\frac{r^2}{2}$$
To evaluate $T_0$, we need a boundary condition
$$T(L) = 0 = T_0 - \frac{1}{2}M\omega^2L$$
thus $T_0 = \frac{1}{2}M\omega^2L$.


## pulleys
A string with tension T is deflected through angle $2\theta_0$ by a smooth fixed pulley. what is the force on the pulley?

![[Pasted image 20251007003903.png]]

Consider a short segment of string between angles $\theta$ and $\theta + \Delta\theta$. Let $\Delta F$ be the outward force on the segment due to the pulley. 
Take limit $\Delta\theta\rightarrow 0$
$$\Delta F - 2T\sin{\frac{\Delta\theta}{2}} = 0$$
since $\Delta\theta$ is small:
$\Delta F = 2T\frac{\Delta\theta}{2} = T\Delta\theta$.
And the segment exerts an inward force $T\Delta\theta$ on the pulley.
$$\int dF_x = T \int \cos{\theta}d\theta = 2T\sin{\theta}$$

