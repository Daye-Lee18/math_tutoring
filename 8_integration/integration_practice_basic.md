# Integration — 기본문제 Mark Scheme

---

## Q01. Identify the types of the following integration

> **Type 분류 기준:**
> - **Standard** — 공식 직접 적용
> - **Expand** — 전개 후 Standard
> - **Trig identity** — 삼각 항등식으로 변환
> - **Reverse chain rule** — $\int f'(x)\cdot g(f(x))\,dx$ 형태
> - **Substitution** — $u$ 치환
> - **Partial fractions** — 부분분수
> - **By parts** — 부분적분 $\int u\,dv = uv - \int v\,du$
> - **Poly division + PF** — 분자 차수 ≥ 분모 → 나눗셈 먼저

---

### (a) $\displaystyle\int \cos x(1+\csc^2 x)\,dx$

**Type:** Expand → Standard + Substitution $(u = \sin x)$

$$= \int \cos x\,dx + \int \frac{\cos x}{\sin^2 x}\,dx \tag{M1}$$

$$= \sin x + \int u^{-2}\,du \quad (u=\sin x,\;du=\cos x\,dx) \tag{M1}$$

$$\boxed{= \sin x - \csc x + C} \tag{A1}$$

---

### (b) $\displaystyle\int (e^x+1)^2\,dx$

**Type:** Expand → Standard

$$= \int (e^{2x}+2e^x+1)\,dx \tag{M1}$$

$$\boxed{= \frac{e^{2x}}{2} + 2e^x + x + C} \tag{A1}$$

---

### (c) $\displaystyle\int \frac{3-5x}{(1-x)(2-3x)}\,dx$

**Type:** Partial Fractions

$$\frac{3-5x}{(1-x)(2-3x)} = \frac{A}{1-x} + \frac{B}{2-3x} \tag{M1}$$

$x=1$: $-2 = A(-1) \Rightarrow A=2$

$x=\tfrac{2}{3}$: $-\tfrac{1}{3} = B\cdot\tfrac{1}{3} \Rightarrow B=-1$ $\tag{A1}$

$$\int \left[\frac{2}{1-x} - \frac{1}{2-3x}\right]dx \tag{M1}$$

$$\boxed{= -2\ln|1-x| + \tfrac{1}{3}\ln|2-3x| + C} \tag{A1}$$

---

### (d) $\displaystyle\int \frac{\cos 2x}{3+\sin 2x}\,dx$

**Type:** Reverse chain rule — $\dfrac{f'(x)}{f(x)}$ form

$$u = 3+\sin 2x,\quad du = 2\cos 2x\,dx \tag{M1}$$

$$= \frac{1}{2}\int \frac{du}{u}$$

$$\boxed{= \frac{1}{2}\ln|3+\sin 2x| + C} \tag{A1}$$

---

### (e) $\displaystyle\int \frac{\cos 2x}{\cos^2 x}\,dx$

**Type:** Trig identity — $\cos 2x = 2\cos^2 x - 1$

$$= \int \frac{2\cos^2 x - 1}{\cos^2 x}\,dx = \int (2 - \sec^2 x)\,dx \tag{M1}$$

$$\boxed{= 2x - \tan x + C} \tag{A1}$$

---

### (f) $\displaystyle\int \sec^2 x(1-\cot^2 x)\,dx$

**Type:** Trig identity — $\sec^2 x \cdot \cot^2 x = \csc^2 x$

$$= \int \sec^2 x\,dx - \int \underbrace{\sec^2 x \cdot \cot^2 x}_{=\,\csc^2 x}\,dx \tag{M1}$$

$$\boxed{= \tan x + \cot x + C} \tag{A1}$$

---

### (g) $\displaystyle\int \cos x\, e^{\sin x}\,dx$

**Type:** Reverse chain rule — $f'(x)\cdot e^{f(x)}$

$$u = \sin x,\quad du = \cos x\,dx \tag{M1}$$

$$= \int e^u\,du$$

$$\boxed{= e^{\sin x} + C} \tag{A1}$$

---

### (h) $\displaystyle\int \frac{x}{\sin^2 x}\,dx$

**Type:** By parts — $\int x\,\csc^2 x\,dx$

$$u = x,\quad dv = \csc^2 x\,dx \;\Rightarrow\; v = -\cot x \tag{M1}$$

$$= -x\cot x + \int \cot x\,dx \tag{A1}$$

$$\boxed{= -x\cot x + \ln|\sin x| + C} \tag{A1}$$

---

### (i) $\displaystyle\int \sin^2 x\cos^2 x\,dx$

**Type:** Trig identity — Double angle twice

$$\sin^2 x\cos^2 x = \tfrac{1}{4}\sin^2 2x = \frac{1}{4}\cdot\frac{1-\cos 4x}{2} = \frac{1-\cos 4x}{8} \tag{M1}$$

$$\boxed{= \frac{x}{8} - \frac{\sin 4x}{32} + C} \tag{A1}$$

---

### (j) $\displaystyle\int \frac{x^3+2x^2+2}{x^2+x}\,dx$

**Type:** Polynomial division + Partial Fractions

**Division:** $x^3+2x^2+2 = (x+1)(x^2+x) + (-x+2)$

$$\frac{x^3+2x^2+2}{x^2+x} = x+1+\frac{-x+2}{x(x+1)} \tag{M1}$$

**Partial fractions:** $\dfrac{-x+2}{x(x+1)} = \dfrac{A}{x}+\dfrac{B}{x+1}$

$x=0$: $A=2$; $\quad x=-1$: $B=-3$ $\tag{A1}$

$$\int \left(x+1+\frac{2}{x}-\frac{3}{x+1}\right)dx \tag{M1}$$

$$\boxed{= \frac{x^2}{2} + x + 2\ln|x| - 3\ln|x+1| + C} \tag{A1}$$

---

### (k) $\displaystyle\int \frac{\sin x\cos x}{\sqrt{\cos 2x+3}}\,dx$

**Type:** Substitution — $u = \cos 2x+3$

$$\sin x\cos x = \tfrac{1}{2}\sin 2x, \qquad \frac{d}{dx}(\cos 2x) = -2\sin 2x \tag{M1}$$

$$u = \cos 2x+3,\quad du = -2\sin 2x\,dx \;\Rightarrow\; \sin x\cos x\,dx = -\tfrac{1}{4}du$$

$$= -\frac{1}{4}\int u^{-1/2}\,du \tag{M1}$$

$$\boxed{= -\frac{1}{2}\sqrt{\cos 2x+3} + C} \tag{A1}$$

---

### (l) $\displaystyle\int \sin x\ln(\sec x)\,dx$

**Type:** By parts — $u = \ln(\sec x)$, $dv = \sin x\,dx$

$$u = \ln(\sec x),\quad du = \tan x\,dx;\qquad v = -\cos x \tag{M1}$$

$$= -\cos x\ln(\sec x) + \int \cos x\cdot\tan x\,dx \tag{A1}$$

$$= -\cos x\ln(\sec x) + \int \sin x\,dx \tag{M1}$$

$$\boxed{= -\cos x\ln(\sec x) - \cos x + C} \tag{A1}$$

> **Note:** $\ln(\sec x) = -\ln(\cos x)$이므로 $\cos x\ln(\cos x) - \cos x + C$로도 쓸 수 있음.

---

### (m) $\displaystyle\int x\sqrt{x+4}\,dx$

**Type:** Substitution — $u = x+4$

$$u = x+4,\quad x = u-4,\quad dx = du \tag{M1}$$

$$= \int (u-4)\sqrt{u}\,du = \int (u^{3/2}-4u^{1/2})\,du \tag{A1}$$

$$\boxed{= \frac{2}{5}(x+4)^{5/2} - \frac{8}{3}(x+4)^{3/2} + C} \tag{A1}$$

---

### (n) $\displaystyle\int \sec x\tan x\sqrt{\sec x+2}\,dx$

**Type:** Substitution — $u = \sec x+2$

$$u = \sec x+2,\quad du = \sec x\tan x\,dx \tag{M1}$$

$$= \int \sqrt{u}\,du = \frac{2}{3}u^{3/2}$$

$$\boxed{= \frac{2}{3}(\sec x+2)^{3/2} + C} \tag{A1}$$

---

## Q02. Evaluate the following

---

### (a) $\displaystyle\int_0^5 x\sqrt{x+4}\,dx$

From Q01(m): $u=x+4$; when $x=0$, $u=4$; when $x=5$, $u=9$.

$$= \left[\frac{2}{5}u^{5/2} - \frac{8}{3}u^{3/2}\right]_4^9 \tag{M1}$$

At $u=9$: $\dfrac{2}{5}(243) - \dfrac{8}{3}(27) = \dfrac{486}{5} - 72 = \dfrac{126}{5}$

At $u=4$: $\dfrac{2}{5}(32) - \dfrac{8}{3}(8) = \dfrac{64}{5} - \dfrac{64}{3} = \dfrac{192-320}{15} = -\dfrac{128}{15}$ $\tag{A1}$

$$= \frac{126}{5} - \left(-\frac{128}{15}\right) = \frac{378}{15} + \frac{128}{15}$$

$$\boxed{= \frac{506}{15}} \tag{A1}$$

---

### (b) $\displaystyle\int_0^{\pi/3} \sec x\tan x\sqrt{\sec x+2}\,dx$

From Q01(n): $u=\sec x+2$; when $x=0$, $u=3$; when $x=\pi/3$, $u=4$.

$$= \int_3^4 \sqrt{u}\,du = \left[\frac{2}{3}u^{3/2}\right]_3^4 \tag{M1}$$

$$= \frac{2}{3}(8) - \frac{2}{3}(3\sqrt{3}) \tag{A1}$$

$$\boxed{= \frac{16}{3} - 2\sqrt{3}} \tag{A1}$$

---

### (c) $\displaystyle\int_2^5 \frac{1}{1+\sqrt{x-1}}\,dx;\quad u^2 = x-1$

$u^2 = x-1 \;\Rightarrow\; x = u^2+1$, $dx = 2u\,du$, $\sqrt{x-1} = u$

When $x=2$: $u=1$; when $x=5$: $u=2$. $\tag{M1}$

$$= \int_1^2 \frac{2u}{1+u}\,du = 2\int_1^2 \left(1 - \frac{1}{1+u}\right)du \tag{M1}$$

$$= 2\Big[u - \ln|1+u|\Big]_1^2 = 2\big[(2-\ln 3)-(1-\ln 2)\big] \tag{A1}$$

$$\boxed{= 2 + 2\ln\frac{2}{3} = 2 - 2\ln\frac{3}{2}} \tag{A1}$$

---

### (d) $\displaystyle\int_0^{\ln 2} xe^{2x}\,dx$

**By parts:** $u=x$, $dv=e^{2x}dx \;\Rightarrow\; v=\dfrac{e^{2x}}{2}$

$$= \left[\frac{xe^{2x}}{2}\right]_0^{\ln 2} - \int_0^{\ln 2}\frac{e^{2x}}{2}\,dx \tag{M1}$$

$$= \frac{\ln 2\cdot e^{2\ln 2}}{2} - \left[\frac{e^{2x}}{4}\right]_0^{\ln 2} \tag{A1}$$

$$= \frac{4\ln 2}{2} - \left(\frac{4}{4} - \frac{1}{4}\right) = 2\ln 2 - \frac{3}{4} \tag{A1}$$

$$\boxed{= 2\ln 2 - \frac{3}{4}} \tag{A1}$$

---

### (e) $\displaystyle\int_1^2 \frac{1}{(x+1)(2x-1)}\,dx$

**Partial fractions:**

$$\frac{1}{(x+1)(2x-1)} = \frac{A}{x+1} + \frac{B}{2x-1}$$

$x=-1$: $1=A(-3) \Rightarrow A=-\tfrac{1}{3}$; $\quad x=\tfrac{1}{2}$: $1=B\cdot\tfrac{3}{2} \Rightarrow B=\tfrac{2}{3}$ $\tag{M1, A1}$

$$= \left[-\frac{1}{3}\ln|x+1| + \frac{1}{3}\ln|2x-1|\right]_1^2 \tag{M1}$$

$$= \frac{1}{3}\Big[\ln|2x-1| - \ln|x+1|\Big]_1^2$$

At $x=2$: $\ln 3 - \ln 3 = 0$; $\quad$ At $x=1$: $\ln 1 - \ln 2 = -\ln 2$ $\tag{A1}$

$$\boxed{= \frac{\ln 2}{3}} \tag{A1}$$

---

### (f) $\displaystyle\int_0^{\pi/3} \sin x\ln(\sec x)\,dx$

From Q01(l): antiderivative $= -\cos x\ln(\sec x) - \cos x$

$$= \Big[-\cos x\ln(\sec x) - \cos x\Big]_0^{\pi/3} \tag{M1}$$

At $x=\tfrac{\pi}{3}$: $\cos\tfrac{\pi}{3}=\tfrac{1}{2}$, $\sec\tfrac{\pi}{3}=2$ $\Rightarrow$ $-\tfrac{1}{2}\ln 2 - \tfrac{1}{2}$

At $x=0$: $\cos 0=1$, $\ln(\sec 0)=0$ $\Rightarrow$ $0 - 1 = -1$ $\tag{A1, A1}$

$$= \left(-\frac{\ln 2}{2} - \frac{1}{2}\right) - (-1) = \frac{1}{2} - \frac{\ln 2}{2}$$

$$\boxed{= \frac{1-\ln 2}{2}} \tag{A1}$$

---

## Q03. Volume of solid of revolution — $y = 2x^{1/2}\sin x$

The shaded region ($0 \leq x \leq \dfrac{\pi}{2}$) is rotated $2\pi$ about the $x$-axis.

$$V = \pi\int_0^{\pi/2} y^2\,dx = \pi\int_0^{\pi/2} 4x\sin^2 x\,dx \tag{M1}$$

**Power reduction:** $\sin^2 x = \dfrac{1-\cos 2x}{2}$

$$V = 4\pi\int_0^{\pi/2} x\cdot\frac{1-\cos 2x}{2}\,dx = 2\pi\int_0^{\pi/2}(x - x\cos 2x)\,dx \tag{M1}$$

**First term:**

$$\int_0^{\pi/2} x\,dx = \left[\frac{x^2}{2}\right]_0^{\pi/2} = \frac{\pi^2}{8} \tag{A1}$$

**Second term** — by parts: $u=x$, $dv=\cos 2x\,dx \;\Rightarrow\; v=\dfrac{\sin 2x}{2}$

$$\int_0^{\pi/2} x\cos 2x\,dx = \left[\frac{x\sin 2x}{2}\right]_0^{\pi/2} - \int_0^{\pi/2}\frac{\sin 2x}{2}\,dx \tag{M1}$$

$$= 0 - \left[-\frac{\cos 2x}{4}\right]_0^{\pi/2} = -\left(\frac{1}{4}+\frac{1}{4}\right)... $$

$$= 0 - \left(-\frac{\cos\pi}{4} + \frac{\cos 0}{4}\right) = -\left(\frac{1}{4} + \frac{1}{4}\right) = -\frac{1}{2} \tag{A1}$$

**Combining:**

$$V = 2\pi\left[\frac{\pi^2}{8} - \left(-\frac{1}{2}\right)\right] = 2\pi\left(\frac{\pi^2}{8}+\frac{1}{2}\right) \tag{M1}$$

$$\boxed{V = \frac{\pi^3}{4} + \pi = \frac{\pi(\pi^2+4)}{4}} \tag{A1}$$

---

## Q04. Parametric curve $x=t(1+t)$, $y=\dfrac{1}{1+t}$

Region $R$: bounded by $C$, the $x$-axis, $x=0$, $x=2$.

**Find parameter range:**
- $x=0$: $t(1+t)=0 \Rightarrow t=0$ (taking $t \geq 0$)
- $x=2$: $t^2+t-2=0 \Rightarrow (t-1)(t+2)=0 \Rightarrow t=1$

$$\frac{dx}{dt} = 1+2t \tag{B1}$$

---

### (a) Exact area of $R$

$$A = \int_0^2 y\,dx = \int_0^1 \frac{1}{1+t}\cdot(1+2t)\,dt \tag{M1}$$

**Long division:** $\dfrac{1+2t}{1+t} = 2 - \dfrac{1}{1+t}$ $\tag{M1}$

$$= \Big[2t - \ln|1+t|\Big]_0^1 \tag{A1}$$

$$= (2-\ln 2) - 0$$

$$\boxed{A = 2 - \ln 2} \tag{A1}$$

---

### (b) Exact volume of solid when $R$ rotated $2\pi$ about $x$-axis

$$V = \pi\int_0^2 y^2\,dx = \pi\int_0^1 \frac{1}{(1+t)^2}\cdot(1+2t)\,dt \tag{M1}$$

**Substitution:** $u=1+t$, $du=dt$; $1+2t = 2u-1$; limits: $u=1\to 2$

$$= \pi\int_1^2 \frac{2u-1}{u^2}\,du = \pi\int_1^2\left(\frac{2}{u} - \frac{1}{u^2}\right)du \tag{M1}$$

$$= \pi\left[2\ln u + \frac{1}{u}\right]_1^2 \tag{A1}$$

$$= \pi\left[\left(2\ln 2 + \frac{1}{2}\right) - \left(0+1\right)\right] \tag{A1}$$

$$\boxed{V = \pi\!\left(2\ln 2 - \frac{1}{2}\right)} \tag{A1}$$
