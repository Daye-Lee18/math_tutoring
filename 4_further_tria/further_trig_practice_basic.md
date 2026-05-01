# Further Trigonometry — Core Practice Mark Scheme

---

## Q01. Find an exact value of sin 75°

**Formula used:** Angle Sum Identity — $\sin(A+B) = \sin A\cos B + \cos A\sin B$

**Why this formula?**
75° is not a standard angle, but it can be written as a sum of two standard angles: $75° = 45° + 30°$.
We know exact values for sin/cos of 45° and 30°, so the Angle Sum identity lets us find sin 75° exactly without a calculator.

**Solution:**

$$\sin 75° = \sin(45° + 30°)$$

$$= \sin 45°\cos 30° + \cos 45°\sin 30° \tag{M1}$$

$$= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2} \cdot \frac{1}{2} \tag{M1}$$

$$= \frac{\sqrt{6}}{4} + \frac{\sqrt{2}}{4}$$

$$\boxed{\sin 75° = \frac{\sqrt{6}+\sqrt{2}}{4}} \tag{A1}$$

---

## Q02. Solve $2\cos^2 x + \sin x = 1$, $\quad 0 \leq x \leq 2\pi$ &emsp; **(C2)**

**Formula used:** Basic Identity — $\cos^2 x = 1 - \sin^2 x$

**Why this formula?**
The equation contains both $\cos^2 x$ and $\sin x$ — two different trig functions of the **same angle**. The hint (C2) confirms: use a Basic Identity to convert everything into a **single trig function**, then solve as a quadratic.

**Solution:**

Replace $\cos^2 x$ using $\cos^2 x = 1 - \sin^2 x$:

$$2(1 - \sin^2 x) + \sin x = 1 \tag{M1}$$

$$2 - 2\sin^2 x + \sin x = 1$$

$$2\sin^2 x - \sin x - 1 = 0 \tag{A1}$$

Factorise:

$$(2\sin x + 1)(\sin x - 1) = 0 \tag{M1}$$

$$\sin x = -\frac{1}{2} \qquad \text{or} \qquad \sin x = 1$$

Solving in $[0, 2\pi]$:

- $\sin x = 1 \;\Rightarrow\; x = \dfrac{\pi}{2}$
- $\sin x = -\dfrac{1}{2} \;\Rightarrow\; x = \pi + \dfrac{\pi}{6} = \dfrac{7\pi}{6}, \quad x = 2\pi - \dfrac{\pi}{6} = \dfrac{11\pi}{6}$

$$\boxed{x = \frac{\pi}{2},\quad \frac{7\pi}{6},\quad \frac{11\pi}{6}} \tag{A1 each}$$

---

## Q03. Solve $2\sec^2 x + \tan x = 3$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Basic Identity — $\sec^2 x = 1 + \tan^2 x$

**Why this formula?**
The equation contains $\sec^2 x$ and $\tan x$ — different trig functions of the **same angle**. Since $\sec^2 x = 1 + \tan^2 x$ (from dividing $\cos^2 x + \sin^2 x = 1$ by $\cos^2 x$), we can convert everything into $\tan x$ and solve as a quadratic.

**Solution:**

Replace $\sec^2 x$ using $\sec^2 x = 1 + \tan^2 x$:

$$2(1 + \tan^2 x) + \tan x = 3 \tag{M1}$$

$$2\tan^2 x + \tan x - 1 = 0 \tag{A1}$$

Factorise:

$$(2\tan x - 1)(\tan x + 1) = 0 \tag{M1}$$

$$\tan x = \frac{1}{2} \qquad \text{or} \qquad \tan x = -1$$

Solving in $[0, 2\pi]$:

- $\tan x = \dfrac{1}{2}$: $x = \arctan\!\left(\dfrac{1}{2}\right),\quad x = \pi + \arctan\!\left(\dfrac{1}{2}\right)$
- $\tan x = -1$: $x = \pi - \dfrac{\pi}{4} = \dfrac{3\pi}{4},\quad x = 2\pi - \dfrac{\pi}{4} = \dfrac{7\pi}{4}$

$$\boxed{x = \arctan\!\tfrac{1}{2},\quad \frac{3\pi}{4},\quad \pi+\arctan\!\tfrac{1}{2},\quad \frac{7\pi}{4}} \tag{A1 each}$$

> **Note:** $\arctan\!\left(\frac{1}{2}\right) \approx 0.464$ rad. If the question asks for exact form, leave as $\arctan\!\left(\frac{1}{2}\right)$.

---

## Q04. Solve $8\cot x - 3\tan x = 2$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Reciprocal Identity — $\cot x = \dfrac{1}{\tan x}$

**Why this formula?**
The equation mixes $\cot x$ and $\tan x$. Since $\cot x = \frac{1}{\tan x}$, substituting $t = \tan x$ eliminates $\cot x$ and converts the equation into a **quadratic in $\tan x$**.

**Solution:**

Let $t = \tan x$. Since $\cot x = \dfrac{1}{\tan x} = \dfrac{1}{t}$:

$$\frac{8}{t} - 3t = 2 \tag{M1}$$

Multiply through by $t$:

$$8 - 3t^2 = 2t$$

$$3t^2 + 2t - 8 = 0 \tag{A1}$$

Factorise:

$$(3t - 4)(t + 2) = 0 \tag{M1}$$

$$\tan x = \frac{4}{3} \qquad \text{or} \qquad \tan x = -2$$

Solving in $[0, 2\pi]$:

- $\tan x = \dfrac{4}{3}$: $x = \arctan\!\left(\dfrac{4}{3}\right),\quad x = \pi + \arctan\!\left(\dfrac{4}{3}\right)$
- $\tan x = -2$: $x = \pi - \arctan 2,\quad x = 2\pi - \arctan 2$

$$\boxed{x = \arctan\!\tfrac{4}{3},\quad \pi-\arctan 2,\quad \pi+\arctan\!\tfrac{4}{3},\quad 2\pi-\arctan 2} \tag{A1 each}$$

> **Note:** $\arctan\!\left(\frac{4}{3}\right) \approx 0.927$ rad, $\arctan 2 \approx 1.107$ rad.

---

## Q05. Solve $\sin x - \sqrt{3}\cos x = 0$, $\quad 0 \leq x \leq 2\pi$ &emsp; **(C2)**

**Formula used:** C2 — Rearrange to $\tan x = -a/b$ form

**Why this formula?**
The RHS is **zero**, so we can divide both sides by $\cos x$ directly (or rearrange). Since $a\sin x + b\cos x = 0$, we just rearrange to $\tan x = \text{const}$. No need for the full Compound formula (D) — C2 is the shortcut when the equation equals 0.

**Solution:**

$$\sin x = \sqrt{3}\cos x \tag{M1}$$

Divide both sides by $\cos x$:

$$\tan x = \sqrt{3} \tag{A1}$$

Solving in $[0, 2\pi]$:

$$x = \frac{\pi}{3}, \qquad x = \pi + \frac{\pi}{3} = \frac{4\pi}{3}$$

$$\boxed{x = \frac{\pi}{3},\quad \frac{4\pi}{3}} \tag{A1 each}$$

---

## Q06. Solve $\sin x - \sqrt{3}\cos x = 1$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Compound Formula (D) — $a\sin x + b\cos x = R\sin(x - \alpha)$

**Why this formula?**
The RHS is **non-zero** ($= 1$), so the C2 shortcut cannot be used. Instead, combine the left side into a single trig term using (D), then solve $R\sin(x - \alpha) = 1$.

Compare Q05 and Q06: the **only difference** is the RHS. Zero → use C2; non-zero → use Compound (D).

**Solution:**

Write $\sin x - \sqrt{3}\cos x = R\sin(x - \alpha)$:

$$R = \sqrt{1^2 + (\sqrt{3})^2} = \sqrt{4} = 2, \qquad \tan\alpha = \frac{\sqrt{3}}{1} = \sqrt{3} \;\Rightarrow\; \alpha = \frac{\pi}{3} \tag{M1}$$

$$2\sin\!\left(x - \frac{\pi}{3}\right) = 1 \tag{A1}$$

$$\sin\!\left(x - \frac{\pi}{3}\right) = \frac{1}{2} \tag{M1}$$

Let $u = x - \dfrac{\pi}{3}$. In range $\left[-\dfrac{\pi}{3},\, \dfrac{5\pi}{3}\right]$:

$$u = \frac{\pi}{6} \quad\Rightarrow\quad x = \frac{\pi}{6}+\frac{\pi}{3} = \frac{\pi}{2}$$

$$u = \pi - \frac{\pi}{6} = \frac{5\pi}{6} \quad\Rightarrow\quad x = \frac{5\pi}{6}+\frac{\pi}{3} = \frac{7\pi}{6}$$

$$\boxed{x = \frac{\pi}{2},\quad \frac{7\pi}{6}} \tag{A1 each}$$

---

## Q07. Solve $6\cos^2 x + \sin 2x = 0$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Double Angle Formula (A) — $\sin 2x = 2\sin x\cos x$

**Why this formula?**
The equation contains $\cos^2 x$ (angle $x$) and $\sin 2x$ (angle $2x$) — a **mixed-angle** equation. Replace $\sin 2x$ with $2\sin x\cos x$ to unify everything to angle $x$, then factorise.

**Solution:**

$$6\cos^2 x + 2\sin x\cos x = 0 \tag{M1}$$

$$2\cos x(3\cos x + \sin x) = 0 \tag{M1 — factorise}$$

**Case 1:** $\cos x = 0$

$$x = \frac{\pi}{2},\quad \frac{3\pi}{2} \tag{A1}$$

**Case 2:** $3\cos x + \sin x = 0$

$$\tan x = -3 \tag{A1}$$

$$x = \pi - \arctan 3,\quad x = 2\pi - \arctan 3 \tag{A1 each}$$

$$\boxed{x = \frac{\pi}{2},\quad \pi-\arctan 3,\quad \frac{3\pi}{2},\quad 2\pi-\arctan 3}$$

> **Note:** $\arctan 3 \approx 1.249$ rad ($\approx 71.6°$).

---

## Q08. Solve $\cos^2\!\dfrac{x}{2} + \cos^2 x = 1$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Half Angle Formula (B) — $\cos^2\!\dfrac{x}{2} = \dfrac{1+\cos x}{2}$

**Why this formula?**
The equation has $\cos^2\!\frac{x}{2}$ (angle $\frac{x}{2}$) and $\cos^2 x$ (angle $x$) — a mixed-angle equation. The Half Angle formula converts $\cos^2\!\frac{x}{2}$ into $\cos x$, unifying the angle to $x$ and giving a solvable quadratic in $\cos x$.

**Solution:**

Replace $\cos^2\!\dfrac{x}{2}$ using $\cos^2\!\dfrac{x}{2} = \dfrac{1+\cos x}{2}$:

$$\frac{1+\cos x}{2} + \cos^2 x = 1 \tag{M1}$$

Multiply through by 2:

$$1 + \cos x + 2\cos^2 x = 2$$

$$2\cos^2 x + \cos x - 1 = 0 \tag{A1}$$

$$(2\cos x - 1)(\cos x + 1) = 0 \tag{M1}$$

$$\cos x = \frac{1}{2} \qquad \text{or} \qquad \cos x = -1$$

$$\cos x = \tfrac{1}{2}:\quad x = \frac{\pi}{3},\quad \frac{5\pi}{3} \qquad\qquad \cos x = -1:\quad x = \pi$$

$$\boxed{x = \frac{\pi}{3},\quad \pi,\quad \frac{5\pi}{3}} \tag{A1 each}$$

---

## Q09. Solve $2(1-\cos 2x) = \tan x$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Double Angle Formula (A) — $\cos 2x = 1 - 2\sin^2 x$

**Why this formula?**
The equation has $\cos 2x$ and $\tan x = \sin x / \cos x$ — mixed angles. Replacing $\cos 2x = 1 - 2\sin^2 x$ makes the left side $4\sin^2 x$, and after multiplying through by $\cos x$, both sides become expressible in $\sin x$ and $\cos x$, allowing factorisation.

**Solution:**

Substitute $\cos 2x = 1 - 2\sin^2 x$:

$$2(1-(1-2\sin^2 x)) = \tan x$$

$$4\sin^2 x = \frac{\sin x}{\cos x} \tag{M1}$$

Multiply both sides by $\cos x$:

$$4\sin^2 x\cos x = \sin x$$

$$\sin x(4\sin x\cos x - 1) = 0$$

$$\sin x(2\sin 2x - 1) = 0 \tag{M1}$$

**Case 1:** $\sin x = 0 \;\Rightarrow\; x = 0,\;\pi,\;2\pi$ &emsp; $\tag{A1}$

**Case 2:** $\sin 2x = \dfrac{1}{2}$

$$2x = \frac{\pi}{6},\;\frac{5\pi}{6},\;\frac{\pi}{6}+2\pi,\;\frac{5\pi}{6}+2\pi \tag{M1}$$

$$x = \frac{\pi}{12},\;\frac{5\pi}{12},\;\frac{13\pi}{12},\;\frac{17\pi}{12} \tag{A1 each}$$

$$\boxed{x = 0,\;\frac{\pi}{12},\;\frac{5\pi}{12},\;\pi,\;\frac{13\pi}{12},\;\frac{17\pi}{12},\;2\pi}$$

---

## Q10. Solve $\sin 5x + \sin 3x = 0$, $\quad 0 \leq x \leq 2\pi$

**Formula used:** Sum-to-Product Identity (E) — $\sin P + \sin Q = 2\sin\!\left(\frac{P+Q}{2}\right)\cos\!\left(\frac{P-Q}{2}\right)$

**Why this formula?**
The equation is a **sum of two sines with different angles** ($5x$ and $3x$). Sum-to-Product converts this sum into a **product**, which equals zero when either factor is zero — splitting into two simpler equations.

**Solution:**

$$\sin 5x + \sin 3x = 2\sin\!\left(\frac{5x+3x}{2}\right)\cos\!\left(\frac{5x-3x}{2}\right) = 2\sin 4x\cos x = 0 \tag{M1}$$

**Case 1:** $\sin 4x = 0$

$$4x = 0,\,\pi,\,2\pi,\,3\pi,\,4\pi,\,5\pi,\,6\pi,\,7\pi,\,8\pi \tag{M1}$$

$$x = 0,\;\frac{\pi}{4},\;\frac{\pi}{2},\;\frac{3\pi}{4},\;\pi,\;\frac{5\pi}{4},\;\frac{3\pi}{2},\;\frac{7\pi}{4},\;2\pi \tag{A1}$$

**Case 2:** $\cos x = 0 \;\Rightarrow\; x = \dfrac{\pi}{2},\;\dfrac{3\pi}{2}$ (already included above)

$$\boxed{x = 0,\;\frac{\pi}{4},\;\frac{\pi}{2},\;\frac{3\pi}{4},\;\pi,\;\frac{5\pi}{4},\;\frac{3\pi}{2},\;\frac{7\pi}{4},\;2\pi} \tag{A1 for complete set}$$

---

## Q11. Solve $2\sin x = \cos(x - 60°)$, $\quad 0 \leq x \leq 360°$

**Formula used:** Angle Difference Identity — $\cos(x-60°) = \cos x\cos 60° + \sin x\sin 60°$

**Why this formula?**
The RHS contains a **compound angle** $(x - 60°)$. Expanding it using the Angle Difference identity brings everything to $\sin x$ and $\cos x$ of the same angle, which can then be rearranged to $\tan x = \text{const}$.

**Solution:**

Expand $\cos(x-60°)$:

$$2\sin x = \cos x\cdot\frac{1}{2} + \sin x\cdot\frac{\sqrt{3}}{2} \tag{M1}$$

$$2\sin x - \frac{\sqrt{3}}{2}\sin x = \frac{1}{2}\cos x$$

$$\frac{4-\sqrt{3}}{2}\sin x = \frac{1}{2}\cos x \tag{A1}$$

$$\tan x = \frac{1}{4-\sqrt{3}} = \frac{4+\sqrt{3}}{(4-\sqrt{3})(4+\sqrt{3})} = \frac{4+\sqrt{3}}{13} \tag{M1 — rationalise}$$

$$\tan x = \frac{4+\sqrt{3}}{13} \approx 0.441$$

Solving in $[0°, 360°]$:

$$x = \arctan\!\left(\frac{4+\sqrt{3}}{13}\right) \approx 23.8°, \qquad x = 180° + 23.8° \approx 203.8° \tag{A1 each}$$

$$\boxed{x \approx 23.8°,\quad 203.8°}$$

---

## Summary — Which Formula and Why?

| Q | Key Formula | Trigger to recognise it |
|---|-------------|------------------------|
| 01 | Angle Sum: $\sin(A+B)$ | Non-standard angle → write as sum of 30°/45°/60° |
| 02 | $\cos^2 x = 1-\sin^2 x$ | $\cos^2$ and $\sin$ mixed, same angle → convert to one function |
| 03 | $\sec^2 x = 1+\tan^2 x$ | $\sec^2$ and $\tan$ mixed, same angle → convert to $\tan$ |
| 04 | $\cot x = 1/\tan x$ | $\cot$ and $\tan$ mixed → let $t=\tan x$ → quadratic |
| 05 | C2: $\tan x = \sin x/\cos x$ | $a\sin x + b\cos x = \mathbf{0}$ → divide by $\cos x$ |
| 06 | Compound (D): $R\sin(x-\alpha)$ | $a\sin x + b\cos x = \mathbf{k \neq 0}$ → single term |
| 07 | Double Angle (A): $\sin 2x = 2\sin x\cos x$ | $\cos^2 x$ and $\sin 2x$ mixed → unify angle, factorise |
| 08 | Half Angle (B): $\cos^2\frac{x}{2} = \frac{1+\cos x}{2}$ | $\cos^2\frac{x}{2}$ present → eliminate half-angle |
| 09 | Double Angle (A): $\cos 2x = 1-2\sin^2 x$ | $\cos 2x$ and $\tan x$ mixed → unify, factorise |
| 10 | Sum-to-Product (E) | Sum of sines/cosines with different angles → product |
| 11 | Angle Difference: $\cos(x-60°)$ | Compound angle on RHS → expand to $\sin x$, $\cos x$ |
