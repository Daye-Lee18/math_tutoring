# Differential Equations — Trig Integration Intensive Practice

> **Target:** Students who get stuck on DEs that involve trig integration  
> **Contents:** Types A–E, 21 questions in total with full solutions  
> **Prerequisites:** $\tan^2 x = \sec^2 x - 1$, $\sin^2 x = \frac{1-\cos 2x}{2}$, $\cos^2 x = \frac{1+\cos 2x}{2}$, $\sin x\cos x = \frac{\sin 2x}{2}$

## Contents

- [Essential Integration Formulae](#essential-integration-formulae)
- [Type A — Direct Integration](#type-a--direct-integration)
- [Type B — Separable, Identity on x Side](#type-b--separable-identity-on-x-side)
- [Type C — Separable, Trig on y Side](#type-c--separable-trig-on-y-side)
- [Type D — Trig functions on both sides](#type-d--trig-functions-on-both-sides)
- [Type E — Challenging mixed: particular solutions with trig](#type-e--challenging-mixed-particular-solutions-with-trig)
- [Type Summary](#type-summary)

---

## Essential Integration Formulae

| Integral | Result | Key conversion |
|---|---|---|
| $\int \sec^2 x\,dx$ | $\tan x + C$ | — |
| $\int \tan^2 x\,dx$ | $\tan x - x + C$ | Apply $\tan^2 x = \sec^2 x - 1$ first |
| $\int \sin^2 x\,dx$ | $\frac{x}{2} - \frac{\sin 2x}{4} + C$ | Apply $\sin^2 x = \frac{1-\cos 2x}{2}$ first |
| $\int \cos^2 x\,dx$ | $\frac{x}{2} + \frac{\sin 2x}{4} + C$ | Apply $\cos^2 x = \frac{1+\cos 2x}{2}$ first |
| $\int \tan x\,dx$ | $\ln\|\sec x\| + C$ | $= -\ln\|\cos x\| + C$ |
| $\int \sin x\cos x\,dx$ | $\frac{1}{2}\sin^2 x + C$ | $= -\frac{1}{4}\cos 2x + C$ |
| $\int \cot x\,dx$ | $\ln\|\sin x\| + C$ | |
| $\int \frac{1}{\sin x\cos x}\,dx$ | $\ln\|\tan x\| + C$ | $\frac{1}{\sin x\cos x} = \frac{2}{\sin 2x} = 2\csc 2x$ |

---

## Type A — Direct Integration

> Form $\frac{dy}{dx} = f(x)$: no $y$ present, so integrate the right-hand side directly.  
> **Common sticking point:** $\tan^2 x$ and $\sin^2 x$ cannot be integrated directly — convert using an identity first.

---

### A1. $\dfrac{dy}{dx} = \tan^2 x$

<details>
<summary>Solution</summary>

Apply $\tan^2 x = \sec^2 x - 1$:

$$y = \int \tan^2 x\,dx = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$\boxed{y = \tan x - x + C} \tag{A1}$$

</details>

---

### A2. $\dfrac{dy}{dx} = \sin^2 x$

<details>
<summary>Solution</summary>

Apply $\sin^2 x = \dfrac{1-\cos 2x}{2}$:

$$y = \int \frac{1-\cos 2x}{2}\,dx \tag{M1}$$

$$\boxed{y = \frac{x}{2} - \frac{\sin 2x}{4} + C} \tag{A1}$$

</details>

---

### A3. $\dfrac{dy}{dx} = \cos^2 x,\quad y = 1 \text{ when } x = 0$

<details>
<summary>Solution</summary>

Apply $\cos^2 x = \dfrac{1+\cos 2x}{2}$:

$$y = \int \frac{1+\cos 2x}{2}\,dx = \frac{x}{2} + \frac{\sin 2x}{4} + C \tag{M1 A1}$$

Initial condition $x=0,\ y=1$:

$$1 = 0 + 0 + C \implies C = 1 \tag{M1}$$

$$\boxed{y = \frac{x}{2} + \frac{\sin 2x}{4} + 1} \tag{A1}$$

</details>

---

### A4. $\dfrac{dy}{dx} = 3\tan^2 x + 2\sec^2 x$

<details>
<summary>Solution</summary>

$$y = \int (3\tan^2 x + 2\sec^2 x)\,dx = \int (3(\sec^2 x - 1) + 2\sec^2 x)\,dx \tag{M1}$$

$$= \int (5\sec^2 x - 3)\,dx$$

$$\boxed{y = 5\tan x - 3x + C} \tag{A1}$$

</details>

---

### A5. $\dfrac{dy}{dx} = \sin^2 x \cdot \cos^2 x$

<details>
<summary>Solution</summary>

Apply $\sin^2 x\cos^2 x = \dfrac{\sin^2 2x}{4} = \dfrac{1-\cos 4x}{8}$:

$$y = \int \frac{1-\cos 4x}{8}\,dx \tag{M1}$$

$$\boxed{y = \frac{x}{8} - \frac{\sin 4x}{32} + C} \tag{A1}$$

> **Derivation:** $\sin^2 x \cos^2 x = (\sin x \cos x)^2 = \left(\frac{\sin 2x}{2}\right)^2 = \frac{\sin^2 2x}{4}$, then apply $\sin^2 2x = \frac{1-\cos 4x}{2}$.

</details>

---

## Type B — Separable, Identity on x Side

> After separating variables, a trig identity conversion is needed to integrate the $x$ side.  
> **Common sticking point:** Variables are separated correctly, but stuck at $\int \tan^2 x\,dx$ or $\int \sin^2 x\,dx$.

---

### B1. $\dfrac{dy}{dx} = y\tan^2 x$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{y} = \tan^2 x\,dx = (\sec^2 x - 1)\,dx \tag{M1}$$

$$\int \frac{dy}{y} = \int (\sec^2 x - 1)\,dx$$

$$\ln|y| = \tan x - x + C \tag{A1}$$

$$\boxed{y = Ae^{\tan x - x}} \tag{A1}$$

</details>

---

### B2. $\cos^2 x\,\dfrac{dy}{dx} = y^2\sin^2 x$

> *(variant of core_concepts Example — make sure you know this)*

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{y^2} = \frac{\sin^2 x}{\cos^2 x}\,dx = \tan^2 x\,dx \tag{M1}$$

$$\int y^{-2}\,dy = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$-\frac{1}{y} = \tan x - x + C \tag{A1}$$

$$\boxed{y = \frac{-1}{\tan x - x + C}} \tag{A1}$$

</details>

---

### B3. $\dfrac{dy}{dx} = \dfrac{y\sin^2 x}{\cos^2 x},\quad y = 2 \text{ when } x = 0$

<details>
<summary>Solution</summary>

Since $\dfrac{\sin^2 x}{\cos^2 x} = \tan^2 x = \sec^2 x - 1$:

$$\frac{dy}{y} = (\sec^2 x - 1)\,dx \tag{M1}$$

$$\ln|y| = \tan x - x + C \tag{A1}$$

Initial condition $x=0,\ y=2$:

$$\ln 2 = 0 - 0 + C \implies C = \ln 2 \tag{M1}$$

$$\ln|y| = \tan x - x + \ln 2$$

$$\boxed{y = 2e^{\tan x - x}} \tag{A1}$$

</details>

---

### B4. $\sec^2 x\,\dfrac{dy}{dx} = y$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{y} = \frac{dx}{\sec^2 x} = \cos^2 x\,dx = \frac{1+\cos 2x}{2}\,dx \tag{M1}$$

$$\ln|y| = \frac{x}{2} + \frac{\sin 2x}{4} + C \tag{A1}$$

$$\boxed{y = Ae^{\,x/2\;+\;\sin 2x/4}} \tag{A1}$$

</details>

---

### B5. $\dfrac{dy}{dx} = y^2\sin^2 x,\quad y = 1 \text{ when } x = \dfrac{\pi}{2}$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{y^2} = \sin^2 x\,dx = \frac{1-\cos 2x}{2}\,dx \tag{M1}$$

$$-\frac{1}{y} = \frac{x}{2} - \frac{\sin 2x}{4} + C \tag{A1}$$

Initial condition $x = \dfrac{\pi}{2},\ y = 1$: $\quad \sin\pi = 0$, so

$$-1 = \frac{\pi}{4} - 0 + C \implies C = -1 - \frac{\pi}{4} \tag{M1}$$

$$-\frac{1}{y} = \frac{x}{2} - \frac{\sin 2x}{4} - 1 - \frac{\pi}{4}$$

$$\boxed{y = \dfrac{-1}{\dfrac{x}{2} - \dfrac{\sin 2x}{4} - 1 - \dfrac{\pi}{4}}} \tag{A1}$$

</details>

---

## Type C — Separable, Trig on y Side

> After separating variables, a trig integral involving $y$ appears.  
> Examples: $\int \sin y\,dy$, $\int \cos y\,dy$, $\int \sec^2 y\,dy$, etc.

---

### C1. $\dfrac{dy}{dx} = \cos y\cdot\sec^2 x,\quad y = \dfrac{\pi}{4} \text{ when } x = 0$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{\cos y} = \sec^2 x\,dx \implies \sec y\,dy = \sec^2 x\,dx \tag{M1}$$

$$\int \sec y\,dy = \int \sec^2 x\,dx$$

$$\ln|\sec y + \tan y| = \tan x + C \tag{A1}$$

Initial condition $x=0,\ y=\dfrac{\pi}{4}$: $\;\sec\frac{\pi}{4} = \sqrt{2},\; \tan\frac{\pi}{4} = 1$

$$\ln(\sqrt{2}+1) = 0 + C \implies C = \ln(\sqrt{2}+1) \tag{M1}$$

$$\boxed{\ln|\sec y + \tan y| = \tan x + \ln(\sqrt{2}+1)} \tag{A1}$$

</details>

---

### C2. $\cos^2 y\,\dfrac{dy}{dx} = e^x$

<details>
<summary>Solution</summary>

Separate variables:

$$\cos^2 y\,dy = e^x\,dx \tag{M1}$$

$$\int \cos^2 y\,dy = \int e^x\,dx$$

$$\int \frac{1+\cos 2y}{2}\,dy = e^x + C$$

$$\frac{y}{2} + \frac{\sin 2y}{4} = e^x + C \tag{A1}$$

$$\boxed{\frac{y}{2} + \frac{\sin 2y}{4} = e^x + C} \tag{A1}$$

> $y$ cannot be made explicit — the implicit form is the final answer.

</details>

---

### C3. $\dfrac{dy}{dx} = \tan^2 y\cdot x^2$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{\tan^2 y} = x^2\,dx \implies \frac{\cos^2 y}{\sin^2 y}\,dy = x^2\,dx \tag{M1}$$

$$\int \cot^2 y\,dy = \int x^2\,dx$$

Since $\cot^2 y = \csc^2 y - 1$:

$$\int (\csc^2 y - 1)\,dy = \int x^2\,dx \tag{M1}$$

$$-\cot y - y = \frac{x^3}{3} + C \tag{A1}$$

$$\boxed{-\cot y - y = \frac{x^3}{3} + C} \tag{A1}$$

</details>

---

## Type D — Trig functions on both sides

> The most challenging type. After separating variables, an identity conversion or substitution is needed on both sides.

---

### D1. $\sin y\,\dfrac{dy}{dx} = \cos x\cos^2 y$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{\sin y}{\cos^2 y}\,dy = \cos x\,dx \implies \sec y\tan y\,dy = \cos x\,dx \tag{M1}$$

$$\int \sec y\tan y\,dy = \int \cos x\,dx$$

$$\sec y = \sin x + C \tag{A1}$$

$$\boxed{\frac{1}{\cos y} = \sin x + C} \tag{A1}$$

</details>

---

### D2. $\dfrac{dy}{dx} = \dfrac{\tan^2 x}{\tan^2 y}$

<details>
<summary>Solution</summary>

Separate variables:

$$\tan^2 y\,dy = \tan^2 x\,dx \tag{M1}$$

Apply $\tan^2 = \sec^2 - 1$ to both sides:

$$\int (\sec^2 y - 1)\,dy = \int (\sec^2 x - 1)\,dx \tag{M1}$$

$$\tan y - y = \tan x - x + C \tag{A1}$$

$$\boxed{\tan y - y = \tan x - x + C} \tag{A1}$$

</details>

---

### D3. $\dfrac{dy}{dx} = \dfrac{\sin^2 y}{\sin x\cos x},\quad y = \dfrac{\pi}{4} \text{ when } x = \dfrac{\pi}{4}$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{\sin^2 y} = \frac{dx}{\sin x\cos x} \tag{M1}$$

Left side: $\int \csc^2 y\,dy = -\cot y$

Right side: $\dfrac{1}{\sin x\cos x} = \dfrac{2}{\sin 2x} = 2\csc 2x$

$$\int 2\csc 2x\,dx = \ln|\tan x| + C \tag{M1}$$

$$-\cot y = \ln|\tan x| + C \tag{A1}$$

Initial condition $x=\frac{\pi}{4},\ y=\frac{\pi}{4}$: $\;\cot\frac{\pi}{4} = 1,\;\tan\frac{\pi}{4} = 1$

$$-1 = \ln 1 + C \implies C = -1 \tag{M1}$$

$$\boxed{-\cot y = \ln|\tan x| - 1} \tag{A1}$$

</details>

---

### D4. $\cos^2 x\,\dfrac{dy}{dx} = \sin^2 y$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{\sin^2 y} = \frac{dx}{\cos^2 x} \implies \csc^2 y\,dy = \sec^2 x\,dx \tag{M1}$$

$$\int \csc^2 y\,dy = \int \sec^2 x\,dx$$

$$-\cot y = \tan x + C \tag{A1}$$

$$\boxed{\cot y + \tan x + C = 0} \tag{A1}$$

</details>

---

## Type E — Challenging mixed: particular solutions with trig

> Combined problems mixing several types.

---

### E1. $\dfrac{dy}{dx} = \sin x\cos^2 x,\quad y = 0 \text{ when } x = \dfrac{\pi}{3}$

> *(core_concepts Ex 2(i) — revision check)*

<details>
<summary>Solution</summary>

$$dy = \sin x\cos^2 x\,dx \tag{M1}$$

Substitution $u = \cos x,\; du = -\sin x\,dx$:

$$y = -\int u^2\,du = -\frac{\cos^3 x}{3} + C \tag{A1}$$

Initial condition $x=\frac{\pi}{3},\ y=0$: $\;\cos\frac{\pi}{3} = \frac{1}{2}$

$$0 = -\frac{(1/2)^3}{3} + C = -\frac{1}{24} + C \implies C = \frac{1}{24} \tag{M1}$$

$$\boxed{y = -\frac{\cos^3 x}{3} + \frac{1}{24}} \tag{A1}$$

</details>

---

### E2. $\dfrac{dy}{dx} = \dfrac{\sec^2 x}{y+1},\quad y = 0 \text{ when } x = 0$

<details>
<summary>Solution</summary>

Separate variables:

$$(y+1)\,dy = \sec^2 x\,dx \tag{M1}$$

$$\frac{(y+1)^2}{2} = \tan x + C \tag{A1}$$

Initial condition $x=0,\ y=0$:

$$\frac{1}{2} = 0 + C \implies C = \frac{1}{2} \tag{M1}$$

$$\frac{(y+1)^2}{2} = \tan x + \frac{1}{2} \implies (y+1)^2 = 2\tan x + 1$$

$$\boxed{y = -1 + \sqrt{2\tan x + 1}} \tag{A1}$$

(take the positive root since $y \geq 0$)

</details>

---

### E3. $(1 + \cos x)\,\dfrac{dy}{dx} = y\sin x,\quad y = 2 \text{ when } x = \pi$

<details>
<summary>Solution</summary>

Separate variables:

$$\frac{dy}{y} = \frac{\sin x}{1+\cos x}\,dx \tag{M1}$$

Right side: substitution $u = 1+\cos x,\; du = -\sin x\,dx$

$$\int \frac{\sin x}{1+\cos x}\,dx = \int \frac{-du}{u} = -\ln|1+\cos x| \tag{M1}$$

$$\ln|y| = -\ln|1+\cos x| + C \tag{A1}$$

Initial condition $x=\pi,\ y=2$: $\;1+\cos\pi = 1-1 = 0$ ...

> **Note:** At $x = \pi$, $1+\cos\pi = 0$ — the denominator is zero and the solution is undefined there. Changing the initial condition to $x = 0$:

Corrected: $x=0,\ y=2$: $\;1+\cos 0 = 2$

$$\ln 2 = -\ln 2 + C \implies C = 2\ln 2 = \ln 4 \tag{M1}$$

$$\ln|y| = \ln 4 - \ln|1+\cos x| = \ln\frac{4}{1+\cos x}$$

$$\boxed{y = \frac{4}{1+\cos x}} \tag{A1}$$

</details>

---

### E4. $\dfrac{dy}{dx} = \dfrac{e^y}{\cos^2 x},\quad y = 0 \text{ when } x = \dfrac{\pi}{4}$

<details>
<summary>Solution</summary>

Separate variables:

$$e^{-y}\,dy = \frac{dx}{\cos^2 x} = \sec^2 x\,dx \tag{M1}$$

$$\int e^{-y}\,dy = \int \sec^2 x\,dx$$

$$-e^{-y} = \tan x + C \tag{A1}$$

Initial condition $x=\frac{\pi}{4},\ y=0$: $\;\tan\frac{\pi}{4} = 1$

$$-1 = 1 + C \implies C = -2 \tag{M1}$$

$$-e^{-y} = \tan x - 2 \implies e^{-y} = 2 - \tan x$$

$$\boxed{y = -\ln(2 - \tan x)} \tag{A1}$$

> **Domain note:** Requires $2 - \tan x > 0$, so the solution is only valid where $\tan x < 2$.

</details>

---

## Type Summary

| Pattern on right-hand side | Why students get stuck | Fix |
|---|---|---|
| $\tan^2 x$ | Cannot integrate directly | Convert to $\sec^2 x - 1$, then integrate |
| $\sin^2 x$ or $\cos^2 x$ | Cannot integrate directly | Convert using the half-angle formula |
| $\frac{\sin^2 x}{\cos^2 x}$ | Fails to recognise $= \tan^2 x$ | Write as $\tan^2 x$ first → then $\sec^2 x - 1$ |
| $\sin x\cos^2 x$ | Unsure which substitution | $u = \cos x$ (its derivative $-\sin x$ is already present) |
| $\frac{1}{\sin x\cos x}$ | Unsure how to integrate | $= \frac{2}{\sin 2x}$, then $\ln\|\tan x\|$ |
| $\cot^2 y$ (on $y$ side) | Unfamiliar with $\cot^2$ | Convert to $\csc^2 y - 1$ |
| $\sec y \tan y$ (on $y$ side) | Fails to recognise $= \frac{d}{dy}\sec y$ | $\int \sec y\tan y\,dy = \sec y$ |
