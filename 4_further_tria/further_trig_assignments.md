# Further Trigonometry — 실전문제 Mark Scheme (A-Level P3 & P4)

---

## Q1. Solve $3\csc\theta° + 8\cos\theta° = 0$, $\quad 0 \leq \theta \leq 180$, to 1 d.p. &emsp; **(6 marks)**

**Strategy:** $\csc\theta = \dfrac{1}{\sin\theta}$ → multiply through by $\sin\theta$ → use Double Angle $\sin 2\theta = 2\sin\theta\cos\theta$.

$$\frac{3}{\sin\theta} + 8\cos\theta = 0 \tag{M1}$$

Multiply both sides by $\sin\theta$:

$$3 + 8\sin\theta\cos\theta = 0 \tag{M1}$$

$$3 + 4\sin 2\theta = 0 \tag{M1 — Double Angle}$$

$$\sin 2\theta = -\frac{3}{4} \tag{A1}$$

Range: $0 \leq \theta \leq 180 \;\Rightarrow\; 0 \leq 2\theta \leq 360$.

Principal value: $\arcsin\!\left(\dfrac{3}{4}\right) \approx 48.59°$

Since $\sin 2\theta < 0$: $2\theta$ lies in the 3rd or 4th quadrant:

$$2\theta = 180° + 48.59° = 228.6° \;\Rightarrow\; \theta = 114.3° \tag{A1}$$

$$2\theta = 360° - 48.59° = 311.4° \;\Rightarrow\; \theta = 155.7° \tag{A1}$$

$$\boxed{\theta = 114.3°,\quad 155.7°}$$

---

## Q2(a). Given $\cos x = \sqrt{3}-1$, find $\cos 2x$ in the form $a + b\sqrt{3}$ &emsp; **(3 marks)**

**Strategy:** Use Double Angle — $\cos 2x = 2\cos^2 x - 1$.

$$\cos 2x = 2(\sqrt{3}-1)^2 - 1 \tag{M1}$$

$$= 2(3 - 2\sqrt{3} + 1) - 1 = 2(4-2\sqrt{3}) - 1 \tag{M1}$$

$$= 8 - 4\sqrt{3} - 1$$

$$\boxed{\cos 2x = 7 - 4\sqrt{3}} \quad (a=7,\; b=-4) \tag{A1}$$

---

## Q2(b). Given $2\cos(y+30)° = \sqrt{3}\sin(y-30)°$, find $\tan y$ in the form $k\sqrt{3}$ &emsp; **(5 marks)**

**Strategy:** Expand both sides using Angle Sum/Difference identities, then collect $\sin y$ and $\cos y$ terms to form $\tan y$.

Expand LHS:

$$2\cos(y+30)° = 2(\cos y\cos 30° - \sin y\sin 30°) = \sqrt{3}\cos y - \sin y \tag{M1}$$

Expand RHS:

$$\sqrt{3}\sin(y-30)° = \sqrt{3}(\sin y\cos 30° - \cos y\sin 30°) = \frac{3}{2}\sin y - \frac{\sqrt{3}}{2}\cos y \tag{M1}$$

Set equal and collect terms:

$$\sqrt{3}\cos y - \sin y = \frac{3}{2}\sin y - \frac{\sqrt{3}}{2}\cos y$$

$$\sqrt{3}\cos y + \frac{\sqrt{3}}{2}\cos y = \frac{3}{2}\sin y + \sin y \tag{M1}$$

$$\frac{3\sqrt{3}}{2}\cos y = \frac{5}{2}\sin y \tag{A1}$$

$$\tan y = \frac{3\sqrt{3}}{5} \tag{A1}$$

$$\boxed{\tan y = \frac{3}{5}\sqrt{3}} \quad \left(k = \frac{3}{5}\right)$$

---

## Q3(a). Prove that $\sin 2x - \tan x \equiv \tan x\cos 2x$, for $\cos x \neq 0$ &emsp; **(5 marks)**

**Strategy:** Work from LHS. Express everything in $\sin x$ and $\cos x$, factor out $\tan x = \sin x/\cos x$.

$$\text{LHS} = \sin 2x - \tan x = 2\sin x\cos x - \frac{\sin x}{\cos x} \tag{M1}$$

$$= \frac{2\sin x\cos^2 x - \sin x}{\cos x} \tag{M1}$$

$$= \frac{\sin x(2\cos^2 x - 1)}{\cos x} \tag{M1}$$

$$= \frac{\sin x}{\cos x}\cdot(2\cos^2 x - 1) \tag{M1}$$

$$= \tan x \cdot \cos 2x = \text{RHS} \quad \blacksquare \tag{A1}$$

---

## Q3(b). Hence solve $\sin 2x - \tan x = 2\cos 2x$, $\quad 0 \leq x \leq 180°$ &emsp; **(5 marks)**

**Strategy:** Substitute the result from (a): $\sin 2x - \tan x = \tan x\cos 2x$.

$$\tan x\cos 2x = 2\cos 2x \tag{M1 — using (a)}$$

$$\tan x\cos 2x - 2\cos 2x = 0$$

$$\cos 2x(\tan x - 2) = 0 \tag{M1 — factorise}$$

**Case 1:** $\cos 2x = 0$

$$2x = 90°,\;270° \;\Rightarrow\; x = 45°,\;135° \tag{A1}$$

**Case 2:** $\tan x = 2$

$$x = \arctan 2 \approx 63.4° \tag{A1}$$

$$\boxed{x = 45°,\quad 63.4°,\quad 135°} \tag{A1 for complete set}$$

> **Note:** Check $\cos x \neq 0$ (condition from part a). None of the solutions give $\cos x = 0$, so all are valid.

---

## Q4(a). Express $3\cos x° + \sin x°$ in the form $R\cos(x-\alpha)°$, $R > 0$, $0 < \alpha < 90$ &emsp; **(4 marks)**

**Strategy:** Compound Formula (D) — $R\cos(x-\alpha) = (R\cos\alpha)\cos x + (R\sin\alpha)\sin x$.

Compare coefficients: $R\cos\alpha = 3$, $R\sin\alpha = 1$

$$R = \sqrt{3^2 + 1^2} = \sqrt{10} \tag{M1, A1}$$

$$\tan\alpha = \frac{1}{3} \;\Rightarrow\; \alpha = \arctan\!\left(\frac{1}{3}\right) \approx 18.4° \tag{M1, A1}$$

$$\boxed{3\cos x° + \sin x° = \sqrt{10}\,\cos(x-18.4°)°}$$

---

## Q4(b). Solve $6\cos^2 x° + \sin 2x° = 0$, $\quad 0 \leq x \leq 360$, to 1 d.p. &emsp; **(6 marks)**

**Strategy:** Apply Double Angle ($\sin 2x = 2\sin x\cos x$), factorise, then use part (a) result for the second factor.

$$6\cos^2 x + 2\sin x\cos x = 0 \tag{M1 — Double Angle}$$

$$2\cos x(3\cos x + \sin x) = 0 \tag{M1 — factorise}$$

**Case 1:** $\cos x = 0$

$$x = 90°,\quad 270° \tag{A1}$$

**Case 2:** $3\cos x + \sin x = 0$

From part (a), $3\cos x + \sin x = \sqrt{10}\,\cos(x-18.4°)$, so:

$$\sqrt{10}\,\cos(x-18.4°) = 0 \tag{M1 — using (a)}$$

$$\cos(x-18.4°) = 0$$

$$x - 18.4° = 90°,\;270°$$

$$x = 108.4°,\quad 288.4° \tag{A1 each}$$

$$\boxed{x = 90°,\quad 108.4°,\quad 270°,\quad 288.4°}$$

---

## Q5(a). Prove $\dfrac{\sin 2x + \sin 2y}{\cos 2x + \cos 2y} \equiv \tan(x+y)$ &emsp; **(4 marks)**

**Strategy:** Apply Sum-to-Product (E) to both numerator and denominator, then cancel the common factor.

Numerator — Sum-to-Product with $P = 2x$, $Q = 2y$:

$$\sin 2x + \sin 2y = 2\sin(x+y)\cos(x-y) \tag{M1}$$

Denominator — Sum-to-Product with $P = 2x$, $Q = 2y$:

$$\cos 2x + \cos 2y = 2\cos(x+y)\cos(x-y) \tag{M1}$$

Divide:

$$\frac{\sin 2x + \sin 2y}{\cos 2x + \cos 2y} = \frac{2\sin(x+y)\cos(x-y)}{2\cos(x+y)\cos(x-y)} \tag{M1}$$

$$= \frac{\sin(x+y)}{\cos(x+y)} = \tan(x+y) \quad \blacksquare \tag{A1}$$

---

## Q5(b). Hence show that $\tan 52.5° = \sqrt{6} - \sqrt{3} - \sqrt{2} + 2$ &emsp; **(5 marks)**

**Strategy:** Apply the result from (a) with $x+y = 52.5°$. Choose $x = 30°$, $y = 22.5°$ so that $2x = 60°$ and $2y = 45°$ are standard angles.

Let $x = 30°$, $y = 22.5°$ so $x + y = 52.5°$:

$$\tan 52.5° = \frac{\sin 60° + \sin 45°}{\cos 60° + \cos 45°} \tag{M1 — applying (a)}$$

$$= \frac{\dfrac{\sqrt{3}}{2} + \dfrac{\sqrt{2}}{2}}{\dfrac{1}{2} + \dfrac{\sqrt{2}}{2}} = \frac{\sqrt{3}+\sqrt{2}}{1+\sqrt{2}} \tag{M1, A1}$$

Rationalise by multiplying by $\dfrac{1-\sqrt{2}}{1-\sqrt{2}}$:

$$= \frac{(\sqrt{3}+\sqrt{2})(1-\sqrt{2})}{(1+\sqrt{2})(1-\sqrt{2})} = \frac{\sqrt{3} - \sqrt{6} + \sqrt{2} - 2}{1 - 2} \tag{M1}$$

$$= \frac{\sqrt{3} - \sqrt{6} + \sqrt{2} - 2}{-1} = \sqrt{6} - \sqrt{3} - \sqrt{2} + 2 \quad \blacksquare \tag{A1}$$

---

## Q6(a). Prove $\cos P - \cos Q \equiv -2\sin\dfrac{P+Q}{2}\sin\dfrac{P-Q}{2}$ &emsp; **(4 marks)**

**Strategy:** Let $A = \dfrac{P+Q}{2}$, $B = \dfrac{P-Q}{2}$ (so $A+B = P$, $A-B = Q$). Subtract the cos Difference identity from the cos Sum identity.

$$\cos(A+B) = \cos A\cos B - \sin A\sin B \tag{M1}$$

$$\cos(A-B) = \cos A\cos B + \sin A\sin B \tag{M1}$$

Subtract:

$$\cos(A+B) - \cos(A-B) = -2\sin A\sin B \tag{M1}$$

Substitute $A+B = P$ and $A-B = Q$:

$$\cos P - \cos Q = -2\sin\!\frac{P+Q}{2}\sin\!\frac{P-Q}{2} \quad \blacksquare \tag{A1}$$

---

## Q6(b). Solve $\cos 5x° + \sin 3x° - \cos x° = 0$, $\quad 0 \leq x < 180$ &emsp; **(7 marks)**

**Strategy:** Rewrite as $(\cos 5x° - \cos x°) + \sin 3x° = 0$. Apply part (a) to the bracket, then factorise.

Group and apply part (a) with $P = 5x$, $Q = x$:

$$\cos 5x - \cos x = -2\sin 3x\sin 2x \tag{M1 — using (a)}$$

Substitute:

$$-2\sin 3x\sin 2x + \sin 3x = 0 \tag{M1}$$

$$\sin 3x(1 - 2\sin 2x) = 0 \tag{M1 — factorise}$$

**Case 1:** $\sin 3x = 0$

$$3x = 0°,\;180°,\;360°,\;540° \;\Rightarrow\; x = 0°,\;60°,\;120°,\;180° \tag{M1}$$

Domain $0 \leq x < 180$: $x = 0°,\;60°,\;120°$ &emsp; $(x = 180°$ excluded$)$ $\tag{A1}$

**Case 2:** $\sin 2x = \dfrac{1}{2}$

$$2x = 30°,\;150° \;\Rightarrow\; x = 15°,\;75° \tag{A1}$$

$$\boxed{x = 0°,\quad 15°,\quad 60°,\quad 75°,\quad 120°} \tag{A1 for complete set}$$

---

## Q7(a). Express $2\sin x° - 3\cos x°$ in the form $R\sin(x-\alpha)°$, $R > 0$, $0 < \alpha < 90$ &emsp; **(4 marks)**

**Strategy:** Compound Formula (D) — $R\sin(x-\alpha) = (R\cos\alpha)\sin x - (R\sin\alpha)\cos x$.

Compare coefficients: $R\cos\alpha = 2$, $R\sin\alpha = 3$

$$R = \sqrt{2^2+3^2} = \sqrt{13} \tag{M1, A1}$$

$$\tan\alpha = \frac{3}{2} \;\Rightarrow\; \alpha = \arctan\!\left(\frac{3}{2}\right) \approx 56.3° \tag{M1, A1}$$

$$\boxed{2\sin x° - 3\cos x° = \sqrt{13}\,\sin(x-56.3°)°}$$

---

## Q7(b). Show that $\csc x° + 3\cot x° = 2$ can be written as $2\sin x° - 3\cos x° = 1$ &emsp; **(1 mark)**

$$\frac{1}{\sin x} + \frac{3\cos x}{\sin x} = 2$$

$$\frac{1 + 3\cos x}{\sin x} = 2$$

Multiply both sides by $\sin x$:

$$1 + 3\cos x = 2\sin x \;\Rightarrow\; 2\sin x - 3\cos x = 1 \quad \blacksquare \tag{B1}$$

---

## Q7(c). Solve $\csc x° + 3\cot x° = 2$, $\quad 0 \leq x \leq 360$, to 1 d.p. &emsp; **(5 marks)**

**Strategy:** From (b) the equation is $2\sin x - 3\cos x = 1$. From (a), substitute the Compound form.

$$\sqrt{13}\,\sin(x - 56.3°) = 1 \tag{M1 — using (a) and (b)}$$

$$\sin(x-56.3°) = \frac{1}{\sqrt{13}} \approx 0.2774 \tag{M1}$$

Principal value: $\arcsin(0.2774) \approx 16.1°$

Range: $x \in [0°,360°]$ so $x - 56.3° \in [-56.3°, 303.7°]$:

$$x - 56.3° = 16.1° \;\Rightarrow\; x = 72.4° \tag{A1}$$

$$x - 56.3° = 180° - 16.1° = 163.9° \;\Rightarrow\; x = 220.2° \tag{A1}$$

$$\boxed{x = 72.4°,\quad 220.2°} \tag{A1}$$

---

## Summary Table

| Q | Marks | Key identity / strategy |
|---|-------|------------------------|
| 1 | 6 | $\csc\theta \to \frac{1}{\sin\theta}$, then Double Angle $\sin2\theta$ |
| 2a | 3 | Double Angle: $\cos 2x = 2\cos^2 x - 1$ |
| 2b | 5 | Expand both sides with Angle Sum/Diff → collect → $\tan y$ |
| 3a | 5 | Prove: express LHS in $\sin/\cos$, factor $\tan x$ |
| 3b | 5 | Substitute (a), factorise $\cos 2x(\tan x - 2) = 0$ |
| 4a | 4 | Compound (D): $R\cos(x-\alpha)$, find $R$ and $\alpha$ |
| 4b | 6 | Double Angle → factorise $2\cos x(3\cos x + \sin x) = 0$ → use (a) |
| 5a | 4 | Sum-to-Product on num & denom, cancel $\cos(x-y)$ |
| 5b | 5 | Let $x=30°$, $y=22.5°$, apply (a), rationalise |
| 6a | 4 | Subtract cos Sum/Diff identities with $A=\frac{P+Q}{2}$, $B=\frac{P-Q}{2}$ |
| 6b | 7 | Group $(\cos5x - \cos x)$, apply (a), factorise $\sin3x(\ldots) = 0$ |
| 7a | 4 | Compound (D): $R\sin(x-\alpha)$, find $R$ and $\alpha$ |
| 7b | 1 | Multiply by $\sin x$, rearrange |
| 7c | 5 | Substitute (a)+(b) → $\sqrt{13}\sin(x-56.3°) = 1$ |
