---
title: Eliminating Pressure for Incompressible MHD
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
In the formulation of Elsasser's variables $\mathbf{U} = \mathbf{v}+\mathbf{b}$ and $\mathbf{W} = \mathbf{v}-\mathbf{b}$,

$$\begin{aligned}
	&&\partial_t \mathbf{U} = -(\mathbf{W}\cdot\nabla)\mathbf{U}-\nabla p,\\
	&&\partial_t \mathbf{W} = -(\mathbf{U}\cdot\nabla)\mathbf{W}-\nabla p,\\
	&&\nabla\cdot\mathbf{U} = \nabla\cdot\mathbf{W} = 0.
\end{aligned}$$

For undisturbed fluid $\mathbf{U} = V_A$ and $\mathbf{W} =- V_A$. Introducing small purturbation $\mathbf{U} = V_A+\mathbf{u}$ and $\mathbf{W} = -V_A+\mathbf{w}$

$$\begin{aligned}
	&&\partial_t\mathbf{u}-V_A\partial_z\mathbf{u} = -(\mathbf{w}\cdot\nabla)\mathbf{u}-\nabla p,\\
	&&\partial_t\mathbf{w}+V_A\partial_z\mathbf{w} = -(\mathbf{u}\cdot\nabla)\mathbf{w}-\nabla p.\\
\end{aligned}$$

Taking the divergence of above equations
$$\begin{aligned}
	\nabla p  = \nabla\cdot[(\mathbf{w}\cdot\nabla)\mathbf{u}].
\end{aligned}$$

In the Fourier space
$$\begin{aligned}
	k^2 \tilde{p} = (\mathbf{k}\cdot\tilde{\mathbf{u}}(\mathbf{k}_1))(\mathbf{k}_1\cdot\tilde{\mathbf{w}}(\mathbf{k}_2))\delta(\mathbf{k}_1+\mathbf{k}_2-\mathbf{k}).
\end{aligned}$$

Therefore the Fourier transformation of $\nabla p $ gives
$$\begin{aligned}
	\mathbf{k}p = (\hat{\mathbf{k}}\cdot\tilde{\mathbf{u}}(\mathbf{k}_1))(\mathbf{k}\cdot\tilde{\mathbf{w}}(\mathbf{k}_2))\delta(\mathbf{k}_1+\mathbf{k}_2-\mathbf{k}),
\end{aligned}$$
where the incompressible condition $\mathbf{k}_2\cdot\tilde{\mathbf{w}}(\mathbf{k}_2)=0$ is used.

Taking the Fourier transform of the perturbed equations and defining $\omega_k = V_A k_z$
$$\begin{aligned}
	&&(\partial_t-i\omega_k)\tilde{\mathbf{u}}(\mathbf{k}) = -\frac{i}{8\pi}\int d^3 k_1 d^3 k_2\:[\tilde{\mathbf{u}}(\mathbf{k}_1)-\hat{\mathbf{k}}(\hat{\mathbf{k}}\cdot\tilde{\mathbf{u}}(\mathbf{k}_1)](\mathbf{k}\cdot\tilde{\mathbf{w}}(\mathbf{k}_2))\delta(\mathbf{k}_1+\mathbf{k}_2-\mathbf{k})\\
	&&(\partial_t-i\omega_k)\tilde{\mathbf{w}}(\mathbf{k}) = -\frac{i}{8\pi}\int d^3 k_1 d^3 k_2\:[\tilde{\mathbf{w}}(\mathbf{k}_1)-\hat{\mathbf{k}}(\hat{\mathbf{k}}\cdot\tilde{\mathbf{w}}(\mathbf{k}_1)](\mathbf{k}\cdot\tilde{\mathbf{u}}(\mathbf{k}_2))\delta(\mathbf{k}_1+\mathbf{k}_2-\mathbf{k})
\end{aligned}$$
