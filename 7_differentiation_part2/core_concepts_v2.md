# Differentiation Part 2 — Core Concepts

---

## 1. Types of Equations (for both differentiation and integration)

<table style="border-collapse: collapse; width: 100%; font-size: 0.95em;">
<thead>
<tr style="background: #f0f0f0;">
  <th style="border: 1px solid #ccc; padding: 8px 12px;" colspan="2">Equation Types</th>
  <th style="border: 1px solid #ccc; padding: 8px 12px;">Differentiation</th>
  <th style="border: 1px solid #ccc; padding: 8px 12px;">Integration</th>
</tr>
</thead>
<tbody>
<tr>
  <td style="border: 1px solid #ccc; padding: 8px 12px; font-weight: bold; vertical-align: middle;" rowspan="2">Cartesian</td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    <strong>Explicit</strong><br>$y = f(x)$
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    1) Product rule<br>
    2) Chain rule<br>
    3) Quotient rule
    <div style="text-align: right; color: #555; font-size: 0.9em;">(C3)</div>
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    1) Substitution<br>
    2) Integration by parts<br>
    3) Using trig. identities<br>
    4) Partial fraction<br>
    5) Trapezium rule <em>(approx.)</em>
  </td>
</tr>
<tr>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    <strong>Implicit</strong><br>$f(x, y) = 0$
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    $$\frac{d}{dx}(y^n) = ny^{n-1}\frac{dy}{dx}$$
    $$\frac{d}{dx}(xy) = y + x\frac{dy}{dx}$$
    <div style="color: #777; font-size: 0.85em;">(chain rule)</div>
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    1) <strong>Separable:</strong><br>
    $\quad f(y)\,dy = g(x)\,dx$<br><br>
    2) <strong>Non-separable</strong> → FP
  </td>
</tr>
<tr>
  <td style="border: 1px solid #ccc; padding: 8px 12px; font-weight: bold; vertical-align: middle;" colspan="2">
    Parametric<br>
    <span style="font-weight: normal;">$\begin{cases} y = f(t) \\ x = g(t) \end{cases}$</span>
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    $$\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$$
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    $$\int y\,dx = \int y\,\frac{dx}{dt}\,dt$$
    <div style="color: #777; font-size: 0.85em;">(chain rule)</div>
  </td>
</tr>
</tbody>
</table>

---

<details>
<summary>**Explicit — Integration techniques (brief notes on 4 and 5)**</summary>

**4) Partial fraction** — covered in detail in the next Integration unit

A technique for splitting a difficult rational expression into a sum of simpler fractions.

$$\frac{1}{x(x+1)} = \frac{1}{x} - \frac{1}{x+1} \implies \int \frac{1}{x(x+1)}\,dx = \ln|x| - \ln|x+1| + C$$

---

**5) Trapezium rule** — not covered in this curriculum

A numerical integration method that approximates the area under a curve using trapezoids. Used when analytical integration is difficult.

$$\int_a^b f(x)\,dx \approx \frac{h}{2}\bigl[y_0 + 2(y_1 + \cdots + y_{n-1}) + y_n\bigr], \qquad h = \frac{b-a}{n}$$

</details>

---

### 1.1 Cartesian — Implicit $f(x, y) = 0$

::: {style="font-size: 0.85em; color: #666;"}
**Explicit** $y = f(x)$: $y$ is isolated on its own, so its value can be read directly (e.g. $y = x^2 + 3x$)  
**Implicit** $f(x,y) = 0$: $x$ and $y$ are mixed together inside the equation — the form itself is implicit regardless of whether rearrangement is possible

| Equation | If rearranged? | Method used in practice |
|---|---|---|
| $x^2 + y = 2$ | $y = 2-x^2$ — easy | Rearrange to explicit form and differentiate |
| $x^2 + y^3 = 2$ | $y = \sqrt[3]{2-x^2}$ — possible but complicated | Implicit differentiation is more convenient |
| $x^2 + y^2 = 1$ | $y = \pm\sqrt{1-x^2}$ — not a single function due to $\pm$ | Implicit differentiation only |

In short, implicit differentiation is useful **when rearrangement is impossible, or when rearranging would be too complicated**.
:::

**Key rules:**

$$\frac{d}{dx}(y^n) = ny^{n-1}\frac{dy}{dx}$$

<table style="border-collapse: collapse; width: 100%; font-size: 0.93em; margin: 0.5em 0 1.2em 0;">
<tr>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>Why does this work? — Chain rule on $y$</strong><br><br>
    In implicit differentiation, $y$ is a <strong>function of $x$</strong>, i.e. $y(x)$.<br>
    So $y^n = [y(x)]^n$ — a <strong>composite function</strong>, so the chain rule applies:<br><br>
    $$\frac{d}{dx}(y^n) = \underbrace{ny^{n-1}}_{\text{outer derivative}} \times \underbrace{\frac{dy}{dx}}_{\text{inner derivative}}$$
  </td>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>Verification</strong><br><br>
    If $y = x^2$:<br><br>
    Direct computation: $\dfrac{d}{dx}(y^3) = \dfrac{d}{dx}(x^6) = 6x^5$<br><br>
    Using the formula: $3y^2 \cdot \dfrac{dy}{dx} = 3x^4 \cdot 2x = 6x^5$ ✓<br><br>
    <span style="color: #555; font-size: 0.9em;">Every time a term in $y$ is differentiated with respect to $x$, a $\dfrac{dy}{dx}$ factor is appended.</span>
  </td>
</tr>
</table>

$$\frac{d}{dx}(xy) = y + x\frac{dy}{dx} \qquad \text{(product rule)}$$

<table style="border-collapse: collapse; width: 100%; font-size: 0.93em; margin: 0.5em 0 1.2em 0;">
<tr>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>Why does this work? — Product rule on $x \cdot y$</strong><br><br>
    Let $u = x,\quad v = y$:<br><br>
    $$\frac{d}{dx}(uv) = u'v + uv'$$
    $$= 1 \cdot y \;+\; x \cdot \frac{dy}{dx} \;=\; y + x\frac{dy}{dx}$$
  </td>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>Why is $v' = \dfrac{dy}{dx}$?</strong><br><br>
    Since $v = y$ is also a function of $x$, differentiating $v$ with respect to $x$ gives $\dfrac{dy}{dx}$.<br><br>
    <span style="color: #555; font-size: 0.9em;">Same reason as Rule 1 above — every time a $y$ term is differentiated with respect to $x$, a $\dfrac{dy}{dx}$ factor is appended.</span>
  </td>
</tr>
</table>

**Integration — Separable equations:**

> **Note:** Differential equations yield a **general solution** (with constant $C$); a given condition pins down the **particular solution**.

<details>
<summary>**Separable vs Non-separable — How to tell them apart**</summary>

If $\dfrac{dy}{dx}$ can be written as $(\text{expression in } x \text{ only}) \times (\text{expression in } y \text{ only})$ → **Separable**

| Equation | Separation attempt | Verdict |
|--------|-----------|------|
| $\dfrac{dy}{dx} = xy$ | $\dfrac{1}{y}\,dy = x\,dx$ | **Separable** ✓ |
| $\dfrac{dy}{dx} = x^2(1+y^2)$ | $\dfrac{1}{1+y^2}\,dy = x^2\,dx$ | **Separable** ✓ |
| $\dfrac{dy}{dx} = x + y$ | Cannot separate ($y$ is added to $x$) | **Non-separable** ✗ |
| $\dfrac{dy}{dx} = \dfrac{x+y}{x}$ | Takes the form $1 + \dfrac{y}{x}$ — cannot separate | **Non-separable** ✗ |

**Quick test:** if the right-hand side is a **product** of $x$ and $y$ → separable; if $x$ and $y$ are mixed by **addition/subtraction** or as $\tfrac{y}{x}$ → non-separable.

**Solution flow:**

$$\frac{dy}{dx} = xy \;\longrightarrow\; \frac{1}{y}\,dy = x\,dx \;\longrightarrow\; \ln|y| = \frac{x^2}{2} + C$$

</details>

**Ex — Differentiate implicitly (find $\dfrac{dy}{dx}$):**

i. $x^2 + y^3 = 2$

ii. $4x^2 - 2xy + y^3 = 1$

iii. $\sqrt{x + y} = x^2 y$

iv. $\sin(x + y) = \cos y$

<details>
<summary>**Mark Scheme**</summary>

**i.** $x^2 + y^3 = 2$

| | |
|---|---|
| Differentiate $x^2$ to get $2x$; differentiate $y^3$ using chain rule to get $3y^2\dfrac{dy}{dx}$ | M1 |
| $2x + 3y^2\dfrac{dy}{dx} = 0$ | A1 |
| $\dfrac{dy}{dx} = -\dfrac{2x}{3y^2}$ | A1 |

---

**ii.** $4x^2 - 2xy + y^3 = 1$

| | |
|---|---|
| Differentiate $4x^2$ to get $8x$ | B1 |
| Differentiate $2xy$ using product rule: $2y + 2x\dfrac{dy}{dx}$ | M1 A1 |
| Differentiate $y^3$ using chain rule: $3y^2\dfrac{dy}{dx}$ | B1 |
| $8x - 2y - 2x\dfrac{dy}{dx} + 3y^2\dfrac{dy}{dx} = 0$ | A1 |
| Collect $\dfrac{dy}{dx}$ terms and factorise: $\dfrac{dy}{dx}(3y^2 - 2x) = 2y - 8x$ | dM1 |
| $\dfrac{dy}{dx} = \dfrac{2y - 8x}{3y^2 - 2x}$ | A1 |

---

**iii.** $\sqrt{x + y} = x^2 y$

| | |
|---|---|
| Differentiate LHS $(x+y)^{1/2}$ using chain rule: $\dfrac{1}{2}(x+y)^{-1/2}\!\left(1+\dfrac{dy}{dx}\right)$ | M1 A1 |
| Differentiate RHS $x^2 y$ using product rule: $2xy + x^2\dfrac{dy}{dx}$ | M1 A1 |
| Multiply through by $2\sqrt{x+y}$ to clear fraction | M1 |
| $1 + \dfrac{dy}{dx} = 4xy\sqrt{x+y} + 2x^2\sqrt{x+y}\,\dfrac{dy}{dx}$ | A1 |
| Collect and factorise: $\dfrac{dy}{dx} = \dfrac{4xy\sqrt{x+y}-1}{1-2x^2\sqrt{x+y}}$ | A1 |

---

**iv.** $\sin(x + y) = \cos y$

| | |
|---|---|
| Differentiate LHS using chain rule: $\cos(x+y)\!\left(1+\dfrac{dy}{dx}\right)$ | M1 A1 |
| Differentiate RHS using chain rule: $-\sin y\,\dfrac{dy}{dx}$ | B1 |
| Expand and collect $\dfrac{dy}{dx}$ terms | dM1 |
| $\cos(x+y) = -\dfrac{dy}{dx}\!\left(\sin y + \cos(x+y)\right)$ | A1 |
| $\dfrac{dy}{dx} = \dfrac{-\cos(x+y)}{\sin y + \cos(x+y)}$ | A1 |

</details>

---

### 1.2 Parametric $\begin{cases} y = f(t) \\ x = g(t) \end{cases}$

::: {style="font-size: 0.85em; color: #666;"}
Instead of linking $x$ and $y$ directly, both are defined indirectly through a third variable **$t$ (parameter)**.  
Example: $x = \cos t,\; y = \sin t$ → eliminating $t$ gives $x^2 + y^2 = 1$ (a circle)  
**When is it used?** When a curve (circle, ellipse, etc.) is difficult to express with $y$ written directly in terms of $x$.
:::

**Differentiation:**

$$\boxed{\frac{dy}{dx} = \frac{dy/dt}{dx/dt}}$$

<details>
<summary>**Why does this hold?**</summary>

Chain rule: $\dfrac{dy}{dx} = \dfrac{dy}{dt} \times \dfrac{dt}{dx} = \dfrac{dy/dt}{dx/dt}$

Intuitively, think of $dt$ cancelling as in a fraction.

</details>

**Integration:**

$$\int y\,dx = \int y\,\frac{dx}{dt}\,dt$$

<details>
<summary>**Why does this hold?**</summary>

If $x = g(t)$, substitute $dx = \dfrac{dx}{dt}\,dt$. Since $y$ is also expressed in terms of $t$, the integral can be written entirely in terms of $t$.

**Example:** $y = t^2,\; x = t^3 \implies \int y\,dx = \int t^2 \cdot 3t^2\,dt = \dfrac{3t^5}{5} + C$

</details>

**Ex — Differentiate (find $\dfrac{dy}{dx}$ in terms of $t$):**

i. $y = 2t^3,\quad x = 3t^2$

ii. $y = 2t,\quad x = t^2 e^t$

iii. $y = 3\cos 3t,\quad x = 4\sin 3t$

<details>
<summary>**Solutions**</summary>

**i.**

$$\frac{dy}{dt} = 6t^2,\quad \frac{dx}{dt} = 6t \implies \boxed{\frac{dy}{dx} = t}$$

---

**ii.**

$$\frac{dy}{dt} = 2,\quad \frac{dx}{dt} = 2te^t + t^2 e^t = te^t(2+t) \implies \boxed{\frac{dy}{dx} = \frac{2}{te^t(2+t)}}$$

---

**iii.**

$$\frac{dy}{dt} = -9\sin 3t,\quad \frac{dx}{dt} = 12\cos 3t \implies \boxed{\frac{dy}{dx} = -\frac{3\tan 3t}{4}}$$

</details>

**Ex — Translate into Cartesian (eliminate $t$):**

i. $y = t^2 - 1,\quad x = 5 - t$

ii. $y = t - \dfrac{1}{t},\quad x = t + \dfrac{1}{t}$

iii. $y = 5\cos t + 4,\quad x = 2\sin t - 1$

<details>
<summary>**Solutions**</summary>

**i.** Substitute $t = 5-x$:

$$\boxed{y = x^2 - 10x + 24}$$

---

**ii.** Compute $x^2 - y^2$:

$$x^2 = t^2 + 2 + \frac{1}{t^2},\quad y^2 = t^2 - 2 + \frac{1}{t^2} \implies \boxed{x^2 - y^2 = 4}$$

---

**iii.** Using $\sin^2 t + \cos^2 t = 1$ — $\sin t = \dfrac{x+1}{2},\; \cos t = \dfrac{y-4}{5}$:

$$\boxed{\frac{(x+1)^2}{4} + \frac{(y-4)^2}{25} = 1} \qquad \text{(ellipse with centre }(-1,4)\text{)}$$

</details>

---

## 2. Finding the Equation of a Tangent

::: {style="font-size: 0.88em; color: #555; margin-bottom: 0.8em;"}
**Tangent:** a straight line touching the curve at a single point. Its slope at that point $= \dfrac{dy}{dx}$.  
Equation of the line through $(x_1, y_1)$ with slope $m$: $y - y_1 = m(x - x_1)$
:::

**General procedure:** find $\dfrac{dy}{dx}$ at the given point → use $y - y_1 = m(x - x_1)$.

<table style="border-collapse: collapse; width: 100%; font-size: 0.95em;">
<thead>
<tr style="background: #f0f0f0;">
  <th style="border: 1px solid #ccc; padding: 8px 12px; width: 18%;">Equation Types</th>
  <th style="border: 1px solid #ccc; padding: 8px 12px; width: 52%;">Questions</th>
  <th style="border: 1px solid #ccc; padding: 8px 12px; width: 30%;">Note</th>
</tr>
</thead>
<tbody>
<tr>
  <td style="border: 1px solid #ccc; padding: 8px 12px; font-weight: bold; vertical-align: middle;">Cartesian Explicit</td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    $y = \dfrac{2}{x}$ &nbsp; at $P(2,\ 1)$
    <details>
    <summary><strong>sol&gt;</strong></summary>

$$\frac{dy}{dx} = -\frac{2}{x^2} \implies \left.\frac{dy}{dx}\right|_{x=2} = -\frac{1}{2}$$

$$y - 1 = -\frac{1}{2}(x-2) \implies \boxed{y = -\frac{1}{2}x + 2}$$

    </details>
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top; font-size: 0.9em;">
    Differentiate directly, substitute $x = 2$
  </td>
</tr>
<tr>
  <td style="border: 1px solid #ccc; padding: 8px 12px; font-weight: bold; vertical-align: middle;">Cartesian Implicit</td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    $xy = 2$ &nbsp; at $P(2,\ 1)$
    <details>
    <summary><strong>sol&gt;</strong></summary>

$$\frac{d}{dx}(xy) = 0 \implies y + x\frac{dy}{dx} = 0 \implies \frac{dy}{dx} = -\frac{y}{x}$$

$$\left.\frac{dy}{dx}\right|_{(2,1)} = -\frac{1}{2} \implies \boxed{y = -\frac{1}{2}x + 2}$$

    </details>
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top; font-size: 0.9em;">
    Differentiate implicitly, solve for $\dfrac{dy}{dx}$, substitute
  </td>
</tr>
<tr>
  <td style="border: 1px solid #ccc; padding: 8px 12px; font-weight: bold; vertical-align: middle;">Parametric</td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top;">
    $x = 2\cos t,\ y = \sec t$ &nbsp; at $P(2,\ 1)$
    <details>
    <summary><strong>sol&gt;</strong></summary>

Find $t$: $\;2\cos t = 2 \implies \cos t = 1 \implies t = 0$ &nbsp;*(principal value)*

$$\frac{dx}{dt} = -2\sin t, \quad \frac{dy}{dt} = \sec t \tan t$$

$$\frac{dy}{dx} = \frac{\sec t \tan t}{-2\sin t} = -\frac{\sec^2 t}{2} \implies \left.\frac{dy}{dx}\right|_{t=0} = -\frac{1}{2}$$

$$\boxed{y = -\frac{1}{2}x + 2}$$

Note: There are infinitely many values of $t$ satisfying $\cos t = 1$: $t = 0,\ \pm 2\pi,\ \pm 4\pi,\ \ldots$ However, since $\sec t$ has period $2\pi$, we have $\sec t = 1$ for every such $t$, giving the same result $\dfrac{dy}{dx} = -\dfrac{\sec^2 t}{2} = -\dfrac{1}{2}$. It is convenient to use $t = 0$.

    </details>
  </td>
  <td style="border: 1px solid #ccc; padding: 8px 12px; vertical-align: top; font-size: 0.9em;">
    Find $t$ from $x = 2\cos t$, then compute $\dfrac{dy/dt}{dx/dt}$
  </td>
</tr>
</tbody>
</table>

---

## 3. Finding Notable Points (tangent parallel / perpendicular to axes)

::: {.callout-tip}
## Key — For Implicit and Parametric equations

For implicit and parametric equations, instead of "turning point" we describe special points by the **direction of the tangent**. **Why?** Because $y$ is not explicitly separated as a function of $x$, making it inconvenient to compute $\dfrac{d^2y}{dx^2}$. Instead, we determine local maxima/minima by checking the **sign change** of $\dfrac{dy}{dx}$.

- A point at which the tangent is **parallel to $x$-axis** $\Rightarrow$ $dy = 0$
  - i.e. $\dfrac{dy}{dt} = 0$ (parametric) &nbsp;or&nbsp; numerator of $\dfrac{dy}{dx} = 0$ (implicit)
- A point at which the tangent is **perpendicular to $x$-axis** $\Rightarrow$ $dx = 0$
  - i.e. $\dfrac{dx}{dt} = 0$ (parametric) &nbsp;or&nbsp; denominator of $\dfrac{dy}{dx} = 0$ (implicit)

<details>
<summary>**Why use $dy = 0$ and $dx = 0$ separately?**</summary>

In parametric/implicit equations, the gradient is always a **fraction**:

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$$

**Horizontal tangent (parallel to $x$-axis)** → slope $= 0$ → numerator $= 0$

$$\frac{dy}{dx} = 0 \iff \frac{dy}{dt} = 0$$

**Vertical tangent (perpendicular to $x$-axis)** → slope $= \infty$ (undefined) → denominator $= 0$

$$\frac{dy}{dx} = \text{undefined} \iff \frac{dx}{dt} = 0$$

For a fraction to equal zero, the numerator must be zero; for it to be undefined, the denominator must be zero — the principle is the same as setting $\dfrac{dy}{dx} = 0$ in the explicit case, except we treat the numerator and denominator separately.

</details>

<details>
<summary>**What is the second derivative test?**</summary>

Method for identifying local maxima and minima from $y = f(x)$.

**Procedure:**

1. Solve $\dfrac{dy}{dx} = 0$ to find stationary points $x = a$
2. Compute $\dfrac{d^2y}{dx^2}$ and substitute $x = a$:

| $\dfrac{d^2y}{dx^2}\big|_{x=a}$ | Conclusion |
|---|---|
| $> 0$ | local minimum — concave up |
| $< 0$ | local maximum — concave down |
| $= 0$ | inconclusive → check sign change directly |

**Why this is inconvenient for implicit/parametric:** $\dfrac{dy}{dx}$ already involves both $x$ and $y$, so differentiating once more gives a very complicated expression. Instead, check the sign change of $\dfrac{dy}{dx}$ directly:

| left of $P$ | $P$ | right of $P$ | Conclusion |
|:---:|:---:|:---:|---|
| $+$ | $0$ | $-$ | local maximum |
| $-$ | $0$ | $+$ | local minimum |
| $+$ | $0$ | $+$ | stationary point of inflection (not a turning point) |

</details>
:::

::: {style="font-size: 0.83em; color: #555; margin-top: -0.4em; margin-bottom: 1.2em;"}
**Terminology**

| Term | Definition |
|---|---|
| **Stationary point** | Any point where $\dfrac{dy}{dx} = 0$ (tangent is horizontal) |
| **Turning point** | A stationary point where the sign of the gradient changes (local max/min) |
| **Point of inflection** | A point where the concavity of the curve changes — $\dfrac{d^2y}{dx^2} = 0$ with sign change |

> Turning point ⊂ Stationary point. A point of inflection does not require $\dfrac{dy}{dx} = 0$ (but if it does, it is a *stationary point of inflection*).

<details>
<summary>**When is a stationary point not a turning point?**</summary>

→ **Stationary point of inflection**

**Example:** $y = x^3$ at $x = 0$

$$\frac{dy}{dx} = 3x^2 \implies \left.\frac{dy}{dx}\right|_{x=0} = 0 \quad \checkmark \text{ (stationary point)}$$

Checking the sign of the gradient:

| Interval | $\dfrac{dy}{dx} = 3x^2$ | Sign |
|---|---|---|
| $x < 0$ | $3x^2 > 0$ | $+$ |
| $x = 0$ | $0$ | $0$ |
| $x > 0$ | $3x^2 > 0$ | $+$ |

The sign **does not change** → not a turning point. However, since the concavity of the curve changes at this point → **point of inflection**.

| | $\dfrac{dy}{dx} = 0$ | gradient sign change | $\dfrac{d^2y}{dx^2} = 0$ |
|---|:---:|:---:|:---:|
| Turning point | ✓ | ✓ | usually ✓ |
| Stationary point of inflection | ✓ | ✗ | ✓ |
| (Non-stationary) point of inflection | ✗ | ✗ | ✓ |

</details>
:::

**Ex 1** &nbsp; Find the coordinates of the points at which the tangents are parallel to the $x$-axis, given:

$$x^2 + 4y^2 - 6x - 16y + 21 = 0$$

<details>
<summary>**Mark Scheme**</summary>

| | |
|---|---|
| Differentiate implicitly: $2x + 8y\dfrac{dy}{dx} - 6 - 16\dfrac{dy}{dx} = 0$ | M1 A1 |
| Collect $\dfrac{dy}{dx}$ terms: $\dfrac{dy}{dx}(8y - 16) = 6 - 2x$ | dM1 |
| $\dfrac{dy}{dx} = \dfrac{6 - 2x}{8y - 16}$ | A1 |
| Set numerator $= 0$ for tangent parallel to $x$-axis: $6 - 2x = 0 \implies x = 3$ | M1 |
| Substitute $x = 3$ into original equation: $9 + 4y^2 - 18 - 16y + 21 = 0$ | M1 |
| $4y^2 - 16y + 12 = 0 \implies y^2 - 4y + 3 = 0 \implies (y-1)(y-3) = 0$ | dM1 A1 |
| $y = 1$ or $y = 3$ | A1 |
| Points: $\boxed{(3,\ 1)}$ and $\boxed{(3,\ 3)}$ | A1 |

</details>

---

**Ex 2** &nbsp; Find the coordinates of the points of intersection of the curve with parametric equations $x = 3t + 2,\ y = 1 - t$ and the line $y + x = 2$.

<details>
<summary>**Mark Scheme**</summary>

| | |
|---|---|
| Substitute parametric equations into $y + x = 2$: $(1 - t) + (3t + 2) = 2$ | M1 |
| $3 + 2t = 2 \implies t = -\dfrac{1}{2}$ | A1 |
| $x = 3\!\left(-\dfrac{1}{2}\right) + 2 = \dfrac{1}{2}$ | A1 |
| $y = 1 - \left(-\dfrac{1}{2}\right) = \dfrac{3}{2}$ | A1 |
| Point: $\boxed{\left(\dfrac{1}{2},\ \dfrac{3}{2}\right)}$ | A1 |

</details>

---

**Ex 3** &nbsp; Find the coordinates of the points at which the tangents are perpendicular to the $x$-axis, given:

$$x = \frac{t^2}{1-t}, \quad y = \frac{t}{1-t}, \qquad t \neq 1$$

<details>
<summary>**Mark Scheme**</summary>

| | |
|---|---|
| Differentiate $x$ using quotient rule: $\dfrac{dx}{dt} = \dfrac{2t(1-t) - t^2(-1)}{(1-t)^2} = \dfrac{2t - t^2}{(1-t)^2} = \dfrac{t(2-t)}{(1-t)^2}$ | M1 A1 |
| Set $\dfrac{dx}{dt} = 0$ for tangent perpendicular to $x$-axis: $t(2-t) = 0$ | M1 |
| $t = 0$ &nbsp;or&nbsp; $t = 2$ | A1 |
| At $t = 0$: $x = 0,\ y = 0$ &nbsp;→&nbsp; $\boxed{(0,\ 0)}$ | A1 |
| At $t = 2$: $x = \dfrac{4}{1-2} = -4,\ y = \dfrac{2}{1-2} = -2$ &nbsp;→&nbsp; $\boxed{(-4,\ -2)}$ | A1 |

</details>
