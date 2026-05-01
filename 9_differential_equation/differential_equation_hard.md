# Differential Equations — Advanced Problems Mark Scheme

> **Level:** A-Level P4 top tier / final exam preparation  
> **Estimated time:** approximately 2 hours (recommended: attempt questions first, then check solutions)

---

## Q1. Separable DE — Double Partial Fractions

> **[Problem notes]**  
> The right-hand side separates completely as a product of a $y$-factor and an $x$-factor. After separating variables, apply partial fractions to **each side** independently (the $y$ side on the left, the $x$ side on the right). Integrating both sides gives two logarithmic expressions; combining these with the initial condition determines $C$ and yields an implicit solution.  
> For (e): substitute $x=6$ into the implicit solution, then solve for $y$ as a quadratic-style equation.

$$\frac{dy}{dx} = \frac{y(y-3)}{x(x+2)}, \qquad y = 6 \text{ when } x = 2$$

**(a)** Show that the equation can be written in the separated form

$$\frac{dy}{y(y-3)} = \frac{dx}{x(x+2)}$$

**(b)** Using partial fractions, show that

$$\int \frac{dy}{y(y-3)} = \frac{1}{3}\ln\left|\frac{y-3}{y}\right| + C$$

**(c)** Using partial fractions, show that

$$\int \frac{dx}{x(x+2)} = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + C$$

**(d)** Hence show that the particular solution satisfies

$$\left(\frac{y-3}{y}\right)^2 = \frac{2x^3}{(x+2)^3}$$

**(e)** Find the value of $y$ when $x = 6$, giving your answer to 3 significant figures.

<details>
<summary>**Solution**</summary>

#### (a) Separation of variables

$$\frac{dy}{dx} = \frac{y(y-3)}{x(x+2)}$$

Collect each variable to its own side:

$$\frac{1}{y(y-3)}\,dy = \frac{1}{x(x+2)}\,dx \tag{M1}$$

Integrate both sides. $\checkmark$

---

#### (b) Partial fractions on the left

$$\frac{1}{y(y-3)} = \frac{A}{y} + \frac{B}{y-3}$$

$$1 = A(y-3) + By$$

- $y = 0$: $1 = -3A \implies A = -\dfrac{1}{3}$
- $y = 3$: $1 = 3B \implies B = \dfrac{1}{3}$

$$\frac{1}{y(y-3)} = \frac{-1/3}{y} + \frac{1/3}{y-3} \tag{M1}$$

$$\int \frac{dy}{y(y-3)} = -\frac{1}{3}\ln|y| + \frac{1}{3}\ln|y-3| = \frac{1}{3}\ln\left|\frac{y-3}{y}\right| \quad \checkmark \tag{A1}$$

---

#### (c) Partial fractions on the right

$$\frac{1}{x(x+2)} = \frac{A}{x} + \frac{B}{x+2}$$

$$1 = A(x+2) + Bx$$

- $x = 0$: $1 = 2A \implies A = \dfrac{1}{2}$
- $x = -2$: $1 = -2B \implies B = -\dfrac{1}{2}$

$$\frac{1}{x(x+2)} = \frac{1/2}{x} - \frac{1/2}{x+2} \tag{M1}$$

$$\int \frac{dx}{x(x+2)} = \frac{1}{2}\ln|x| - \frac{1}{2}\ln|x+2| = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| \quad \checkmark \tag{A1}$$

---

#### (d) Apply initial condition → implicit solution

From (b) and (c):

$$\frac{1}{3}\ln\left|\frac{y-3}{y}\right| = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + C \tag{M1}$$

**Initial condition** $x = 2,\ y = 6$:

$$\frac{1}{3}\ln\left|\frac{3}{6}\right| = \frac{1}{2}\ln\left|\frac{2}{4}\right| + C$$

$$\frac{1}{3}\ln\frac{1}{2} = \frac{1}{2}\ln\frac{1}{2} + C$$

$$-\frac{\ln 2}{3} = -\frac{\ln 2}{2} + C \implies C = \frac{\ln 2}{2} - \frac{\ln 2}{3} = \frac{\ln 2}{6} \tag{A1}$$

Therefore:

$$\frac{1}{3}\ln\left|\frac{y-3}{y}\right| = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + \frac{\ln 2}{6}$$

Multiply both sides by $6$:

$$2\ln\left|\frac{y-3}{y}\right| = 3\ln\left|\frac{x}{x+2}\right| + \ln 2 \tag{M1}$$

Simplify using log laws:

$$\ln\left(\frac{y-3}{y}\right)^2 = \ln\left(\frac{x}{x+2}\right)^3 + \ln 2 = \ln\frac{2x^3}{(x+2)^3}$$

$$\boxed{\left(\frac{y-3}{y}\right)^2 = \frac{2x^3}{(x+2)^3}} \quad \checkmark \tag{A1}$$

---

#### (e) Value of $y$ when $x = 6$

$$\left(\frac{y-3}{y}\right)^2 = \frac{2 \times 6^3}{(6+2)^3} = \frac{2 \times 216}{512} = \frac{432}{512} = \frac{27}{32} \tag{M1}$$

At $x = 2$, $y = 6 > 3$, so $\dfrac{y-3}{y} > 0$. Therefore:

$$\frac{y-3}{y} = \sqrt{\frac{27}{32}} = \frac{3\sqrt{3}}{4\sqrt{2}} = \frac{3\sqrt{6}}{8} \tag{M1}$$

$$1 - \frac{3}{y} = \frac{3\sqrt{6}}{8} \implies \frac{3}{y} = 1 - \frac{3\sqrt{6}}{8} = \frac{8 - 3\sqrt{6}}{8}$$

$$y = \frac{24}{8 - 3\sqrt{6}} \approx \frac{24}{8 - 7.348} \approx \frac{24}{0.652}$$

$$\boxed{y \approx 36.8} \tag{A1}$$

> **Verification:** $\left(\frac{36.8-3}{36.8}\right)^2 = \left(\frac{33.8}{36.8}\right)^2 \approx 0.919^2 \approx 0.844 \approx \frac{27}{32}$ ✓
</detail>

---

## Q2. Separable DE — Substitution $u = \ln y$ + partial fractions

> **[Problem notes]**  
> The presence of $\ln y$ on the right means direct separation gives $\int \frac{dy}{y \ln y}$ — a signal that the substitution $u = \ln y$ is needed to simplify it. After the substitution the equation becomes a separable DE in $u$, and $\frac{1}{x(x+1)}$ on the right is handled with partial fractions. The final explicit solution has the form $y = e^{u(x)}$.  
> Finding the asymptotic value as $x \to \infty$ is also an important part of this question.

$$x(x+1)\,\frac{dy}{dx} = y\ln y, \qquad y = e \text{ when } x = 1$$

**(a)** Let $u = \ln y$. Show that this substitution transforms the equation into

$$x(x+1)\,\frac{du}{dx} = u$$

**(b)** Hence separate variables and, using partial fractions, integrate both sides.

**(c)** Apply the initial condition to find $u$ in terms of $x$.

**(d)** Hence find $y$ in terms of $x$, and state the value that $y$ approaches as $x \to \infty$.

<details>
<summary>Solution</summary>
#### (a) Substitution $u = \ln y$

Since $u = \ln y \implies y = e^u$, by the chain rule:

$$\frac{dy}{dx} = e^u \cdot \frac{du}{dx} = y\,\frac{du}{dx} \tag{M1}$$

Substitute into the original equation:

$$x(x+1) \cdot y\,\frac{du}{dx} = y \cdot \ln y = y \cdot u$$

Divide both sides by $y > 0$:

$$x(x+1)\,\frac{du}{dx} = u \quad \checkmark \tag{A1}$$

---

#### (b) Separate variables + partial fractions

$$\frac{du}{u} = \frac{dx}{x(x+1)} \tag{M1}$$

Partial fractions on the right:

$$\frac{1}{x(x+1)} = \frac{1}{x} - \frac{1}{x+1}$$

Integrate both sides:

$$\int \frac{du}{u} = \int \left(\frac{1}{x} - \frac{1}{x+1}\right)dx \tag{M1}$$

$$\ln|u| = \ln|x| - \ln|x+1| + C = \ln\frac{x}{x+1} + C \tag{A1}$$

$$|u| = e^C \cdot \frac{x}{x+1} \implies u = A\,\frac{x}{x+1} \quad (A \in \mathbb{R}) \tag{A1}$$

---

#### (c) Apply initial condition

Since $x = 1,\ y = e$, we have $u = \ln e = 1$:

$$1 = A \cdot \frac{1}{1+1} = \frac{A}{2} \implies A = 2 \tag{M1 A1}$$

$$\boxed{u = \frac{2x}{x+1}}$$

---

#### (d) Express $y$ in terms of $x$

Since $u = \ln y$:

$$\ln y = \frac{2x}{x+1}$$

$$\boxed{y = e^{2x/(x+1)}} \tag{A1}$$

**As $x \to \infty$:**

$$\frac{2x}{x+1} = \frac{2}{1 + 1/x} \to 2$$

$$y \to e^2 \approx 7.39 \tag{A1}$$

> **Interpretation:** $y$ starts at $e$ and approaches $e^2$ asymptotically. Verification of initial condition: at $x=1$, $y = e^{2/2} = e$ ✓
</detail>

## Q3. Connected Rates of Change — Draining a Cylindrical Tank

> **[Problem notes]**  
> The given quantity is $\frac{dV}{dt}$, but the required quantity is $\frac{dh}{dt}$. For a cylinder, $V = \pi r^2 h$ connects $V$ and $h$; differentiating both sides with respect to $t$ links $\frac{dV}{dt}$ and $\frac{dh}{dt}$ — this is the key idea behind connected rates. The resulting $\frac{dh}{dt} = -\frac{2}{9\pi}\sqrt{h}$ is then solved as a separable DE to obtain $h(t)$.  
> It is worth understanding the physical meaning: as $h$ decreases, the outflow rate slows down — the tank drains more slowly as it empties.

A large cylindrical water tank has a circular cross-section of radius 3 metres. Water drains through a small hole at the base. By Torricelli's Law, the volume flow rate satisfies

$$\frac{dV}{dt} = -2\sqrt{h}$$

where $V$ m$^3$ is the volume of water and $h$ metres is the depth. Initially, the depth is 9 metres.

**(a)** Show that $\dfrac{dh}{dt} = -\dfrac{2}{9\pi}\sqrt{h}$.

**(b)** By solving the differential equation, show that

$$h = \left(3 - \frac{t}{9\pi}\right)^2$$

**(c)** Find the time at which the tank empties completely. Give your answer in exact form and to the nearest minute.

**(d)** Find the depth of water after 30 minutes, to 3 significant figures.

**(e)** Find the rate at which the depth is decreasing at the instant when $h = 1$ m. Give units.

<details>
<summary>Solution</summary>

#### (a) Connected rates

For a cylinder: $V = \pi r^2 h = \pi(3)^2 h = 9\pi h$

$$\frac{dV}{dt} = 9\pi\,\frac{dh}{dt} \tag{M1}$$

$$9\pi\,\frac{dh}{dt} = -2\sqrt{h} \implies \frac{dh}{dt} = -\frac{2}{9\pi}\sqrt{h} \quad \checkmark \tag{A1}$$

---

#### (b) Solve the DE

$$h^{-1/2}\,dh = -\frac{2}{9\pi}\,dt \tag{M1}$$

$$\int h^{-1/2}\,dh = \int -\frac{2}{9\pi}\,dt$$

$$2\sqrt{h} = -\frac{2}{9\pi}t + C \tag{A1}$$

**Initial condition** $t = 0,\ h = 9$:

$$2\sqrt{9} = C \implies C = 6 \tag{M1}$$

$$2\sqrt{h} = 6 - \frac{2t}{9\pi} \implies \sqrt{h} = 3 - \frac{t}{9\pi}$$

$$\boxed{h = \left(3 - \frac{t}{9\pi}\right)^2} \quad \checkmark \tag{A1}$$

---

#### (c) Time for the tank to empty

Condition for $h = 0$:

$$3 - \frac{t}{9\pi} = 0 \implies t = 27\pi \tag{M1}$$

$$\boxed{t = 27\pi \approx 85 \text{ minutes}} \tag{A1}$$

---

#### (d) Depth $h$ when $t = 30$ minutes

$$\sqrt{h} = 3 - \frac{30}{9\pi} = 3 - \frac{10}{3\pi} \tag{M1}$$

$$\sqrt{h} \approx 3 - 1.0610 = 1.9390$$

$$h \approx 1.9390^2 \approx \boxed{3.76 \text{ m}} \tag{A1}$$

---

#### (e) Rate of decrease when $h = 1$ m

$$\frac{dh}{dt} = -\frac{2}{9\pi}\sqrt{1} = -\frac{2}{9\pi} \approx -0.0707 \text{ m/min} \tag{A1}$$

> The depth is decreasing at approximately 0.0707 m (7.07 cm) per minute.

> **Key point:** As $h$ decreases, $\sqrt{h}$ decreases, so the drainage rate slows down — the tank empties more slowly as it approaches empty.
</detail>

## Q4. Applied DE — Drug Infusion Model (multi-step problem)

> **[Problem notes]**  
> The model has drug entering at a constant rate and being eliminated proportionally, giving the form $\frac{dQ}{dt} = R - kQ$. Finding the long-term equilibrium $Q_\infty = R/k$ first lets you predict the shape of the solution. Crucially, in (e), the moment the infusion **stops**, a new initial condition $Q_0 = 400$ is set and an entirely different DE ($\frac{dQ}{d\tau} = -kQ$) must be solved from scratch — continuing the original equation past this point is wrong.  
> Understanding the symmetric structure where answers to (d) and (e)(ii) match helps consolidate the underlying concept.

A drug is administered intravenously at a constant rate of $60$ mg/hour. The body eliminates the drug at a rate proportional to the current amount $Q$ mg present, with elimination constant $k = 0.15$ hr$^{-1}$.

**(a)** Write down the differential equation for $\dfrac{dQ}{dt}$.

**(b)** Find the equilibrium (long-term) level $Q_\infty$ and determine whether it lies within the safe therapeutic range of $[200,\ 500]$ mg.

**(c)** Solve the DE with the initial condition $Q = 0$ at $t = 0$, giving $Q$ in terms of $t$.

**(d)** Find the time at which the drug first reaches the minimum therapeutic level of $200$ mg. Give your answer to 3 significant figures.

**(e)** The infusion is stopped at the moment when $Q = 400$ mg. After this point the drug decays according to $\dfrac{dQ}{dt} = -0.15Q$.

   **(i)** Write down the solution for $Q$ after the infusion stops (let $\tau = 0$ be the moment the infusion stops).

   **(ii)** Find the time after stopping the infusion for $Q$ to fall below 200 mg. Give your answer to 3 significant figures.

**(f)** Sketch a graph of $Q$ against $t$ for the entire process described in parts (c)–(e), labelling key values.

<details>
<summary>Solution</summary>

#### (a) Setting up the DE

$$\boxed{\frac{dQ}{dt} = 60 - 0.15Q} \tag{B1}$$

*(inflow 60 mg/hr, outflow $0.15Q$ mg/hr)*

---

#### (b) Equilibrium level

Setting $\dfrac{dQ}{dt} = 0$:

$$60 - 0.15Q_\infty = 0 \implies Q_\infty = \frac{60}{0.15} = 400 \text{ mg} \tag{B1}$$

Since $400 \in [200,\ 500]$, this is **within the safe range** — therapeutic concentration is maintained without reaching toxic levels. \tag{A1}

---

#### (c) Solve the DE

$$\int \frac{dQ}{60 - 0.15Q} = \int dt \tag{M1}$$

Substitution: $u = 60 - 0.15Q,\; du = -0.15\,dQ$

$$-\frac{1}{0.15}\ln|60 - 0.15Q| = t + C \tag{A1}$$

$$\ln|60 - 0.15Q| = -0.15t + C'$$

$$60 - 0.15Q = Ae^{-0.15t}$$

**Initial condition** $t = 0,\ Q = 0$:

$$60 = A \tag{M1}$$

$$60 - 0.15Q = 60e^{-0.15t}$$

$$0.15Q = 60(1 - e^{-0.15t})$$

$$\boxed{Q = 400\left(1 - e^{-0.15t}\right)} \tag{A1}$$

> **Structure check:** as $t\to\infty$, $Q \to 400$ ✓; at $t=0$, $Q=0$ ✓

---

#### (d) Time for $Q$ to reach 200 mg

$$200 = 400(1 - e^{-0.15t}) \tag{M1}$$

$$1 - e^{-0.15t} = 0.5 \implies e^{-0.15t} = 0.5$$

$$-0.15t = \ln 0.5 = -\ln 2$$

$$t = \frac{\ln 2}{0.15} \tag{A1}$$

$$\boxed{t \approx 4.62 \text{ hours}} \tag{A1}$$

---

#### (e)(i) Decay after infusion stops

At $\tau = 0$, $Q_0 = 400$ mg; from this point the drug decays purely:

$$\frac{dQ}{d\tau} = -0.15Q \implies Q = 400\,e^{-0.15\tau} \tag{B1}$$

---

#### (e)(ii) Time for $Q$ to fall below 200 mg

$$400e^{-0.15\tau} = 200 \implies e^{-0.15\tau} = 0.5 \tag{M1}$$

$$\tau = \frac{\ln 2}{0.15} \tag{A1}$$

$$\boxed{\tau \approx 4.62 \text{ hours}} \tag{A1}$$

> **Symmetric result:** The time to reach 200 mg after starting the infusion equals the time to fall from 400 mg to 200 mg after stopping it. This is not a coincidence — both cases reduce to the same equation $e^{-0.15t} = 0.5$.

---

#### (f) Graph sketch guide

```
Q (mg)
500 |
    |
400 |·············································· Q∞ = 400 (asymptote)
    |                              ╲ (decay after infusion stops)
    |                         ╱────╲
300 |                    ╱───       ╲
    |               ╱──              ╲
200 |──────────╱                      ╲──────────── 200 (min. therapeutic)
    |       ↑                          ↑
    |    t≈4.62                     τ≈4.62
  0 +──────────────────────────────────────────── t
    0                    ↑ infusion stops (Q=400)
```

**Labels:**
- $Q_\infty = 400$ (horizontal asymptote)
- Rising phase: $Q = 400(1 - e^{-0.15t})$ — concave, curving upward
- Falling phase: $Q = 400e^{-0.15\tau}$ — exponential decay, convex
</detail>

## Summary: Key techniques for Q1–Q4

| Question | Key technique | Common mistake |
|---|---|---|
| Q1 | Partial fractions on both sides → combine logs, compare exponents | Substituting the initial condition before multiplying through by 6 |
| Q2 | $u = \ln y$ substitution linearises the equation | Forgetting the chain rule when converting $\frac{dy}{dx}$ to $\frac{du}{dx}$ |
| Q3 | Connected rates: link $V$ and $h$ first | Dropping the squared radius and writing $\frac{dV}{dt} = \frac{dh}{dt}$ |
| Q4 | $R - kQ$ form integration → initial condition applied twice (during / after infusion) | Continuing the original equation past the stopping point instead of resetting $Q_0$ |
