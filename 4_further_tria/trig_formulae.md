# Trigonometry — Formula Sheet

## Reciprocal Identities

| | Formula |
|---|---------|
| $\sec x$ | $\dfrac{1}{\cos x}$ |
| $\csc x$ | $\dfrac{1}{\sin x}$ |
| $\cot x$ | $\dfrac{1}{\tan x} = \dfrac{\cos x}{\sin x}$ |

---

## Pythagorean Identities

| # | Formula |
|---|---------|
| 1 | $\sin^2 x + \cos^2 x = 1$ |
| 2 | $1 + \tan^2 x = \sec^2 x$ |
| 3 | $\cot^2 x + 1 = \csc^2 x$ |

---

## Angle Sum & Difference

| | Formula |
|---|---------|
| $\sin(A \pm B)$ | $\sin A\cos B \pm \cos A\sin B$ |
| $\cos(A \pm B)$ | $\cos A\cos B \mp \sin A\sin B$ |
| $\tan(A \pm B)$ | $\dfrac{\tan A \pm \tan B}{1 \mp \tan A\tan B}$ |

---

## Double Angle

| | Formula |
|---|---------|
| $\sin 2x$ | $2\sin x\cos x$ |
| $\cos 2x$ | $\cos^2 x - \sin^2 x$ |
| | $= 2\cos^2 x - 1$ |
| | $= 1 - 2\sin^2 x$ |
| $\tan 2x$ | $\dfrac{2\tan x}{1 - \tan^2 x}$ |

---

## Triple Angle

| | Formula |
|---|---------|
| $\sin 3x$ | $3\sin x - 4\sin^3 x$ |
| $\cos 3x$ | $4\cos^3 x - 3\cos x$ |

---

## Half Angle

*삼각함수 제곱 → $\cos 2x$ 형태로 변환 (derived from Pythagorean + Double Angle)*

| | Formula |
|---|---------|
| $\sin^2 x$ | $\dfrac{1 - \cos 2x}{2}$ |
| $\cos^2 x$ | $\dfrac{1 + \cos 2x}{2}$ |
| $\tan^2 x$ | $\dfrac{1 - \cos 2x}{1 + \cos 2x}$ |

---

## R-form (Compound Angle)

$$a\sin x + b\cos x = R\sin(x + \alpha)$$
$$a\cos x + b\sin x = R\cos(x - \alpha)$$

| | Formula |
|---|---------|
| $R$ | $\sqrt{a^2 + b^2}$ |
| $\alpha$ | $\tan^{-1}\!\left(\dfrac{b}{a}\right)$ |

---

## Sum-to-Product

| | Formula |
|---|---------|
| $\sin P + \sin Q$ | $2\sin\dfrac{P+Q}{2}\cos\dfrac{P-Q}{2}$ |
| $\sin P - \sin Q$ | $2\cos\dfrac{P+Q}{2}\sin\dfrac{P-Q}{2}$ |
| $\cos P + \cos Q$ | $2\cos\dfrac{P+Q}{2}\cos\dfrac{P-Q}{2}$ |
| $\cos P - \cos Q$ | $-2\sin\dfrac{P+Q}{2}\sin\dfrac{P-Q}{2}$ |

---

## Product-to-Sum

| | Formula |
|---|---------|
| $\sin A\cos B$ | $\dfrac{1}{2}[\sin(A+B) + \sin(A-B)]$ |
| $\cos A\sin B$ | $\dfrac{1}{2}[\sin(A+B) - \sin(A-B)]$ |
| $\cos A\cos B$ | $\dfrac{1}{2}[\cos(A-B) + \cos(A+B)]$ |
| $\sin A\sin B$ | $\dfrac{1}{2}[\cos(A-B) - \cos(A+B)]$ |

---

## Derivatives

| $f(x)$ | $f'(x)$ |
|--------|---------|
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |
| $\tan x$ | $\sec^2 x$ |
| $\sec x$ | $\sec x\tan x$ |
| $\csc x$ | $-\csc x\cot x$ |
| $\cot x$ | $-\csc^2 x$ |

---

## Integrals

> **이것만 외우면 끝:**
> 단일 함수 6개 ($\sin$, $\cos$, $\tan$, $\cot$, $\sec$★, $\csc$★) +
> 제곱 6개 ($\sin^2$, $\cos^2$, $\tan^2$, $\cot^2$, $\sec^2$, $\csc^2$) +
> 곱 2개 ($\sec\tan$, $\csc\cot$)
> — 나머지는 이 형태로 변환하는 테크닉의 문제

| $f(x)$ | $\int f(x)\,dx$ |
|--------|----------------|
| $\sin x$ | $-\cos x + C$ |
| $\cos x$ | $\sin x + C$ |
| $\tan x$ | $\ln\|\sec x\| + C$ |
| $\cot x$ | $-\ln\|\csc x\| + C$ |
| $\sec x$ | $\ln\|\sec x + \tan x\| + C$ &nbsp; ★ |
| $\csc x$ | $-\ln\|\csc x + \cot x\| + C$ &nbsp; ★ |
| $\sec^2 x$ | $\tan x + C$ |
| $\csc^2 x$ | $-\cot x + C$ |
| $\sec x\tan x$ | $\sec x + C$ |
| $\csc x\cot x$ | $-\csc x + C$ |
| $\sin^2 x$ | $\dfrac{x}{2} - \dfrac{\sin 2x}{4} + C$ |
| $\cos^2 x$ | $\dfrac{x}{2} + \dfrac{\sin 2x}{4} + C$ |
| $\tan^2 x$ | $\tan x - x + C$ |
| $\cot^2 x$ | $-\cot x - x + C$ |

★ FP (Further Pure) only — P3/P4에서는 시험에서 유도 과정 주어짐

---

### Derivations

<details>
<summary>$\int \sec x\,dx$ 유도</summary>

분자·분모에 $(\sec x + \tan x)$를 곱한다:

$$\int \sec x\,dx = \int \sec x \cdot \frac{\sec x + \tan x}{\sec x + \tan x}\,dx = \int \frac{\sec^2 x + \sec x\tan x}{\sec x + \tan x}\,dx$$

$u = \sec x + \tan x$으로 치환하면 $du = (\sec x\tan x + \sec^2 x)\,dx$ — 분자와 정확히 일치:

$$= \int \frac{1}{u}\,du = \ln|u| + C = \ln|\sec x + \tan x| + C$$

</details>

<details>
<summary>$\int \csc x\,dx$ 유도</summary>

분자·분모에 $(\csc x + \cot x)$를 곱한다:

$$\int \csc x\,dx = \int \csc x \cdot \frac{\csc x + \cot x}{\csc x + \cot x}\,dx = \int \frac{\csc^2 x + \csc x\cot x}{\csc x + \cot x}\,dx$$

$u = \csc x + \cot x$으로 치환하면 $du = (-\csc x\cot x - \csc^2 x)\,dx$ — 분자에 $-1$을 곱한 것:

$$= \int \frac{-1}{u}\,du = -\ln|u| + C = -\ln|\csc x + \cot x| + C$$

</details>

<details>
<summary>$\int \sin^2 x\,dx$,  $\int \cos^2 x\,dx$ 유도</summary>

Half angle 공식으로 제곱을 없앤다:

$$\int \sin^2 x\,dx = \int \frac{1 - \cos 2x}{2}\,dx = \frac{x}{2} - \frac{\sin 2x}{4} + C$$

$$\int \cos^2 x\,dx = \int \frac{1 + \cos 2x}{2}\,dx = \frac{x}{2} + \frac{\sin 2x}{4} + C$$

</details>

<details>
<summary>$\int \tan^2 x\,dx$,  $\int \cot^2 x\,dx$ 유도</summary>

Pythagorean identity로 $\sec^2$ 또는 $\csc^2$ 형태로 바꾼다:

$$\int \tan^2 x\,dx = \int (\sec^2 x - 1)\,dx = \tan x - x + C$$

$$\int \cot^2 x\,dx = \int (\csc^2 x - 1)\,dx = -\cot x - x + C$$

</details>
