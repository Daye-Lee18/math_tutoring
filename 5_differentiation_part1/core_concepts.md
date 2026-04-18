# Differentiation — Core Concepts

---

## 1. Basic Differentiation (▶ = proof required)

### 1) Power Rule

$$
(x^n)' = nx^{n-1}
$$

---

### 2) Exponential & Logarithmic

| Function | Derivative |
|----------|-----------|
| $(e^x)'$ | $= e^x$ |
| $(\ln x)'$ | $= \dfrac{1}{x}$ |
| ▶ $(a^x)'$ | $= a^x \ln a$ |
| ▶ $(\log_a x)'$ | $= \dfrac{1}{x \ln a}$ |

**▶ Proof — $(a^x)'$:**

$$
a^x = e^{x \ln a} \implies (a^x)' = e^{x \ln a} \cdot \ln a = a^x \ln a
$$

**▶ Proof — $(\log_a x)'$:**

$$
\log_a x = \frac{\ln x}{\ln a} \implies (\log_a x)' = \frac{1}{x \ln a}
$$

---

### 3) Trigonometric

#### 공식표 (패턴별 그룹)

**[Group A] sin / cos — 4-cycle**

| Function | Derivative | 부호 |
|----------|------------|------|
| $(\sin x)'$ | $= \cos x$ | $+$ |
| $(\cos x)'$ | $= -\sin x$ | $-$ ← **co**sine |

**[Group B] tan / sec 쌍**

| Function | Derivative | 패턴 |
|----------|------------|------|
| ▶ $(\tan x)'$ | $= \sec^2 x$ | $+$ · tan 미분 → sec 등장 |
| ▶ $(\sec x)'$ | $= \sec x \tan x$ | $+$ · sec이 자기 자신 생존 |

**[Group C] cot / csc 쌍 — Group B의 "co-" 버전 (전부 음수)**

| Function | Derivative | 패턴 |
|----------|------------|------|
| ▶ $(\cot x)'$ | $= -\csc^2 x$ | $-$ · **co**t 미분 → csc 등장 |
| ▶ $(\csc x)'$ | $= -\csc x \cot x$ | $-$ · **co**sc이 자기 자신 생존 |

**[Group D] 역삼각함수**

| Function | Derivative | 패턴 |
|----------|------------|------|
| ▶ $(\arcsin x)'$ | $= \dfrac{1}{\sqrt{1-x^2}}$ | $+$ |
| ▶ $(\arccos x)'$ | $= -\dfrac{1}{\sqrt{1-x^2}}$ | $-$ ← **arc·co**s, co- rule 동일 |
| ▶ $(\arctan x)'$ | $= \dfrac{1}{1+x^2}$ | $+$ · 별도 암기 |

---

#### 암기 Tips

**Tip 1 — "co-" 붙으면 항상 음수**

미분 결과에 minus가 붙는 함수는 전부 "co-"로 시작:

$$\cos,\quad \cot,\quad \csc,\quad \arccos \quad \longrightarrow \text{ 전부 } (-)$$

> 이것만 기억하면 9개 공식의 부호는 전부 해결.

**Tip 2 — tan↔sec, cot↔csc 쌍으로 다님**

미분하면 자기 쌍의 파트너가 튀어나옴:

$$\tan' = \sec^2 \quad\longleftrightarrow\quad \cot' = -\csc^2$$
$$\sec' = \sec\cdot\tan \quad\longleftrightarrow\quad \csc' = -\csc\cdot\cot$$

> Group B(tan/sec)를 외우고, Group C는 "전부 co-로 교체 + 음수"로 도출.

**Tip 3 — sec / csc는 자기 자신이 살아남음**

$$(\sec x)' = \underbrace{\sec x}_{\text{자기 자신}} \cdot \tan x \qquad (\csc x)' = -\underbrace{\csc x}_{\text{자기 자신}} \cdot \cot x$$

> $e^x$처럼 미분 후에도 자기 자신이 인수로 남는다.

**Tip 4 — sin/cos는 4-cycle**

$$\sin \xrightarrow{\;'\;} \cos \xrightarrow{\;'\;} -\sin \xrightarrow{\;'\;} -\cos \xrightarrow{\;'\;} \sin \xrightarrow{\;'\;} \cdots$$

> 4번 미분하면 원래로. "앞으로 한 칸 이동"으로 기억.

**Tip 5 — 역삼각함수는 외우지 말고 유도**

$y = \arcsin x$이면 $x = \sin y$. 양변을 $x$로 미분:

$$1 = \cos y \cdot \frac{dy}{dx} \implies \frac{dy}{dx} = \frac{1}{\cos y} = \frac{1}{\sqrt{1-\sin^2 y}} = \frac{1}{\sqrt{1-x^2}}$$

같은 방법으로 $\arccos$, $\arctan$ 모두 유도 가능. ($\arccos$는 $x = \cos y$로 시작 → 결과에 음수 붙음.)

---

#### ▶ Proofs

**▶ Proof — $(\tan x)'$:**

$$
(\tan x)' = \left(\frac{\sin x}{\cos x}\right)' = \frac{\cos x \cdot \cos x - \sin x \cdot (-\sin x)}{\cos^2 x} = \frac{\cos^2 x + \sin^2 x}{\cos^2 x} = \frac{1}{\cos^2 x} = \sec^2 x
$$

**▶ Proof — $(\arctan x)'$:**

Let $y = \arctan x$, so $x = \tan y$. Differentiating both sides w.r.t. $x$:

$$
1 = \sec^2 y \cdot \frac{dy}{dx} \implies \frac{dy}{dx} = \frac{1}{\sec^2 y} = \frac{1}{1 + \tan^2 y} = \frac{1}{1+x^2}
$$

> **Graph — $\arctan x$:** [View on Desmos](https://www.desmos.com/calculator) → enter `arctan(x)`

---

## 2. Applied Differentiation

### 1) Product Rule

For the product of two (or more) functions:

$$
\boxed{\{f(x)g(x)\}' = f'(x)g(x) + f(x)g'(x)}
$$

In general:

$$
\{f(x)g(x)h(x)\}' = f'(x)g(x)h(x) + f(x)g'(x)h(x) + f(x)g(x)h'(x)
$$

**Ex — Differentiate:**

i. $y = x^3 = x \cdot x^2$ (by product rule)

$$
y' = (x)' \cdot x^2 + x \cdot (x^2)' = x^2 + x \cdot 2x = x^2 + 2x^2 = 3x^2
$$

ii. $y = 2e^x \cos x$

$$
y' = 2e^x \cos x + 2e^x(-\sin x) = 2e^x(\cos x - \sin x)
$$

iii. $y = (x^3 + 2x - 1)e^x$

$$
y' = (3x^2 + 2)e^x + (x^3 + 2x - 1)e^x = (x^3 + 3x^2 + 2x + 1)e^x
$$

---

### 2) Chain Rule

For a composite function:

$$
\boxed{\{f(g(x))\}' = f'(g(x)) \cdot g'(x)}
$$

In general:

$$
\{f(g(h(x)))\}' = f'(g(h(x))) \cdot g'(h(x)) \cdot h'(x) \quad \text{and so on}
$$

**Ex — Differentiate:**

i. $y = \sin 2x$

$$
y' = \cos(2x) \cdot 2 = 2\cos 2x
$$

ii. $y = \sin^2 x$

$$
y' = 2\sin x \cdot \cos x = \sin 2x
$$

iii. $y = \sin^3 2x$

$$
y' = 3\sin^2(2x) \cdot \cos(2x) \cdot 2 = 6\sin^2 2x \cos 2x
$$

---

### 3) Quotient Rule

For the quotient of two functions **(derive this from the product rule)**:

$$
\boxed{\left\{\frac{f(x)}{g(x)}\right\}' = \frac{f'(x)g(x) - f(x)g'(x)}{\{g(x)\}^2}}
$$

**▶ Derivation from product rule:**

Write $\dfrac{f}{g} = f \cdot g^{-1}$ and apply the product rule:

$$
\left(f \cdot g^{-1}\right)' = f' g^{-1} + f \cdot (-g^{-2})g' = \frac{f'}{g} - \frac{fg'}{g^2} = \frac{f'g - fg'}{g^2}
$$

**Ex — Differentiate:**

i. $y = \dfrac{1}{x^2+1}$ (use chain rule)

$$
y' = -\frac{2x}{(x^2+1)^2}
$$

ii. $y = \dfrac{x^2}{\sin x}$

$$
y' = \frac{2x \sin x - x^2 \cos x}{\sin^2 x}
$$

iii. $y = \dfrac{e^x}{x}$

$$
y' = \frac{e^x \cdot x - e^x \cdot 1}{x^2} = \frac{e^x(x-1)}{x^2}
$$
