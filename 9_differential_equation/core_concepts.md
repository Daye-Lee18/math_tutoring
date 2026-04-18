# Differential Equations — Core Concepts

---

## 1. Solving Separable 1st Order Differential Equations

### What is a Differential Equation?

A **differential equation (D.E.)** is any equation that contains a derivative.

- **1st order**: involves only $\dfrac{dy}{dx}$ (no higher derivatives)
- **Separable**: can be written in the form $\dfrac{dy}{dx} = f(x)\,g(y)$ — the right-hand side factorises into a function of $x$ **only** times a function of $y$ **only**

### Method: Separation of Variables

$$\frac{dy}{dx} = f(x)\,g(y)$$

| Step | What to do | Result |
|------|-----------|--------|
| **1. Separate** | Move all $y$ terms to the left, all $x$ terms to the right | $\dfrac{1}{g(y)}\,dy = f(x)\,dx$ |
| **2. Integrate** | Integrate both sides | $\displaystyle\int \frac{1}{g(y)}\,dy = \int f(x)\,dx$ |
| **3. Solve** | Write $y$ explicitly (if possible); add constant $C$ | $F(y) = F(x) + C$ |

::: {.callout-tip title="KEY"}
- A **general solution** contains an arbitrary constant $C$ — it represents a **family** of curves
- A **particular solution** is found by substituting given initial conditions to determine $C$
- Add only **one** constant $C$ at the end (constants from both sides merge into one)
:::

---

<details>
<summary>**Ex 1 — General solutions** (분리변수로 일반해 구하기)</summary>

**i.** $\displaystyle\frac{dy}{dx} = (1+2y)(1-2x)$

Separate: $\dfrac{1}{1+2y}\,dy = (1-2x)\,dx$

$$\int \frac{1}{1+2y}\,dy = \int (1-2x)\,dx$$

$$\frac{1}{2}\ln|1+2y| = x - x^2 + C$$

$$\boxed{\ln|1+2y| = 2x - 2x^2 + A \quad (A = 2C)}$$

또는 $y = \dfrac{1}{2}\!\left(e^{2x-2x^2+A}-1\right)$로 쓸 수도 있다.

---

**ii.** $\displaystyle\cos^2 x\,\frac{dy}{dx} = y^2\sin^2 x$

Separate: $\dfrac{1}{y^2}\,dy = \dfrac{\sin^2 x}{\cos^2 x}\,dx = \tan^2 x\,dx$

$$\int y^{-2}\,dy = \int \tan^2 x\,dx = \int (\sec^2 x - 1)\,dx$$

$$-\frac{1}{y} = \tan x - x + C$$

$$\boxed{y = \frac{-1}{\tan x - x + C}}$$

---

**iii.** $\displaystyle\frac{dy}{dx} = 2e^{x-y}$

$e^{x-y} = e^x \cdot e^{-y}$이므로 분리 가능:

Separate: $e^y\,dy = 2e^x\,dx$

$$\int e^y\,dy = \int 2e^x\,dx$$

$$e^y = 2e^x + C$$

$$\boxed{y = \ln(2e^x + C)}$$

</details>

---

<details>
<summary>**Ex 2 — Particular solutions** (초기조건으로 특수해 구하기)</summary>

**i.** $\displaystyle\frac{dy}{dx} = \sin x\cos^2 x;\quad y = 0 \text{ when } x = \frac{\pi}{3}$

Separate: $dy = \sin x\cos^2 x\,dx$

$$\int dy = \int \sin x\cos^2 x\,dx$$

**치환:** $u = \cos x,\; du = -\sin x\,dx$

$$y = -\int u^2\,du = -\frac{u^3}{3} + C = -\frac{\cos^3 x}{3} + C$$

**초기조건 대입:** $x = \dfrac{\pi}{3},\; y = 0$:

$$0 = -\frac{(1/2)^3}{3} + C \implies C = \frac{1}{24}$$

$$\boxed{y = -\frac{\cos^3 x}{3} + \frac{1}{24}}$$

---

**ii.** $\displaystyle(1-x^2)\frac{dy}{dx} = xy + y;\quad x = 0.5,\; y = 6$

우변 인수분해: $xy + y = y(x+1)$

$$\frac{dy}{dx} = \frac{y(x+1)}{1-x^2} = \frac{y(x+1)}{(1-x)(1+x)} = \frac{y}{1-x}$$

Separate: $\dfrac{1}{y}\,dy = \dfrac{1}{1-x}\,dx$

$$\int \frac{1}{y}\,dy = \int \frac{1}{1-x}\,dx$$

$$\ln|y| = -\ln|1-x| + C$$

**초기조건 대입:** $x = 0.5,\; y = 6$:

$$\ln 6 = -\ln(0.5) + C \implies C = \ln 6 - \ln 2 = \ln 3$$

$$\ln|y| = -\ln|1-x| + \ln 3 = \ln\frac{3}{|1-x|}$$

$$\boxed{y = \frac{3}{1-x} \quad (x < 1)}$$

</details>

---

## 2. Important Applied D.E.s (in relation to C3)

These three models appear frequently in exam questions. Understand the **physical meaning** of each equation, not just the formula.

| | **Decay** | **Newton's Law of Cooling** | **Leaking Container** |
|---|---|---|---|
| **Scenario** | Radioactivity $N$ decreasing over time | Body temperature $\theta$ cooling toward surroundings $\theta_0$ | Liquid poured in at constant rate $P$, leaks out proportionally |
| **Assumption** | Rate of decay proportional to amount remaining | Rate of cooling proportional to temperature *difference* from surroundings | Rate in $= P$; rate out $= kV$ |
| **D.E.** | $\dfrac{dN}{dt} = -kN \quad (k>0)$ | $\dfrac{d\theta}{dt} = -k(\theta-\theta_0) \quad (k>0)$ | $\dfrac{dV}{dt} = P - kV \quad (k>0)$ |
| **General solution** | $N = Ae^{-kt}$ | $\theta = \theta_0 + Ae^{-kt}$ | $V = \dfrac{P}{k} - Ae^{-kt}$ |

::: {.callout-tip title="KEY"}
- All three are separable — solve each by separating variables  
- The $-k$ in the exponent means all three **approach a limit** as $t \to \infty$: $N \to 0$, $\theta \to \theta_0$, $V \to P/k$  
- In exam questions, the constant $A$ is always determined by the **initial condition** (값을 알고 있는 시점 = $t = 0$)
:::

---

<details>
<summary>**Deriving the solutions** (풀이과정 — 시험에 나오면 반드시 쓸 것)</summary>

### Decay: $\dfrac{dN}{dt} = -kN$

$$\int \frac{1}{N}\,dN = \int -k\,dt$$

$$\ln|N| = -kt + C$$

$$N = e^{-kt+C} = e^C \cdot e^{-kt} = Ae^{-kt} \quad (A = e^C > 0)$$

---

### Cooling: $\dfrac{d\theta}{dt} = -k(\theta - \theta_0)$

Let $u = \theta - \theta_0$, then $\dfrac{du}{dt} = \dfrac{d\theta}{dt}$:

$$\int \frac{1}{u}\,du = \int -k\,dt$$

$$\ln|u| = -kt + C \implies u = Ae^{-kt}$$

$$\boxed{\theta - \theta_0 = Ae^{-kt} \implies \theta = \theta_0 + Ae^{-kt}}$$

---

### Leaking: $\dfrac{dV}{dt} = P - kV$

$$\int \frac{1}{P-kV}\,dV = \int dt$$

$$-\frac{1}{k}\ln|P-kV| = t + C$$

$$P - kV = e^{-k(t+C)} = Be^{-kt}$$

$$V = \frac{P}{k} - \frac{B}{k}e^{-kt} = \frac{P}{k} - Ae^{-kt} \quad \left(A = \frac{B}{k}\right)$$

</details>

---

<details>
<summary>**Ex 3 — Applied example: Newton's Law of Cooling**</summary>

A cup of coffee cools from $90°C$ to $70°C$ in 5 minutes. The room temperature is $20°C$.

**(a)** Show that $\theta = 20 + 70e^{-kt}$, where $t$ is in minutes.

**(b)** Find the value of $k$.

**(c)** Find the temperature after 20 minutes.

---

**(a)** By Newton's Law of Cooling:

$$\frac{d\theta}{dt} = -k(\theta - 20)$$

General solution: $\theta = 20 + Ae^{-kt}$

At $t=0$: $\theta = 90 \implies 90 = 20 + A \implies A = 70$

$$\boxed{\theta = 20 + 70e^{-kt}}$$

---

**(b)** At $t=5$: $\theta = 70$

$$70 = 20 + 70e^{-5k} \implies 50 = 70e^{-5k} \implies e^{-5k} = \frac{5}{7}$$

$$-5k = \ln\frac{5}{7} \implies \boxed{k = \frac{1}{5}\ln\frac{7}{5} \approx 0.0673}$$

---

**(c)** At $t=20$:

$$\theta = 20 + 70e^{-20k} = 20 + 70\left(\frac{5}{7}\right)^4 = 20 + 70\cdot\frac{625}{2401}$$

$$\boxed{\theta \approx 38.2°C}$$

</details>

---

<details>
<summary>**Ex 4 — Applied example: Leaking container**</summary>

Water flows into a tank at $5\ \text{litres/min}$. It also leaks out at a rate proportional to the volume $V$ of water, with constant $k = 0.1$. Initially the tank is empty.

**(a)** Write down and solve the D.E.

**(b)** Find the long-term volume of water in the tank.

---

**(a)**

$$\frac{dV}{dt} = 5 - 0.1V$$

$$\int \frac{1}{5-0.1V}\,dV = \int dt \implies -10\ln|5-0.1V| = t + C$$

$$5 - 0.1V = Ae^{-0.1t}$$

At $t=0$: $V=0 \implies 5 = A$

$$V = \frac{5 - 5e^{-0.1t}}{0.1} = 50(1 - e^{-0.1t})$$

$$\boxed{V = 50(1 - e^{-0.1t})}$$

---

**(b)** As $t \to \infty$: $e^{-0.1t} \to 0$

$$\boxed{V \to 50\ \text{litres}}$$

이것이 **평형 부피**: 유입 속도 = 유출 속도인 상태.

</details>

---

## 3. Quick Reference — Solution Shapes

| D.E. form | Solution type | Shape |
|---|---|---|
| $\dfrac{dy}{dx} = ky$ | Exponential growth | $y = Ae^{kx}$ |
| $\dfrac{dy}{dx} = -ky$ | Exponential decay | $y = Ae^{-kx}$ |
| $\dfrac{dy}{dx} = k(L - y)$ | Approaches limit $L$ | $y = L - Ae^{-kx}$ |
| $\dfrac{dy}{dx} = ky(L-y)$ | Logistic (S-curve) | Not in C3/C4 |

::: {.callout-tip title="Exam Strategy"}
1. **Identify the type**: is it separable? What form does the right-hand side take?
2. **Separate carefully** — don't forget to move $g(y)$ to the left before integrating
3. **Integrate both sides** — check which side needs a substitution
4. **Apply initial conditions** — substitute and solve for $C$ (or $A$) immediately
5. **Answer the question** — general solution vs particular solution vs numerical value
:::
