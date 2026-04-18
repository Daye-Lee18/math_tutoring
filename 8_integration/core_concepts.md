# Integration — Core Concepts

---

## 1. Basic Integration

| Power | Trigonometry | Exponential |
|---|---|---|
| $\displaystyle\int x^n\,dx = \dfrac{x^{n+1}}{n+1} + C \quad (n \neq -1)$ | $\displaystyle\int \sin x\,dx = -\cos x + C$ | $\displaystyle\int e^x\,dx = e^x + C$ |
| $\displaystyle\int x^{-1}\,dx = \ln\lvert x\rvert + C$ | $\displaystyle\int \cos x\,dx = \sin x + C$ | |

::: {.callout-tip title="KEY"}          
- Remember only **these five basic forms** (just as anti-differentiation).
- The following methods are all about **transforming** given integrals into these basic forms.                                     
:::  

---

## 2. Four Ways to Transform into Basic Forms

### (1) Substitution to cancel out

<details>
<summary>**TYPE 1 — 단번에 해치워야 하는 놈들** (straightforward linear substitution)</summary>

$$\int (2x+3)^5\,dx \qquad \int \cos(3-2x)\,dx \qquad \int 4e^{4x-1}\,dx$$

---

**Solutions:**

$\displaystyle\int (2x+3)^5\,dx$: &nbsp; $u = 2x+3,\ du = 2\,dx$

$$= \frac{1}{2}\int u^5\,du = \frac{u^6}{12} + C = \boxed{\frac{(2x+3)^6}{12} + C}$$

$\displaystyle\int \cos(3-2x)\,dx$: &nbsp; $u = 3-2x,\ du = -2\,dx$

$$= -\frac{1}{2}\int \cos u\,du = \boxed{-\frac{1}{2}\sin(3-2x) + C}$$

$\displaystyle\int 4e^{4x-1}\,dx$: &nbsp; $u = 4x-1,\ du = 4\,dx$

$$= \int e^u\,du = \boxed{e^{4x-1} + C}$$

</details>

<details>
<summary>**TYPE 2 — 단번에 해치울 수도 있지만 풀이과정을 보여줘야 하는 놈들** (derivative of inner function is visible in the integrand)</summary>

::: {style="font-size: 0.8em; color: #666;"}
integrand = 피적분함수 — $\int \underbrace{f(x)}_{\text{integrand}} \, dx$ 에서 $\int$와 $dx$ 사이에 있는 식 전체
:::

$$\int (2x+3)(x^2+3x+3)^5\,dx \qquad \int \sin^2 x\cos x\,dx \qquad \int xe^{x^2}\,dx$$

$$\int \frac{2x+3}{x^2+3x+3}\,dx \qquad \int \sec^2 x\tan^2 x\,dx \qquad \int \frac{e^x}{(2e^x-3)^2}\,dx$$

---

**Solutions:**

$\displaystyle\int (2x+3)(x^2+3x+3)^5\,dx$: &nbsp; $\tfrac{d}{dx}(x^2+3x+3) = 2x+3$ ✓ &nbsp; $u = x^2+3x+3,\ du = (2x+3)\,dx$

$$= \int u^5\,du = \boxed{\frac{(x^2+3x+3)^6}{6} + C}$$

$\displaystyle\int \sin^2 x\cos x\,dx$: &nbsp; $\tfrac{d}{dx}(\sin x) = \cos x$ ✓ &nbsp; $u = \sin x,\ du = \cos x\,dx$

$$= \int u^2\,du = \boxed{\frac{\sin^3 x}{3} + C}$$

$\displaystyle\int xe^{x^2}\,dx$: &nbsp; $\tfrac{d}{dx}(x^2) = 2x$ ✓ (factor $\tfrac{1}{2}$) &nbsp; $u = x^2,\ du = 2x\,dx$

$$= \frac{1}{2}\int e^u\,du = \boxed{\frac{1}{2}e^{x^2} + C}$$

$\displaystyle\int \frac{2x+3}{x^2+3x+3}\,dx$: &nbsp; $\tfrac{d}{dx}(x^2+3x+3) = 2x+3$ ✓ &nbsp; $u = x^2+3x+3,\ du = (2x+3)\,dx$

$$= \int \frac{1}{u}\,du = \boxed{\ln|x^2+3x+3| + C}$$

$\displaystyle\int \sec^2 x\tan^2 x\,dx$: &nbsp; $\tfrac{d}{dx}(\tan x) = \sec^2 x$ ✓ &nbsp; $u = \tan x,\ du = \sec^2 x\,dx$

$$= \int u^2\,du = \boxed{\frac{\tan^3 x}{3} + C}$$

$\displaystyle\int \frac{e^x}{(2e^x-3)^2}\,dx$: &nbsp; $\tfrac{d}{dx}(2e^x-3) = 2e^x$ ✓ (factor $\tfrac{1}{2}$) &nbsp; $u = 2e^x-3,\ du = 2e^x\,dx$

$$= \frac{1}{2}\int u^{-2}\,du = \boxed{-\frac{1}{2(2e^x-3)} + C}$$

</details>

<details>
<summary>**TYPE 3 — 대체 허점을 안보이는 센 놈들** (보통 문제에서 급소를 알려 줌 — substitution given)</summary>

$$\int \frac{1}{x^2+1}\,dx; \quad x = \tan\theta \qquad\qquad \int \sec^3 x\,dx; \quad u = \sec x$$

$$\int \frac{2}{\sqrt{x}(x-4)}\,dx; \quad u = \sqrt{x} \qquad\qquad \int \sin^3 x\,dx; \quad u = \cos x$$

---

**Solutions:**

$\displaystyle\int \frac{1}{x^2+1}\,dx$; &nbsp; $x = \tan\theta,\ dx = \sec^2\theta\,d\theta,\ x^2+1 = \sec^2\theta$

$$= \int \frac{\sec^2\theta}{\sec^2\theta}\,d\theta = \int 1\,d\theta = \theta + C = \boxed{\arctan x + C}$$

$\displaystyle\int \sec^3 x\,dx$; &nbsp; IBP: $u = \sec x,\ v' = \sec^2 x,\ u' = \sec x\tan x,\ v = \tan x$

$$= \sec x\tan x - \int \sec x\tan^2 x\,dx = \sec x\tan x - \int \sec x(\sec^2 x-1)\,dx$$

$$= \sec x\tan x - \int\sec^3 x\,dx + \int\sec x\,dx$$

$$2\int\sec^3 x\,dx = \sec x\tan x + \ln|\sec x+\tan x| \implies \boxed{\int\sec^3 x\,dx = \frac{1}{2}\bigl(\sec x\tan x + \ln|\sec x+\tan x|\bigr) + C}$$

$\displaystyle\int \frac{2}{\sqrt{x}(x-4)}\,dx$; &nbsp; $u = \sqrt{x},\ u^2 = x,\ 2u\,du = dx$

$$= \int \frac{2}{u(u^2-4)}\cdot 2u\,du = \int \frac{4}{(u-2)(u+2)}\,du$$

Partial fractions: $A=1,\ B=-1$ &nbsp;→

$$= \ln|u-2| - \ln|u+2| + C = \boxed{\ln\left|\frac{\sqrt{x}-2}{\sqrt{x}+2}\right| + C}$$

$\displaystyle\int \sin^3 x\,dx$; &nbsp; $u = \cos x,\ du = -\sin x\,dx,\ \sin^2 x = 1-u^2$

$$= \int (1-u^2)(-du) = -u + \frac{u^3}{3} + C = \boxed{-\cos x + \frac{\cos^3 x}{3} + C}$$

</details>

::: {.callout-tip title="KEY"}          
- About 50% of all integration questions use substitution — always try it first!
- If you cannot see how to integrate at all, it would probably belong to **Type 2**                                  
:::  

---

### (2) Partial Fractions

<details>
<summary>**TYPE 1a — 서로 다른 일차 인수** (distinct linear factors)</summary>

$$\int \frac{1}{x(x+2)}\,dx$$

$$\frac{1}{x(x+2)} = \frac{A}{x} + \frac{B}{x+2}$$

> 분모 각 인수마다 분자를 상수 $A, B$로 놓는다. 양변에 분모를 곱한 뒤 편한 $x$ 값 대입으로 $A, B$ 결정.

$$\int \frac{1}{x(x+2)}\,dx \;\longrightarrow\; \int \frac{A}{x}\,dx + \int \frac{B}{x+2}\,dx = A\ln|x| + B\ln|x+2| + C$$

---

**Solution:** &nbsp; $1 = A(x+2) + Bx$; &nbsp; $x=0$: $A = \tfrac{1}{2}$; &nbsp; $x=-2$: $B = -\tfrac{1}{2}$

$$\boxed{\frac{1}{2}\ln|x| - \frac{1}{2}\ln|x+2| + C = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + C}$$

</details>

<details>
<summary>**TYPE 1b — 반복되는 일차 인수** (repeated linear factor)</summary>

$$\int \frac{1}{x(x+2)^2}\,dx$$

$$\frac{1}{x(x+2)^2} = \frac{A}{x} + \frac{B}{x+2} + \frac{C}{(x+2)^2}$$

> **"각 거듭제곱마다 항을 추가"란?**
> $(x+2)^2$이 분모에 있으면, $(x+2)^1$과 $(x+2)^2$ **두 항을 모두** 써야 한다는 뜻.
> 즉 $\frac{B}{x+2}$ 하나만 쓰면 안 되고, $\frac{B}{x+2} + \frac{C}{(x+2)^2}$ 둘 다 필요.
>
> 비유: $(x+2)^3$이면 → $\dfrac{B}{x+2} + \dfrac{C}{(x+2)^2} + \dfrac{D}{(x+2)^3}$ 세 항 모두 필요.

$$\int \frac{C}{(x+2)^2}\,dx = -\frac{C}{x+2} + C' \quad\leftarrow\text{ ln이 아니라 역수 형태로 적분}$$

---

**Solution:** &nbsp; $1 = A(x+2)^2 + Bx(x+2) + Cx$

$x=0$: $4A=1 \Rightarrow A=\tfrac{1}{4}$; &nbsp; $x=-2$: $-2C=1 \Rightarrow C=-\tfrac{1}{2}$; &nbsp; $x^2$ 계수: $A+B=0 \Rightarrow B=-\tfrac{1}{4}$

$$\boxed{\frac{1}{4}\ln|x| - \frac{1}{4}\ln|x+2| + \frac{1}{2(x+2)} + C}$$

</details>

<details>
<summary>**TYPE 1c — 분자 차수 ≥ 분모 차수** (improper fraction → long division first)</summary>

$$\int \frac{x^2}{x^2-4}\,dx$$

> **Improper fraction (가분수)이란?**
> 분자의 최고 차수 $\geq$ 분모의 최고 차수인 분수식.
> 예: $\dfrac{x^2}{x^2-4}$ → 분자도 2차, 분모도 2차 → improper.
> 이 상태에서는 부분분수 분해를 **바로 적용할 수 없다**.
>
> **Polynomial long division (다항식 나눗셈)이란?**
> 분자를 분모로 나눠서 **정수 부분 + 나머지 분수** 형태로 바꾸는 것.
> 숫자 나눗셈 $\dfrac{7}{3} = 2 + \dfrac{1}{3}$과 같은 원리를 다항식에 적용.

$$\frac{x^2}{x^2-4} \xrightarrow{\text{나눗셈}} 1 + \frac{4}{x^2-4} \xrightarrow{\text{부분분수}} 1 + \frac{A}{x-2} + \frac{B}{x+2}$$

$$\int \frac{x^2}{x^2-4}\,dx = \int 1\,dx + \int \frac{A}{x-2}\,dx + \int \frac{B}{x+2}\,dx$$

> **Note:** 분자 차수 $\geq$ 분모 차수이면 **항상 나눗셈 먼저** — 나누지 않고 부분분수 시도하면 형태가 성립하지 않는다.

---

**Solution:** &nbsp; $4 = A(x+2)+B(x-2)$; &nbsp; $x=2$: $A=1$; &nbsp; $x=-2$: $B=-1$

$$\boxed{\int \frac{x^2}{x^2-4}\,dx = x + \ln|x-2| - \ln|x+2| + C}$$

</details>

---

### (3) Using Trigonometric Identities

*(Study together with **The Table** in Section 3)*

<details>
<summary>**TYPE 1 — 형태를 바꿔야 하는 놈들** (use basic identities to rewrite the integrand)</summary>

$$\int \tan^2 x\,dx \qquad \int \sec^2 x\cot^2 x\,dx \qquad \int \cos x\csc^2 x\,dx$$

::: {.callout-tip title="KEY"}          
- $\sec^2 x$ and $\csc^2 x$ are **the most favourable forms** — always look for them. 
- Trig functions with **"co"** and **"without co"** never come together in a stable form.                             
:::

---

**Solutions:**

$\displaystyle\int \tan^2 x\,dx$: &nbsp; identity: $\tan^2 x = \sec^2 x - 1$

$$= \int(\sec^2 x - 1)\,dx = \boxed{\tan x - x + C}$$

$\displaystyle\int \sec^2 x\cot^2 x\,dx$: &nbsp; $\sec^2 x\cot^2 x = \dfrac{1}{\cos^2 x}\cdot\dfrac{\cos^2 x}{\sin^2 x} = \dfrac{1}{\sin^2 x} = \csc^2 x$

$$= \int \csc^2 x\,dx = \boxed{-\cot x + C}$$

$\displaystyle\int \cos x\csc^2 x\,dx$: &nbsp; $\cos x\csc^2 x = \dfrac{\cos x}{\sin^2 x}$ &nbsp;→&nbsp; $u = \sin x,\ du = \cos x\,dx$

$$= \int u^{-2}\,du = \boxed{-\csc x + C}$$

</details>

<details>
<summary>**TYPE 2 — 각을 바꿔서라도 힘(Power)을 깨야 하는 놈들** (use double-angle formulae to reduce powers)</summary>

$$\int \sin^2 x\,dx \qquad \int \sin^4 x\,dx \qquad \int \sin^3 x\,dx$$

> Use: $\sin^2 x = \dfrac{1-\cos 2x}{2}$, $\quad\cos^2 x = \dfrac{1+\cos 2x}{2}$

---

**Solutions:**

$\displaystyle\int \sin^2 x\,dx$:

$$= \int \frac{1-\cos 2x}{2}\,dx = \boxed{\frac{x}{2} - \frac{\sin 2x}{4} + C}$$

$\displaystyle\int \sin^4 x\,dx$: &nbsp; $\sin^4 x = \left(\dfrac{1-\cos 2x}{2}\right)^2 = \dfrac{1 - 2\cos 2x + \cos^2 2x}{4}$, &nbsp; $\cos^2 2x = \dfrac{1+\cos 4x}{2}$

$$= \frac{1}{4}\int\!\left(\frac{3}{2} - 2\cos 2x + \frac{\cos 4x}{2}\right)dx = \boxed{\frac{3x}{8} - \frac{\sin 2x}{4} + \frac{\sin 4x}{32} + C}$$

$\displaystyle\int \sin^3 x\,dx$: &nbsp; $\sin^3 x = \sin x(1-\cos^2 x)$ &nbsp;→&nbsp; $u = \cos x,\ du = -\sin x\,dx$

$$= \int(1-u^2)(-du) = \boxed{-\cos x + \frac{\cos^3 x}{3} + C}$$

</details>

<details>
<summary>**TYPE 3 — Product-to-sum으로 해체시켜야 하는 놈들** (products of trig functions with different angles)</summary>

$$\int \sin 2x\cos 3x\,dx \qquad \int 2\cos x\cos 3x\,dx$$

---

**공식 유도 — 원래 배운 식에서 적분 폼까지**

**① sin × cos 의 경우**

| 단계 | 식 |
|------|-----|
| 원래 배운 식 (Sum-to-Product) | $\sin P + \sin Q = 2\sin\!\left(\dfrac{P+Q}{2}\right)\cos\!\left(\dfrac{P-Q}{2}\right)$ |
| 변환: $P = A+B,\; Q = A-B$ 로 치환 | $\sin(A+B) + \sin(A-B) = 2\sin A\cos B$ |
| 적분에서 사용되는 폼 (÷2) | $\sin A\cos B = \tfrac{1}{2}[\sin(A+B)+\sin(A-B)]$ |

**② cos × cos 의 경우**

| 단계 | 식 |
|------|-----|
| 원래 배운 식 (Sum-to-Product) | $\cos P + \cos Q = 2\cos\!\left(\dfrac{P+Q}{2}\right)\cos\!\left(\dfrac{P-Q}{2}\right)$ |
| 변환: $P = A-B,\; Q = A+B$ 로 치환 | $\cos(A-B) + \cos(A+B) = 2\cos A\cos B$ |
| 적분에서 사용되는 폼 (÷2) | $\cos A\cos B = \tfrac{1}{2}[\cos(A-B)+\cos(A+B)]$ |

---

**Solutions:**

$\displaystyle\int \sin 2x\cos 3x\,dx$: &nbsp; $\sin A\cos B = \tfrac{1}{2}[\sin(A+B)+\sin(A-B)]$

$$\sin 2x\cos 3x = \tfrac{1}{2}[\sin 5x + \sin(-x)] = \tfrac{1}{2}(\sin 5x - \sin x)$$

$$= \boxed{-\frac{\cos 5x}{10} + \frac{\cos x}{2} + C}$$

$\displaystyle\int 2\cos x\cos 3x\,dx$: &nbsp; $2\cos A\cos B = \cos(A-B)+\cos(A+B)$

$$2\cos x\cos 3x = \cos(-2x)+\cos 4x = \cos 2x + \cos 4x$$

$$= \boxed{\frac{\sin 2x}{2} + \frac{\sin 4x}{4} + C}$$

</details>

---

### (4) Integration by Parts

$$\boxed{\int u\,v'\,dx = uv - \int u'v\,dx}$$

**Rhythm — how to choose $u$:**

$$\ln x \;\leftarrow\; 1,\; x,\; x^2\;\cdots \;\leftarrow\; \sin x,\; \cos x\;\cdots \;\leftarrow\; e^x \;\Rightarrow\; v'$$

*(Priority: $\ln x$ is always $u$; $e^x$ is almost always $v'$.)*

<details>
<summary>**왜 저 순서인가? — Rhythm의 이유**</summary>

Parts 공식을 적용하면 $\displaystyle\int u'v\,dx$ 가 남는다.  
즉 **$u$를 미분했을 때 남은 적분이 더 쉬워지는 방향**으로 선택해야 한다.

| 함수 | 미분하면? | 적분하면? |
|------|-----------|-----------|
| $\ln x$ | $\dfrac{1}{x}$ — 사라짐 | $x\ln x - x$ — 더 복잡해짐 |
| $x^n$ | $nx^{n-1}$ — 차수 줄어듦 | $x^{n+1}$ — 차수 늘어남 |
| $\sin x,\,\cos x$ | 서로 순환 | 서로 순환 |
| $e^x$ | $e^x$ — 그대로 | $e^x$ — 그대로 |

따라서 **흐름의 왼쪽일수록 $u$로 쓰는 게 유리** — 미분할수록 단순해지고, 오른쪽에 남는 적분이 쉬워지기 때문.

- $\ln x$는 적분하면 더 복잡해지므로 무조건 $u$
- $e^x$는 미분/적분해도 그대로이므로 $v'$로 써도 손해 없음

> **핵심:** "미분이 잘 된다"는 결과적으로 맞긴 하지만, 진짜 기준은 **미분 후 남는 $\int u'v\,dx$ 가 더 쉬워지는가** 이다.

</details>

- Don't apply the formula mechanically — follow the **rhythm**.

<details>
<summary>**TYPE 1 — 단번에 죽는 놈들** (one application)</summary>

$$\int xe^x\,dx \qquad \int x\sec^2 x\,dx \qquad \int \ln x\,dx$$

> **왜 TYPE 1?** $u$를 한 번만 미분하면 상수가 되어 남은 적분이 바로 풀린다.

**Ex:** $\displaystyle\int xe^x\,dx$

| | 선택 | 이유 |
|---|---|---|
| $u = x$ | $u' = 1$ | Rhythm상 $x$가 $e^x$보다 왼쪽 → $u$ |
| $v' = e^x$ | $v = e^x$ | $e^x$는 적분해도 그대로 |

$$\int xe^x\,dx = xe^x - \int e^x\,dx = xe^x - e^x + C = e^x(x-1) + C$$

→ $u = x$를 미분하니 $u' = 1$ (상수)이 되어 **한 번에 종료**.

---

$\displaystyle\int x\sec^2 x\,dx$: &nbsp; $u = x,\ u'=1,\quad v'=\sec^2 x,\ v=\tan x$

$$= x\tan x - \int \tan x\,dx = \boxed{x\tan x - \ln|\sec x| + C}$$

$\displaystyle\int \ln x\,dx$: &nbsp; $u = \ln x,\ u'=\tfrac{1}{x},\quad v'=1,\ v=x$

$$= x\ln x - \int x\cdot\frac{1}{x}\,dx = x\ln x - x + C = \boxed{x(\ln x - 1) + C}$$

</details>

<details>
<summary>**TYPE 2 — 두 번 치야 죽는 놈들** (apply twice)</summary>

$$\int x^2 e^{-x}\,dx \qquad \int x^2\sin x\,dx \qquad \int (\ln x)^2\,dx$$

> **왜 TYPE 2?** $u = x^2$처럼 차수가 2인 경우, 한 번 미분하면 $2x$가 남아 아직 안 죽는다. 한 번 더 쳐야 상수가 된다.

**Ex:** $\displaystyle\int x^2 e^{-x}\,dx$

**1st application:** $u = x^2,\; u' = 2x,\quad v' = e^{-x},\; v = -e^{-x}$

$$= -x^2 e^{-x} + 2\int xe^{-x}\,dx$$

**2nd application:** $u = x,\; u' = 1,\quad v' = e^{-x},\; v = -e^{-x}$

$$\int xe^{-x}\,dx = -xe^{-x} + \int e^{-x}\,dx = -xe^{-x} - e^{-x} + C$$

$$\therefore\quad \int x^2 e^{-x}\,dx = -x^2 e^{-x} + 2(-xe^{-x} - e^{-x}) + C = -e^{-x}(x^2+2x+2) + C$$

→ $x^2 \xrightarrow{\text{1st}} 2x \xrightarrow{\text{2nd}} 2$ (상수) → **두 번째에 종료**.

---

$\displaystyle\int x^2\sin x\,dx$:

**1st:** $u=x^2,\ u'=2x,\quad v'=\sin x,\ v=-\cos x$

$$= -x^2\cos x + 2\int x\cos x\,dx$$

**2nd:** $u=x,\ u'=1,\quad v'=\cos x,\ v=\sin x$

$$\int x\cos x\,dx = x\sin x - \int\sin x\,dx = x\sin x + \cos x$$

$$\boxed{\int x^2\sin x\,dx = -x^2\cos x + 2x\sin x + 2\cos x + C}$$

$\displaystyle\int (\ln x)^2\,dx$: &nbsp; $u=(\ln x)^2,\ u'=\tfrac{2\ln x}{x},\quad v'=1,\ v=x$

$$= x(\ln x)^2 - 2\int \ln x\,dx = x(\ln x)^2 - 2x(\ln x-1) + C = \boxed{x(\ln x)^2 - 2x\ln x + 2x + C}$$

</details>

<details>
<summary>**TYPE 3 — 정공으로는 아무래도 안 죽는 놈들 — 돌려치기** (cyclic)</summary>

$$\int e^x\cos x\,dx \qquad \int e^{3x}\sin x\,dx$$

> **왜 TYPE 3?** $e^x$와 $\sin x / \cos x$는 아무리 미분/적분해도 서로 순환한다. Parts를 두 번 적용하면 원래 적분 $I$가 우변에 다시 나타남 → 방정식으로 풀기.

**Ex:** $I = \displaystyle\int e^x\cos x\,dx$

**1st:** $u = \cos x,\; u' = -\sin x,\quad v' = e^x,\; v = e^x$

$$I = e^x\cos x + \int e^x\sin x\,dx$$

**2nd:** $u = \sin x,\; u' = \cos x,\quad v' = e^x,\; v = e^x$

$$\int e^x\sin x\,dx = e^x\sin x - \int e^x\cos x\,dx = e^x\sin x - I$$

$$I = e^x\cos x + e^x\sin x - I$$

$$2I = e^x(\cos x + \sin x) \implies \boxed{I = \tfrac{1}{2}e^x(\cos x + \sin x) + C}$$

→ 두 번 Parts를 써도 $I$가 다시 나옴 → **우변의 $-I$를 좌변으로 넘겨서** 방정식으로 해결.

---

$I = \displaystyle\int e^{3x}\sin x\,dx$:

**1st:** $u=\sin x,\ u'=\cos x,\quad v'=e^{3x},\ v=\tfrac{e^{3x}}{3}$

$$I = \frac{e^{3x}\sin x}{3} - \frac{1}{3}\int e^{3x}\cos x\,dx$$

**2nd:** $u=\cos x,\ u'=-\sin x,\quad v'=e^{3x},\ v=\tfrac{e^{3x}}{3}$

$$\int e^{3x}\cos x\,dx = \frac{e^{3x}\cos x}{3} + \frac{1}{3}\int e^{3x}\sin x\,dx = \frac{e^{3x}\cos x}{3} + \frac{I}{3}$$

$$I = \frac{e^{3x}\sin x}{3} - \frac{1}{3}\!\left(\frac{e^{3x}\cos x}{3} + \frac{I}{3}\right) = \frac{e^{3x}\sin x}{3} - \frac{e^{3x}\cos x}{9} - \frac{I}{9}$$

$$\frac{10I}{9} = \frac{e^{3x}(3\sin x - \cos x)}{9} \implies \boxed{I = \frac{e^{3x}(3\sin x - \cos x)}{10} + C}$$

</details>

<details>
<summary>**TYPE 3★ — 1회 Parts + 치환으로 마무리되는 놈들**</summary>

$$\int \sin^{-1} x\,dx$$

> **왜 TYPE 3★?** Parts 한 번 후 남은 적분이 $\displaystyle\int\frac{x}{\sqrt{1-x^2}}\,dx$ — 순환하지 않고, 치환으로 깔끔하게 끝난다. TYPE 3의 돌려치기와 달리 **한 번에 종료**.

**Ex:** $\displaystyle\int \sin^{-1}x\,dx$

$u = \sin^{-1}x,\; u' = \dfrac{1}{\sqrt{1-x^2}},\quad v' = 1,\; v = x$

$$= x\sin^{-1}x - \int \frac{x}{\sqrt{1-x^2}}\,dx$$

**치환:** $t = 1-x^2,\; dt = -2x\,dx \;\Rightarrow\; x\,dx = -\tfrac{1}{2}dt$

$$\int \frac{x}{\sqrt{1-x^2}}\,dx = \int \frac{1}{\sqrt{t}}\cdot\left(-\tfrac{1}{2}\right)dt = -\sqrt{t} = -\sqrt{1-x^2}$$

$$\therefore\quad \int \sin^{-1}x\,dx = x\sin^{-1}x + \sqrt{1-x^2} + C$$

</details>

<details>
<summary>**Ex — Worked solution:** $\displaystyle\int_0^1 x^2 e^x\,dx$</summary>

$$\int_0^1 x^2 e^x\,dx = \Bigl[x^2 e^x\Bigr]_0^1 - 2\int_0^1 xe^x\,dx$$

$$= e - 2\!\left(\Bigl[xe^x\Bigr]_0^1 - \int_0^1 e^x\,dx\right)$$

$$= e - 2\!\left(e - \Bigl[e^x\Bigr]_0^1\right)$$

$$= e - 2\bigl(e - (e - 1)\bigr) = e - 2$$

> **모범 풀이 습관:** 숫자나 괄호는 $[\ ]$ 밖으로 | 한 칸 내려 지고 새로운 기본으로 | 박스를 한 칸씩 오른쪽으로 이동

</details>

---

## 3. The Table — Differentiation and Integration of Trig Functions

*(Notice the pattern and memorise!)*

| | $\sin x$ | $\cos x$ | $\tan x$ | $\csc x$ | $\sec x$ | $\cot x$ |
|---|---|---|---|---|---|---|
| $\dfrac{d}{dx}$ | $\cos x$ | $-\sin x$ | $\sec^2 x$ | $-\csc x\cot x$ | $\sec x\tan x$ | $-\csc^2 x$ |
| $\displaystyle\int$ | $-\cos x + C$ | $\sin x + C$ | $\ln\lvert\sec x\rvert + C$ ▶ | $-\ln\lvert\csc x+\cot x\rvert + C$ ★ | $\ln\lvert\sec x+\tan x\rvert + C$ ★ | $\ln\lvert\sin x\rvert + C$ ▶ |

| | $\sin^2 x$ | $\cos^2 x$ | $\tan^2 x$ | $\csc^2 x$ | $\sec^2 x$ | $\cot^2 x$ |
|---|---|---|---|---|---|---|
| $\dfrac{d}{dx}$ | $\sin 2x$ | $-\sin 2x$ | $2\tan x\sec^2 x$ | $-2\csc^2 x\cot x$ | $2\sec^2 x\tan x$ | $-2\cot x\csc^2 x$ |
| $\displaystyle\int$ | $\dfrac{x}{2}-\dfrac{\sin 2x}{4}+C$ ▶ | $\dfrac{x}{2}+\dfrac{\sin 2x}{4}+C$ ▶ | $\tan x - x + C$ ▶ | $-\cot x + C$ | $\tan x + C$ | $-\cot x - x + C$ ▶ |

**Key:**
- ▶ Integration or differentiation of shaded cells requires **proof**
- ★ Integration of $\csc x$ and $\sec x$ is **Further Math** only
- Find the **co-rule**: if you know $\int\sin x$, flip to get $\int\cos x$; the same mirror pattern holds across the table
