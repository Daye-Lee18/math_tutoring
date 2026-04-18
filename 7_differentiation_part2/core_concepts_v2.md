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
<summary>**Explicit — Integration techniques (4, 5번 간단 메모)**</summary>

**4) Partial fraction (부분분수)** — 다음 Integration 파트에서 자세히 다룸

적분하기 어려운 분수식을 단순한 분수들의 합으로 쪼개는 기법.

$$\frac{1}{x(x+1)} = \frac{1}{x} - \frac{1}{x+1} \implies \int \frac{1}{x(x+1)}\,dx = \ln|x| - \ln|x+1| + C$$

---

**5) Trapezium rule (사다리꼴 공식)** — 커리큘럼에서 다루지 않음

곡선 아래 넓이를 사다리꼴로 근사하는 수치 적분법. 해석적으로 적분이 어려울 때 사용.

$$\int_a^b f(x)\,dx \approx \frac{h}{2}\bigl[y_0 + 2(y_1 + \cdots + y_{n-1}) + y_n\bigr], \qquad h = \frac{b-a}{n}$$

</details>

---

### 1.1 Cartesian — Implicit $f(x, y) = 0$

::: {style="font-size: 0.85em; color: #666;"}
**Explicit** $y = f(x)$: $y$가 혼자 분리돼 있어 값을 바로 읽을 수 있음 (ex. $y = x^2 + 3x$)  
**Implicit** $f(x,y) = 0$: $x$와 $y$가 식 안에 섞여 있는 형태 — 이항 가능 여부와 무관하게 형태 자체가 implicit

| 방정식 | 이항하면? | 실제로 쓰는 방법 |
|---|---|---|
| $x^2 + y = 2$ | $y = 2-x^2$ — 쉽게 가능 | explicit으로 바꿔서 미분 |
| $x^2 + y^3 = 2$ | $y = \sqrt[3]{2-x^2}$ — 가능하지만 복잡 | implicit 미분이 더 편함 |
| $x^2 + y^2 = 1$ | $y = \pm\sqrt{1-x^2}$ — $\pm$ 때문에 단일 함수 불가 | implicit 미분만 가능 |

즉, implicit 미분을 쓰는 이유는 **이항이 불가능하거나, 이항해도 너무 복잡할 때** 편리하기 때문.
:::

**Key rules:**

$$\frac{d}{dx}(y^n) = ny^{n-1}\frac{dy}{dx}$$

<table style="border-collapse: collapse; width: 100%; font-size: 0.93em; margin: 0.5em 0 1.2em 0;">
<tr>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>왜 이렇게 되는가? — Chain rule on $y$</strong><br><br>
    Implicit에서 $y$는 <strong>$x$의 함수</strong> $y(x)$다.<br>
    즉 $y^n = [y(x)]^n$ — <strong>합성함수</strong>이므로 chain rule 적용:<br><br>
    $$\frac{d}{dx}(y^n) = \underbrace{ny^{n-1}}_{\text{바깥 미분}} \times \underbrace{\frac{dy}{dx}}_{\text{안쪽 미분}}$$
  </td>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>확인</strong><br><br>
    $y = x^2$이면:<br><br>
    직접 계산: $\dfrac{d}{dx}(y^3) = \dfrac{d}{dx}(x^6) = 6x^5$<br><br>
    공식 적용: $3y^2 \cdot \dfrac{dy}{dx} = 3x^4 \cdot 2x = 6x^5$ ✓<br><br>
    <span style="color: #555; font-size: 0.9em;">$y$에 관한 항을 $x$로 미분할 때마다 끝에 $\dfrac{dy}{dx}$가 붙는다.</span>
  </td>
</tr>
</table>

$$\frac{d}{dx}(xy) = y + x\frac{dy}{dx} \qquad \text{(product rule)}$$

<table style="border-collapse: collapse; width: 100%; font-size: 0.93em; margin: 0.5em 0 1.2em 0;">
<tr>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>왜 이렇게 되는가? — Product rule on $x \cdot y$</strong><br><br>
    $u = x,\quad v = y$로 놓으면:<br><br>
    $$\frac{d}{dx}(uv) = u'v + uv'$$
    $$= 1 \cdot y \;+\; x \cdot \frac{dy}{dx} \;=\; y + x\frac{dy}{dx}$$
  </td>
  <td style="border: 1px solid #ddd; padding: 10px 14px; width: 50%; vertical-align: top;">
    <strong>왜 $v' = \dfrac{dy}{dx}$인가?</strong><br><br>
    $v = y$도 $x$의 함수이므로, $v$를 $x$로 미분하면 $\dfrac{dy}{dx}$.<br><br>
    <span style="color: #555; font-size: 0.9em;">위 Rule 1과 같은 이유 — $y$항을 $x$로 미분할 때마다 $\dfrac{dy}{dx}$가 붙는다.</span>
  </td>
</tr>
</table>

**Integration — Separable equations:**

> **Note:** Differential equations yield a **general solution** (with constant $C$); a given condition pins down the **particular solution**.

<details>
<summary>**Separable vs Non-separable — 어떻게 구분하는가?**</summary>

$\dfrac{dy}{dx} = (\text{x만의 식}) \times (\text{y만의 식})$ 형태면 → **Separable**

| 방정식 | 분리 시도 | 판정 |
|--------|-----------|------|
| $\dfrac{dy}{dx} = xy$ | $\dfrac{1}{y}\,dy = x\,dx$ | **Separable** ✓ |
| $\dfrac{dy}{dx} = x^2(1+y^2)$ | $\dfrac{1}{1+y^2}\,dy = x^2\,dx$ | **Separable** ✓ |
| $\dfrac{dy}{dx} = x + y$ | 분리 불가 ($y$가 $x$와 더해짐) | **Non-separable** ✗ |
| $\dfrac{dy}{dx} = \dfrac{x+y}{x}$ | $1 + \dfrac{y}{x}$ 형태 — 분리 불가 | **Non-separable** ✗ |

**빠른 판별:** 우변이 $x$와 $y$의 **곱** → separable, **합/차** or $\tfrac{y}{x}$처럼 섞임 → non-separable.

**풀이 흐름:**

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
$x$와 $y$를 직접 연결하는 대신, 제3의 변수 **$t$ (parameter)**를 통해 간접적으로 정의.  
예: $x = \cos t,\; y = \sin t$ → $t$ 소거하면 $x^2 + y^2 = 1$ (원)  
**언제 쓰는가?** $y$를 $x$로 직접 쓰기 어려운 곡선(원, 타원 등)을 표현할 때.
:::

**Differentiation:**

$$\boxed{\frac{dy}{dx} = \frac{dy/dt}{dx/dt}}$$

<details>
<summary>**왜 이렇게 되는가?**</summary>

Chain rule: $\dfrac{dy}{dx} = \dfrac{dy}{dt} \times \dfrac{dt}{dx} = \dfrac{dy/dt}{dx/dt}$

직관적으로 $dt$가 약분되는 분수처럼 생각하면 됨.

</details>

**Integration:**

$$\int y\,dx = \int y\,\frac{dx}{dt}\,dt$$

<details>
<summary>**왜 이렇게 되는가?**</summary>

$x = g(t)$이면 $dx = \dfrac{dx}{dt}\,dt$로 치환. 이제 $y$도 $t$로 표현돼 있으니 $t$에 대한 적분으로 완전히 바꿀 수 있다.

**예:** $y = t^2,\; x = t^3 \implies \int y\,dx = \int t^2 \cdot 3t^2\,dt = \dfrac{3t^5}{5} + C$

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

**i.** $t = 5-x$ 대입:

$$\boxed{y = x^2 - 10x + 24}$$

---

**ii.** $x^2 - y^2$ 계산:

$$x^2 = t^2 + 2 + \frac{1}{t^2},\quad y^2 = t^2 - 2 + \frac{1}{t^2} \implies \boxed{x^2 - y^2 = 4}$$

---

**iii.** $\sin^2 t + \cos^2 t = 1$ 이용 — $\sin t = \dfrac{x+1}{2},\; \cos t = \dfrac{y-4}{5}$:

$$\boxed{\frac{(x+1)^2}{4} + \frac{(y-4)^2}{25} = 1} \qquad \text{(중심 }(-1,4)\text{인 타원)}$$

</details>

---

## 2. Finding the Equation of a Tangent

::: {style="font-size: 0.88em; color: #555; margin-bottom: 0.8em;"}
**Tangent (접선):** 곡선 위 한 점에서 곡선에 접하는 직선. 그 점에서의 기울기 $= \dfrac{dy}{dx}$.  
직선의 방정식은 점 $(x_1, y_1)$과 기울기 $m$으로부터: $y - y_1 = m(x - x_1)$
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

※ $\cos t = 1$을 만족하는 $t$는 $0,\ \pm 2\pi,\ \pm 4\pi,\ \ldots$ 로 무한히 많다. 그러나 $\sec t$는 주기 $2\pi$인 함수이므로 $\cos t = 1$인 모든 $t$에서 $\sec t = 1$로 동일 → $\dfrac{dy}{dx} = -\dfrac{\sec^2 t}{2} = -\dfrac{1}{2}$로 결과가 같다. 편의상 $t = 0$을 사용.

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

Implicit/Parametric에서는 "turning point"라는 표현 대신 **접선의 방향**으로 특이점을 표현한다. **왜?** $y$가 $x$로 명시적으로 분리되어 있지 않아 $\dfrac{d^2y}{dx^2}$를 구하는 것이 번거롭기 때문. 대신 $\dfrac{dy}{dx}$의 **부호 변화**로 극대/극소를 판별한다.

*For implicit and parametric equations, instead of "turning point" we describe special points by the **direction of the tangent**. **Why?** Because $y$ is not explicitly separated as a function of $x$, making it inconvenient to compute $\dfrac{d^2y}{dx^2}$. Instead, we determine local maxima/minima by checking the **sign change** of $\dfrac{dy}{dx}$.*

- A point at which the tangent is **parallel to $x$-axis** $\Rightarrow$ $dy = 0$
  - i.e. $\dfrac{dy}{dt} = 0$ (parametric) &nbsp;or&nbsp; numerator of $\dfrac{dy}{dx} = 0$ (implicit)
- A point at which the tangent is **perpendicular to $x$-axis** $\Rightarrow$ $dx = 0$
  - i.e. $\dfrac{dx}{dt} = 0$ (parametric) &nbsp;or&nbsp; denominator of $\dfrac{dy}{dx} = 0$ (implicit)

<details>
<summary>**왜 dy = 0, dx = 0 으로 구분하는가?**</summary>

Parametric/Implicit에서 기울기는 항상 **분수** 형태:

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$$

**수평 접선 (horizontal tangent / parallel to $x$-axis)** → 기울기 (slope) $= 0$ → 분자 (numerator) $= 0$

$$\frac{dy}{dx} = 0 \iff \frac{dy}{dt} = 0$$

**수직 접선 (vertical tangent / perpendicular to $x$-axis)** → 기울기 (slope) $= \infty$ (정의 불가, undefined) → 분모 (denominator) $= 0$

$$\frac{dy}{dx} = \text{undefined} \iff \frac{dx}{dt} = 0$$

분수 (fraction)가 0이 되려면 위 (분자, numerator)가 0, 무한대가 되려면 아래 (분모, denominator)가 0 — 원리는 explicit의 $\dfrac{dy}{dx} = 0$과 같고, 분자·분모를 **각각 따로 (separately)** 보는 것뿐이다.

*For a fraction to equal zero, the numerator must be zero; for it to be undefined, the denominator must be zero — the principle is the same as setting $\dfrac{dy}{dx} = 0$ in the explicit case, except we treat the numerator and denominator separately.*

</details>

<details>
<summary>**Second derivative test 란?**</summary>

Explicit $y = f(x)$에서 극대/극소 (local max/min)를 판별하는 방법.

**절차 (procedure):**

1. $\dfrac{dy}{dx} = 0$ 을 풀어 stationary point $x = a$ 를 찾는다
2. $\dfrac{d^2y}{dx^2}$를 계산하여 $x = a$에 대입:

| $\dfrac{d^2y}{dx^2}\big|_{x=a}$ | 판정 |
|---|---|
| $> 0$ | 극소 (local minimum) — 아래로 볼록 (concave up) |
| $< 0$ | 극대 (local maximum) — 위로 볼록 (concave down) |
| $= 0$ | 판별 불가 (inconclusive) → 부호 변화 (sign change)로 직접 확인 |

**Implicit/Parametric에서 번거로운 이유 (why it's inconvenient):** $\dfrac{dy}{dx}$가 이미 $x$, $y$ 모두 포함한 복잡한 식이라, 한 번 더 미분하면 식이 매우 복잡해진다. 그래서 대신 $\dfrac{dy}{dx}$의 **부호 변화 (sign change)**를 직접 확인하는 방법을 쓴다.

*Since $\dfrac{dy}{dx}$ already involves both $x$ and $y$, differentiating once more yields a very complicated expression. Instead, we directly check the sign change of $\dfrac{dy}{dx}$:*

| $P$ 왼쪽 (left of $P$) | $P$ | $P$ 오른쪽 (right of $P$) | 판정 |
|:---:|:---:|:---:|---|
| $+$ | $0$ | $-$ | 극대 (local maximum) |
| $-$ | $0$ | $+$ | 극소 (local minimum) |
| $+$ | $0$ | $+$ | Stationary point of inflection (극값 아님, not a turning point) |

</details>
:::

::: {style="font-size: 0.83em; color: #555; margin-top: -0.4em; margin-bottom: 1.2em;"}
**용어 정리**

| 한국어 | 영어 | 설명 |
|---|---|---|
| 정류점 (접선이 수평) | **Stationary point** | $\dfrac{dy}{dx} = 0$인 모든 점 |
| 극값점 (극대/극소) | **Turning point** | Stationary point 중 기울기 부호가 바뀌는 점 (local max/min) |
| 변곡점 | **Point of inflection** | 곡선의 오목/볼록이 바뀌는 점 — $\dfrac{d^2y}{dx^2} = 0$이고 부호 변화 |

> Turning point ⊂ Stationary point. 변곡점은 $\dfrac{dy}{dx} = 0$일 필요 없음 (단, $\dfrac{dy}{dx} = 0$이면서 변곡점인 경우 → *stationary point of inflection*).

<details>
<summary>**Stationary point인데 turning point가 아닌 경우는?**</summary>

→ **Stationary point of inflection**

**예시:** $y = x^3$ at $x = 0$

$$\frac{dy}{dx} = 3x^2 \implies \left.\frac{dy}{dx}\right|_{x=0} = 0 \quad \checkmark \text{ (stationary point)}$$

그런데 기울기 부호 (sign of gradient)를 확인하면:

| 구간 (interval) | $\dfrac{dy}{dx} = 3x^2$ | 부호 (sign) |
|---|---|---|
| $x < 0$ | $3x^2 > 0$ | $+$ |
| $x = 0$ | $0$ | $0$ |
| $x > 0$ | $3x^2 > 0$ | $+$ |

부호가 **바뀌지 않음 (no sign change)** → turning point 아님. 대신 이 점에서 곡선의 오목/볼록 (concavity)이 바뀌므로 → **point of inflection**.

*The sign does not change, so this is not a turning point. However, since the concavity of the curve changes at this point, it is a point of inflection.*

| | $\dfrac{dy}{dx} = 0$ | 기울기 부호 변화 | $\dfrac{d^2y}{dx^2} = 0$ |
|---|:---:|:---:|:---:|
| Turning point | ✓ | ✓ | 보통 ✓ |
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
