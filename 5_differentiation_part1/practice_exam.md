
# Practice — Exam Questions (Differentiation)

---

## Q1

**(a)** Differentiate each of the following with respect to $x$ and simplify your answers.

&emsp;(i) $\sqrt{1-\cos x}$

&emsp;(ii) $x^3 \ln x$ **(6)**

**(b)** Given that

$$x = \frac{y+1}{3-2y},$$

find and simplify an expression for $\dfrac{dy}{dx}$ in terms of $y$. **(5)**

---

### Q1 — Mark Scheme

**(a)(i)** $y = (1-\cos x)^{1/2}$, chain rule:

$$\frac{dy}{dx} = \frac{1}{2}(1-\cos x)^{-1/2} \cdot \sin x = \boxed{\frac{\sin x}{2\sqrt{1-\cos x}}} \tag{M1, A1}$$

**(a)(ii)** Product rule:

$$\frac{dy}{dx} = 3x^2 \ln x + x^3 \cdot \frac{1}{x} = 3x^2\ln x + x^2 = \boxed{x^2(3\ln x + 1)} \tag{M1, A1, A1}$$

**(b)** Differentiate $x$ w.r.t. $y$ using the quotient rule:

$$\frac{dx}{dy} = \frac{(3-2y)\cdot 1 - (y+1)\cdot(-2)}{(3-2y)^2} = \frac{3-2y+2y+2}{(3-2y)^2} = \frac{5}{(3-2y)^2} \tag{M1, A1}$$

Invert:

$$\boxed{\frac{dy}{dx} = \frac{(3-2y)^2}{5}} \tag{M1, A1, A1}$$

---

## Q2

$$f(x) = \frac{x^2+3}{4x+1}, \quad x \in \mathbb{R},\ x \neq -\tfrac{1}{4}$$

**(a)** Find and simplify an expression for $f'(x)$. **(3)**

**(b)** Find the set of values of $x$ for which $f(x)$ is increasing. **(5)**

---

### Q2 — Mark Scheme

**(a)** Quotient rule:

$$f'(x) = \frac{2x(4x+1)-(x^2+3)\cdot 4}{(4x+1)^2} = \frac{8x^2+2x-4x^2-12}{(4x+1)^2} = \frac{4x^2+2x-12}{(4x+1)^2} \tag{M1, A1}$$

$$\boxed{f'(x) = \frac{2(2x-3)(x+2)}{(4x+1)^2}} \tag{A1}$$

**(b)** $f$ increasing $\Rightarrow f'(x) > 0$

$(4x+1)^2 > 0$ always (for $x \neq -\tfrac{1}{4}$), so sign is determined by numerator: $\tag{B1}$

$$2(2x-3)(x+2) > 0$$

Critical values: $x = \tfrac{3}{2}$ and $x = -2$ $\tag{M1}$

Sign table:

| interval | $(2x-3)$ | $(x+2)$ | product |
|----------|----------|---------|---------|
| $x < -2$ | $-$ | $-$ | $+$ |
| $-2 < x < \frac{3}{2}$ | $-$ | $+$ | $-$ |
| $x > \frac{3}{2}$ | $+$ | $+$ | $+$ |

$$\boxed{\left\{x : x < -2\right\} \cup \left\{x : x > \tfrac{3}{2}\right\}} \tag{A1, A1}$$

---

## Q3

The curve with equation $y = x^{\frac{3}{2}}\ln\dfrac{x}{4}$, $\; x > 0$, crosses the $x$-axis at the point $P$.

**(a)** Write down the coordinates of $P$. **(1)**

The normal to the curve at $P$ crosses the $y$-axis at the point $Q$.

**(b)** Find the area of triangle $OPQ$ where $O$ is the origin. **(6)**

The curve has a stationary point at $R$.

**(c)** Find the $x$-coordinate of $R$ in exact form. **(3)**

---

### Q3 — Mark Scheme

**(a)** At $x$-axis: $y = 0 \Rightarrow x^{3/2}\ln\dfrac{x}{4} = 0$. Since $x > 0$, $x^{3/2} \neq 0$, so $\ln\dfrac{x}{4} = 0 \Rightarrow x = 4$.

$$\boxed{P = (4,\;0)} \tag{B1}$$

**(b)** Differentiate using the product rule:

$$\frac{dy}{dx} = \frac{3}{2}x^{1/2}\ln\frac{x}{4} + x^{3/2}\cdot\frac{1}{x} = x^{1/2}\!\left(\frac{3}{2}\ln\frac{x}{4}+1\right) \tag{M1, A1}$$

At $P$ ($x = 4$): $\dfrac{dy}{dx} = \sqrt{4}\!\left(\dfrac{3}{2}\cdot 0 + 1\right) = 2$, so gradient of tangent $= 2$ $\tag{M1}$

Normal gradient $= -\dfrac{1}{2}$ $\tag{B1}$

Normal at $P(4,0)$: $y = -\dfrac{1}{2}(x-4)$

At $x = 0$: $y = 2$, so $Q = (0, 2)$ $\tag{A1}$

Triangle $OPQ$: right-angled at $O$, base $OP = 4$, height $OQ = 2$:

$$\text{Area} = \frac{1}{2}\times 4 \times 2 = \boxed{4} \tag{A1}$$

**(c)** Set $\dfrac{dy}{dx} = 0$:

$$x^{1/2}\!\left(\frac{3}{2}\ln\frac{x}{4}+1\right) = 0 \implies \ln\frac{x}{4} = -\frac{2}{3} \tag{M1, A1}$$

$$\frac{x}{4} = e^{-2/3} \implies \boxed{x = 4e^{-2/3}} \tag{A1}$$

---

## Q4

**(a)** Use the derivative of $\cos x$ to prove that

$$\frac{d}{dx}(\sec x) = \sec x\tan x. \tag{4}$$

The curve $C$ has equation $y = e^{2x}\sec x$, $-\dfrac{\pi}{2} < x < \dfrac{\pi}{2}$.

**(b)** Find an equation for the tangent to $C$ at the point where it crosses the $y$-axis. **(4)**

**(c)** Find, to 2 decimal places, the $x$-coordinate of the stationary point of $C$. **(3)**

---

### Q4 — Mark Scheme

**(a)**

$$\frac{d}{dx}(\sec x) = \frac{d}{dx}(\cos x)^{-1} = -(\cos x)^{-2}\cdot(-\sin x) \tag{M1, A1}$$

$$= \frac{\sin x}{\cos^2 x} = \frac{1}{\cos x}\cdot\frac{\sin x}{\cos x} = \sec x\tan x \quad \blacksquare \tag{A1, A1}$$

**(b)** Crosses $y$-axis at $x = 0$: $y = e^0\sec 0 = 1$, point $(0,1)$. $\tag{B1}$

$$\frac{dy}{dx} = 2e^{2x}\sec x + e^{2x}\sec x\tan x = e^{2x}\sec x(2+\tan x) \tag{M1, A1}$$

At $x = 0$: $m = 1\cdot 1\cdot(2+0) = 2$

Tangent: $\boxed{y = 2x+1}$ $\tag{A1}$

**(c)** Stationary point: $e^{2x}\sec x(2+\tan x) = 0$

$e^{2x} \neq 0$, $\sec x \neq 0$ on domain, so $\tan x = -2$ $\tag{M1, A1}$

$$x = \arctan(-2) \approx \boxed{-1.11} \tag{A1}$$

---

## Q5

A curve has equation $y = e^{3x}\cos 2x$.

**(a)** Find $\dfrac{dy}{dx}$. **(2)**

**(b)** Show that $\dfrac{d^2y}{dx^2} = e^{3x}(5\cos 2x - 12\sin 2x)$. **(3)**

The curve has a stationary point in the interval $[0, 1]$.

**(c)** Find the $x$-coordinate of the stationary point to 3 significant figures. **(4)**

**(d)** Determine whether the stationary point is a maximum or minimum point and justify your answer. **(2)**

---

### Q5 — Mark Scheme

**(a)** Product rule:

$$\frac{dy}{dx} = 3e^{3x}\cos 2x - 2e^{3x}\sin 2x = \boxed{e^{3x}(3\cos 2x - 2\sin 2x)} \tag{M1, A1}$$

**(b)** Differentiate $\dfrac{dy}{dx}$ using product rule:

$$\frac{d^2y}{dx^2} = 3e^{3x}(3\cos 2x-2\sin 2x) + e^{3x}(-6\sin 2x - 4\cos 2x) \tag{M1, A1}$$

$$= e^{3x}(9\cos 2x - 6\sin 2x - 6\sin 2x - 4\cos 2x) = e^{3x}(5\cos 2x - 12\sin 2x) \quad \blacksquare \tag{A1}$$

**(c)** Stationary point: $\dfrac{dy}{dx} = 0 \Rightarrow 3\cos 2x = 2\sin 2x \Rightarrow \tan 2x = \dfrac{3}{2}$ $\tag{M1, A1}$

$$2x = \arctan\!\left(\tfrac{3}{2}\right) \approx 0.9828 \implies x \approx 0.4913 \approx \boxed{0.491} \tag{A1, A1}$$

**(d)** At $x \approx 0.491$:

$$\frac{d^2y}{dx^2} = e^{3(0.491)}\bigl(5\cos(0.983)-12\sin(0.983)\bigr) \approx e^{1.473}(2.77-9.98) < 0 \tag{M1}$$

Since $\dfrac{d^2y}{dx^2} < 0$, the stationary point is a **maximum**. $\tag{A1}$

---

## Q6

A curve has equation $y = x^2 - \sqrt{4+\ln x}$.

**(a)** Show that the tangent to the curve at the point where $x = 1$ has the equation

$$7x - 4y = 11. \tag{5}$$

The curve has a stationary point with $x$-coordinate $\alpha$.

**(b)** Show that $0.3 < \alpha < 0.4$. **(3)**

**(c)** Show that $\alpha$ is a solution of the equation

$$x = \tfrac{1}{2}(4+\ln x)^{-\frac{1}{4}}. \tag{2}$$

**(d)** Use the iteration formula

$$x_{n+1} = \tfrac{1}{2}(4+\ln x_n)^{-\frac{1}{4}},$$

with $x_0 = 0.35$, to find $x_1, x_2, x_3$ and $x_4$, giving your answers to 5 decimal places. **(3)**

---

### Q6 — Mark Scheme

**(a)** Differentiate using chain rule:

$$\frac{dy}{dx} = 2x - \frac{1}{2}(4+\ln x)^{-1/2}\cdot\frac{1}{x} = 2x - \frac{1}{2x\sqrt{4+\ln x}} \tag{M1, A1}$$

At $x = 1$: $y = 1 - \sqrt{4} = -1$, point $(1, -1)$. $\tag{B1}$

$$\left.\frac{dy}{dx}\right|_{x=1} = 2 - \frac{1}{2\cdot 1\cdot\sqrt{4}} = 2 - \frac{1}{4} = \frac{7}{4} \tag{A1}$$

Tangent: $y-(-1) = \dfrac{7}{4}(x-1) \implies 4y+4 = 7x-7 \implies 7x-4y = 11 \quad \blacksquare$ $\tag{A1}$

**(b)** At a stationary point $\dfrac{dy}{dx} = 0$:

$$2x = \frac{1}{2x\sqrt{4+\ln x}} \implies 4x^2\sqrt{4+\ln x} = 1$$

Let $g(x) = 4x^2\sqrt{4+\ln x} - 1$. $\tag{M1}$

At $x = 0.3$: $\ln(0.3) \approx -1.2040$, $\sqrt{2.796} \approx 1.672$, $g(0.3) \approx 4(0.09)(1.672)-1 = -0.398 < 0$ $\tag{A1}$

At $x = 0.4$: $\ln(0.4) \approx -0.9163$, $\sqrt{3.084} \approx 1.756$, $g(0.4) \approx 4(0.16)(1.756)-1 = +0.124 > 0$ $\tag{A1}$

Sign change $\Rightarrow 0.3 < \alpha < 0.4 \quad \blacksquare$

**(c)** From $4x^2\sqrt{4+\ln x} = 1$:

$$\sqrt{4+\ln x} = \frac{1}{4x^2} \tag{M1}$$

Square both sides: $4+\ln x = \dfrac{1}{16x^4} \implies$ rearranging,

$$4x^2 = (4+\ln x)^{-1/2} \implies x^2 = \frac{1}{4}(4+\ln x)^{-1/2} \implies x = \frac{1}{2}(4+\ln x)^{-1/4} \quad \blacksquare \tag{A1}$$

(taking positive root since $x > 0$)

**(d)**

| $n$ | $x_n$ |
|-----|-------|
| 0 | 0.35000 |
| 1 | 0.38150 |
| 2 | 0.37879 |
| 3 | 0.37900 |
| 4 | 0.37899 |

$$x_1 = 0.38150,\quad x_2 = 0.37879,\quad x_3 = 0.37900,\quad x_4 = 0.37899 \tag{A1, A1, A1}$$
