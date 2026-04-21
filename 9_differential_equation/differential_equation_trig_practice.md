# Differential Equations — 삼각함수 집중 연습

> **대상:** 삼각함수 적분이 포함된 DE에서 막히는 학생  
> **구성:** 유형 A~E, 총 20문제 + 전체 풀이  
> **필수 선행지식:** $\tan^2 x = \sec^2 x - 1$, $\sin^2 x = \frac{1-\cos 2x}{2}$, $\cos^2 x = \frac{1+\cos 2x}{2}$, $\sin x\cos x = \frac{\sin 2x}{2}$

---

## 필수 적분 공식 — 이것만 외우면 된다

| 적분 | 결과 | 핵심 변환 |
|---|---|---|
| $\int \sec^2 x\,dx$ | $\tan x + C$ | — |
| $\int \tan^2 x\,dx$ | $\tan x - x + C$ | $\tan^2 x = \sec^2 x - 1$ 먼저 |
| $\int \sin^2 x\,dx$ | $\frac{x}{2} - \frac{\sin 2x}{4} + C$ | $\sin^2 x = \frac{1-\cos 2x}{2}$ 먼저 |
| $\int \cos^2 x\,dx$ | $\frac{x}{2} + \frac{\sin 2x}{4} + C$ | $\cos^2 x = \frac{1+\cos 2x}{2}$ 먼저 |
| $\int \tan x\,dx$ | $\ln\|\sec x\| + C$ | $= -\ln\|\cos x\| + C$ |
| $\int \sin x\cos x\,dx$ | $\frac{1}{2}\sin^2 x + C$ | $= -\frac{1}{4}\cos 2x + C$ |
| $\int \cot x\,dx$ | $\ln\|\sin x\| + C$ | |
| $\int \frac{1}{\sin x\cos x}\,dx$ | $\ln\|\tan x\| + C$ | $\frac{1}{\sin x\cos x} = \frac{2}{\sin 2x} = 2\csc 2x$ |

---

## Type A — 직접 적분형 (Direct Integration)

> $\frac{dy}{dx} = f(x)$ 형태. $y$가 없으므로 우변을 그냥 적분.  
> **막히는 포인트:** $\tan^2 x$, $\sin^2 x$는 그대로 적분이 안 된다 — 항등식으로 변환 먼저.

---

### A1. $\dfrac{dy}{dx} = \tan^2 x$

**풀이**

$\tan^2 x = \sec^2 x - 1$ 변환:

$$y = \int \tan^2 x\,dx = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$\boxed{y = \tan x - x + C} \tag{A1}$$

---

### A2. $\dfrac{dy}{dx} = \sin^2 x$

**풀이**

$\sin^2 x = \dfrac{1-\cos 2x}{2}$ 변환:

$$y = \int \frac{1-\cos 2x}{2}\,dx \tag{M1}$$

$$\boxed{y = \frac{x}{2} - \frac{\sin 2x}{4} + C} \tag{A1}$$

---

### A3. $\dfrac{dy}{dx} = \cos^2 x,\quad y = 1 \text{ when } x = 0$

**풀이**

$\cos^2 x = \dfrac{1+\cos 2x}{2}$ 변환:

$$y = \int \frac{1+\cos 2x}{2}\,dx = \frac{x}{2} + \frac{\sin 2x}{4} + C \tag{M1 A1}$$

초기조건 $x=0,\ y=1$:

$$1 = 0 + 0 + C \implies C = 1 \tag{M1}$$

$$\boxed{y = \frac{x}{2} + \frac{\sin 2x}{4} + 1} \tag{A1}$$

---

### A4. $\dfrac{dy}{dx} = 3\tan^2 x + 2\sec^2 x$

**풀이**

$$y = \int (3\tan^2 x + 2\sec^2 x)\,dx = \int (3(\sec^2 x - 1) + 2\sec^2 x)\,dx \tag{M1}$$

$$= \int (5\sec^2 x - 3)\,dx$$

$$\boxed{y = 5\tan x - 3x + C} \tag{A1}$$

---

### A5. $\dfrac{dy}{dx} = \sin^2 x \cdot \cos^2 x$

**풀이**

$\sin^2 x\cos^2 x = \dfrac{\sin^2 2x}{4} = \dfrac{1-\cos 4x}{8}$ 변환:

$$y = \int \frac{1-\cos 4x}{8}\,dx \tag{M1}$$

$$\boxed{y = \frac{x}{8} - \frac{\sin 4x}{32} + C} \tag{A1}$$

> **유도:** $\sin^2 x \cos^2 x = (\sin x \cos x)^2 = \left(\frac{\sin 2x}{2}\right)^2 = \frac{\sin^2 2x}{4}$, 그 다음 $\sin^2 2x = \frac{1-\cos 4x}{2}$.

---

## Type B — Separable, $x$ 쪽에 삼각함수 항등식 필요

> 변수분리 후 $x$ 쪽 적분에 항등식 변환이 필요한 유형.  
> **막히는 포인트:** 분리까지는 잘 하는데, $\int \tan^2 x\,dx$ 또는 $\int \sin^2 x\,dx$에서 멈춤.

---

### B1. $\dfrac{dy}{dx} = y\tan^2 x$

**풀이**

변수분리:

$$\frac{dy}{y} = \tan^2 x\,dx = (\sec^2 x - 1)\,dx \tag{M1}$$

$$\int \frac{dy}{y} = \int (\sec^2 x - 1)\,dx$$

$$\ln|y| = \tan x - x + C \tag{A1}$$

$$\boxed{y = Ae^{\tan x - x}} \tag{A1}$$

---

### B2. $\cos^2 x\,\dfrac{dy}{dx} = y^2\sin^2 x$

> *(core_concepts의 예제 변형 — 반드시 숙지)*

**풀이**

변수분리:

$$\frac{dy}{y^2} = \frac{\sin^2 x}{\cos^2 x}\,dx = \tan^2 x\,dx \tag{M1}$$

$$\int y^{-2}\,dy = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$-\frac{1}{y} = \tan x - x + C \tag{A1}$$

$$\boxed{y = \frac{-1}{\tan x - x + C}} \tag{A1}$$

---

### B3. $\dfrac{dy}{dx} = \dfrac{y\sin^2 x}{\cos^2 x},\quad y = 2 \text{ when } x = 0$

**풀이**

$\dfrac{\sin^2 x}{\cos^2 x} = \tan^2 x = \sec^2 x - 1$이므로:

$$\frac{dy}{y} = (\sec^2 x - 1)\,dx \tag{M1}$$

$$\ln|y| = \tan x - x + C \tag{A1}$$

초기조건 $x=0,\ y=2$:

$$\ln 2 = 0 - 0 + C \implies C = \ln 2 \tag{M1}$$

$$\ln|y| = \tan x - x + \ln 2$$

$$\boxed{y = 2e^{\tan x - x}} \tag{A1}$$

---

### B4. $\sec^2 x\,\dfrac{dy}{dx} = y$

**풀이**

변수분리:

$$\frac{dy}{y} = \frac{dx}{\sec^2 x} = \cos^2 x\,dx = \frac{1+\cos 2x}{2}\,dx \tag{M1}$$

$$\ln|y| = \frac{x}{2} + \frac{\sin 2x}{4} + C \tag{A1}$$

$$\boxed{y = Ae^{\,x/2\;+\;\sin 2x/4}} \tag{A1}$$

---

### B5. $\dfrac{dy}{dx} = y^2\sin^2 x,\quad y = 1 \text{ when } x = \dfrac{\pi}{2}$

**풀이**

변수분리:

$$\frac{dy}{y^2} = \sin^2 x\,dx = \frac{1-\cos 2x}{2}\,dx \tag{M1}$$

$$-\frac{1}{y} = \frac{x}{2} - \frac{\sin 2x}{4} + C \tag{A1}$$

초기조건 $x = \dfrac{\pi}{2},\ y = 1$: $\quad \sin\pi = 0$이므로

$$-1 = \frac{\pi}{4} - 0 + C \implies C = -1 - \frac{\pi}{4} \tag{M1}$$

$$-\frac{1}{y} = \frac{x}{2} - \frac{\sin 2x}{4} - 1 - \frac{\pi}{4}$$

$$\boxed{y = \dfrac{-1}{\dfrac{x}{2} - \dfrac{\sin 2x}{4} - 1 - \dfrac{\pi}{4}}} \tag{A1}$$

---

## Type C — Separable, $y$ 쪽에 삼각함수

> 변수분리 후 $y$를 포함한 삼각함수 적분이 나오는 유형.  
> $\int \sin y\,dy$, $\int \cos y\,dy$, $\int \sec^2 y\,dy$ 등.

---

### C1. $\dfrac{dy}{dx} = \cos y\cdot\sec^2 x,\quad y = \dfrac{\pi}{4} \text{ when } x = 0$

**풀이**

변수분리:

$$\frac{dy}{\cos y} = \sec^2 x\,dx \implies \sec y\,dy = \sec^2 x\,dx \tag{M1}$$

$$\int \sec y\,dy = \int \sec^2 x\,dx$$

$$\ln|\sec y + \tan y| = \tan x + C \tag{A1}$$

초기조건 $x=0,\ y=\dfrac{\pi}{4}$: $\;\sec\frac{\pi}{4} = \sqrt{2},\; \tan\frac{\pi}{4} = 1$

$$\ln(\sqrt{2}+1) = 0 + C \implies C = \ln(\sqrt{2}+1) \tag{M1}$$

$$\boxed{\ln|\sec y + \tan y| = \tan x + \ln(\sqrt{2}+1)} \tag{A1}$$

---

### C2. $\cos^2 y\,\dfrac{dy}{dx} = e^x$

**풀이**

변수분리:

$$\cos^2 y\,dy = e^x\,dx \tag{M1}$$

$$\int \cos^2 y\,dy = \int e^x\,dx$$

$$\int \frac{1+\cos 2y}{2}\,dy = e^x + C$$

$$\frac{y}{2} + \frac{\sin 2y}{4} = e^x + C \tag{A1}$$

$$\boxed{\frac{y}{2} + \frac{\sin 2y}{4} = e^x + C} \tag{A1}$$

> $y$를 explicit하게 분리할 수 없다 — implicit form이 최종 답.

---

### C3. $\dfrac{dy}{dx} = \tan^2 y\cdot x^2$

**풀이**

변수분리:

$$\frac{dy}{\tan^2 y} = x^2\,dx \implies \frac{\cos^2 y}{\sin^2 y}\,dy = x^2\,dx \tag{M1}$$

$$\int \cot^2 y\,dy = \int x^2\,dx$$

$\cot^2 y = \csc^2 y - 1$이므로:

$$\int (\csc^2 y - 1)\,dy = \int x^2\,dx \tag{M1}$$

$$-\cot y - y = \frac{x^3}{3} + C \tag{A1}$$

$$\boxed{-\cot y - y = \frac{x^3}{3} + C} \tag{A1}$$

---

## Type D — 양변 모두 삼각함수

> 가장 까다로운 유형. 분리 후 양변 모두 항등식 변환 또는 치환이 필요.

---

### D1. $\sin y\,\dfrac{dy}{dx} = \cos x\cos^2 y$

**풀이**

변수분리:

$$\frac{\sin y}{\cos^2 y}\,dy = \cos x\,dx \implies \sec y\tan y\,dy = \cos x\,dx \tag{M1}$$

$$\int \sec y\tan y\,dy = \int \cos x\,dx$$

$$\sec y = \sin x + C \tag{A1}$$

$$\boxed{\frac{1}{\cos y} = \sin x + C} \tag{A1}$$

---

### D2. $\dfrac{dy}{dx} = \dfrac{\tan^2 x}{\tan^2 y}$

**풀이**

변수분리:

$$\tan^2 y\,dy = \tan^2 x\,dx \tag{M1}$$

양변 모두 $\tan^2 = \sec^2 - 1$ 변환:

$$\int (\sec^2 y - 1)\,dy = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$\tan y - y = \tan x - x + C \tag{A1}$$

$$\boxed{\tan y - y = \tan x - x + C} \tag{A1}$$

---

### D3. $\dfrac{dy}{dx} = \dfrac{\sin^2 y}{\sin x\cos x},\quad y = \dfrac{\pi}{4} \text{ when } x = \dfrac{\pi}{4}$

**풀이**

변수분리:

$$\frac{dy}{\sin^2 y} = \frac{dx}{\sin x\cos x} \tag{M1}$$

좌변: $\int \csc^2 y\,dy = -\cot y$

우변: $\dfrac{1}{\sin x\cos x} = \dfrac{2}{\sin 2x} = 2\csc 2x$

$$\int 2\csc 2x\,dx = \ln|\tan x| + C \tag{M1}$$

$$-\cot y = \ln|\tan x| + C \tag{A1}$$

초기조건 $x=\frac{\pi}{4},\ y=\frac{\pi}{4}$: $\;\cot\frac{\pi}{4} = 1,\;\tan\frac{\pi}{4} = 1$

$$-1 = \ln 1 + C \implies C = -1 \tag{M1}$$

$$\boxed{-\cot y = \ln|\tan x| - 1} \tag{A1}$$

---

### D4. $\cos^2 x\,\dfrac{dy}{dx} = \sin^2 y$

**풀이**

변수분리:

$$\frac{dy}{\sin^2 y} = \frac{dx}{\cos^2 x} \implies \csc^2 y\,dy = \sec^2 x\,dx \tag{M1}$$

$$\int \csc^2 y\,dy = \int \sec^2 x\,dx$$

$$-\cot y = \tan x + C \tag{A1}$$

$$\boxed{\cot y + \tan x + C = 0} \tag{A1}$$

---

## Type E — 까다로운 특수해 + 삼각함수 혼합

> 여러 유형이 섞인 종합 문제.

---

### E1. $\dfrac{dy}{dx} = \sin x\cos^2 x,\quad y = 0 \text{ when } x = \dfrac{\pi}{3}$

> *(core_concepts Ex 2(i) — 복습 확인용)*

**풀이**

$$dy = \sin x\cos^2 x\,dx \tag{M1}$$

치환 $u = \cos x,\; du = -\sin x\,dx$:

$$y = -\int u^2\,du = -\frac{\cos^3 x}{3} + C \tag{A1}$$

초기조건 $x=\frac{\pi}{3},\ y=0$: $\;\cos\frac{\pi}{3} = \frac{1}{2}$

$$0 = -\frac{(1/2)^3}{3} + C = -\frac{1}{24} + C \implies C = \frac{1}{24} \tag{M1}$$

$$\boxed{y = -\frac{\cos^3 x}{3} + \frac{1}{24}} \tag{A1}$$

---

### E2. $\dfrac{dy}{dx} = \dfrac{\sec^2 x}{y+1},\quad y = 0 \text{ when } x = 0$

**풀이**

변수분리:

$$(y+1)\,dy = \sec^2 x\,dx \tag{M1}$$

$$\frac{(y+1)^2}{2} = \tan x + C \tag{A1}$$

초기조건 $x=0,\ y=0$:

$$\frac{1}{2} = 0 + C \implies C = \frac{1}{2} \tag{M1}$$

$$\frac{(y+1)^2}{2} = \tan x + \frac{1}{2} \implies (y+1)^2 = 2\tan x + 1$$

$$\boxed{y = -1 + \sqrt{2\tan x + 1}} \tag{A1}$$

($y \geq 0$이므로 양의 근 선택)

---

### E3. $(1 + \cos x)\,\dfrac{dy}{dx} = y\sin x,\quad y = 2 \text{ when } x = \pi$

**풀이**

변수분리:

$$\frac{dy}{y} = \frac{\sin x}{1+\cos x}\,dx \tag{M1}$$

우변: 치환 $u = 1+\cos x,\; du = -\sin x\,dx$

$$\int \frac{\sin x}{1+\cos x}\,dx = \int \frac{-du}{u} = -\ln|1+\cos x| \tag{M1}$$

$$\ln|y| = -\ln|1+\cos x| + C \tag{A1}$$

초기조건 $x=\pi,\ y=2$: $\;1+\cos\pi = 1-1 = 0$ ...

> **주의:** $x = \pi$에서 $1+\cos\pi = 0$ — 분모가 0이 되어 해가 불안정하다. 초기조건을 $x = 0$으로 바꾸면:

$x=0,\ y=2$로 수정: $\;1+\cos 0 = 2$

$$\ln 2 = -\ln 2 + C \implies C = 2\ln 2 = \ln 4 \tag{M1}$$

$$\ln|y| = \ln 4 - \ln|1+\cos x| = \ln\frac{4}{1+\cos x}$$

$$\boxed{y = \frac{4}{1+\cos x}} \tag{A1}$$

---

### E4. $\dfrac{dy}{dx} = \dfrac{e^y}{\cos^2 x},\quad y = 0 \text{ when } x = \dfrac{\pi}{4}$

**풀이**

변수분리:

$$e^{-y}\,dy = \frac{dx}{\cos^2 x} = \sec^2 x\,dx \tag{M1}$$

$$\int e^{-y}\,dy = \int \sec^2 x\,dx$$

$$-e^{-y} = \tan x + C \tag{A1}$$

초기조건 $x=\frac{\pi}{4},\ y=0$: $\;\tan\frac{\pi}{4} = 1$

$$-1 = 1 + C \implies C = -2 \tag{M1}$$

$$-e^{-y} = \tan x - 2 \implies e^{-y} = 2 - \tan x$$

$$\boxed{y = -\ln(2 - \tan x)} \tag{A1}$$

> **정의역 주의:** $2 - \tan x > 0$이어야 하므로 $\tan x < 2$인 범위에서만 유효하다.

---

## 유형별 총정리 — 어떤 패턴에서 어떤 항등식이 필요한가

| 우변 패턴 | 막히는 이유 | 처방 |
|---|---|---|
| $\tan^2 x$ | 직접 적분 불가 | $\sec^2 x - 1$로 변환 후 적분 |
| $\sin^2 x$ 또는 $\cos^2 x$ | 직접 적분 불가 | 반각 공식으로 변환 |
| $\frac{\sin^2 x}{\cos^2 x}$ | $= \tan^2 x$임을 인식 못함 | 먼저 $\tan^2 x$로 쓰고 → $\sec^2 x - 1$ |
| $\sin x\cos^2 x$ | 어떤 치환인지 모름 | $u = \cos x$ (미분하면 $-\sin x$가 이미 있음) |
| $\frac{1}{\sin x\cos x}$ | 어떻게 적분하나? | $= \frac{2}{\sin 2x}$, 그 다음 $\ln\|\tan x\|$ |
| $\cot^2 y$ ($y$ 쪽) | $\cot^2$을 모름 | $\csc^2 y - 1$로 변환 |
| $\sec y \tan y$ ($y$ 쪽) | $= \frac{d}{dy}\sec y$임을 인식 못함 | $\int \sec y\tan y\,dy = \sec y$ |
