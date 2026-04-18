
# Practice Problems — Basic Differentiation

---

## Q01 — Differentiate each of the following

a) $y = (1+x^2)^8$

b) $y = e^x \sec 3x$

c) $y = \{x + \ln(2x)\}^3$

d) $y = (x^2+3)\sqrt{x+2}$

e) $y = \dfrac{5x}{x^3+2}$

f) $y = \dfrac{\tan 2x}{x}$

g) $y = \dfrac{\cos(2x^3)}{3x}$

h) $y = \dfrac{1+\sin x}{1+\cos x}$

---

### Q01 — Solutions

**(a)** Chain rule:

$$\frac{dy}{dx} = 8(1+x^2)^7 \cdot 2x = \boxed{16x(1+x^2)^7}$$

**(b)** Product rule:

$$\frac{dy}{dx} = e^x \sec 3x + e^x \cdot 3\sec 3x \tan 3x = \boxed{e^x \sec 3x\,(1 + 3\tan 3x)}$$

**(c)** Chain rule — inner derivative: $\dfrac{d}{dx}[x+\ln(2x)] = 1 + \dfrac{1}{x} = \dfrac{x+1}{x}$

$$\frac{dy}{dx} = 3\{x+\ln(2x)\}^2 \cdot \frac{x+1}{x} = \boxed{\frac{3(x+1)}{x}\{x+\ln(2x)\}^2}$$

**(d)** Product rule, then combine over $2\sqrt{x+2}$:

$$\frac{dy}{dx} = 2x\sqrt{x+2} + \frac{x^2+3}{2\sqrt{x+2}} = \frac{4x(x+2)+x^2+3}{2\sqrt{x+2}} = \boxed{\frac{5x^2+8x+3}{2\sqrt{x+2}}} = \frac{(5x+3)(x+1)}{2\sqrt{x+2}}$$

**(e)** Quotient rule:

$$\frac{dy}{dx} = \frac{5(x^3+2)-5x\cdot 3x^2}{(x^3+2)^2} = \frac{10-10x^3}{(x^3+2)^2} = \boxed{\frac{10(1-x^3)}{(x^3+2)^2}}$$

**(f)** Quotient rule:

$$\frac{dy}{dx} = \frac{2x\sec^2 2x - \tan 2x}{x^2}$$

**(g)** Chain rule on numerator, then quotient rule:

$$\frac{d}{dx}[\cos(2x^3)] = -6x^2\sin(2x^3)$$

$$\frac{dy}{dx} = \frac{-18x^3\sin(2x^3)-3\cos(2x^3)}{9x^2} = \boxed{\frac{-6x^3\sin(2x^3)-\cos(2x^3)}{3x^2}}$$

**(h)** Quotient rule, use $\sin^2 x + \cos^2 x = 1$:

$$\frac{dy}{dx} = \frac{\cos x(1+\cos x)+(1+\sin x)\sin x}{(1+\cos x)^2} = \frac{\cos x+\cos^2 x+\sin x+\sin^2 x}{(1+\cos x)^2} = \boxed{\frac{1+\sin x+\cos x}{(1+\cos x)^2}}$$

---

## Q02

The curve $C$ has equation $y = 4x^{3/2} - \ln(5x)$, where $x > 0$.
The tangent at the point on $C$ where $x = 1$ meets the $x$-axis at the point $A$.

Find the $x$-coordinate of $A$ in its simplest form.

---

### Q02 — Solution

$$\frac{dy}{dx} = 6x^{1/2} - \frac{1}{x}$$

At $x = 1$: gradient $m = 6 - 1 = 5$, and $y = 4 - \ln 5$

Tangent: $y - (4-\ln 5) = 5(x-1) \implies y = 5x - 1 - \ln 5$

Set $y = 0$:

$$5x = 1 + \ln 5 \implies \boxed{x_A = \frac{1+\ln 5}{5}}$$

---

## Q03

a) Given $f(x) = \dfrac{x}{x^2+2}$, find the set of values of $x$ for which $f'(x) < 0$.

b) Given $f(x) = 12\ln x - x^{3/2}$, find the set of values of $x$ for which $f(x)$ is an increasing function of $x$.

---

### Q03 — Solutions

**(a)** Quotient rule:

$$f'(x) = \frac{(x^2+2)-2x^2}{(x^2+2)^2} = \frac{2-x^2}{(x^2+2)^2}$$

$(x^2+2)^2 > 0$ always, so $f'(x) < 0 \iff 2 - x^2 < 0 \iff x^2 > 2$

$$\boxed{\{x : x < -\sqrt{2}\} \cup \{x : x > \sqrt{2}\}}$$

**(b)**

$$f'(x) = \frac{12}{x} - \frac{3}{2}x^{1/2}$$

$f$ increasing $\Rightarrow f'(x) > 0$:

$$\frac{12}{x} - \frac{3}{2}x^{1/2} > 0$$

Since $\ln x$ requires $x > 0$, multiply both sides by $\dfrac{2x}{3} > 0$ (direction unchanged):

$$\frac{12}{x} \cdot \frac{2x}{3} - \frac{3}{2}x^{1/2} \cdot \frac{2x}{3} > 0$$

$$8 - x^{3/2} > 0 \implies x^{3/2} < 8$$

Raise both sides to the power $\dfrac{2}{3}$:

$$x < 8^{2/3} = \left(\sqrt[3]{8}\right)^2 = 2^2 = 4$$

With domain $x > 0$:

$$\boxed{\{x : 0 < x < 4\}}$$

---

## Q04

Given $f(x) = e^{2x}\sin 2x$, find the turning points of the graph of $y = f(x)$, $\;0 < x < \pi$.

---

### Q04 — Solution

Product rule:

$$f'(x) = 2e^{2x}\sin 2x + 2e^{2x}\cos 2x = 2e^{2x}(\sin 2x + \cos 2x)$$

$f'(x) = 0$: since $e^{2x} \neq 0$,

$$\sin 2x + \cos 2x = 0 \implies \tan 2x = -1$$

For $0 < 2x < 2\pi$: $\;2x = \dfrac{3\pi}{4},\; \dfrac{7\pi}{4}$, so $x = \dfrac{3\pi}{8},\; \dfrac{7\pi}{8}$

At $x = \dfrac{3\pi}{8}$: $y = e^{3\pi/4}\sin\dfrac{3\pi}{4} = \dfrac{\sqrt{2}}{2}e^{3\pi/4}$

At $x = \dfrac{7\pi}{8}$: $y = e^{7\pi/4}\sin\dfrac{7\pi}{4} = -\dfrac{\sqrt{2}}{2}e^{7\pi/4}$

$$\boxed{\left(\frac{3\pi}{8},\; \frac{\sqrt{2}}{2}e^{3\pi/4}\right) \quad \text{and} \quad \left(\frac{7\pi}{8},\; -\frac{\sqrt{2}}{2}e^{7\pi/4}\right)}$$

---

## Q05

Given that $y = \log_a x$, $\; x > 0$, where $a$ is a positive constant,

(a)  (i) express $x$ in terms of $a$ and $y$

     (ii) deduce that $\ln x = y\ln a$

(b) Show that $\dfrac{dy}{dx} = \dfrac{1}{x\ln a}$

---

### Q05 — Solutions

**(a)(i)** $y = \log_a x \implies x = a^y$

**(a)(ii)** Take $\ln$ of both sides: $\ln x = \ln(a^y) = y\ln a \quad \blacksquare$

**(b)** Differentiate $\ln x = y\ln a$ w.r.t. $x$:

$$\frac{1}{x} = \ln a \cdot \frac{dy}{dx} \implies \boxed{\frac{dy}{dx} = \frac{1}{x\ln a}} \quad \blacksquare$$

*Alternative:* from $x = a^y$, $\dfrac{dx}{dy} = a^y \ln a = x\ln a$, so $\dfrac{dy}{dx} = \dfrac{1}{x\ln a}$.

---

## Q06

a) Given $y = \arctan x$, show that $\dfrac{dy}{dx} = \dfrac{1}{1+x^2}$

b) Given $y = \arccos x$, show that $\dfrac{dy}{dx} = -\dfrac{1}{\sqrt{1-x^2}}$

---

### Q06 — Solutions

**(a)** Let $x = \tan y$. Differentiate w.r.t. $y$: $\dfrac{dx}{dy} = \sec^2 y$

$$\frac{dy}{dx} = \frac{1}{\sec^2 y} = \frac{1}{1+\tan^2 y} = \boxed{\frac{1}{1+x^2}} \quad \blacksquare$$

**(b)** Let $x = \cos y$, $y \in [0, \pi]$. Differentiate: $\dfrac{dx}{dy} = -\sin y$

$$\frac{dy}{dx} = -\frac{1}{\sin y}$$

Since $\sin y \geq 0$ on $[0,\pi]$: $\sin y = \sqrt{1-\cos^2 y} = \sqrt{1-x^2}$

$$\frac{dy}{dx} = \boxed{-\frac{1}{\sqrt{1-x^2}}} \quad \blacksquare$$
