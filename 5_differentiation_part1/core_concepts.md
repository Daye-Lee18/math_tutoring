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

#### Formula Table (by pattern group)

**[Group A] sin / cos — 4-cycle**

| Function | Derivative | Sign |
|----------|------------|------|
| $(\sin x)'$ | $= \cos x$ | $+$ |
| $(\cos x)'$ | $= -\sin x$ | $-$ ← **co**sine |

**[Group B] tan / sec pair**

| Function | Derivative | Pattern |
|----------|------------|---------|
| ▶ $(\tan x)'$ | $= \sec^2 x$ | $+$ · differentiating tan produces sec |
| ▶ $(\sec x)'$ | $= \sec x \tan x$ | $+$ · sec survives as a factor |

**[Group C] cot / csc pair — the "co-" version of Group B (all negative)**

| Function | Derivative | Pattern |
|----------|------------|---------|
| ▶ $(\cot x)'$ | $= -\csc^2 x$ | $-$ · differentiating **co**t produces csc |
| ▶ $(\csc x)'$ | $= -\csc x \cot x$ | $-$ · **co**sc survives as a factor |

**[Group D] Inverse trigonometric functions**

| Function | Derivative | Pattern |
|----------|------------|---------|
| ▶ $(\arcsin x)'$ | $= \dfrac{1}{\sqrt{1-x^2}}$ | $+$ |
| ▶ $(\arccos x)'$ | $= -\dfrac{1}{\sqrt{1-x^2}}$ | $-$ ← **arc·co**s, same co- rule |
| ▶ $(\arctan x)'$ | $= \dfrac{1}{1+x^2}$ | $+$ · memorise separately |

---

#### Memory Tips

**Tip 1 — "co-" prefix always means negative**

Every function whose derivative carries a minus sign starts with "co-":

$$\cos,\quad \cot,\quad \csc,\quad \arccos \quad \longrightarrow \text{ all } (-)$$

> Remember this and the sign of all 9 formulas is solved.

**Tip 2 — tan↔sec, cot↔csc travel in pairs**

Differentiating produces the partner from the same pair:

$$\tan' = \sec^2 \quad\longleftrightarrow\quad \cot' = -\csc^2$$
$$\sec' = \sec\cdot\tan \quad\longleftrightarrow\quad \csc' = -\csc\cdot\cot$$

> Memorise Group B (tan/sec); derive Group C by replacing everything with "co-" and negating.

**Tip 3 — sec / csc survive in their own derivative**

$$(\sec x)' = \underbrace{\sec x}_{\text{itself}} \cdot \tan x \qquad (\csc x)' = -\underbrace{\csc x}_{\text{itself}} \cdot \cot x$$

> Like $e^x$, after differentiation the function itself remains as a factor.

**Tip 4 — sin/cos form a 4-cycle**

$$\sin \xrightarrow{\;'\;} \cos \xrightarrow{\;'\;} -\sin \xrightarrow{\;'\;} -\cos \xrightarrow{\;'\;} \sin \xrightarrow{\;'\;} \cdots$$

> Four differentiations return to the original. Think "shift forward by one step".

**Tip 5 — derive inverse trig derivatives rather than memorising them**

If $y = \arcsin x$ then $x = \sin y$. Differentiate both sides with respect to $x$:

$$1 = \cos y \cdot \frac{dy}{dx} \implies \frac{dy}{dx} = \frac{1}{\cos y} = \frac{1}{\sqrt{1-\sin^2 y}} = \frac{1}{\sqrt{1-x^2}}$$

The same method gives $\arccos$ and $\arctan$. ($\arccos$: start with $x = \cos y$ → result carries a minus sign.)

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
