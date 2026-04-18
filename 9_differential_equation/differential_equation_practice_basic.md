# Differential Equations — 기본문제 Mark Scheme

---

## Q01. Classify the following differential equations

> **분류 기준:**
> - **Direct integration** — $\dfrac{dy}{dx} = f(x)$ 형태, $y$가 없으므로 그냥 적분
> - **Separable** — 우변이 $f(x)\,g(y)$로 인수분해됨
> - **Separable (exponential)** — $\dfrac{dy}{dx} = ky$ 형태, 지수함수 해
> - **Applied (Decay / Cooling / Leaking)** — 실생활 모델

---

### (a) $\displaystyle\frac{dy}{dx} = (1+2y)(1-2x)$

**Type:** Separable

$$\frac{1}{1+2y}\,dy = (1-2x)\,dx$$

$$\int \frac{1}{1+2y}\,dy = \int (1-2x)\,dx \tag{M1}$$

$$\frac{1}{2}\ln|1+2y| = x - x^2 + C \tag{A1}$$

$$\boxed{\ln|1+2y| = 2x - 2x^2 + A} \tag{A1}$$

---

### (b) $\displaystyle\cos^2 x\,\frac{dy}{dx} = y^2\sin^2 x$

**Type:** Separable

$$\frac{1}{y^2}\,dy = \frac{\sin^2 x}{\cos^2 x}\,dx = \tan^2 x\,dx \tag{M1}$$

$$\int y^{-2}\,dy = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$-\frac{1}{y} = \tan x - x + C \tag{A1}$$

$$\boxed{y = \frac{-1}{\tan x - x + C}} \tag{A1}$$

---

### (c) $\displaystyle\frac{dy}{dx} = 2e^{x-y}$

**Type:** Separable ($e^{x-y} = e^x \cdot e^{-y}$)

$$e^y\,dy = 2e^x\,dx \tag{M1}$$

$$\int e^y\,dy = \int 2e^x\,dx$$

$$e^y = 2e^x + C \tag{A1}$$

$$\boxed{y = \ln(2e^x + C)} \tag{A1}$$

---

### (d) $\displaystyle\frac{dy}{dx} = \sin x\cos^2 x;\quad y = 0,\; x = \frac{\pi}{3}$

**Type:** Separable (particular solution)

$$dy = \sin x\cos^2 x\,dx \tag{M1}$$

**치환:** $u = \cos x,\; du = -\sin x\,dx$

$$y = -\int u^2\,du = -\frac{\cos^3 x}{3} + C \tag{A1}$$

**초기조건:** $x = \dfrac{\pi}{3},\; y = 0$: $\quad \cos\dfrac{\pi}{3} = \dfrac{1}{2}$

$$0 = -\frac{(1/2)^3}{3} + C \implies C = \frac{1}{24} \tag{M1}$$

$$\boxed{y = -\frac{\cos^3 x}{3} + \frac{1}{24}} \tag{A1}$$

---

### (e) $\displaystyle(1-x^2)\frac{dy}{dx} = xy + y;\quad x = 0.5,\; y = 6$

**Type:** Separable (particular solution)

**인수분해:** $xy + y = y(x+1)$, $\quad 1-x^2 = (1-x)(1+x)$

$$\frac{dy}{dx} = \frac{y(1+x)}{(1-x)(1+x)} = \frac{y}{1-x} \tag{M1}$$

$$\frac{1}{y}\,dy = \frac{1}{1-x}\,dx \tag{M1}$$

$$\ln|y| = -\ln|1-x| + C \tag{A1}$$

**초기조건:** $x = 0.5,\; y = 6$:

$$\ln 6 = -\ln(0.5) + C = \ln 2 + C \implies C = \ln 3 \tag{M1}$$

$$\ln|y| = \ln\frac{3}{|1-x|} \implies \boxed{y = \frac{3}{1-x}} \tag{A1}$$

---

## Q02. Applied Differential Equations

---

### (a) Radioactive decay

A radioactive substance decays so that its mass $m$ (grams) at time $t$ (years) satisfies

$$\frac{dm}{dt} = -0.02m$$

Initially $m = 500\text{ g}$.

**(i)** Find $m$ in terms of $t$.

**(ii)** Find the mass after 100 years.

**(iii)** Find the time at which $m = 100\text{ g}$.

---

**(i)**

$$\int \frac{1}{m}\,dm = \int -0.02\,dt \tag{M1}$$

$$\ln m = -0.02t + C \implies m = Ae^{-0.02t}$$

At $t=0$: $500 = A$ $\tag{A1}$

$$\boxed{m = 500e^{-0.02t}} \tag{A1}$$

---

**(ii)** $t = 100$:

$$m = 500e^{-2} \approx 500 \times 0.1353 \approx \boxed{67.7\text{ g}} \tag{A1}$$

---

**(iii)** $m = 100$:

$$100 = 500e^{-0.02t} \implies e^{-0.02t} = 0.2 \tag{M1}$$

$$-0.02t = \ln 0.2 \implies t = \frac{-\ln 0.2}{0.02} = \frac{\ln 5}{0.02} \tag{A1}$$

$$\boxed{t = 50\ln 5 \approx 80.5\text{ years}} \tag{A1}$$

---

### (b) Newton's Law of Cooling

A metal rod is heated to $200°C$ and left to cool in a room at $20°C$. After 10 minutes its temperature is $100°C$. The temperature $\theta°C$ at time $t$ minutes satisfies Newton's Law of Cooling.

**(i)** Show that $\theta = 20 + 180e^{-kt}$.

**(ii)** Find the exact value of $k$.

**(iii)** Find the temperature after 30 minutes, to 1 decimal place.

**(iv)** Find the time at which the rod reaches $50°C$.

---

**(i)**

$$\frac{d\theta}{dt} = -k(\theta - 20) \tag{M1}$$

$$\int \frac{1}{\theta - 20}\,d\theta = \int -k\,dt \implies \ln|\theta-20| = -kt + C$$

$$\theta - 20 = Ae^{-kt}$$

At $t=0$: $\theta = 200 \implies A = 180$ $\tag{A1}$

$$\boxed{\theta = 20 + 180e^{-kt}} \quad \checkmark \tag{A1}$$

---

**(ii)** At $t=10$: $\theta = 100$:

$$100 = 20 + 180e^{-10k} \implies e^{-10k} = \frac{80}{180} = \frac{4}{9} \tag{M1}$$

$$k = -\frac{1}{10}\ln\frac{4}{9} = \frac{1}{10}\ln\frac{9}{4} \tag{A1}$$

$$\boxed{k = \frac{\ln(9/4)}{10}} \tag{A1}$$

---

**(iii)** At $t=30$:

$$\theta = 20 + 180e^{-30k} = 20 + 180\left(\frac{4}{9}\right)^3 \tag{M1}$$

$$= 20 + 180 \times \frac{64}{729} = 20 + \frac{11520}{729} \approx 20 + 15.8 \tag{A1}$$

$$\boxed{\theta \approx 35.8°C} \tag{A1}$$

---

**(iv)** $\theta = 50$:

$$50 = 20 + 180e^{-kt} \implies e^{-kt} = \frac{30}{180} = \frac{1}{6} \tag{M1}$$

$$-kt = \ln\frac{1}{6} \implies t = \frac{\ln 6}{k} = \frac{10\ln 6}{\ln(9/4)} \tag{A1}$$

$$\boxed{t = \frac{10\ln 6}{\ln(9/4)} \approx 22.3\text{ min}} \tag{A1}$$

---

### (c) Leaking container

Liquid flows into a container at a constant rate of $3\ \text{litres/min}$. It leaks out at a rate proportional to the volume $V$ litres of liquid in the container, with constant of proportionality $k$.

When $t=0$, $V = 10$. When $t=5$, $V = 20$. The long-term volume approaches $30$ litres.

**(i)** Write down the differential equation for $V$.

**(ii)** Show that the long-term volume implies $k = 0.1$, and find $P$.

**(iii)** Solve the D.E. to find $V$ in terms of $t$.

---

**(i)**

$$\boxed{\frac{dV}{dt} = P - kV} \tag{B1}$$

---

**(ii)** At equilibrium $\dfrac{dV}{dt} = 0$: $\quad P - kV_\infty = 0 \implies V_\infty = \dfrac{P}{k} = 30$

Given $P = 3$: $\quad k = \dfrac{3}{30} = 0.1$ $\tag{M1, A1}$

$$\boxed{P = 3,\quad k = 0.1} \tag{A1}$$

---

**(iii)**

$$\frac{dV}{dt} = 3 - 0.1V \tag{M1}$$

$$\int \frac{1}{3-0.1V}\,dV = \int dt \implies -10\ln|3-0.1V| = t + C \tag{M1}$$

$$3 - 0.1V = Ae^{-0.1t} \implies V = 30 - 10Ae^{-0.1t} = 30 - Be^{-0.1t}$$

At $t=0$: $V=10 \implies B = 20$ $\tag{A1}$

**Verify:** At $t=5$: $V = 30 - 20e^{-0.5} \approx 30 - 12.1 = 17.9$ ✓ (close to 20, or $B$ found using $t=5$ data)

> **Note:** If using $t=5$, $V=20$: $20 = 30 - Be^{-0.5} \implies B = 10e^{0.5} \approx 16.5$.  
> The two conditions ($V_0 = 10$ vs $V_5 = 20$) over-determine the problem — use the one given in the specific question.

$$\boxed{V = 30 - 20e^{-0.1t}} \tag{A1}$$

---

## Q03. Mixed practice

---

### (a) $\displaystyle\frac{dy}{dx} = \frac{x+1}{y^2};\quad y = 2\text{ when }x = 0$

**Type:** Separable (particular solution)

$$y^2\,dy = (x+1)\,dx \tag{M1}$$

$$\frac{y^3}{3} = \frac{x^2}{2} + x + C \tag{A1}$$

At $x=0$, $y=2$: $\quad \dfrac{8}{3} = C$ $\tag{M1}$

$$\frac{y^3}{3} = \frac{x^2}{2} + x + \frac{8}{3}$$

$$\boxed{y = \left(\frac{3x^2}{2} + 3x + 8\right)^{1/3}} \tag{A1}$$

---

### (b) $\displaystyle x\frac{dy}{dx} = y + xy$

**Type:** Separable (인수분해 필요)

**인수분해:** $y + xy = y(1+x)$

$$x\frac{dy}{dx} = y(1+x) \implies \frac{1}{y}\,dy = \frac{1+x}{x}\,dx = \left(\frac{1}{x} + 1\right)dx \tag{M1}$$

$$\ln|y| = \ln|x| + x + C \tag{A1}$$

$$\boxed{y = Axe^x} \quad (A > 0) \tag{A1}$$

---

### (c) $\displaystyle\frac{dy}{dx} = \frac{e^y}{1+e^y}\cdot\sec^2 x$

**Type:** Separable

$$\frac{1+e^y}{e^y}\,dy = \sec^2 x\,dx \tag{M1}$$

$$\int (e^{-y} + 1)\,dy = \int \sec^2 x\,dx$$

$$-e^{-y} + y = \tan x + C \tag{A1}$$

$$\boxed{y - e^{-y} = \tan x + C} \tag{A1}$$

> **Note:** 이 경우 $y$를 명시적으로 분리할 수 없다 — implicit form이 최종 답.

---

### (d) Population growth model

A population $P$ at time $t$ years grows according to

$$\frac{dP}{dt} = 0.03P\left(1 - \frac{P}{5000}\right)$$

Initially $P = 500$.

**(i)** Show that this is equivalent to $\dfrac{dP}{dt} = \dfrac{3P(5000-P)}{500000}$.

**(ii)** Find $P$ at $t = 10$ (leave answer in exact form).

> **Hint:** Use partial fractions: $\dfrac{1}{P(5000-P)} = \dfrac{1}{5000}\!\left(\dfrac{1}{P}+\dfrac{1}{5000-P}\right)$

---

**(i)**

$$0.03P\left(1-\frac{P}{5000}\right) = 0.03P\cdot\frac{5000-P}{5000} = \frac{0.03P(5000-P)}{5000} = \frac{3P(5000-P)}{500000} \quad\checkmark \tag{B1}$$

---

**(ii)**

$$\int \frac{1}{P(5000-P)}\,dP = \int \frac{3}{500000}\,dt \tag{M1}$$

Using hint: $\displaystyle\frac{1}{5000}\int\left(\frac{1}{P}+\frac{1}{5000-P}\right)dP = \frac{3t}{500000}$

$$\frac{1}{5000}\left(\ln P - \ln(5000-P)\right) = \frac{3t}{500000} \tag{M1}$$

$$\ln\frac{P}{5000-P} = \frac{3t}{100} \tag{A1}$$

At $t=0$, $P=500$: $\quad \ln\dfrac{500}{4500} = \ln\dfrac{1}{9} = C$

$$\ln\frac{P}{5000-P} = \frac{3t}{100} + \ln\frac{1}{9}$$

$$\frac{P}{5000-P} = \frac{1}{9}e^{3t/100} \tag{A1}$$

At $t=10$: $\dfrac{P}{5000-P} = \dfrac{e^{0.3}}{9}$

$$9P = (5000-P)e^{0.3} \implies P(9 + e^{0.3}) = 5000e^{0.3}$$

$$\boxed{P = \frac{5000e^{0.3}}{9 + e^{0.3}} \approx 622} \tag{A1}$$

---

## Summary: 자주 하는 실수

| 실수 | 올바른 접근 |
|---|---|
| 양변 적분 후 상수 $C$를 양쪽에 각각 쓴다 | $C$는 **한쪽에만** — 어차피 합쳐서 하나 |
| $\ln\|y\| = \ldots$ 에서 $e$를 씌울 때 $A$ 부호를 빠트린다 | $y = e^C \cdot e^{f(x)} = Ae^{f(x)}$ — $A > 0$이지만 $\pm$를 포함하면 $A \in \mathbb{R} \setminus \{0\}$ |
| 특수해 구할 때 $C$를 결정하지 않고 답을 쓴다 | 항상 **초기조건 대입 → $C$ 계산 → 대입** 3단계 |
| Cooling 문제에서 $\theta$ 대신 $\theta - \theta_0$를 분리하지 않고 그냥 $\theta$를 분리 | $\dfrac{d\theta}{dt} = -k(\theta - \theta_0)$: $u = \theta - \theta_0$으로 치환하거나, 인수를 그대로 분리 |
| Leaking 문제에서 평형 조건 ($P - kV_\infty = 0$)을 모른다 | 장기 해 $V \to V_\infty$이면 $\dfrac{dV}{dt} \to 0$ |
