---
title: Conservation of Topological Quantities in Euler Equation
summary: ""
date: 2026-03-27
draft: false
authors:
  - me
tags:
  - Research
content_meta:
  trending: false

---

<!-- Tip: open with the why, then show results, code, and next steps. -->
The fluid equations in the conservative form are
$$\begin{aligned}
	\partial_t \rho +\nabla\cdot(\rho \boldsymbol{u})&=&0 \\
	\partial_t (\rho u^i)+\nabla\cdot(\rho u^i\boldsymbol{u})&=&-\nabla p.
  \end{aligned}
$$

The Euler equation follows
$$\begin{equation}
	\partial_t \boldsymbol{u}+(\boldsymbol{u}\cdot\nabla) \boldsymbol{u}=-\nabla p,
\end{equation}$$
where $\boldsymbol{u}$ is the fluid velocity, $p$ is the pressure. 
This equation still holds when the fluid \textit{is compressible}.

Conservative quantities from fluid equations are matter, momentum (directly seen in the conservative form), energy, vorticity and kinetic helicity.
The last two are topological quantities, related the the shape of integration curve of the velocity field.
Then we would like to ask if we can get a better geometric/topological description of the fluid.

To do this, usually, the Euler equation is written using differential form. 
Let $u$ to be the velocity field, and $u*$ to be a 1-form,
$$\begin{equation}
	\partial_t u^*+\mathcal{L}_u u^*=-d(\frac{1}{2}|u|^2+p)\equiv df
\end{equation}$$
is exactly the Euler equation.

The vorticity 2-form is given by $\omega=du^*$, by taking exterior derivative of Euler equation we get
$$\begin{equation}
	\partial_t \omega+\mathcal{L}_u\omega=0.
\end{equation}$$

Compare with the normal vorticity evolution equation
$$\begin{equation}
	\partial_t \boldsymbol{\omega}+\nabla\times(\boldsymbol{u}\times\boldsymbol{\omega})=0,
\end{equation}$$
the two equations differ by a term $\boldsymbol{u}(\nabla\cdot\boldsymbol{\omega})$.
However $\nabla\cdot\boldsymbol{\omega}=d\omega=0$, the nice form of vorticity equation is exact.

### Vorticity

One can get 
$$\begin{equation}
	\partial_t \int_S \omega = -\int_S\mathcal{L}_u\omega = \int_S u\cdot d\omega+d(u\cdot\omega) = \int_S d(u\cdot\omega)=0
\end{equation}$$
for area $S$ transported with the flow.

Using Stokes theorem, we can also derive the Kelvin's circulation theorem
$$\begin{equation}
	\partial_t \int_\gamma u^* = \partial_t\int_S\omega = 0
\end{equation}$$
for a closed loop $\gamma$ transported by the flow and spans area $S$.

### Kinetic helicity

$h = u\wedge\omega$ is defined in three dimensional space.
The equation of $h$ is 
$$\begin{equation}
	\partial_t h+\mathcal{L}_u h = df\wedge \omega.
\end{equation}$$

Therefore 
$$\begin{equation}
	\partial_t \int_V h = -\int_V \mathcal{L}_u h +\int_V df\wedge\omega = \int_V df\wedge\omega-d(u\cdot h)-u\cdot dh.
\end{equation}$$

In 3D, $h$ is a 3-form, so $dh=0$. 
$$\begin{equation}
	\partial_t \int_V h = \int_V d(f\wedge\omega-u\cdot h).
\end{equation}$$
Therefore the kinetic helicity is conserved given the boundary term vanishes.

### General Conservation

The conservation relation can be extended to more general cases. 
Let us focus in 3D, for any 1-form $v$ satisfying the equation
$$\begin{equation}
	\partial_t v +\mathcal{L}_u v = dg
\end{equation}$$
with some function $g$, we have the conservation of 3-form $p = \omega\wedge v$ using $dp = 0$
$$\begin{aligned}
		\partial_t \int_V p = -\int_V\mathcal{L}_u p +\int_V \omega\wedge dg = \int_V d(\omega\wedge g-u\cdot p).
\end{aligned}$$

Similarly, for any 2-form $w$ satisfying the equation
$$\begin{equation}
	\partial_t w +\mathcal{L}_u w = dG
\end{equation}$$
with some 1-form $G$, we have the conservation of 3-form $q = u^*\wedge w$ using $dq = 0$
$$\begin{aligned}
		\partial_t \int_V q &=& -\int_V\mathcal{L}_u q +\int_V u\wedge dG+\int_V df\wedge w \nonumber\\
		&=& \int_V d(H-u\cdot q).
\end{aligned}$$
The above expression is valid for simple geometry, say $\mathbb{R}^3$ where all closed form are exact.
So we can write $u\wedge dG +df\wedge w = dH$, for some 2-form $H$.

### Questions

1. How to understand the difference between Lie derivative and advection derivative? In the Euler equation, they differ by some exact form. When deriving conservation laws, this boundary term is usually taken to vanish on the boundary. But the dynamical part of the equation is altered. The exact form is like adding a potential force.
2. What is the role of dimensionality in the picture. The last two conservation laws make use of the fact that they are proportional to the volume form.
3. How can the conservation of topological quantities change the dynamics? e.g. difference of energy cascade direction in 2D and 3D turbulence. In 2D vorticity is locally conserved (transported by the fluid).
4. The kinetic helicity is similar to magnetic helicity $A\wedge dA$ (Chern-Simons form?). Is there any similar gauge transformation in the Euler equation?