Consider $I$ of a body around an axis in the $z$ direction.
$$\rho_j = x_j\mathbf{\hat{i}} + y_j\mathbf{\hat{k}}$$
![[Pasted image 20251013180438.png]]
if center of mass is at $\mathbf{R}$, then the vector perpendicular from the $z$ axis to $\mathbf{R}$ is
$$\mathbf{R}_\perp = X\mathbf{\hat{i}} + Y\mathbf{\hat{j}}$$
So, if $\rho'_j$ is the vector from the axis through the center of mass to particle $j$, then 
$$I_0 = \sum m_j\rho_j^2$$
since $\rho_j = \rho'_j + \mathbf{R}_\perp$ (visible from diagram, apparently)

$$I = \sum m_j\rho_j^2$$
$$ = \sum m_j(\rho'_j + \mathbf{R}_\perp)^2$$
$$ = \sum m_j({\rho'}_j^2 + 2\mathbf{\rho}'_j \cdot\mathbf{R}_\perp + R_\perp^2)$$
since $\sum m_j\mathbf{\rho'}_j = \sum m_j(\mathbf{\rho}_j - \mathbf{R}_j) = M(\mathbf{R_\perp} - \mathbf{R_\perp})$, $\sum m_j \rho'_j = 0$ and the middle term disappears

and if $\mathbf{R_\perp}$ is designated by $l$, then:
$$I = I_0 + Ml^2$$
