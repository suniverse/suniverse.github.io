---
title: MHD Turbulence Cascade
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
Consider the ideal incompressible MHD wave governed by the equations
$$\begin{aligned}
 \frac{\partial \vec{v}}{\partial t}+\vec{v}\cdot \nabla\vec{v}&=&\vec{B}\cdot\nabla\vec{B}\\
 \frac{\partial \vec{B}}{\partial t}+\vec{v}\cdot \nabla\vec{B}&=&\vec{B}\cdot\nabla\vec{v}.
\end{aligned}$$

If we write $\vec{B}=\vec{B}_0+\vec{b}$, and introduce Elsasser variables $\vec{z}^{\pm} = \vec{v}\pm\vec{b}$, the above equations can be formulated into
$$\begin{aligned}
	\frac{\partial \vec{z}^{\pm}}{\partial t}\mp \vec{B}_0\cdot \nabla\vec{z}^{\pm}+\vec{z}^{\mp}\cdot \nabla\vec{z}^{\pm}=0.
\end{aligned}$$
It can be easily seen that nonlinear interactions can only occur between two different modes $z^{+}$ and $z^{-}$.

Let $v$ be the amplitude of the wave, by dimensional analysis $d v/d t \sim v\cdot \nabla v\sim k_{\perp} v^2$. Where the perpendicular direction is relative to the direction of $\vec{B}_0$. For a shear Alfven wave, the perturbation direction of $\vec{v}$ and $\vec{b}$ are both perpendicular, while the group velocity is parallel. Also by dimensional analysis $d^2 v/d t^2 \sim d(k_\perp v^2)/d t \sim k_{\perp}^2 v^3$.
$$\begin{aligned}
	\frac{d v}{d t}\sim k_\perp v^2,\quad\frac{d^2 v}{d t^2}\sim k_\perp^2 v^3.
\end{aligned}$$

The change of $v$ in a given time interval $\delta t$ is $\delta v = k_\perp v^2 \delta t +k_\perp^2 v^3 (\delta t)^2/2$.
The 1st term $k_\perp v^2$, since it involves $v^2$, is a three-wave interaction term. In Fourier space, it describes the change of a wave with momentum $p$ from the interaction of two waves with momentum $q$ and $p-q$. The 2nd term $k_\perp^2 v^3$, involving $v^3$, is a four-wave interaction term. For the three wave interaction, the three waves can't all be Alfven wave, for energy and momentum conservations can't be both satisfied from the dispersion relation $\omega = v_A k$.

For the collision of two Alven wave packets with size $1/k_z$ and $1/k_\perp$ in parallel and perpendicular directions. The collision time is ~$(k_z v_A)^{-1}$. For three-wave interaction, $\delta v\sim d v/d t (k_z v_A)^{-1}\sim k_\perp v^2/(k_z v_A)$. And for four-wave interaction  $\delta v\sim d^2 v/d t^2 (k_z v_A)^{-2}\sim k_\perp^2 v^3/(k_z v_A)$.
$$\begin{aligned}
	\frac{\delta v}{v}&\sim& \frac{k_\perp v}{k_z v_A}\quad \textrm{for three-wave interaction}\\
	\frac{\delta v}{v}&\sim& \left(\frac{k_\perp v}{k_z v_A}\right)^2 \quad \textrm{for four-wave interaction}.
\end{aligned}$$

For the collision of two Alven wave packets with size $1/k_z$ and $1/k_\perp$ in parallel and perpendicular directions. The collision time is ~$(k_z v_A)^{-1}$. For three-wave interaction, $\delta v\sim d v/d t (k_z v_A)^{-1}\sim k_\perp v^2/(k_z v_A)$. And for four-wave interaction  $\delta v\sim d^2 v/d t^2 (k_z v_A)^{-2}\sim k_\perp^2 v^3/(k_z v_A)$.
$$\begin{aligned}
	\frac{\delta v}{v}&\sim& \frac{k_\perp v}{k_z v_A}\quad \textrm{for three-wave interaction}\\
	\frac{\delta v}{v}&\sim& \left(\frac{k_\perp v}{k_z v_A}\right)^2 \quad \textrm{for four-wave interaction}.
\end{aligned}$$

In our paper, $v_A=c$, $(k_z v_A)^{-1}\sim \lambda/c$, and we expect $k_\perp\approx k_z$, and $v\sim cA/\lambda \sim s_0 c$.
$$\begin{aligned}
	t_d &\sim& s_0^2\frac{\lambda}{c}\quad \textrm{for three-wave interaction}\\
	t_d &\sim& s_0^4\frac{\lambda}{c}\quad \textrm{for four-wave interaction}.
\end{aligned}$$
I think the above argument can well apply to normal hydrodynamics by just replacing $v_A$ with the fluid speed to get the damping rate for collision of two waves. Nothing special of MHD is assumed here.

In (Thompson \& Blaes 1998) for the relativistic MHD, they denote $\xi$ for the displacement and wirte $\xi = \xi_{+}+\xi_{-}+\xi_{I}$, where $\pm$ denotes the wave propagating along two lightcones $z_\pm = z\pm t$ and $I$ for the transverse direction. $\xi_{\pm}$ are similar to Elsasser variable. Three-wave interactions ($A+A\rightarrow F$) occur when $\xi_+$ and $\xi_-$ collide and cascade to $\xi_I$. The dynamical equation is 
$$\begin{aligned}
	(\partial _t^2-\partial _z^2)\xi_{I}-\nabla_\perp(\nabla_\perp\cdot \xi_I)=2\nabla_\perp (\xi'_+\cdot\xi'_-).
\end{aligned}$$

Here $\xi'_\pm =\partial_\mp \xi_\pm= (\partial_{z}\mp\partial_{t})\xi_\pm$. Then they consider a $\xi_-$ wave is at rest (at const $z_-$) and a $\xi_+$ wave passing through it, so what is the change of $\xi_+$. The $\xi_-$ wave is injected into a box of size $L$, while on both ends, $\xi_-\neq 0$. They argue that the change in $\xi_+$ integrated over the collision is equal to the asymptotic value of $\xi_I$ at $z$ and $t$ large compared to the collision coordinates'' (which I don't quite understand). Assume that, they can write
$$\begin{aligned}
	\delta \xi'_+(z_-,x_\perp) = \frac{1}{2}(\partial_z-\partial_t)\xi_I(z,t,x_\perp)\quad (z,t\rightarrow\infty).
\end{aligned}$$

$$\begin{aligned}
	\delta \xi'_+(z_-,x_\perp) 
	&=& -\frac{1}{2}\int d z_+(\partial^2_z-\partial^2_t)\xi_I\\
	&=& -\frac{1}{2}\int d z_+\nabla_\perp(\partial_-\xi_+\cdot\partial_+\xi_-)\\
	&=& -\frac{1}{2}\nabla_\perp(\xi'_+\cdot\Delta\xi_-).
\end{aligned}$$

$\Delta \xi_- = \int_{-\infty}^{\infty} d z_+\partial_+\xi_-$. From dimensional analysis of above equations $\delta\xi'_+/\xi'_+\sim k_\perp \Delta \xi_-$. Then they argue that in their setting up of boundary conditions, when the $\xi_+$ wave propagates through the box of length $L$, then $\Delta \xi_-\sim\xi$. Therefore, $\delta \xi'/\xi'\sim k_\perp\xi$. Then they get the damping time $t_d/(L/c)\sim (k_\perp \xi)^{-2}$. Compared with previous results for three-wave interaction, this expression just replaces $(k_z v_A)^{-1}$ by $L/c$. All the confusions come from their set-up of the physical picture. The description is vague and they admit that if you impose a wave packet where displacement on the boundary is 0 as in (Goldreich \& Sridhar 1997), $\Delta\xi_-$ vanishes. I think they just try to set up a scenario that their approximation and estimation can work.