# Differentiation Part 2 — Exam Problems Mark Scheme

---

## Q1. A curve has the equation $x^2(2 + y) - y^2 = 0$ &emsp; **(6)**

Find $\dfrac{dy}{dx}$ in terms of $x$ and $y$.

**Solution:**

Differentiate both sides with respect to $x$. Expand $x^2(2+y) = 2x^2 + x^2 y$ first, then apply the product rule to $x^2 y$:

$$\frac{d}{dx}(2x^2) + \frac{d}{dx}(x^2 y) - \frac{d}{dx}(y^2) = 0 \tag{M1}$$

$$4x + \left(2xy + x^2\frac{dy}{dx}\right) - 2y\frac{dy}{dx} = 0 \tag{M1 — product rule, chain rule}$$

Collect $\dfrac{dy}{dx}$ terms:

$$4x + 2xy + (x^2 - 2y)\frac{dy}{dx} = 0 \tag{A1}$$

$$\frac{dy}{dx} = \frac{-(4x + 2xy)}{x^2 - 2y} \tag{M1}$$

$$\boxed{\frac{dy}{dx} = \frac{-2x(2 + y)}{x^2 - 2y}} \tag{A2}$$

> **Note:** The numerator $-2x(2+y)$ reflects exactly the original bracket from the equation — a useful self-check.

---

## Q2. A curve has the equation $4x^2 - 2xy - y^2 + 11 = 0$ &emsp; **(8)**

Find the equation of the normal at $(-1,\ -3)$.

**Solution:**

**Step 1 — Verify the point lies on the curve.**

$$4(1) - 2(-1)(-3) - 9 + 11 = 4 - 6 - 9 + 11 = 0 \checkmark \tag{B1}$$

**Step 2 — Differentiate implicitly.**

$$8x - 2y - 2x\frac{dy}{dx} - 2y\frac{dy}{dx} = 0 \tag{M1 — product rule on $2xy$}$$

$$8x - 2y = (2x + 2y)\frac{dy}{dx} \tag{A1}$$

$$\frac{dy}{dx} = \frac{8x - 2y}{2(x + y)} = \frac{4x - y}{x + y} \tag{A1}$$

**Step 3 — Find gradient of tangent at $(-1,\ -3)$.**

$$\left.\frac{dy}{dx}\right|_{(-1,-3)} = \frac{4(-1) - (-3)}{(-1) + (-3)} = \frac{-4 + 3}{-4} = \frac{-1}{-4} = \frac{1}{4} \tag{M1, A1}$$

**Step 4 — Gradient of normal = $-4$ (negative reciprocal).**

$$y - (-3) = -4\bigl(x - (-1)\bigr) \tag{M1}$$

$$y + 3 = -4x - 4$$

$$\boxed{4x + y + 7 = 0} \tag{A1}$$

---

## Q3. Curve $y = 4^x - 2^{x-1} + 1$

### (a) Prove $\dfrac{d}{dx}(a^x) = a^x \ln a$ &emsp; **(3)**

Write $a^x$ as an exponential with base $e$:

$$a^x = e^{x \ln a} \tag{M1}$$

Differentiate using the chain rule:

$$\frac{d}{dx}\!\left(e^{x\ln a}\right) = e^{x\ln a} \cdot \ln a \tag{M1}$$

$$= a^x \ln a \tag{A1}$$

---

### (b) Show tangent at $y$-axis has equation $3x\ln 2 - 2y + 3 = 0$ &emsp; **(5)**

**Step 1 — Find the point where the curve crosses the $y$-axis** ($x = 0$):

$$y = 4^0 - 2^{-1} + 1 = 1 - \frac{1}{2} + 1 = \frac{3}{2} \tag{B1}$$

Point: $\left(0,\ \dfrac{3}{2}\right)$

**Step 2 — Differentiate $y = 4^x - 2^{x-1} + 1$.**

Rewrite: $4^x = (2^2)^x = 2^{2x}$ and $2^{x-1} = \tfrac{1}{2}\cdot 2^x$, so:

$$\frac{dy}{dx} = 2^{2x}\cdot 2\ln 2 - \tfrac{1}{2}\cdot 2^x \cdot \ln 2 \tag{M1, A1 — using part (a)}$$

**Step 3 — Evaluate at $x = 0$:**

$$\left.\frac{dy}{dx}\right|_{x=0} = 1 \cdot 2\ln 2 - \tfrac{1}{2}\cdot 1 \cdot \ln 2 = 2\ln 2 - \tfrac{1}{2}\ln 2 = \frac{3\ln 2}{2} \tag{A1}$$

**Step 4 — Form the tangent equation:**

$$y - \frac{3}{2} = \frac{3\ln 2}{2}(x - 0) \tag{M1}$$

Multiply through by 2:

$$2y - 3 = 3x\ln 2 \implies \boxed{3x\ln 2 - 2y + 3 = 0} \tag{A1}$$

---

### (c) Find the exact coordinates of the stationary point &emsp; **(4)**

Set $\dfrac{dy}{dx} = 0$. Let $u = 2^x$ (so $u > 0$):

$$2^{2x}\cdot 2\ln 2 - \tfrac{1}{2}\cdot 2^x\cdot\ln 2 = 0 \tag{M1}$$

$$\ln 2\cdot 2^x\!\left(2\cdot 2^x - \tfrac{1}{2}\right) = 0$$

Since $\ln 2 \neq 0$ and $2^x \neq 0$:

$$2\cdot 2^x = \frac{1}{2} \implies 2^x = \frac{1}{4} = 2^{-2} \implies x = -2 \tag{A1}$$

Substitute $x = -2$:

$$y = 4^{-2} - 2^{-3} + 1 = \frac{1}{16} - \frac{1}{8} + 1 = \frac{1 - 2 + 16}{16} = \frac{15}{16} \tag{M1, A1}$$

$$\boxed{\left(-2,\ \frac{15}{16}\right)}$$

---

## Q4. A curve has the equation $2x^2 + xy - y^2 + 18 = 0$ &emsp; **(8)**

Find coordinates where tangent is parallel to the $x$-axis.

**Solution:**

**Step 1 — Differentiate implicitly.**

$$4x + y + x\frac{dy}{dx} - 2y\frac{dy}{dx} = 0 \tag{M1 — product rule on $xy$}$$

$$(x - 2y)\frac{dy}{dx} = -4x - y \tag{A1}$$

$$\frac{dy}{dx} = \frac{4x + y}{2y - x} \tag{A1}$$

**Step 2 — Set $\dfrac{dy}{dx} = 0$: numerator $= 0$.**

$$4x + y = 0 \implies y = -4x \tag{M1, A1}$$

**Step 3 — Substitute $y = -4x$ into the curve equation.**

$$2x^2 + x(-4x) - (-4x)^2 + 18 = 0 \tag{M1}$$

$$2x^2 - 4x^2 - 16x^2 + 18 = 0$$

$$-18x^2 + 18 = 0 \implies x^2 = 1 \implies x = \pm 1 \tag{A1}$$

**Step 4 — Find $y$-coordinates.**

- $x = 1$: $y = -4$
- $x = -1$: $y = 4$

$$\boxed{(1,\ -4) \quad \text{and} \quad (-1,\ 4)} \tag{A1}$$

---

## Q5. Parametric curve: $x = -1 + 4\cos\theta$, $\;y = 2\sqrt{2}\sin\theta$, $\;P = (1,\ \sqrt{6})$

### (a) Find $\theta$ at $P$ &emsp; **(2)**

From $x = 1$:

$$-1 + 4\cos\theta = 1 \implies \cos\theta = \frac{1}{2} \implies \theta = \frac{\pi}{3} \text{ or } \frac{5\pi}{3} \tag{M1}$$

From $y = \sqrt{6}$:

$$2\sqrt{2}\sin\theta = \sqrt{6} \implies \sin\theta = \frac{\sqrt{6}}{2\sqrt{2}} = \frac{\sqrt{3}}{2} \implies \theta = \frac{\pi}{3} \text{ or } \frac{2\pi}{3}$$

Both conditions are satisfied only at:

$$\boxed{\theta = \frac{\pi}{3}} \tag{A1}$$

---

### (b) Show normal at $P$ passes through origin &emsp; **(7)**

**Step 1 — Find $\dfrac{dy}{dx}$.**

$$\frac{dx}{d\theta} = -4\sin\theta, \qquad \frac{dy}{d\theta} = 2\sqrt{2}\cos\theta \tag{M1}$$

$$\frac{dy}{dx} = \frac{2\sqrt{2}\cos\theta}{-4\sin\theta} = -\frac{\sqrt{2}\cos\theta}{2\sin\theta} \tag{M1}$$

**Step 2 — Evaluate at $\theta = \dfrac{\pi}{3}$.**

$$\frac{dy}{dx} = -\frac{\sqrt{2}\cdot\tfrac{1}{2}}{2\cdot\tfrac{\sqrt{3}}{2}} = -\frac{\tfrac{\sqrt{2}}{2}}{\sqrt{3}} = -\frac{\sqrt{2}}{2\sqrt{3}} = -\frac{\sqrt{6}}{6} \tag{A1}$$

**Step 3 — Gradient of normal.**

$$m_{\text{normal}} = \frac{6}{\sqrt{6}} = \sqrt{6} \tag{M1, A1}$$

**Step 4 — Equation of normal at $P(1,\ \sqrt{6})$.**

$$y - \sqrt{6} = \sqrt{6}(x - 1) \tag{M1}$$

$$y = \sqrt{6}\,x \tag{A1}$$

This passes through the origin $(0, 0)$ since $y = \sqrt{6}\cdot 0 = 0$. $\checkmark$

---

### (c) Find Cartesian equation &emsp; **(3)**

From the parametric equations:

$$\cos\theta = \frac{x+1}{4}, \qquad \sin\theta = \frac{y}{2\sqrt{2}} \tag{M1}$$

Apply $\cos^2\theta + \sin^2\theta = 1$:

$$\left(\frac{x+1}{4}\right)^2 + \left(\frac{y}{2\sqrt{2}}\right)^2 = 1 \tag{M1}$$

$$\boxed{\frac{(x+1)^2}{16} + \frac{y^2}{8} = 1} \tag{A1}$$

> This is an ellipse centred at $(-1, 0)$.

---

## Q6. Parametric curve: $x = 3\cos^2 t$, $\;y = \sin 2t$, $\;0 \leq t < \pi$

### (a) Show $\dfrac{dy}{dx} = -\dfrac{2}{3}\cot 2t$ &emsp; **(4)**

$$\frac{dx}{dt} = 3\cdot 2\cos t\cdot(-\sin t) = -6\cos t\sin t = -3\sin 2t \tag{M1, A1}$$

$$\frac{dy}{dt} = 2\cos 2t \tag{A1}$$

$$\frac{dy}{dx} = \frac{2\cos 2t}{-3\sin 2t} = -\frac{2}{3}\cdot\frac{\cos 2t}{\sin 2t} = \boxed{-\frac{2}{3}\cot 2t} \tag{A1}$$

---

### (b) Find coordinates where tangent is parallel to $x$-axis &emsp; **(3)**

$$\frac{dy}{dx} = 0 \implies \cos 2t = 0 \implies 2t = \frac{\pi}{2},\;\frac{3\pi}{2} \implies t = \frac{\pi}{4},\;\frac{3\pi}{4} \tag{M1}$$

(Check $\sin 2t \neq 0$ at both values — $\sin(\pi/2) = 1 \neq 0$ and $\sin(3\pi/2) = -1 \neq 0$. $\checkmark$)

At $t = \dfrac{\pi}{4}$:

$$x = 3\cos^2\!\tfrac{\pi}{4} = 3\cdot\tfrac{1}{2} = \frac{3}{2}, \qquad y = \sin\tfrac{\pi}{2} = 1 \tag{A1}$$

At $t = \dfrac{3\pi}{4}$:

$$x = 3\cos^2\!\tfrac{3\pi}{4} = 3\cdot\tfrac{1}{2} = \frac{3}{2}, \qquad y = \sin\tfrac{3\pi}{2} = -1 \tag{A1}$$

$$\boxed{\left(\frac{3}{2},\ 1\right) \quad \text{and} \quad \left(\frac{3}{2},\ -1\right)}$$

---

### (c) Show tangent at $t = \dfrac{\pi}{6}$ has equation $2x + 3\sqrt{3}\,y = 9$ &emsp; **(3)**

**Point at $t = \dfrac{\pi}{6}$:**

$$x = 3\cos^2\!\tfrac{\pi}{6} = 3\cdot\tfrac{3}{4} = \frac{9}{4}, \qquad y = \sin\tfrac{\pi}{3} = \frac{\sqrt{3}}{2} \tag{B1}$$

**Gradient:**

$$\frac{dy}{dx} = -\frac{2}{3}\cot\tfrac{\pi}{3} = -\frac{2}{3}\cdot\frac{\cos(\pi/3)}{\sin(\pi/3)} = -\frac{2}{3}\cdot\frac{1/2}{\sqrt{3}/2} = -\frac{2}{3\sqrt{3}} = -\frac{2\sqrt{3}}{9} \tag{M1}$$

**Tangent equation:**

$$y - \frac{\sqrt{3}}{2} = -\frac{2\sqrt{3}}{9}\!\left(x - \frac{9}{4}\right)$$

Multiply through by 18:

$$18y - 9\sqrt{3} = -4\sqrt{3}\!\left(x - \frac{9}{4}\right) = -4\sqrt{3}\,x + 9\sqrt{3}$$

$$4\sqrt{3}\,x + 18y = 18\sqrt{3}$$

Divide by $2\sqrt{3}$:

$$2x + \frac{18}{2\sqrt{3}}\,y = 9 \implies 2x + 3\sqrt{3}\,y = 9 \tag{A1} \checkmark$$

---

### (d) Find Cartesian equation $y^2 = f(x)$ &emsp; **(4)**

From $x = 3\cos^2 t$:

$$\cos^2 t = \frac{x}{3} \tag{M1}$$

From $\cos^2 t + \sin^2 t = 1$:

$$\sin^2 t = 1 - \frac{x}{3} = \frac{3-x}{3} \tag{A1}$$

Now use $y = \sin 2t = 2\sin t\cos t$, so:

$$y^2 = 4\sin^2 t\cos^2 t = 4\cdot\frac{3-x}{3}\cdot\frac{x}{3} \tag{M1}$$

$$\boxed{y^2 = \frac{4x(3-x)}{9}} \tag{A1}$$
