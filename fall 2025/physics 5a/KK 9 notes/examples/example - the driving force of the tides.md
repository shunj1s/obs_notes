- the earth is in free fall towards the sun
- according to the principle of equivalence, it should be impossible to observe the sun's gravitational force
- however, since the system is large, we can notice non-local effects like the tides!

gravitational field of the sun:
$$\mathbf{G}_0 = \frac{GM_s}{r_s^2}\mathbf{\hat{n}}$$
where $M_s$ is the sun's mass and $r_s$ is the distance between the center of the sun and the center of the Earth. 
Thus, for the Earth, $\mathbf{A} = \mathbf{G}_0$.
thus, the force on mass $m$ at $\mathbf{r}$ is $\mathbf{F} = m\mathbf{G}(\mathbf{r})$.
To an earthbound observer:
$$\mathbf{F'} = \mathbf{F} - m\mathbf{A} = m\mathbf{G}(\mathbf{r}) - m\mathbf{G_0}$$
and thus, the apparent field:
$$\begin{array}{c}\mathbf{G'(r)} = \frac{\mathbf{F'}}{m} \\ = \mathbf{G}(\mathbf{r}) - \mathbf{G}_0\end{array}$$

![[Pasted image 20251026164902.png]]
Thus, the fields differ very slightly depending on their location on the earth--while the magnitudes are all very similar, the directions are slightly different

so, let's look at what $\mathbf{G'}$ is at each of the points:
- $\mathbf{G'_a}$ and $\mathbf{G'_c}$:
	the distance from $a$ to the center of the sun = $r_s - R_e$. Thus, the magnitude:
	$$G_a = \frac{GM_s}{(r_s - R_e)^2}$$
	$\mathbf{G_a}$ is parallel to $\mathbf{G_0}$ -- thus, the magnitude:
	$$\begin{array}{ccc}G'_a&=& G_a - G_0 \\ & =& \frac{GM_s}{(r_s - R_e)^2} - \frac{GM_s}{r_s^2} \\ & = & \frac{GM_s}{r_s^2}\left[\frac{1}{[1-(R_e/r_s)]^2} - 1\right] \\ & =& G_0\left[\frac{1}{[1-(R_e/r_s)]^2} - 1\right]\end{array}$$
	Since $R_e/r_s \gg 1$:
	$$\begin{array}{lll}G'_a &=& G_0\left[\left(1-\frac{R_e}{r_s}\right)^{-2} - 1\right] \\ & = & G_0\left[1+2\frac{R_e}{r_s} + ... - 1\right]\\ & \approx & 2G_0\frac{R_e}{r_s}\end{array}$$
	furthermore, $\mathbf{G'_a}$ and $\mathbf{G'_c}$ point radially out from earth.
	![[Pasted image 20251026165727.png]]
- $\mathbf{G'_b}$ and $\mathbf{G'_d}$
	$b$ and $d$ are roughly the same distance to the sun, but $\mathbf{G_b}$ is not parallel to $\mathbf{G_0}$. The angle between them is roughly $\alpha\approx R_e/r_s = 4.3\times10^{-5}\ll 1$.
	Thus:
	$$\begin{array}{lll}G'_b&\approx&G_0\alpha \\ &\approx&G_0\frac{R_e}{r_s}\end{array}$$
	both $\mathbf{G'_b}$ and $\mathbf{G'_d}$ point towards the center of earth--they are equal and opposite.

We notice this effect manifest itself in the tides. The forces at $a$ and $c$ tend to lift the oceans, while the forces at $b$ and $d$ tend to depress them. 