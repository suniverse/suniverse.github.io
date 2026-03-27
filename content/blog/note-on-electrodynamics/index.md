---
title: Note on Electrodynamics
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
# Particle Motion in Uniform Perpendicular Electromagnetic Fields

A test particle with mass $m$ and charge $q$ moving at velocity $\boldsymbol{v}$ in an electromagnetic field feels the Lorentz force
$$\frac{d }{d t} (\gamma m\boldsymbol{v}) = q\left(\boldsymbol{E} + \frac{\boldsymbol{v}}{c} \times \boldsymbol{B}\right).$$
Since the magnetic force $\boldsymbol{v}\times\boldsymbol{B}/c$ does no work on the particle, the change of particle energy arises only from the electrical force
$$\frac{d \gamma}{d t} = \frac{q}{m c^2} \boldsymbol{E}\cdot\boldsymbol{v}.$$
When the electromagnetic field is constant in time, analytical solution can be sought by changing the reference frame so that only the electrical or magnetic field exists.

- $B>E$
If the magnetic field dominates, the electrical field vanishes in a reference frame which is moving with drift velocity
$$\boldsymbol{v}_d = \frac{\boldsymbol{E}\times\boldsymbol{B}}{B^2}c.$$
In that reference frame, the test particle will gyrate around the constant magnetic field.
Therefore, the particle's motion in the lab frame will be a combination of gyration around the $\boldsymbol{B}$ and drift with $\boldsymbol{v}_d$.
The energy of the test particle oscillates on the short timescale of the gyration period as $\boldsymbol{E}\cdot\boldsymbol{v}$ varies, but there is no net change of particle energy on the timescale much larger than the gyration period.

- $E>B$
In case the electrical field dominates, the magnetic field will vanishes in a reference frame moving with drift velocity
$$\boldsymbol{v}_d = \frac{\boldsymbol{E}\times\boldsymbol{B}}{E^2}c.$$
The test particle is accelerated in the new reference frame and the resulting motion in the lab frame will be a combination of acceleration along $\boldsymbol{E}$ and drift with $\boldsymbol{v}_d$.
The particle is continuously gaining energy as $\boldsymbol{E}\cdot\boldsymbol{v}$ is always positive. 

- $E=B$

For the speical case where $E=B$, there is no special reference frame that only one field is present.
The analytical solution is given by Landau and Lifshitz.
Assume that the magnetic field is pointing in the $x$ direction and the electrical field in the $z$ direction, there are two constants of motion: the momentum in the $x$ direction $p_x=\gamma m v_x$ and $\alpha\equiv \gamma m c^2(1-v_y/c)$.
The particle is accelerated in the direction of the electrical field following
$$2eEt = \left( 1+\frac{\varepsilon^2}{\alpha^2} \right)p_z +\frac{c^2}{3\alpha^2}p_z^3$$
with $\varepsilon^2=m^2c^4+p_y^2 c^2$.
But the particle is accelerated fastest in the $y$ direction (parallel to $\boldsymbol{E}\times\boldsymbol{B}$)
$$p_y = -\frac{\alpha}{2c} + \frac{p_z^2c^2+\varepsilon^2}{2\alpha c}.$$
And the particle energy increases as 
$$\gamma mc^2 = \frac{\alpha}{2} + \frac{p_z^2c^2+\varepsilon^2}{2\alpha}.$$

# Relativistic Plasma Oscillation
Consider plasma consisting of particles with charge $q$, mass $m$ and number density $n$ in an electrical field, the Lorentz force will accelerate the particle and induce a current density $\boldsymbol{j} = n q \boldsymbol{v}$,
$$\frac{d \boldsymbol{j}}{d t} = nq\frac{d \boldsymbol{v}}{d t} = \frac{n q^2}{\gamma m}\left(\boldsymbol{E}-\frac{\boldsymbol{V}}{c^2}\boldsymbol{E}\cdot\boldsymbol{V}\right).$$
The nonzero charge density will then feedback to the electrical field
$$\frac{\partial \boldsymbol{E}}{\partial t} = -4\pi \boldsymbol{j}.$$
Combining the equation together, we have 
$$\frac{d^2 \boldsymbol{E}}{d t^2} = -\frac{4\pi n q^2}{\gamma m}\left(\boldsymbol{E}-\frac{\boldsymbol{V}}{c^2}\boldsymbol{E}\cdot\boldsymbol{V}\right).$$
This equation exhibits the oscillatory behaviour for the electrical field at approximately the relativistic plasma frequency
$$\omega_{\rm p} = \sqrt{\frac{4\pi n q^2}{\gamma m}}.$$
If the plasma is confined to move in the direction of the electrical field, $\boldsymbol{V}\parallel\boldsymbol{E}$, the oscillation frequency is modified as $\omega_{\rm p} = \sqrt{4\pi n q^2/\gamma^3 m}$.

# Speiser Orbits

Let us consider the motion of a positron in a static electromagnetic field $\boldsymbol{B}=(B_0,B_y(x),0)$ and $\boldsymbol{E}=(0,0,E_z)$, where 
$$ E_z=-aB_0, \qquad 
 B_y=bB_0 h(x).$$
Here $a>0$ and $b>0$ are constants, and $h(x)$ is a smooth function monotonically decreasing from $h\approx 1$ at $x<- \Delta$ to $h\approx -1$ at $x>\Delta$. 
This electromagnetic configuration  describes the jump of $B_y(x)$ on the scale $\Delta$ that forms during the collision of two symmetric Alfven packets, as observed in our simulations (with $b=2A-1$).
Non-relativistic particle motion in a magnetic jump with $h(x)=-x/\Delta$ at $|x|<\Delta$ was studied by Speiser 1965. We are interested here in the relativistic case where the particle is accelerated by $E_z$ to a high Lorentz factor $\gamma$.
The constant $a$ is smaller than unity but close to it.

$\gamma'\sim\gamma_u\gamma_0\sim\gamma_u$ where $\gamma_0$ is the initial particle energy in the lab frame.
We are interested in the case $a$ close to unity, so initially the particle has $v'_y\sim ac\gg |v'_x|=v_x/\gamma_u$, therefore we can approximate the equations of motion as
$$\dot{v'_y} = \frac{q}{\gamma' mc}B'_x v'_z,\qquad
\dot{v'_z} = -\frac{q}{\gamma' mc}B'_x v'_y.$$
The particle will undergo a gyration around $B_x$ with solutions given by (assuming initially $v'_z=0$, $v'_y=v'_0$)
$$
v'_y = v'_0\cos\left(\frac{qB'_x}{\gamma'mc}t'\right),\qquad
v'_z = -v'_0\sin\left(\frac{qB'_x}{\gamma'mc}t'\right).
$$
$v'_z$ will develop values along $qE_z$ in the first half cycle of gyration before it reverses sign.
Now consider the particle is inside the magnetic jump, the equation for $v'_x$ is
$$\ddot{x'} = \dot{v'_x} = -\frac{q B_0b v'_z}{\gamma' mc\Delta}x'.$$
Before $v'_z$ reverses sign, the quantity $\omega^{'2}_{\rm osc}=q B_0bv'_z/\gamma'mc\Delta>0$, so the particle oscillates between magnetic jump with frequency $\omega'_{\rm osc}$.
When $v'_z$ reverses sign, $|x|$ will increase exponentially and the particle will be ejected from the magnetic jump.

After the particle finishes half cycle of the gyration $v'_z$ reverses sign and $v'_y=-ac\approx -c$ is almost a constant, we can approximate the equation as
$$
\dot{v'_x} = -\frac{q}{\gamma' mc}B'_y v'_z,\qquad
\dot{v'_z} = \frac{q}{\gamma' mc}(B'_y v'_x+B'_x c).
$$
Assuming the particle has reached the edge of the magnetic jump where $B'_y$ is also almost constant, the solution of the particle motion is
$$
v'_x = V'\cos\left(\frac{qB'_y}{\gamma'mc}t'+\phi\right) - c\frac{B'_x}{B'_y},\qquad
v'_z = V'\sin\left(\frac{qB'_y}{\gamma'mc}t'+\phi\right)
$$
with $V'$ and $\phi$ being two constants for the amplitude and phase.
Therefore, the particle will gyrate around $B_y$ with a net drift along $x$ away from the center.

In the lab frame, a particle initially with $|v_y|\ll c$ will be ejected with $|v_y|\sim 2u/(1+u^2/c^2)=2ac/(1+a^2)$ with energy gain
$$\gamma=\frac{1+a^2}{1-a^2}$$
and its ejection velocity along $x$ is
$$
    |v_x| \sim \frac{|B'_x/B'_y|c}{\gamma_u(1+u^2/c^2)} = \frac{(1-a^2)c}{(1+a^2)b}= \frac{c}{\gamma b}.
$$
The ejection velocity will decrease with $\gamma$.
