---
title: Relativistic MHD Shock
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
The energy momentum tensor for a relativistic pressureless fluid is
$$T^{\mu\nu} = (\rho h + \frac{b^2}{4\pi})u^\mu u^\nu + \frac{b^2}{8\pi}g^{\mu\nu} - \frac{b^\mu b^\nu}{4\pi}.$$
For 1D shock with perpendicular magnetic field, the jump conditions are
$$[\rho\gamma\beta]=0$$
$$[b\gamma\beta]=0$$
$$[(\rho h + \frac{b^2}{4\pi})\gamma^2\beta]=0$$
$$[(\rho h + \frac{b^2}{4\pi})\gamma^2\beta^2 + \frac{b^2}{8\pi}] = 0.$$
Denote the subscript 1 for the upstream quantities and 2 for the downstream and define $\beta_2/\beta_1 =r$.
Hence
$$\frac{\gamma_2}{\gamma_1} = \sqrt{\frac{1-\beta_1^2}{1-r^2\beta_1^2}}.$$
$$\frac{\rho_2}{\rho_1} = \frac{b_2}{b_1}= \frac{\gamma_1\beta_1}{\gamma_2\beta_2} = \frac{1}{r}\sqrt{\frac{1-r^2\beta_1^2}{1-\beta_1^2}}.$$
Divide them, one gets
$$\beta_2 = \frac{b_1^2-b_2^2}{8\pi} \frac{1}{(\rho_1 h_1 + b_1^2/4\pi)\gamma_1^2\beta_1} + \beta_1.$$
Define $b_1^2/4\pi\rho_1 h_1=\sigma_1$,
$$r = \frac{\sigma_1}{2}\frac{1-(b_2/b_1)^2}{\gamma_1^2\beta_1^2(1+\sigma_1)}+1$$
and one can solve for
$$r = \frac{\sigma_1^2}{4(1+\sigma_1)\beta_1^2}(1+\sqrt{1+\frac{8(1+\sigma_1)\beta_1^2}{\sigma_1^2}}).$$
For high magnetization and $\beta_1\rightarrow 1$, $r\sim\sigma_1/2$.
From Eq 4,
$$\frac{\rho_2 h_2 + b_2^2/4\pi}{\rho_1 h_1 + b_1^2/4\pi} = \frac{\gamma_1^2\beta_1}{\gamma_2^2\beta_2}$$
$$\frac{h_2}{h_1} = \frac{\gamma_1}{\gamma_2}+\sigma_1\frac{\gamma_1}{\gamma_2}(1-\frac{\beta_1}{\beta_2}).$$