# Integration — Exam Problems Solutions (Mark Scheme)

---

## Q1(a) &nbsp; Find $\displaystyle\int 2\sin 3x\sin 2x\,dx$ &nbsp;&nbsp;&nbsp; **(4 marks)**

| | |
|---|---|
| Use product-to-sum identity: $2\sin A\sin B = \cos(A-B) - \cos(A+B)$ | M1 |
| $2\sin 3x\sin 2x = \cos(3x-2x) - \cos(3x+2x) = \cos x - \cos 5x$ | A1 |
| Integrate term by term | M1 |
| $\displaystyle\boxed{\sin x - \frac{\sin 5x}{5} + C}$ | A1 |

---

## Q1(b) &nbsp; Use $u^2 = x+1$ to evaluate $\displaystyle\int_0^3 \frac{x^2}{\sqrt{x+1}}\,dx$ &nbsp;&nbsp;&nbsp; **(8 marks)**

| | |
|---|---|
| $u^2 = x+1 \implies x = u^2-1, \quad 2u\,du = dx$ | M1 A1 |
| Change limits: $x=0 \Rightarrow u=1$; $\quad x=3 \Rightarrow u=2$ | M1 A1 |
| Substitute: $\displaystyle\int_1^2 \frac{(u^2-1)^2}{u}\cdot 2u\,du = 2\int_1^2(u^2-1)^2\,du$ | M1 |
| Expand: $2\displaystyle\int_1^2(u^4 - 2u^2 + 1)\,du$ | A1 |
| $= 2\left[\dfrac{u^5}{5} - \dfrac{2u^3}{3} + u\right]_1^2 = 2\!\left[\left(\dfrac{32}{5}-\dfrac{16}{3}+2\right)-\left(\dfrac{1}{5}-\dfrac{2}{3}+1\right)\right]$ | dM1 |
| $= 2\!\left[\dfrac{31}{5} - \dfrac{14}{3} + 1\right] = 2\cdot\dfrac{93-70+15}{15} = 2\cdot\dfrac{38}{15}$ | |
| $\boxed{\dfrac{76}{15}}$ | A1 |

---

## Q2 &nbsp; Show that $\displaystyle\int_1^2 x\ln x\,dx = 2\ln 2 - \tfrac{3}{4}$ &nbsp;&nbsp;&nbsp; **(6 marks)**

| | |
|---|---|
| IBP: $u = \ln x,\ u' = \dfrac{1}{x}; \quad v' = x,\ v = \dfrac{x^2}{2}$ | M1 A1 |
| $= \left[\dfrac{x^2}{2}\ln x\right]_1^2 - \displaystyle\int_1^2 \frac{x^2}{2}\cdot\frac{1}{x}\,dx$ | A1 |
| $= \left[\dfrac{x^2}{2}\ln x\right]_1^2 - \dfrac{1}{2}\left[\dfrac{x^2}{2}\right]_1^2$ | dM1 |
| $= \!\left(2\ln 2 - 0\right) - \dfrac{1}{2}\!\left(2 - \dfrac{1}{2}\right)$ | A1 |
| $= 2\ln 2 - \dfrac{3}{4}$ &nbsp; ✓ | A1 |

---

## Q3(a) &nbsp; Find the area of the shaded region ($y = \tfrac{1}{\sqrt{3x+1}}$, $x=1$ to $x=5$) &nbsp;&nbsp;&nbsp; **(4 marks)**

| | |
|---|---|
| $\displaystyle\int_1^5 (3x+1)^{-1/2}\,dx$ | M1 |
| $= \left[\dfrac{2}{3}\sqrt{3x+1}\right]_1^5$ | A1 |
| $= \dfrac{2}{3}\!\left(\sqrt{16} - \sqrt{4}\right) = \dfrac{2}{3}(4-2)$ | dM1 |
| $\boxed{\dfrac{4}{3}}$ | A1 |

---

## Q3(b) &nbsp; Find the volume of revolution about the $x$-axis, in the form $k\pi\ln 2$ &nbsp;&nbsp;&nbsp; **(5 marks)**

| | |
|---|---|
| $V = \pi\displaystyle\int_1^5 y^2\,dx = \pi\int_1^5 \frac{1}{3x+1}\,dx$ | M1 |
| $= \pi\left[\dfrac{\ln|3x+1|}{3}\right]_1^5$ | A1 |
| $= \dfrac{\pi}{3}\!\left(\ln 16 - \ln 4\right) = \dfrac{\pi}{3}\ln 4$ | dM1 A1 |
| $= \dfrac{\pi}{3}\cdot 2\ln 2 = \boxed{\dfrac{2}{3}\pi\ln 2}$ &nbsp;&nbsp; ($k = \dfrac{2}{3}$) | A1 |

---

## Q4 &nbsp; $x = \cos 2t,\ y = \csc t,\ 0 < t < \tfrac{\pi}{2}$; &nbsp; $P$ has $x$-coordinate $\tfrac{1}{2}$

### (a) Find $t$ at $P$ &nbsp;&nbsp;&nbsp; **(2 marks)**

| | |
|---|---|
| $\cos 2t = \dfrac{1}{2} \implies 2t = \dfrac{\pi}{3}$ | M1 |
| $\boxed{t = \dfrac{\pi}{6}}$ | A1 |

### (b) Show tangent at $P$ is $y = 2x+1$ &nbsp;&nbsp;&nbsp; **(5 marks)**

| | |
|---|---|
| $\dfrac{dx}{dt} = -2\sin 2t, \quad \dfrac{dy}{dt} = -\csc t\cot t$ | B1 B1 |
| $\dfrac{dy}{dx} = \dfrac{-\csc t\cot t}{-2\sin 2t} = \dfrac{\csc t\cot t}{2\sin 2t}$ | M1 |
| At $t = \dfrac{\pi}{6}$: $\csc\dfrac{\pi}{6} = 2,\ \cot\dfrac{\pi}{6} = \sqrt{3},\ \sin\dfrac{\pi}{3} = \dfrac{\sqrt{3}}{2}$ | |
| $\dfrac{dy}{dx} = \dfrac{2\cdot\sqrt{3}}{2\cdot\dfrac{\sqrt{3}}{2}\cdot 2}$... $= \dfrac{2\sqrt{3}}{\sqrt{3}} = 2$ | A1 |
| Point: $y = \csc\dfrac{\pi}{6} = 2$, $x = \dfrac{1}{2}$. &nbsp; $y-2 = 2\!\left(x-\dfrac{1}{2}\right) \implies y = 2x+1$ &nbsp; ✓ | A1 |

### (c) Show area $= \displaystyle\int_{\pi/6}^{\pi/4} k\cos t\,dt$, find $k$ &nbsp;&nbsp;&nbsp; **(4 marks)**

| | |
|---|---|
| Area $= \displaystyle\int y\,dx = \int y\,\frac{dx}{dt}\,dt$; &nbsp; when $x=0$: $\cos 2t=0 \Rightarrow t=\dfrac{\pi}{4}$ | M1 |
| $= \displaystyle\int_{\pi/4}^{\pi/6}\csc t\cdot(-2\sin 2t)\,dt = \int_{\pi/6}^{\pi/4} 2\csc t\sin 2t\,dt$ | A1 |
| Use $\sin 2t = 2\sin t\cos t$: $\quad 2\csc t\cdot 2\sin t\cos t = 4\cos t$ | M1 A1 |
| $\displaystyle\boxed{\int_{\pi/6}^{\pi/4} 4\cos t\,dt}$ &nbsp;&nbsp; ($k = 4$) | A1 |

### (d) Find the exact area &nbsp;&nbsp;&nbsp; **(3 marks)**

| | |
|---|---|
| $\left[4\sin t\right]_{\pi/6}^{\pi/4}$ | M1 |
| $= 4\!\left(\dfrac{\sqrt{2}}{2} - \dfrac{1}{2}\right)$ | A1 |
| $\boxed{2\sqrt{2} - 2}$ | A1 |

---

## Q5 &nbsp; Use $x = 2\tan u$ to show $\displaystyle\int_0^2 \frac{x^2}{x^2+4}\,dx = \tfrac{1}{2}(4-\pi)$ &nbsp;&nbsp;&nbsp; **(8 marks)**

| | |
|---|---|
| $x = 2\tan u \implies dx = 2\sec^2 u\,du, \quad x^2+4 = 4\sec^2 u$ | M1 A1 |
| Change limits: $x=0 \Rightarrow u=0$; &nbsp; $x=2 \Rightarrow \tan u=1 \Rightarrow u=\dfrac{\pi}{4}$ | M1 A1 |
| $\displaystyle\int_0^{\pi/4}\frac{4\tan^2 u}{4\sec^2 u}\cdot 2\sec^2 u\,du = \int_0^{\pi/4} 2\tan^2 u\,du$ | A1 |
| Use $\tan^2 u = \sec^2 u - 1$: $\quad 2\displaystyle\int_0^{\pi/4}(\sec^2 u-1)\,du$ | M1 |
| $= 2\left[\tan u - u\right]_0^{\pi/4} = 2\!\left(1 - \dfrac{\pi}{4}\right)$ | A1 |
| $= 2 - \dfrac{\pi}{2} = \dfrac{1}{2}(4-\pi)$ &nbsp; ✓ | A1 |

---

## Q6 &nbsp; $f(x) = \dfrac{15-17x}{(2+x)(1-3x)^2}$

### (a) Find $A$, $B$, $C$ &nbsp;&nbsp;&nbsp; **(4 marks)**

$$f(x) = \frac{A}{2+x} + \frac{B}{1-3x} + \frac{C}{(1-3x)^2}$$

| | |
|---|---|
| $15-17x \equiv A(1-3x)^2 + B(2+x)(1-3x) + C(2+x)$ | M1 |
| $x = -2$: $49 = 49A \implies A = 1$ | A1 |
| $x = \dfrac{1}{3}$: $\dfrac{28}{3} = C\cdot\dfrac{7}{3} \implies C = 4$ | A1 |
| Coeff. of $x^2$: $9A - 3B = 0 \implies B = 3$ | A1 |

$$\boxed{A=1,\quad B=3,\quad C=4}$$

### (b) Find $\displaystyle\int_{-1}^0 f(x)\,dx$ in the form $p + \ln q$ &nbsp;&nbsp;&nbsp; **(7 marks)**

| | |
|---|---|
| $\displaystyle\int\frac{1}{2+x}\,dx = \ln|2+x|$ | B1 |
| $\displaystyle\int\frac{3}{1-3x}\,dx = -\ln|1-3x|$ | B1 |
| $\displaystyle\int\frac{4}{(1-3x)^2}\,dx = \frac{4}{3(1-3x)}$ | M1 A1 |
| $= \left[\ln|2+x| - \ln|1-3x| + \dfrac{4}{3(1-3x)}\right]_{-1}^0$ | dM1 |
| At $x=0$: $\ln 2 - \ln 1 + \dfrac{4}{3} = \ln 2 + \dfrac{4}{3}$ | |
| At $x=-1$: $\ln 1 - \ln 4 + \dfrac{4}{12} = -\ln 4 + \dfrac{1}{3}$ | A1 |
| $= \left(\ln 2 + \dfrac{4}{3}\right) - \left(-\ln 4 + \dfrac{1}{3}\right) = \ln 2 + \ln 4 + 1 = \ln 8 + 1$ | |
| $\boxed{1 + \ln 8}$ &nbsp;&nbsp; ($p=1,\ q=8$) | A1 |

---

## Q7(a) &nbsp; Find $\displaystyle\int\tan^2 x\,dx$ &nbsp;&nbsp;&nbsp; **(3 marks)**

| | |
|---|---|
| Use identity: $\tan^2 x = \sec^2 x - 1$ | M1 |
| $= \displaystyle\int(\sec^2 x - 1)\,dx$ | A1 |
| $\boxed{\tan x - x + C}$ | A1 |

---

## Q7(b) &nbsp; Show $\displaystyle\int\tan x\,dx = \ln|\sec x| + c$ &nbsp;&nbsp;&nbsp; **(4 marks)**

| | |
|---|---|
| Write $\displaystyle\int\tan x\,dx = \int\frac{\sin x}{\cos x}\,dx$ | M1 |
| Let $u = \cos x,\ du = -\sin x\,dx$ | M1 |
| $= \displaystyle\int\frac{-du}{u} = -\ln|u| + c = -\ln|\cos x| + c$ | A1 |
| $= \ln|\cos x|^{-1} + c = \ln|\sec x| + c$ &nbsp; ✓ | A1 |

---

## Q7(c) &nbsp; Show volume $= \tfrac{1}{18}\pi^2(6\sqrt{3}-\pi) - \pi\ln 2$ &nbsp; ($y = \sqrt{x}\tan x$, rotated about $x$-axis to $x = \tfrac{\pi}{3}$) &nbsp;&nbsp;&nbsp; **(6 marks)**

| | |
|---|---|
| $V = \pi\displaystyle\int_0^{\pi/3} y^2\,dx = \pi\int_0^{\pi/3} x\tan^2 x\,dx$ | M1 |
| Use $\tan^2 x = \sec^2 x - 1$: $\quad \pi\displaystyle\int_0^{\pi/3}(x\sec^2 x - x)\,dx$ | M1 |
| IBP on $\displaystyle\int x\sec^2 x\,dx$: $u=x,\ v'=\sec^2 x \implies x\tan x - \int\tan x\,dx = x\tan x - \ln|\sec x|$ | M1 A1 |
| $\pi\left[x\tan x - \ln|\sec x| - \dfrac{x^2}{2}\right]_0^{\pi/3}$ | dM1 |
| At $x=\dfrac{\pi}{3}$: $\dfrac{\pi}{3}\cdot\sqrt{3} - \ln 2 - \dfrac{\pi^2}{18}$ &nbsp;&nbsp; (since $\tan\dfrac{\pi}{3}=\sqrt{3}$, $\sec\dfrac{\pi}{3}=2$) | |
| At $x=0$: $0 - 0 - 0 = 0$ | |
| $V = \pi\!\left(\dfrac{\pi\sqrt{3}}{3} - \ln 2 - \dfrac{\pi^2}{18}\right) = \dfrac{\pi^2\sqrt{3}}{3} - \pi\ln 2 - \dfrac{\pi^3}{18}$ | |
| $= \dfrac{6\pi^2\sqrt{3}}{18} - \dfrac{\pi^3}{18} - \pi\ln 2 = \dfrac{\pi^2(6\sqrt{3}-\pi)}{18} - \pi\ln 2$ | |
| $= \dfrac{1}{18}\pi^2(6\sqrt{3}-\pi) - \pi\ln 2$ &nbsp; ✓ | A1 |
