why do gyrocompasses work?
- a flywheel free to rotate around two perpendicular axes tends to orient its spin axis parallel to the axis of rotation of the system
- for a gyrocompass, the system is earth, and so the parallel comes to rest with its axis parallel to the polar axis

![[Pasted image 20251024182219.png]]

assume the axle is horizontal with $\mathbf{L}_s$ and points along the $x$ axis.
suppose we attempt to rotate the gyro around the $z$ axis with rate $\omega_z$ by applying some torque $\tau_z$. 

thus, $L_z$ begins to increase. because the flywheel is spinning and $\mathbf{L}_s$ exists, if the gyro rotates around the $A-B$ axis, $\mathbf{L}_s$ will swing towards the $z$ direction.

If $\mathbf{L}_s$ is large, then most of the torque goes into reorienting the spin angular momentum.


### motion of a gyrocompass
![[Pasted image 20251024183505.png]]![[Pasted image 20251024183509.png]]
gyrocompass consisting of a balanced spinning disk held in a light frame supported by a horizontal axle.

placed on a turntable, rotating at steady angular velocity $\Omega$.
has spin angular momentum $L_s = I_s\omega_s$ along the spin axis.
Also possesses angular momentum about the vertical axis at rate $\Omega$.

Since the $A-B$ axis has a pivoted axle, $\tau = 0$ and $dL_h/dt = 0$
thus, there are two contributions to $dL_h/dt$:
	as $\theta$ changes, angular momentum $L_h = I_h\dot{\theta}$ is generated, thus contributing $I_\perp\ddot{\theta}$ 
	change in the direction of $\mathbf{L}_s$ can also cause a change in $L_h$
		since the horizontal component of $\mathbf{L}_s$ is $L_s\sin\theta$, the rate of increase is $\Omega L_s\sin\theta$
Thus, we can consider $\Delta L_h$ to be the sum of the two changes:

$$\frac{dL_h}{dt} = I_\perp\ddot{\theta}+\Omega L_s\sin\theta$$
and since $dL_h/dt = 0$:
$$\ddot{\theta} + (\frac{L_s\Omega}{I_\perp})\sin\theta = 0$$
which is identical to the equation of the pendulum! when the spin axis is near the vertical, small angle approx:
$$\ddot{\theta} + (\frac{L_s\Omega}{I_\perp})\theta= 0$$
thus, axis of the gyroscope executes simple harmonic motion given by 
$$\theta = \theta_0\sin\beta t$$
where $$\beta=\sqrt{\frac{\omega_s\Omega I_s}{I_\perp}}$$
Eventually, the oscillations will be dampened by friction in the bearings at A and B, and thus the spin axis will come to rest parallel to $\Omega$. 




