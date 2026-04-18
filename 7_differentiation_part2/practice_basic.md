# Differentiation Part 2 — 기본문제 Mark Scheme

---

## Q03. Find the points of zero gradient on the curve with parametric equations

$$x = \frac{t}{1-t}, \qquad y = \frac{t^2}{1-t}$$

**What does "zero gradient" mean?**
Zero gradient means $\dfrac{dy}{dx} = 0$. For parametric equations, $\dfrac{dy}{dx} = \dfrac{dy/dt}{dx/dt}$, so this happens when $\dfrac{dy}{dt} = 0$ (provided $\dfrac{dx}{dt} \neq 0$).

**Solution:**

**Step 1 — Differentiate $y$ and $x$ with respect to $t$.**

Write $y = t^2(1-t)^{-1}$ and apply the product rule:

$$\frac{dy}{dt} = 2t(1-t)^{-1} + t^2 \cdot (1-t)^{-2} = \frac{2t(1-t) + t^2}{(1-t)^2} = \frac{2t - t^2}{(1-t)^2} = \frac{t(2-t)}{(1-t)^2} \tag{M1}$$

Write $x = t(1-t)^{-1}$ and apply the product rule:

$$\frac{dx}{dt} = (1-t)^{-1} + t(1-t)^{-2} = \frac{(1-t)+t}{(1-t)^2} = \frac{1}{(1-t)^2} \tag{M1}$$

**Step 2 — Set $\dfrac{dy}{dt} = 0$ (check $\dfrac{dx}{dt} \neq 0$).**

Note $\dfrac{dx}{dt} = \dfrac{1}{(1-t)^2} \neq 0$ for all $t \neq 1$, so:

$$\frac{dy}{dt} = 0 \implies t(2-t) = 0 \implies t = 0 \quad \text{or} \quad t = 2 \tag{A1}$$

**Step 3 — Find coordinates.**

At $t = 0$:

$$x = \frac{0}{1} = 0, \qquad y = \frac{0}{1} = 0 \tag{A1}$$

At $t = 2$:

$$x = \frac{2}{1-2} = -2, \qquad y = \frac{4}{1-2} = -4 \tag{A1}$$

$$\boxed{(0,\ 0) \quad \text{and} \quad (-2,\ -4)}$$

---

## Q04. The curve is defined by $e^{2y} = x^2 + y$

Find the coordinates of point $P$, where the curve has **infinite gradient**, correct to 2 d.p.

**What does "infinite gradient" mean?**
Infinite gradient means $\dfrac{dy}{dx} \to \infty$, i.e. the tangent is **vertical**. This occurs when the **denominator** of $\dfrac{dy}{dx}$ equals zero — equivalently, when $\dfrac{dx}{dy} = 0$.

**Solution:**

**Step 1 — Differentiate implicitly with respect to $x$.**

$$\frac{d}{dx}(e^{2y}) = \frac{d}{dx}(x^2 + y)$$

$$2e^{2y}\frac{dy}{dx} = 2x + \frac{dy}{dx} \tag{M1}$$

$$\left(2e^{2y} - 1\right)\frac{dy}{dx} = 2x$$

$$\frac{dy}{dx} = \frac{2x}{2e^{2y} - 1} \tag{A1}$$

**Step 2 — Set denominator = 0 for infinite gradient.**

$$2e^{2y} - 1 = 0 \implies e^{2y} = \frac{1}{2} \tag{M1}$$

$$2y = \ln\frac{1}{2} = -\ln 2 \implies y = -\frac{\ln 2}{2} \approx -0.35 \tag{A1}$$

**Step 3 — Find $x$ using the original equation.**

Substitute $e^{2y} = \dfrac{1}{2}$ and $y = -\dfrac{\ln 2}{2}$ into $e^{2y} = x^2 + y$:

$$\frac{1}{2} = x^2 - \frac{\ln 2}{2} \tag{M1}$$

$$x^2 = \frac{1}{2} + \frac{\ln 2}{2} = \frac{1 + \ln 2}{2} \approx \frac{1 + 0.6931}{2} \approx 0.8466$$

$$x = \pm\sqrt{\frac{1+\ln 2}{2}} \approx \pm 0.92 \tag{A1}$$

From the graph, $P$ is on the positive $x$-axis side:

$$\boxed{P \approx (0.92,\ -0.35)}$$

> **Note:** The negative root $x \approx -0.92$ gives a second vertical-tangent point on the left branch, but the graph labels only the right-hand point as $P$.

---

## Q05. Find $\dfrac{d^2y}{dx^2}$ for the implicit equation $y^3 + 3x^2y - 4x = 0$

**Strategy:** Differentiate implicitly once to get $\dfrac{dy}{dx}$, then differentiate the resulting equation again to get $\dfrac{d^2y}{dx^2}$ — it is easier to differentiate the **intermediate equation** than to differentiate the $\dfrac{dy}{dx}$ formula using the quotient rule.

**Solution:**

**Step 1 — Differentiate once with respect to $x$.**

$$3y^2\frac{dy}{dx} + 6xy + 3x^2\frac{dy}{dx} - 4 = 0 \tag{M1}$$

$$\left(3y^2 + 3x^2\right)\frac{dy}{dx} = 4 - 6xy \tag{A1}$$

$$\frac{dy}{dx} = \frac{4 - 6xy}{3(x^2 + y^2)} \tag{A1}$$

**Step 2 — Differentiate the intermediate equation $\left(3y^2 + 3x^2\right)\dfrac{dy}{dx} = 4 - 6xy$ again.**

Left side — product rule on $\left(3y^2 + 3x^2\right)\dfrac{dy}{dx}$:

$$\frac{d}{dx}\!\left[(3y^2+3x^2)\frac{dy}{dx}\right] = \left(6y\frac{dy}{dx}+6x\right)\frac{dy}{dx} + \left(3y^2+3x^2\right)\frac{d^2y}{dx^2} \tag{M1}$$

Right side:

$$\frac{d}{dx}(4-6xy) = -6y - 6x\frac{dy}{dx}$$

Equating both sides and solving for $\dfrac{d^2y}{dx^2}$:

$$\left(3y^2+3x^2\right)\frac{d^2y}{dx^2} = -6y - 6x\frac{dy}{dx} - \left(6y\frac{dy}{dx}+6x\right)\frac{dy}{dx} \tag{M1}$$

$$= -6y - 6x\frac{dy}{dx} - 6y\!\left(\frac{dy}{dx}\right)^{\!2} - 6x\frac{dy}{dx}$$

$$= -6y - 12x\frac{dy}{dx} - 6y\!\left(\frac{dy}{dx}\right)^{\!2}$$

$$\boxed{\frac{d^2y}{dx^2} = \frac{-6\!\left[y + 2x\dfrac{dy}{dx} + y\!\left(\dfrac{dy}{dx}\right)^{\!2}\right]}{3(x^2+y^2)} = \frac{-2\!\left[y + 2x\dfrac{dy}{dx} + y\!\left(\dfrac{dy}{dx}\right)^{\!2}\right]}{x^2+y^2}} \tag{A1}$$

> **How to use this result:** If a specific point $(x_0, y_0)$ is given, first compute $\dfrac{dy}{dx}$ from Step 1, then substitute into the boxed formula to get a numerical value for $\dfrac{d^2y}{dx^2}$.
