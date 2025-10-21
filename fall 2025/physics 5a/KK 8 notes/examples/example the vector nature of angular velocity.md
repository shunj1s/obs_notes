### example the vector nature of angular velocity

- consider a particle rotating in a vertical plane.
- $\omega$ lies in the x-y plane, making an angle of 45$\degree$ with the $x-y$ axes. 
- $\omega$ is constant, so $\theta = \omega t$.
![[Pasted image 20251020130943.png]]
thus, we can calculate $\mathbf{v}$ from $\mathbf{v} = d\mathbf{r}/dt$.
from the sketch, we note that $x = -r\cos\theta/\sqrt{2}$ and $y = r\cos\theta/\sqrt{2}$ and $z = r\sin\theta$.
thus:
$$\mathbf{r} = r(-\frac{\cos\theta}{\sqrt{2}}\mathbf{\hat{i}} + \frac{\cos\theta}{\sqrt{2}}\mathbf{\hat{j}} + \sin\theta\mathbf{\hat{k}})$$
differentiating with respect to time:
$$\frac{d\mathbf{r}}{dt} = \omega r(\frac{\sin\theta}{\sqrt{2}}\mathbf{\hat{i}} - \frac{\sin\theta}{\sqrt{2}}\mathbf{\hat{j}} + \cos\theta\mathbf{\hat{k}})$$
but, to prove, we can also use $\mathbf{v} = \omega\times\mathbf{r}$ as a way to find the velocity.
$$\omega = \frac{\omega}{\sqrt{2}}\mathbf{\hat{i}} + \frac{\omega}{\sqrt{2}}\mathbf{\hat{j}}$$
thus, $\omega\times\mathbf{r}$:
$$= \omega r(\frac{\sin\theta}{\sqrt{2}}\mathbf{\hat{i}} - \frac{\sin\theta}{\sqrt{2}}\mathbf{\hat{j}} + \cos\theta\mathbf{\hat{k}})$$

with this, we prove that $\omega$ can be treated like any other vector



