# Binomial Expansion (P3) — Practice

---

**1** &nbsp; Expand each of the following in ascending powers of $x$, up to and including the term in $x^3$.

&emsp;*(a)* &ensp; $(1+3x)^{-2}$ &emsp; **(3)**

<details>
<summary>Solution</summary>

$$= 1 + (-2)(3x) + \frac{(-2)(-3)}{2!}(3x)^2 + \frac{(-2)(-3)(-4)}{3!}(3x)^3 \quad \textbf{M1}$$

$$\boxed{= 1 - 6x + 27x^2 - 108x^3} \quad \textbf{A1 A1}$$

A1 for $1 - 6x$ correct; A1 for $x^2$ and $x^3$ terms correct.

</details>

&emsp;*(b)* &ensp; $\left(1-\dfrac{x}{2}\right)^{1/2}$ &emsp; **(3)**

<details>
<summary>Solution</summary>

$n = \dfrac{1}{2}$, substitute $x \to -\dfrac{x}{2}$ **M1**

$$= 1 + \frac{1}{2}\!\left(-\frac{x}{2}\right) + \frac{\frac{1}{2}\cdot\!\left(-\frac{1}{2}\right)}{2!}\!\left(-\frac{x}{2}\right)^2 + \frac{\frac{1}{2}\cdot\!\left(-\frac{1}{2}\right)\!\cdot\!\left(-\frac{3}{2}\right)}{3!}\!\left(-\frac{x}{2}\right)^3$$

$$\boxed{= 1 - \frac{x}{4} - \frac{x^2}{32} - \frac{x^3}{128}} \quad \textbf{A1 A1}$$

A1 for first two terms correct; A1 for $x^2$ and $x^3$ terms correct.

</details>

---

**2** &nbsp; Expand each of the following in ascending powers of $x$, up to and including the stated term.

&emsp;*(a)* &ensp; $(4+x)^{-1}$, up to and including the term in $x^3$ &emsp; **(4)**

<details>
<summary>Solution</summary>

Factor out 4 first: **M1**

$$= \left[4\!\left(1+\frac{x}{4}\right)\right]^{-1} = \frac{1}{4}\!\left(1+\frac{x}{4}\right)^{-1} \quad \textbf{A1}$$

$$= \frac{1}{4}\left[1 - \frac{x}{4} + \frac{x^2}{16} - \frac{x^3}{64} + \cdots\right] \quad \textbf{M1}$$

$$\boxed{= \frac{1}{4} - \frac{x}{16} + \frac{x^2}{64} - \frac{x^3}{256}} \quad \textbf{A1}$$

</details>

&emsp;*(b)* &ensp; $(8-x)^{1/3}$, up to and including the term in $x^2$ &emsp; **(4)**

<details>
<summary>Solution</summary>

Factor out 8 first: **M1**

$$= \left[8\!\left(1-\frac{x}{8}\right)\right]^{1/3} = 2\!\left(1-\frac{x}{8}\right)^{1/3} \quad \textbf{A1}$$

$n = \dfrac{1}{3}$, substitute $x \to -\dfrac{x}{8}$: **M1**

$$= 2\left[1 + \frac{1}{3}\!\left(-\frac{x}{8}\right) + \frac{\frac{1}{3}\cdot\!\left(-\frac{2}{3}\right)}{2!}\!\left(\frac{x}{8}\right)^2\right] = 2\left[1 - \frac{x}{24} - \frac{x^2}{576}\right]$$

$$\boxed{= 2 - \frac{x}{12} - \frac{x^2}{288}} \quad \textbf{A1}$$

</details>

---

**3** &nbsp; *(a)* &ensp; Expand $(3-2x)^{-1}$ in ascending powers of $x$ up to and including the term in $x^2$. &emsp; **(3)**

<details>
<summary>Solution</summary>

Factor out 3: **M1**

$$= \frac{1}{3}\!\left(1-\frac{2x}{3}\right)^{-1}$$

$$= \frac{1}{3}\left[1 + \frac{2x}{3} + \left(\frac{2x}{3}\right)^2 + \cdots\right] \quad \textbf{M1}$$

$$\boxed{= \frac{1}{3} + \frac{2x}{9} + \frac{4x^2}{27}} \quad \textbf{A1}$$

</details>

&emsp;*(b)* &ensp; State the values of $x$ for which your expansion is valid. &emsp; **(2)**

<details>
<summary>Solution</summary>

Expansion valid when $\left|\dfrac{2x}{3}\right| < 1$ **M1**

$$\boxed{-\frac{3}{2} < x < \frac{3}{2}} \quad \textbf{A1}$$

</details>

---

**4** &nbsp; Given that

$$f(x) = \frac{3-x}{(1+x)(1-3x)}$$

&emsp;*(a)* &ensp; Express $f(x)$ in partial fractions. &emsp; **(3)**

<details>
<summary>Solution</summary>

$$\frac{3-x}{(1+x)(1-3x)} = \frac{A}{1+x} + \frac{B}{1-3x} \quad \textbf{M1}$$

$$3-x = A(1-3x) + B(1+x)$$

$x = -1$: $\quad 4 = 4A \Rightarrow A = 1$ **A1**

$x = \dfrac{1}{3}$: $\quad \dfrac{8}{3} = \dfrac{4B}{3} \Rightarrow B = 2$ **A1**

$$\boxed{f(x) = \frac{1}{1+x} + \frac{2}{1-3x}}$$

</details>

&emsp;*(b)* &ensp; Hence expand $f(x)$ in ascending powers of $x$, up to and including the term in $x^3$. &emsp; **(5)**

<details>
<summary>Solution</summary>

$$f(x) = (1+x)^{-1} + 2(1-3x)^{-1} \quad \textbf{M1}$$

$(1+x)^{-1} = 1 - x + x^2 - x^3 + \cdots$ **M1**

$(1-3x)^{-1} = 1 + 3x + 9x^2 + 27x^3 + \cdots$ **M1**

$$f(x) = (1 - x + x^2 - x^3) + 2(1 + 3x + 9x^2 + 27x^3) \quad \textbf{M1}$$

$$\boxed{= 3 + 5x + 19x^2 + 53x^3} \quad \textbf{A1}$$

</details>

&emsp;*(c)* &ensp; State the values of $x$ for which your expansion is valid. &emsp; **(2)**

<details>
<summary>Solution</summary>

Both expansions must hold simultaneously:

- $(1+x)^{-1}$ valid for $|x| < 1$
- $(1-3x)^{-1}$ valid for $|3x| < 1 \Rightarrow |x| < \dfrac{1}{3}$

Take the stricter condition: **M1**

$$\boxed{-\frac{1}{3} < x < \frac{1}{3}} \quad \textbf{A1}$$

</details>

---

**5** &nbsp; *(a)* &ensp; Expand $\dfrac{3}{\sqrt{4-x}}$ in ascending powers of $x$, up to and including the term in $x^2$. &emsp; **(5)**

<details>
<summary>Solution</summary>

$$\frac{3}{\sqrt{4-x}} = 3(4-x)^{-1/2} \quad \textbf{M1}$$

Factor out 4: **M1**

$$= 3\cdot\left[4\!\left(1-\frac{x}{4}\right)\right]^{-1/2} = 3 \cdot 4^{-1/2}\!\left(1-\frac{x}{4}\right)^{-1/2} = \frac{3}{2}\!\left(1-\frac{x}{4}\right)^{-1/2} \quad \textbf{A1}$$

$n = -\dfrac{1}{2}$, substitute $x \to -\dfrac{x}{4}$: **M1**

$$= \frac{3}{2}\left[1 + \frac{1}{2}\cdot\frac{x}{4} + \frac{\frac{1}{2}\cdot\frac{3}{2}}{2!}\cdot\frac{x^2}{16}\right] = \frac{3}{2}\left[1 + \frac{x}{8} + \frac{3x^2}{128}\right]$$

$$\boxed{= \frac{3}{2} + \frac{3x}{16} + \frac{9x^2}{256}} \quad \textbf{A1}$$

</details>

&emsp;*(b)* &ensp; State the values of $x$ for which your expansion is valid. &emsp; **(1)**

<details>
<summary>Solution</summary>

Valid when $\left|\dfrac{x}{4}\right| < 1$:

$$\boxed{-4 < x < 4} \quad \textbf{B1}$$

</details>
