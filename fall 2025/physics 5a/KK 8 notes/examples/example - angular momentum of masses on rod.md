resolving $\omega$ into components can greatly simplify a problem
angular momentum is not necessarily $\parallel$ to angular velocity!
	only in fixed axis rotation where $\mathbf{L}$ and $\omega$ are parallel

consider a simple rigid body consisting of two particles of mass $m$ connected by a massless rod of length $2l$.
![[Pasted image 20251020132457.png]]
the midpoint is attached to a vertical axis rotating at angular speed $\omega$ around the z axis.
the rod is skewed at angle $\alpha$.
what is the angular momentum of the system?
- first, we can attempt to calculate the angular momentum from the definition $L = \sum(r_i \times p_i)$. since each mass moves in a circle with radius $l\cos\alpha$, the linear momentum of each mass is $|\mathbf{p}| = mwl\cos\alpha$, and is tangential to the circular path. taking the midpoint of the skew rod as the origin, $|\mathbf{L}| = 2m\omega l^2\cos\alpha$. 
- or, we can calculate $L$ using $\omega$ as a vector by separating $\omega$ into components $\omega_\perp = \omega\cos\alpha$ and $\omega_\parallel = \omega\sin\alpha$.  $\omega_\parallel$ produces no angular momentum, but since $L$ is parallel to $\omega_\perp$, we can use $L = I\omega$ to calculate $L$. The angular momentum will be $2ml^2$, thus: $$L = 2ml^2\omega\cos\alpha$$. we can also look at how the rod uses [[torque on the rotating skew rod | torque]] to cause $\mathbf{L}$ to change directions. 
