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

*Convert squared trig functions to $\cos 2x$ form (derived from Pythagorean + Double Angle identities)*

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

> **These are all you need to memorise:**
> 6 single functions ($\sin$, $\cos$, $\tan$, $\cot$, $\sec$★, $\csc$★) +
> 6 squared functions ($\sin^2$, $\cos^2$, $\tan^2$, $\cot^2$, $\sec^2$, $\csc^2$) +
> 2 products ($\sec\tan$, $\csc\cot$)
> — everything else is a matter of converting to one of these forms

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

★ FP (Further Pure) only — in P3/P4 the derivation is provided in the exam

---

### Derivations

<details>
<summary>$\int \sec x\,dx$ derivation</summary>

Multiply numerator and denominator by $(\sec x + \tan x)$:

$$\int \sec x\,dx = \int \sec x \cdot \frac{\sec x + \tan x}{\sec x + \tan x}\,dx = \int \frac{\sec^2 x + \sec x\tan x}{\sec x + \tan x}\,dx$$

Substitute $u = \sec x + \tan x$, so $du = (\sec x\tan x + \sec^2 x)\,dx$ — exactly the numerator:

$$= \int \frac{1}{u}\,du = \ln|u| + C = \ln|\sec x + \tan x| + C$$

</details>

<details>
<summary>$\int \csc x\,dx$ derivation</summary>

Multiply numerator and denominator by $(\csc x + \cot x)$:

$$\int \csc x\,dx = \int \csc x \cdot \frac{\csc x + \cot x}{\csc x + \cot x}\,dx = \int \frac{\csc^2 x + \csc x\cot x}{\csc x + \cot x}\,dx$$

Substitute $u = \csc x + \cot x$, so $du = (-\csc x\cot x - \csc^2 x)\,dx$ — the numerator multiplied by $-1$:

$$= \int \frac{-1}{u}\,du = -\ln|u| + C = -\ln|\csc x + \cot x| + C$$

</details>

<details>
<summary>$\int \sin^2 x\,dx$,  $\int \cos^2 x\,dx$ derivation</summary>

Use the half-angle identities to eliminate the squares:

$$\int \sin^2 x\,dx = \int \frac{1 - \cos 2x}{2}\,dx = \frac{x}{2} - \frac{\sin 2x}{4} + C$$

$$\int \cos^2 x\,dx = \int \frac{1 + \cos 2x}{2}\,dx = \frac{x}{2} + \frac{\sin 2x}{4} + C$$

</details>

<details>
<summary>$\int \tan^2 x\,dx$,  $\int \cot^2 x\,dx$ derivation</summary>

Use the Pythagorean identity to rewrite as $\sec^2$ or $\csc^2$:

$$\int \tan^2 x\,dx = \int (\sec^2 x - 1)\,dx = \tan x - x + C$$

$$\int \cot^2 x\,dx = \int (\csc^2 x - 1)\,dx = -\cot x - x + C$$

</details>
