$\mathbf{L}$ is fixed with respect to the rod and rotates in space with the rod. 
$\tau$ is given by $d\mathbf{L}/dt$, and we can compose $d\mathbf{L}/dt$ via the sketch.
$L_z$ is constant ($=L\sin\alpha$), so there is no torque in the $z$ direction. ![[Pasted image 20251021131737.png]]
horizontal component = $L_h = L\sin\alpha$, and it swings with the rod. 
We choose our $x-y$ axes so that $L_h$ coincides with the $x$ axis at $t=0$. 
Thus, at time $t$:
$$L_x = L_h\cos\omega t$$
$$ = L\sin\alpha\cos\omega t$$
$$L_y = L_h\sin\omega t$$
$$ = L\sin\alpha\sin\omega t$$
Thus:
$$\mathbf{L} = L\sin\alpha(\hat{\mathbf{i}}\cos\omega t + \hat{\mathbf{j}}\sin\omega t) + L\cos\alpha\hat{\mathbf{k}}$$
and since the torque is $d\mathbf{L}/dt$:
$$\tau = L\omega\sin\alpha(-\hat{\mathbf{i}}\sin\omega t + \hat{\mathbf{j}}\cos\omega t)$$
using $L = 2ml^2\cos\alpha$:
$$\tau_x = -2ml^2\omega^2\sin\alpha\cos\alpha\sin\omega t$$
$$\tau_y = 2ml^2\omega^2\sin\alpha\cos\alpha\cos\omega t$$
Thus:
$$\tau = \sqrt{\tau_x^2 + \tau_y^2}$$
$$ = \omega L\sin\alpha$$

## geometric method
here, we use a geometric argument emphasizing the connection between torque and $d\mathbf{L}/dt$.

- still using $\mathbf{L}_h$ which rotates with the rod.
- $dL_h/dt = \omega L_h$, which we can learn from the vector diagram
- thus: $$\tau = \frac{dL_h}{dt} = L_h\omega = \omega L \sin\alpha$$
in this case, rather than torque causing $\omega$ to change, torque only causes the direction of $\mathbf{L}$ to change. 
Since a uniform gravitation field exerts no torque on the skew rod, the rod is "statically balanced".
However, since there is a torque on the rod when it rotates, it is not "dynamically balanced".
