# Differential Equations — 심화문제 Mark Scheme

> **난이도:** A-Level P4 최상위 / 시험 전 마무리용  
> **예상 소요:** 약 2시간 (문제만 먼저 풀고 풀이 확인 권장)

---

## Q1. Separable DE — 양변 모두 부분분수 (Double Partial Fractions)

> **[문제 해석]**  
> 우변이 $y$끼리의 곱 × $x$끼리의 곱으로 완전히 분리되는 형태다. 각 변수를 한쪽으로 몰아 변수분리한 뒤, 좌변($y$ 쪽)과 우변($x$ 쪽) **각각에** 부분분수를 적용해야 한다. 적분하면 양변 모두 로그 형태가 나오고, 이 로그들을 합치면서 초기조건으로 $C$를 결정해 implicit solution을 도출하는 것이 핵심이다.  
> (e)는 implicit solution에 $x=6$을 대입한 뒤, 2차방정식처럼 $y$를 풀어내면 된다.

$$\frac{dy}{dx} = \frac{y(y-3)}{x(x+2)}, \qquad y = 6 \text{ when } x = 2$$

**(a)** Show that the equation can be written in the separated form

$$\frac{dy}{y(y-3)} = \frac{dx}{x(x+2)}$$

**(b)** Using partial fractions, show that

$$\int \frac{dy}{y(y-3)} = \frac{1}{3}\ln\left|\frac{y-3}{y}\right| + C$$

**(c)** Using partial fractions, show that

$$\int \frac{dx}{x(x+2)} = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + C$$

**(d)** Hence show that the particular solution satisfies

$$\left(\frac{y-3}{y}\right)^2 = \frac{2x^3}{(x+2)^3}$$

**(e)** Find the value of $y$ when $x = 6$, giving your answer to 3 significant figures.

<details>
<summary>**Solution**</summary>

#### (a) Separation of variables

$$\frac{dy}{dx} = \frac{y(y-3)}{x(x+2)}$$

두 변수를 각각 한쪽으로 모은다:

$$\frac{1}{y(y-3)}\,dy = \frac{1}{x(x+2)}\,dx \tag{M1}$$

양변을 적분하면 된다. $\checkmark$

---

#### (b) 좌변 부분분수

$$\frac{1}{y(y-3)} = \frac{A}{y} + \frac{B}{y-3}$$

$$1 = A(y-3) + By$$

- $y = 0$: $1 = -3A \implies A = -\dfrac{1}{3}$
- $y = 3$: $1 = 3B \implies B = \dfrac{1}{3}$

$$\frac{1}{y(y-3)} = \frac{-1/3}{y} + \frac{1/3}{y-3} \tag{M1}$$

$$\int \frac{dy}{y(y-3)} = -\frac{1}{3}\ln|y| + \frac{1}{3}\ln|y-3| = \frac{1}{3}\ln\left|\frac{y-3}{y}\right| \quad \checkmark \tag{A1}$$

---

#### (c) 우변 부분분수

$$\frac{1}{x(x+2)} = \frac{A}{x} + \frac{B}{x+2}$$

$$1 = A(x+2) + Bx$$

- $x = 0$: $1 = 2A \implies A = \dfrac{1}{2}$
- $x = -2$: $1 = -2B \implies B = -\dfrac{1}{2}$

$$\frac{1}{x(x+2)} = \frac{1/2}{x} - \frac{1/2}{x+2} \tag{M1}$$

$$\int \frac{dx}{x(x+2)} = \frac{1}{2}\ln|x| - \frac{1}{2}\ln|x+2| = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| \quad \checkmark \tag{A1}$$

---

#### (d) 초기조건 적용 → implicit solution

(b), (c)로부터:

$$\frac{1}{3}\ln\left|\frac{y-3}{y}\right| = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + C \tag{M1}$$

**초기조건** $x = 2,\ y = 6$ 대입:

$$\frac{1}{3}\ln\left|\frac{3}{6}\right| = \frac{1}{2}\ln\left|\frac{2}{4}\right| + C$$

$$\frac{1}{3}\ln\frac{1}{2} = \frac{1}{2}\ln\frac{1}{2} + C$$

$$-\frac{\ln 2}{3} = -\frac{\ln 2}{2} + C \implies C = \frac{\ln 2}{2} - \frac{\ln 2}{3} = \frac{\ln 2}{6} \tag{A1}$$

따라서:

$$\frac{1}{3}\ln\left|\frac{y-3}{y}\right| = \frac{1}{2}\ln\left|\frac{x}{x+2}\right| + \frac{\ln 2}{6}$$

양변에 $\times 6$:

$$2\ln\left|\frac{y-3}{y}\right| = 3\ln\left|\frac{x}{x+2}\right| + \ln 2 \tag{M1}$$

로그 법칙으로 정리:

$$\ln\left(\frac{y-3}{y}\right)^2 = \ln\left(\frac{x}{x+2}\right)^3 + \ln 2 = \ln\frac{2x^3}{(x+2)^3}$$

$$\boxed{\left(\frac{y-3}{y}\right)^2 = \frac{2x^3}{(x+2)^3}} \quad \checkmark \tag{A1}$$

---

#### (e) $x = 6$일 때 $y$ 값

$$\left(\frac{y-3}{y}\right)^2 = \frac{2 \times 6^3}{(6+2)^3} = \frac{2 \times 216}{512} = \frac{432}{512} = \frac{27}{32} \tag{M1}$$

$x = 2$에서 $y = 6 > 3$이므로 $\dfrac{y-3}{y} > 0$. 따라서:

$$\frac{y-3}{y} = \sqrt{\frac{27}{32}} = \frac{3\sqrt{3}}{4\sqrt{2}} = \frac{3\sqrt{6}}{8} \tag{M1}$$

$$1 - \frac{3}{y} = \frac{3\sqrt{6}}{8} \implies \frac{3}{y} = 1 - \frac{3\sqrt{6}}{8} = \frac{8 - 3\sqrt{6}}{8}$$

$$y = \frac{24}{8 - 3\sqrt{6}} \approx \frac{24}{8 - 7.348} \approx \frac{24}{0.652}$$

$$\boxed{y \approx 36.8} \tag{A1}$$

> **검증:** $\left(\frac{36.8-3}{36.8}\right)^2 = \left(\frac{33.8}{36.8}\right)^2 \approx 0.919^2 \approx 0.844 \approx \frac{27}{32}$ ✓
</detail>

---

## Q2. Separable DE — 치환 $u = \ln y$ + 부분분수

> **[문제 해석]**  
> 우변에 $\ln y$가 붙어 있어서 그냥 변수분리하면 $\int \frac{dy}{y \ln y}$가 나온다 — 이 적분이 $u = \ln y$로 치환해야 깔끔해진다는 신호다. 치환 후 방정식이 $u$에 대한 separable DE로 바뀌고, 우변 $\frac{1}{x(x+1)}$은 다시 부분분수로 처리한다. 최종적으로 $y = e^{u(x)}$ 형태로 explicit solution을 구할 수 있다.  
> $x \to \infty$일 때의 점근값을 구하는 것도 중요한 포인트.

$$x(x+1)\,\frac{dy}{dx} = y\ln y, \qquad y = e \text{ when } x = 1$$

**(a)** Let $u = \ln y$. Show that this substitution transforms the equation into

$$x(x+1)\,\frac{du}{dx} = u$$

**(b)** Hence separate variables and, using partial fractions, integrate both sides.

**(c)** Apply the initial condition to find $u$ in terms of $x$.

**(d)** Hence find $y$ in terms of $x$, and state the value that $y$ approaches as $x \to \infty$.

<details>
<summary>Solution</summary>
#### (a) 치환 $u = \ln y$

$u = \ln y \implies y = e^u$이므로, 체인 룰:

$$\frac{dy}{dx} = e^u \cdot \frac{du}{dx} = y\,\frac{du}{dx} \tag{M1}$$

원래 방정식에 대입:

$$x(x+1) \cdot y\,\frac{du}{dx} = y \cdot \ln y = y \cdot u$$

양변을 $y > 0$으로 나누면:

$$x(x+1)\,\frac{du}{dx} = u \quad \checkmark \tag{A1}$$

---

#### (b) 변수분리 + 부분분수

$$\frac{du}{u} = \frac{dx}{x(x+1)} \tag{M1}$$

우변 부분분수:

$$\frac{1}{x(x+1)} = \frac{1}{x} - \frac{1}{x+1}$$

양변 적분:

$$\int \frac{du}{u} = \int \left(\frac{1}{x} - \frac{1}{x+1}\right)dx \tag{M1}$$

$$\ln|u| = \ln|x| - \ln|x+1| + C = \ln\frac{x}{x+1} + C \tag{A1}$$

$$|u| = e^C \cdot \frac{x}{x+1} \implies u = A\,\frac{x}{x+1} \quad (A \in \mathbb{R}) \tag{A1}$$

---

#### (c) 초기조건 적용

$x = 1,\ y = e$이므로 $u = \ln e = 1$:

$$1 = A \cdot \frac{1}{1+1} = \frac{A}{2} \implies A = 2 \tag{M1 A1}$$

$$\boxed{u = \frac{2x}{x+1}}$$

---

#### (d) $y$ 를 $x$로 표현

$u = \ln y$이므로:

$$\ln y = \frac{2x}{x+1}$$

$$\boxed{y = e^{2x/(x+1)}} \tag{A1}$$

**$x \to \infty$일 때:**

$$\frac{2x}{x+1} = \frac{2}{1 + 1/x} \to 2$$

$$y \to e^2 \approx 7.39 \tag{A1}$$

> **해석:** $y$는 $e$에서 시작해 $e^2$에 점근적으로 접근한다. 초기조건 검증: $x=1$이면 $y = e^{2/2} = e$ ✓
</detail>

## Q3. Connected Rates of Change — 원통형 탱크 배수

> **[문제 해석]**  
> 주어진 건 $\frac{dV}{dt}$인데, 구해야 하는 건 $\frac{dh}{dt}$다. 원통형이므로 $V = \pi r^2 h$로 $V$와 $h$를 연결한 뒤 양변을 $t$로 미분하면 $\frac{dV}{dt}$와 $\frac{dh}{dt}$가 연결된다 — 이게 connected rates의 핵심이다. 이후 나온 $\frac{dh}{dt} = -\frac{2}{9\pi}\sqrt{h}$를 separable DE로 풀면 $h(t)$를 구할 수 있다.  
> $h$가 작아질수록 배수 속도가 느려진다는 물리적 의미도 이해해두면 좋다.

A large cylindrical water tank has a circular cross-section of radius 3 metres. Water drains through a small hole at the base. By Torricelli's Law, the volume flow rate satisfies

$$\frac{dV}{dt} = -2\sqrt{h}$$

where $V$ m$^3$ is the volume of water and $h$ metres is the depth. Initially, the depth is 9 metres.

**(a)** Show that $\dfrac{dh}{dt} = -\dfrac{2}{9\pi}\sqrt{h}$.

**(b)** By solving the differential equation, show that

$$h = \left(3 - \frac{t}{9\pi}\right)^2$$

**(c)** Find the time at which the tank empties completely. Give your answer in exact form and to the nearest minute.

**(d)** Find the depth of water after 30 minutes, to 3 significant figures.

**(e)** Find the rate at which the depth is decreasing at the instant when $h = 1$ m. Give units.

<details>
<summary>Solution</summary>

#### (a) Connected rates

원통형이므로: $V = \pi r^2 h = \pi(3)^2 h = 9\pi h$

$$\frac{dV}{dt} = 9\pi\,\frac{dh}{dt} \tag{M1}$$

$$9\pi\,\frac{dh}{dt} = -2\sqrt{h} \implies \frac{dh}{dt} = -\frac{2}{9\pi}\sqrt{h} \quad \checkmark \tag{A1}$$

---

#### (b) DE 풀기

$$h^{-1/2}\,dh = -\frac{2}{9\pi}\,dt \tag{M1}$$

$$\int h^{-1/2}\,dh = \int -\frac{2}{9\pi}\,dt$$

$$2\sqrt{h} = -\frac{2}{9\pi}t + C \tag{A1}$$

**초기조건** $t = 0,\ h = 9$:

$$2\sqrt{9} = C \implies C = 6 \tag{M1}$$

$$2\sqrt{h} = 6 - \frac{2t}{9\pi} \implies \sqrt{h} = 3 - \frac{t}{9\pi}$$

$$\boxed{h = \left(3 - \frac{t}{9\pi}\right)^2} \quad \checkmark \tag{A1}$$

---

#### (c) 탱크가 비는 시간

$h = 0$이 되는 조건:

$$3 - \frac{t}{9\pi} = 0 \implies t = 27\pi \tag{M1}$$

$$\boxed{t = 27\pi \approx 85 \text{ minutes}} \tag{A1}$$

---

#### (d) $t = 30$분일 때 $h$

$$\sqrt{h} = 3 - \frac{30}{9\pi} = 3 - \frac{10}{3\pi} \tag{M1}$$

$$\sqrt{h} \approx 3 - 1.0610 = 1.9390$$

$$h \approx 1.9390^2 \approx \boxed{3.76 \text{ m}} \tag{A1}$$

---

#### (e) $h = 1$ m일 때 감소 속도

$$\frac{dh}{dt} = -\frac{2}{9\pi}\sqrt{1} = -\frac{2}{9\pi} \approx -0.0707 \text{ m/min} \tag{A1}$$

> 깊이가 분당 약 0.0707 m (7.07 cm)씩 줄어들고 있다.

> **핵심 포인트:** $h$가 작을수록 $\sqrt{h}$가 작아져 배수 속도가 느려진다 — 비어가면서 점점 느리게 빠진다.
</detail>

## Q4. Applied DE — Drug Infusion Model (다단계 문제)

> **[문제 해석]**  
> 약물이 일정 속도로 들어오고 체내에서 비율로 빠져나가는 모델로, 형태는 $\frac{dQ}{dt} = R - kQ$다. 장기 평형값 $Q_\infty = R/k$를 먼저 구하면 해의 형태를 미리 예측할 수 있다. 특히 (e)에서 주입이 **중단되는 순간** 새로운 초기조건 $Q_0 = 400$이 설정되며, 이후는 완전히 다른 DE ($\frac{dQ}{d\tau} = -kQ$)를 새로 풀어야 한다 — 원래 식을 그대로 이어가면 틀린다.  
> (d)와 (e)(ii)의 답이 같게 나오는 대칭 구조를 이해하면 개념이 잡힌다.

A drug is administered intravenously at a constant rate of $60$ mg/hour. The body eliminates the drug at a rate proportional to the current amount $Q$ mg present, with elimination constant $k = 0.15$ hr$^{-1}$.

**(a)** Write down the differential equation for $\dfrac{dQ}{dt}$.

**(b)** Find the equilibrium (long-term) level $Q_\infty$ and determine whether it lies within the safe therapeutic range of $[200,\ 500]$ mg.

**(c)** Solve the DE with the initial condition $Q = 0$ at $t = 0$, giving $Q$ in terms of $t$.

**(d)** Find the time at which the drug first reaches the minimum therapeutic level of $200$ mg. Give your answer to 3 significant figures.

**(e)** The infusion is stopped at the moment when $Q = 400$ mg. After this point the drug decays according to $\dfrac{dQ}{dt} = -0.15Q$.

   **(i)** Write down the solution for $Q$ after the infusion stops (let $\tau = 0$ be the moment the infusion stops).

   **(ii)** Find the time after stopping the infusion for $Q$ to fall below 200 mg. Give your answer to 3 significant figures.

**(f)** Sketch a graph of $Q$ against $t$ for the entire process described in parts (c)–(e), labelling key values.

<details>
<summary>Solution</summary>

#### (a) DE 세우기

$$\boxed{\frac{dQ}{dt} = 60 - 0.15Q} \tag{B1}$$

*(유입 60 mg/hr, 유출 $0.15Q$ mg/hr)*

---

#### (b) 평형 수준

$\dfrac{dQ}{dt} = 0$일 때:

$$60 - 0.15Q_\infty = 0 \implies Q_\infty = \frac{60}{0.15} = 400 \text{ mg} \tag{B1}$$

$400 \in [200,\ 500]$이므로 **안전 범위 내** — 치료 농도를 유지하면서 독성 수준에 도달하지 않는다. \tag{A1}

---

#### (c) DE 풀기

$$\int \frac{dQ}{60 - 0.15Q} = \int dt \tag{M1}$$

치환: $u = 60 - 0.15Q,\; du = -0.15\,dQ$

$$-\frac{1}{0.15}\ln|60 - 0.15Q| = t + C \tag{A1}$$

$$\ln|60 - 0.15Q| = -0.15t + C'$$

$$60 - 0.15Q = Ae^{-0.15t}$$

**초기조건** $t = 0,\ Q = 0$:

$$60 = A \tag{M1}$$

$$60 - 0.15Q = 60e^{-0.15t}$$

$$0.15Q = 60(1 - e^{-0.15t})$$

$$\boxed{Q = 400\left(1 - e^{-0.15t}\right)} \tag{A1}$$

> **구조 확인:** $t\to\infty$이면 $Q \to 400$ ✓, $t=0$이면 $Q=0$ ✓

---

#### (d) $Q = 200$mg에 도달하는 시간

$$200 = 400(1 - e^{-0.15t}) \tag{M1}$$

$$1 - e^{-0.15t} = 0.5 \implies e^{-0.15t} = 0.5$$

$$-0.15t = \ln 0.5 = -\ln 2$$

$$t = \frac{\ln 2}{0.15} \tag{A1}$$

$$\boxed{t \approx 4.62 \text{ hours}} \tag{A1}$$

---

#### (e)(i) 주입 중단 후 감쇠

$\tau = 0$일 때 $Q_0 = 400$ mg, 이후 순수 감쇠:

$$\frac{dQ}{d\tau} = -0.15Q \implies Q = 400\,e^{-0.15\tau} \tag{B1}$$

---

#### (e)(ii) $Q < 200$mg이 되는 시간

$$400e^{-0.15\tau} = 200 \implies e^{-0.15\tau} = 0.5 \tag{M1}$$

$$\tau = \frac{\ln 2}{0.15} \tag{A1}$$

$$\boxed{\tau \approx 4.62 \text{ hours}} \tag{A1}$$

> **대칭적 결과 해석:** 주입 시작 후 200mg에 도달하는 시간과, 주입 중단 후 400mg에서 200mg으로 내려가는 시간이 같다. 이것은 우연이 아니다 — 두 경우 모두 $e^{-0.15t} = 0.5$라는 동일한 방정식에서 비롯된다.

---

#### (f) 그래프 스케치 가이드

```
Q (mg)
500 |
    |
400 |·············································· Q∞ = 400 (점근선)
    |                              ╲ (주입 중단 후 감쇠)
    |                         ╱────╲
300 |                    ╱───       ╲
    |               ╱──              ╲
200 |──────────╱                      ╲──────────── 200 (치료 최솟값)
    |       ↑                          ↑
    |    t≈4.62                     τ≈4.62
  0 +──────────────────────────────────────────── t
    0                    ↑ 주입 중단 (Q=400)
```

**레이블:**
- $Q_\infty = 400$ (수평 점근선)
- 상승 구간: $Q = 400(1 - e^{-0.15t})$ — 위로 볼록, 오목
- 하강 구간: $Q = 400e^{-0.15\tau}$ — 지수감쇠, 아래로 볼록
</detail>

## Summary: Q1–Q4 핵심 기법 정리

| 문제 | 핵심 기법 | 자주 하는 실수 |
|---|---|---|
| Q1 | 양변 부분분수 → 로그를 합쳐서 지수 비교 | $C$ 계산 후 양변을 6배 하기 전에 대입하는 실수 |
| Q2 | $u = \ln y$ 치환으로 비선형 → 선형화 | $\frac{dy}{dx}$를 $\frac{du}{dx}$로 바꿀 때 체인 룰 빠트림 |
| Q3 | Connected rates: $V$와 $h$ 관계 먼저 | 반지름 제곱 빠트려서 $\frac{dV}{dt} = \frac{dh}{dt}$로 잘못 씀 |
| Q4 | $R - kQ$형 적분 → 초기조건 두 번 (주입 중/후) | 주입 중단 후 $Q_0$를 다시 설정하지 않고 원래 식 연장 |
