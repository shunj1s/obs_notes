now, lets look at basic kinematic eqs. in polar coords:

velocity $\leftarrow$ time derivative of:
$$\mathbf{r} = r\hat{\mathbf{r}}(\theta)$$
$$\frac{d\mathbf{r}}{dt} = \frac{dr}{dt}\hat{\mathbf{r}}(\theta) + r\frac{\mathbf{d\hat{r}}(\theta)}{dt}$$
so, we need the time derivative of $\hat{\mathbf{r}}$. but how do we do this?

## base vector time derivatives

$\hat{\mathbf{r}}$ and $\hat{\mathbf{\theta}}$ have time derivatives we need to find.
$$\frac{d\hat{\mathbf{r}}}{dt} = \frac{d}{dt}\cos{\theta}\hat{\mathbf{i}} + \frac{d}{dt}\sin{\theta}\hat{\mathbf{j}}$$
$$ = -\sin{\theta}\dot{\theta}\hat{\mathbf{i}} + \cos{\theta}\dot{\theta}\hat{\mathbf{j}}$$
$$ = (\sin{\theta}\hat{\mathbf{i}} + \cos{\theta}\hat{\mathbf{j}}){\dot{\theta}}$$
since $\hat{\mathbf{\theta}} = \sin{\theta}\hat{\mathbf{i}} + \cos{\theta}\hat{\mathbf{j}}$ 
$$ \frac{d\hat{\mathbf{r}}}{dt} = \dot{\theta}\hat{\mathbf{\theta}}$$
$$\frac{d\hat{\mathbf{\theta}}}{dt} = -\dot{\theta}\hat{\mathbf{r}}$$

so:
$$ \mathbf{v} = \dot{r}\hat{\mathbf{r}} + r\dot{\theta}\hat{\mathbf{\theta}}$$

## acceleration in polar coords
$$ \mathbf{a} = \frac{d\mathbf{v}}{dt}$$ $$ a = \frac{d}{dt}(\dot{r}\hat{\mathbf{r}} + r\dot{\theta}\hat{\mathbf{\theta}})$$
$$= \ddot{r}\hat{\mathbf{r}} + \dot{r}\frac{d\hat{\mathbf{r}}}{dt} + \dot{r}\dot{\theta}\hat{\mathbf{\theta}} + r\ddot{\theta}\hat{\mathbf{\theta}} + r\dot{\theta}\frac{d\hat{\mathbf{\theta}}}{dt}$$
plug in earlier values for $\frac{d\mathbf{\hat{r}}}{dt}$ and $\frac{d\hat{\mathbf{\theta}}}{dt}$:
$$\mathbf{a} = \ddot{r}\hat{\mathbf{r}} + 2\dot{r}\dot{\theta}{\hat{\mathbf{\theta}}} + r\ddot{\theta}\mathbf{\hat{\theta}} -r\dot{\theta}^2\hat{\mathbf{r}}$$
$$\mathbf{a} = (\ddot{r} - r\theta^2)\hat{\mathbf{r}} + (r\ddot{\theta} + 2\dot{r}\dot{\theta})\hat{\mathbf{\theta}}$$
- radial acceleration ($\hat{\mathbf{r}}$)
	- $\ddot{r}\hat{\mathbf{r}}$ is the acceleration due to a change in radial speed
	- $-r\dot{\theta}^2\hat{\mathbf{r}}$ is the centripetal acceleration
- tangential acceleration ($\hat{\mathbf{\theta}}$)
	- $r\ddot{\theta}\hat{\theta}$ - acceleration due to changing tangential speed
	- $2\dot{r}\dot{\theta}\hat{\mathbf{\theta}}$ - coriolis acceleration

 