---
id: epsilon-N-delta
aliases:
  - 엡실론논법
  - 엡실론-N
  - 엡실론-델타
  - ε-N
  - ε-δ
  - ε-M
  - 좌극한우극한
  - 극한의유일성
  - 극한의기본정리
  - 무한극한
tags:
  - calculus-1
  - limits
  - rigorous-proof
  - one-sided-limit
  - limit-laws
---

# 엡실론 논법 — 수열의 극한과 함수의 극한 엄밀한 증명

> 큐스터디 권태원 대학미적분학1 강의 기준 보완 정리.
> 강의에서 누락되거나 생략된 사전탐색, 비선형 케이스, 양화사 순서의 의미 등 포함.

---

## 1. ε-N 논법 (수열의 극한)

### 1.1 정의

$$\lim_{n \to \infty} a_n = L \iff \forall \epsilon > 0, \; \exists k \in \mathbb{N} \quad \text{s.t.} \quad n \ge k \implies |a_n - L| < \epsilon$$

**구조 해부:**

| 기호                       | 역할                      | 비고                |
| -------------------------- | ------------------------- | ------------------- | ---------------- | ------ |
| $\forall \epsilon > 0$     | 외부 도전장               | ε이 먼저 주어짐     |
| $\exists k \in \mathbb{N}$ | 응답 — 고정된 자연수 장벽 | $k = k(\epsilon)$   |
| $n \ge k$                  | 모든 그 이상의 항         | n은 흘러다니는 변수 |
| $                          | a_n - L                   | < \epsilon$         | 결론 — 오차 통제 | strict |

**핵심 원칙**: $k$ 는 $\epsilon$ 의 함수. ε이 작아질수록 k는 커진다.

### 1.2 양화사 순서의 의미

| 명제                                    | 의미                      | 잡아내는 수열         |
| --------------------------------------- | ------------------------- | --------------------- |
| $\forall \epsilon, \exists k(\epsilon)$ | k가 ε에 응답              | **모든 수렴수열**     |
| $\exists k, \forall \epsilon$           | 단 하나의 k로 모든 ε 처리 | **종국적 상수수열만** |

**종국적 상수수열**: 어떤 자연수 $k$ 이후로 $a_n = L$ 인 수열. ($a_n = 1/n$ 같은 진짜 수렴수열은 못 잡음.)

→ 그래서 정의는 **반드시 $\forall \epsilon$ 이 먼저, $\exists k$ 가 나중**.

### 1.3 예제 — 단일 수열

**예제 2.** $\lim_{n \to \infty} \frac{2n+1}{n} = 2$

$$\because \forall \epsilon > 0, \; \exists k \in \mathbb{N} \quad \text{s.t.} \quad n \ge k \implies \left| \frac{2n+1}{n} - 2 \right| = \frac{1}{n} \le \frac{1}{k} < \epsilon$$
$$\therefore \lim_{n \to \infty} \frac{2n+1}{n} = 2 \quad \text{Q.E.D.}$$

**예제 3.** $\lim_{n \to \infty} \frac{2 + (-1)^n}{n} = 0$ (분자 진동)

분자가 진동해도 **삼각부등식 상한** $|2 + (-1)^n| \le 3$ 으로 찍어 누름:
$$\left| \frac{2 + (-1)^n}{n} \right| \le \frac{3}{n} \le \frac{3}{k} < \epsilon$$

### 1.4 정리 — 곱의 극한

**정리**: $\lim a_n = \alpha$, $\lim b_n = \beta$ 이면 $\lim (a_n b_n) = \alpha\beta$.

**핵심 도구 4종:**

1. **가감 트릭**: 직접 안 보이는 무기를 등장시킴
   $$a_n b_n - \alpha\beta = a_n b_n - a_n \beta + a_n \beta - \alpha\beta = a_n(b_n - \beta) + \beta(a_n - \alpha)$$

2. **수렴 ⟹ 유계**: $\exists M > 0$ s.t. $|a_n| \le M$ (∀n)
   - **단조 ≠ 필요조건!** $(-1)^n / n$ 같은 진동수렴 반례.
   - 진짜 메커니즘: 유한 머리 max + 무한 꼬리 ε-N 가둠
   - $M = \max(|a_1|, \ldots, |a_{N-1}|, |\alpha| + 1) \ge 1 > 0$

3. **ε/2 분배**: 두 조각 각각 ε/2 → 합 ε

4. **max(N₁, N₂)**: 두 가정 동시 발동

**증명:**

$\because$ $a_n \to \alpha$ 이므로 $\exists M \ge 0$ s.t. $|a_n| \le M$ (∀n)
$\forall \epsilon > 0$ 에 대하여:

- $a_n \to \alpha$ 이므로 $\exists N_2$ s.t. $n \ge N_2 \implies |a_n - \alpha| < \frac{\epsilon}{2|\beta| + 1}$
- $b_n \to \beta$ 이므로 $\exists N_1$ s.t. $n \ge N_1 \implies |b_n - \beta| < \frac{\epsilon}{2M + 1}$

$N = \max(N_1, N_2)$ 로 잡으면, $n \ge N$ ⟹

$$
\begin{aligned}
|a_n b_n - \alpha\beta| &= |a_n(b_n - \beta) + \beta(a_n - \alpha)| \\
&\le |a_n| \cdot |b_n - \beta| + |\beta| \cdot |a_n - \alpha| \\
&\le M \cdot |b_n - \beta| + |\beta| \cdot |a_n - \alpha| \\
&< M \cdot \frac{\epsilon}{2M+1} + |\beta| \cdot \frac{\epsilon}{2|\beta|+1} \\
&= \frac{M}{2M+1} \cdot \epsilon + \frac{|\beta|}{2|\beta|+1} \cdot \epsilon \\
&\le \frac{1}{2}\epsilon + \frac{1}{2}\epsilon \\
&= \epsilon
\end{aligned}
$$

$\therefore \lim_{n \to \infty} (a_n b_n) = \alpha\beta \quad \text{Q.E.D.}$

**+1 padding 잔재주**: 분모의 $M$, $|\beta|$ 가 0이 될 가능성이 있을 때 `+1` 을 끼워 strict 양수 보장. 사슬은 `≤ ε` 으로 닫힘. **0 케이스 자동 흡수.**

핵심 부등식 $\frac{M}{2M+1} \le \frac{1}{2}$ 와 $\frac{|\beta|}{2|\beta|+1} \le \frac{1}{2}$ 는 자명한 $2M \le 2M+1$ 에서 나옴.

---

## 2. ε-δ 논법 (함수의 극한)

### 2.1 정의 (강의 판서 기반)

함수 $f: E \to \mathbb{R}$ 에 대하여 실수 $L$ 이 존재하여

$$\forall \epsilon > 0, \; \exists \delta > 0 \quad \text{s.t.} \quad 0 < |x - a| < \delta, \; x \in E \implies |f(x) - L| < \epsilon$$

를 만족할 때 $x \to a$ 일 때 $f(x)$ 는 $L$ 에 수렴, $L$ 을 극한값이라 하고 $\lim_{x \to a} f(x) = L$ 로 표기.

**강의 강조 사항**: $\delta = \delta(\epsilon)$ — **δ 는 ε 만의 함수**. x가 끼면 안 됨.

### 2.2 정의의 미세 구조

**ε vs δ 비대칭:**

| 기호 | 축         | 역할                    | 능동/수동 |
| ---- | ---------- | ----------------------- | --------- |
| ε    | y (치역)   | 도달 정밀도 요구 (오차) | 외부 도전 |
| δ    | x (정의역) | 입력 통제 반경          | 우리 응답 |

**`0 < |x - a|` 의 의미**: $x = a$ 그 한 점을 검사에서 **제외**. 덕분에:

- 제거 가능 불연속 (구멍) 잡음 — $\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = 2$ (분모 0인 점 회피)
- 점 이상 (한 점만 튀어오름) 잡음 — $f(0) = 100$ 이어도 $\lim_{x \to 0} x^2 = 0$
- **잡을 수 없음**: 점프 불연속 (좌우 극한 다름), 본질적 진동 ($\sin(1/x)$)

### 2.3 선형 예제

**예제 1.** $\lim_{x \to 1} (5x - 3) = 2$

**사전탐색**: $|(5x-3) - 2| = |5(x-1)| = 5|x-1| < \epsilon \iff |x-1| < \epsilon/5$. 따라서 $\delta = \epsilon/5$.

$$\because \forall \epsilon > 0, \; \exists \delta > 0 \; (\delta = \epsilon/5) \; \text{s.t.} \; 0 < |x - 1| < \delta \implies |(5x-3) - 2| = 5|x-1| < 5\delta = 5 \cdot \frac{\epsilon}{5} = \epsilon$$
$$\therefore \lim_{x \to 1} (5x - 3) = 2 \quad \text{Q.E.D.}$$

### 2.4 비선형 예제 — 분자 변수 케이스

**예제.** $\lim_{x \to 2} x^2 = 4$

**난관**: $|x^2 - 4| = |x+2| \cdot |x-2|$. `|x+2|` 가 x에 따라 변하므로 $\delta = \epsilon / |x+2|$ 같은 식으로는 못 잡음 (δ가 ε만의 함수가 아니게 됨).

**해결 — 이중 제약 + min**:

| 제약                       | 효과 |
| -------------------------- | ---- | --- | ------------------------------- | --- | ------------------------------------ |
| A: $\delta \le 1$          | $    | x-2 | < 1 \implies 1 < x < 3 \implies | x+2 | < 5$ (변수 인자를 **상한**으로 가둠) |
| B: $\delta \le \epsilon/5$ | $5   | x-2 | < \epsilon$ 보장                |

**최종**: $\delta = \min(1, \epsilon/5)$

$$
\begin{aligned}
|x^2 - 4| &= |x+2| \cdot |x-2| \\
&< 5 \cdot |x-2|        &&\leftarrow \delta \le 1 \text{ 덕분에 } |x+2| < 5 \\
&< 5 \cdot \delta        &&\leftarrow |x-2| < \delta \\
&\le 5 \cdot \epsilon/5  &&\leftarrow \delta \le \epsilon/5 \\
&= \epsilon
\end{aligned}
$$

**δ 의 이중 정체성:**

1. **국소화 모자** — 변하는 인자를 상수로 잡기 위한 사전 제약 (여기 1)
2. **정밀도 다이얼** — ε 만큼의 정밀도 맞추기 위한 제약 (여기 ε/5)

ε 큰 영역: A binding (δ = 1). ε 작은 영역: B binding (δ = ε/5).

### 2.5 비선형 예제 — 분모 변수 케이스

**예제.** $\lim_{x \to 3} \frac{1}{x} = \frac{1}{3}$

**공통분모**: $\left| \frac{1}{x} - \frac{1}{3} \right| = \frac{|x-3|}{3|x|}$

**난관**: $|x|$ 가 분모에 등장. 분모가 작아지면 분수 폭발. 따라서 $|x|$ 를 **하한**으로 가둬야 함.

**해결 — 분자 케이스와 방향 반대**:

| 케이스       | 변수 인자 위치 | 처리 방향 |
| ------------ | -------------- | --------- | --------- | -------------------- |
| 분자 ($x^2$) | $              | x+2       | $ in 분자 | 위에서 막음 (상한)   |
| 분모 ($1/x$) | $              | x         | $ in 분모 | 아래에서 막음 (하한) |

**역수 부등호 뒤집기**: $|x| > 2 \implies \frac{1}{|x|} < \frac{1}{2}$ (양수일 때만 유효)

| 제약                      | 효과 |     |                                 |     |                 |     |        |
| ------------------------- | ---- | --- | ------------------------------- | --- | --------------- | --- | ------ |
| A: $\delta \le 1$         | $    | x-3 | < 1 \implies 2 < x < 4 \implies | x   | > 2 \implies 1/ | x   | < 1/2$ |
| B: $\delta \le 6\epsilon$ | $    | x-3 | /6 < \epsilon$ 보장             |     |                 |     |        |

**최종**: $\delta = \min(1, 6\epsilon)$

$$
\begin{aligned}
\left| \frac{1}{x} - \frac{1}{3} \right| &= \frac{|x-3|}{3|x|} \\
&< \frac{|x-3|}{3 \cdot 2}   &&\leftarrow |x| > 2 \\
&= \frac{|x-3|}{6} \\
&< \frac{\delta}{6}           &&\leftarrow |x-3| < \delta \\
&\le \frac{6\epsilon}{6}      &&\leftarrow \delta \le 6\epsilon \\
&= \epsilon
\end{aligned}
$$

**min 의 동시성**: $\delta = \min(1, 6\epsilon)$ 정의 자체가 가정 $|x-3| < \delta$ 한 줄로 $|x-3| < 1$ AND $|x-3| < 6\epsilon$ 두 정보 동시 박음.

### 2.6 분수형 추가 케이스 — 양쪽 특이점 / 제곱근

> 큐스터디 5강 보강. 분수형 ε-δ의 일반 절차와 제곱근 케이스.

**(a) 분모가 목표점 근처에서 0 — 특이점까지의 거리**

예: $\lim_{x \to -1} \dfrac{x}{2x+1} = 1$. 특이점 $x = -\tfrac12$ (분모 0). **목표점 $-1$ 에서 특이점 $-\tfrac12$ 까지 거리 $= \tfrac12$.**

| 원칙 | 내용 |
| ---- | ---- |
| 국소화반경 $d$ | **목표점→특이점 거리보다 작게** ($d < \tfrac12$). 안 그러면 δ-이웃이 특이점에 닿아 분모 폭발 |
| 일반식 | $d$ 하나 정하면 $\delta = \min\big(d,\ (1-2d)\epsilon\big)$ 자동 결정 |
| 발산 ↔ 문턱 | $\delta = $ 거리 인 순간 이웃 끝이 특이점에 닿음. 그래서 strict 하게 작게 |

$d = \tfrac1{10}$ 이면: $|2x+1| = |2(x+1)-1| \ge 1 - 2|x+1| > \tfrac45$ 이므로 $\tfrac1{|2x+1|} < \tfrac54$. 따라서 $\delta = \min(\tfrac1{10}, \tfrac45\epsilon)$.

**(b) 분자·분모 변수 동시 — $\lim_{x \to 1} \dfrac{1}{x^2} = 1$**

$\left|\dfrac{1}{x^2} - 1\right| = \dfrac{|1-x^2|}{x^2} = |x-1| \cdot \dfrac{|x+1|}{x^2}$. **분자 인자 $|x+1|$ 은 위로, 분모 $x^2$ 은 아래로** 동시 묶음.

$\delta \le \tfrac12 \Rightarrow \tfrac12 < x < \tfrac32 \Rightarrow |x+1| < \tfrac52,\ x^2 > \tfrac14 \Rightarrow \dfrac{|x+1|}{x^2} < 10$. 따라서 $\delta = \min(\tfrac12, \tfrac{\epsilon}{10})$.

> ⚠️ **분모는 하한(아래)으로 묶는다.** 분모에 상한(위)을 넣으면 분수의 *하한*만 나와 증명이 깨짐.

**(c) 제곱근 — 결론을 제곱해 δ 역산**: $\lim_{x \to 0^+} \sqrt{x} = 0$

목표 $\sqrt x < \epsilon$ 을 **제곱** (양변 음 아님): $\sqrt x < \epsilon \iff x < \epsilon^2$. 따라서 $\delta = \epsilon^2$ (국소화 불필요).
$$|\sqrt x - 0| = \sqrt x < \sqrt\delta = \sqrt{\epsilon^2} = \epsilon$$

**(d) 분자형 "성립하는 δ" 판정식**: $\lim_{x \to a} x^2$ 류에서 $\delta = \min(a_0, c\epsilon)$ 형태가 성립할 필요충분조건은
$$(\text{움직이는 인자의 상한}) \cdot (\text{ε계수 } c) \le 1$$
ε이 약분돼 **ε-무관 상수조건**만 남는 게 핵심. (예: $x^2 \to 4$ 에서 상한 $4+a_0$, 조건 $(4+a_0)c \le 1$.)

---

## 3. 좌극한 · 우극한

### 3.1 정의 (Def(2))

함수 $f: E \to \mathbb{R}$, 실수 $L$ 에 대하여:

$$\lim_{x \to a^+} f(x) = L \iff \forall \epsilon > 0,\ \exists \delta > 0 \ \text{s.t.}\ 0 < x - a < \delta,\ x \in E \implies |f(x) - L| < \epsilon \quad (\text{우극한})$$
$$\lim_{x \to a^-} f(x) = L \iff \forall \epsilon > 0,\ \exists \delta > 0 \ \text{s.t.}\ -\delta < x - a < 0,\ x \in E \implies |f(x) - L| < \epsilon \quad (\text{좌극한})$$

**양쪽극한과의 차이는 가정 한 줄뿐:**

| 극한 | 가정 | 의미 |
| ---- | ---- | ---- |
| 양쪽 | $0 < \lvert x-a \rvert < \delta$ | $a$ 양옆 전부 (중심 $a$ 제외) |
| 우극한 | $0 < x-a < \delta$ | $a$ 오른쪽만 |
| 좌극한 | $-\delta < x-a < 0$ | $a$ 왼쪽만 |

### 3.2 "벽" 해부 — δ가 정하는 것 / 부등호가 정하는 것

각 부등호 = 수직선 위의 **벽 하나**. 우극한 $0 < x-a < \delta$:

- **바깥 벽 ($x-a < \delta$)**: 오른쪽으로 얼마나 멀리까지 → **반경**. δ가 정함.
- **안쪽 벽 ($0 < x-a$)**: 중심 $a$ 막음 + 오른쪽 한정 → **방향 + ($x \ne a$)**. 부등호 *형태*가 정함.

> **핵심**: δ는 바깥 벽(반경)만 정한다. 안쪽 벽(방향·중심 제외)은 δ와 무관하게 부등식의 형태(`0<` 냐 `<0` 이냐)가 정한다. → 좌·우극한은 δ를 어떻게 잡든 "어느 반쪽을 보느냐"가 부등호 방향으로 이미 고정.

**절댓값 벗기기** (방향 고정 덕에 case 분석 불필요):
- 우극한 $x > a$: $x - a > 0$ 이므로 $|x-a| = x-a$ (그대로)
- 좌극한 $x < a$: $x - a < 0$ 이므로 $|x-a| = -(x-a) = a-x$ (부호 뒤집기). 일반규칙: $A < B < 0 \Rightarrow |A| > |B| > 0$.

### 3.3 예제 — 조각함수 / 톱니함수

**예제7.** $f(x) = \begin{cases} x+1 & (x \le 2) \\ 2x-3 & (x > 2) \end{cases}$, $\lim_{x \to 2^+} f = 1$, $\lim_{x \to 2^-} f = 3$.

- 우극한 ($x > 2$, $f = 2x-3$): $|f(x) - 1| = |2x-4| = 2|x-2| < \epsilon$ → $\delta = \tfrac\epsilon2$
- 좌극한 ($x < 2$, $f = x+1$): $|f(x) - 3| = |x-2| = 2-x < \epsilon$ → $\delta = \epsilon$

> ⚠️ **조각함수는 어느 조각을 쓰는지 명시.** 좌극한이면 $x < a$ 쪽 조각을 골라 "$f(x) = \dots$ 이므로" 부터 시작. $[x]$ 같은 데서 조각 잘못 고르면 값 자체가 틀림.

**예제9.** $f(x) = x - [x]$ (소수부분, 톱니). $\lim_{x \to 1^-} f = 1$ ($x<1$ 이면 $[x]=0$, $f=x$), $\lim_{x \to 1^+} f = 0$ ($1 \le x < 2$ 이면 $[x]=1$, $f=x-1$). 정수점에서 좌우 다름.

### 3.4 Thm(1) — 양쪽극한 ⟺ 좌·우극한 일치

$$\lim_{x \to a} f(x) = L \iff \lim_{x \to a^+} f(x) = L \ \text{이고}\ \lim_{x \to a^-} f(x) = L$$

연료가 되는 동치: $0 < |x-a| < \delta \iff (-\delta < x-a < 0)\ \text{또는}\ (0 < x-a < \delta)$. 즉 **양쪽 가정 = 좌쪽 가정 OR 우쪽 가정.**

**($\Leftarrow$) 증명** (가정: 좌·우 둘 다 $=L$ / 목표: 양쪽 $=L$):
$\forall \epsilon$, 우극한에서 $\delta_1$, 좌극한에서 $\delta_2$. $\delta = \min(\delta_1, \delta_2)$. $0 < |x-a| < \delta$ 인 $x$ 는 $x \ne a$ 라 두 경우:
- $x > a$: $0 < x-a < \delta \le \delta_1$ → (우극한) $|f(x)-L| < \epsilon$
- $x < a$: $-\delta_2 \le -\delta < x-a < 0$ → (좌극한) $|f(x)-L| < \epsilon$

**($\Rightarrow$) 증명** (가정: 양쪽 $=L$ / 목표: 좌·우 각각 $=L$):
$\forall \epsilon$, 양쪽극한에서 $\delta$ 하나. **같은 $\delta$** 로:
- 우극한: $0 < x-a < \delta$ 면 $x>a$ 라 $|x-a| = x-a$, 즉 $0<|x-a|<\delta$ → $|f(x)-L|<\epsilon$
- 좌극한: $-\delta < x-a < 0$ 면 $x<a$ 라 $|x-a| = a-x$, $\times(-1)$ 로 $0<|x-a|<\delta$ → $|f(x)-L|<\epsilon$

> **방향의 비대칭**: ($\Rightarrow$)은 **강한 가정(양쪽)을 쪼개** 쓰므로 δ 하나. ($\Leftarrow$)는 **약한 둘(좌·우)을 합쳐야** 하므로 $\min$. ⟺ 증명은 항상 두 화살표를 따로, 가정·목표가 맞바뀐다.

**활용**: 예제7은 좌($3$) $\ne$ 우($1$) → Thm(1) 대우로 $\lim_{x\to2} f$ **부존재**.

---

## 4. 극한의 기본정리 (Thm(2))

$\lim_{x \to a} f = L$, $\lim_{x \to a} g = M$ 이면:

### 4.1 극한의 유일성 (귀류법 + ε/2)

**정리**: $\lim_{x \to a} f = L_1$ 이고 $= L_2$ 이면 $L_1 = L_2$.

**증명** (귀류법): $L_1 \ne L_2$ 가정 → $d = |L_1 - L_2| > 0$. $\epsilon = \tfrac d2 > 0$.
- $\lim f = L_1$: $\exists \delta_1$, $0<|x-a|<\delta_1 \Rightarrow |f(x)-L_1| < \tfrac d2$
- $\lim f = L_2$: $\exists \delta_2$, $0<|x-a|<\delta_2 \Rightarrow |f(x)-L_2| < \tfrac d2$

$\delta = \min(\delta_1, \delta_2)$, $0<|x-a|<\delta$ 인 $x$ 잡으면 (가감 트릭 + 삼각부등식):
$$d = |L_1 - L_2| = |(L_1 - f(x)) + (f(x) - L_2)| \le |L_1 - f(x)| + |f(x) - L_2| < \frac d2 + \frac d2 = d$$
$d < d$ 모순. $\therefore L_1 = L_2$. ∎

> **왜 절반?** $\tfrac d2 + \tfrac d2 = d$ 라 시작값 $d$ 로 정확히 돌아와 충돌. $\epsilon = d$ 면 $d < 2d$ 라 모순 안 남.

### 4.2 합·차의 극한 — $\lim(f \pm g) = L \pm M$

$\forall \epsilon$: $f$ 에서 $|f-L| < \tfrac\epsilon2$ ($\delta_1$), $g$ 에서 $|g-M| < \tfrac\epsilon2$ ($\delta_2$). $\delta = \min(\delta_1, \delta_2)$:
$$|(f+g) - (L+M)| = |(f-L) + (g-M)| \le |f-L| + |g-M| < \frac\epsilon2 + \frac\epsilon2 = \epsilon$$

> **정밀도 vs 울타리**: δ는 **하위 극한에서 받아 $\min$** 하는 것. `δ = ε/2` 처럼 직접 못 씀 (f,g가 임의라 전개 불가). $\tfrac\epsilon2$ 는 결론부 *정밀도*, δ는 가정부 *울타리* — 다른 층위.

### 4.3 곱의 극한 — $\lim(fg) = LM$

가감 트릭: $fg - LM = f(g-M) + M(f-L)$. 삼각부등식 + $|f|$ 유계화.
- $|f - L| < \min\big(1,\ \tfrac{\epsilon}{2|M|}\big)$ → `1` 로 $|f| < |L|+1$ 유계 (수렴⟹유계를 min에 압축)
- $|g - M| < \tfrac{\epsilon}{2(|L|+1)}$ → 분모 **`+1` padding** ($|L|=0$ 회피)

$$|fg - LM| \le |f||g-M| + |M||f-L| < \frac\epsilon2 + \frac\epsilon2 = \epsilon$$

### 4.4 몫의 극한 — $\lim \dfrac fg = \dfrac LM$ (단 $M \ne 0$)

$\dfrac fg = f \cdot \dfrac1g$ 이므로 $\lim \dfrac1g = \dfrac1M$ 만 보이면 곱에 귀착.

**핵심 — 분모 하한**: $|g-M| < \tfrac{|M|}2 \Rightarrow |g| \ge |M| - |g-M| > \tfrac{|M|}2 \Rightarrow \dfrac1{|g|} < \dfrac2{|M|}$.
$$\left|\frac1g - \frac1M\right| = \frac{|g-M|}{|M||g|} < |g-M| \cdot \frac2{|M|^2}$$
$\delta = \min\big(\tfrac{|M|}2,\ \tfrac{|M|^2}2 \epsilon\big)$ 로 닫힘.

> **분수형 ε-δ의 일반화**: §2.6의 $|x|>2$ (구체적 하한) → 여기선 $|g| > \tfrac{|M|}2$ (임의 함수의 추상 하한). 같은 "분모 0 회피" 동작.

### 4.5 부등식 보존 (예제12)

$a$ 근방에서 $f \ge g$ 이고 두 극한 존재 → $\lim f \ge \lim g$. **유일성과 같은 귀류법 골격**: $\beta - \alpha > 0$ 가정 → $\epsilon = \tfrac{\beta-\alpha}2$ → "ε는 임의 양수"와 모순.

---

## 5. 무한에서의 극한 · 발산 (양화사 변형)

ε-δ를 두 축으로 변형. **정의역이 무한이면 가정 변형, 치역이 무한이면 결론 변형.**

### 5.1 Def(3) — $x \to \infty$ (ε-M 논법)

$$\lim_{x \to \infty} f(x) = L \iff \forall \epsilon > 0,\ \exists M > 0 \ \text{s.t.}\ x > M \implies |f(x) - L| < \epsilon$$

δ-반경 → **M-문턱**. ε-N(수열)과 사실상 같은 구조 ($n \ge N$ → $x > M$). 예제13: $\lim_{x\to\infty} \tfrac1{x^n} = 0$.

### 5.2 Def(4) — $\lim f = \infty$ (M-δ 논법)

$$\lim_{x \to a} f(x) = \infty \iff \forall M > 0,\ \exists \delta > 0 \ \text{s.t.}\ 0 < |x-a| < \delta \implies f(x) > M$$

ε(오차 목표)가 사라지고 **M(높이 목표)이 도전자**. 결론이 $|f-L|<\epsilon$ (수렴) → $f(x) > M$ (발산). 예제14: $\lim_{x\to0}\tfrac1{x^2} = \infty$, 예제15: $\tfrac1x$ 의 좌우 $\pm\infty$.

### 5.3 양화사 4종 지도

| 종류 | 도전자 | 응답자 | 가정 (정의역) | 결론 (치역) |
| ---- | ------ | ------ | ------------- | ----------- |
| ε-δ | ε ↓ | δ | $\lvert x-a \rvert < \delta$ (안) | $\lvert f-L \rvert < \epsilon$ (수렴) |
| ε-M | ε ↓ | M | $x > M$ (바깥) | $\lvert f-L \rvert < \epsilon$ (수렴) |
| M-δ | M ↑ | δ | $\lvert x-a \rvert < \delta$ (안) | $f > M$ (발산) |

> 도전자가 점점 엄격해지고(ε↓ 또는 M↑) 응답자가 대응하는 같은 게임. **수렴은 ε이 작아지며 조여듦, 발산은 M이 커지며 조여듦.**

---

## 6. 핵심 도구 및 패턴 모음

### 6.1 양화사 순서

- 정의의 첫 양화사는 도전 ($\forall \epsilon$ 또는 $\forall M$), 두 번째는 응답 ($\exists k / \exists \delta / \exists M$).
- 뒤집으면 의미 자체가 달라짐.
- **4종 구조**: ε-δ / ε-M ($x\to\infty$) / M-δ ($f\to\infty$). §5.3 표 참조.

### 6.2 응답 변수의 종속성

- $k = k(\epsilon)$, $\delta = \delta(\epsilon)$
- 응답 변수에 다른 자유변수 ($n$ 또는 $x$) 가 끼면 안 됨.
- **단, 극한법칙 증명에서 δ는 직접 계산 대상이 아니라 하위 극한에서 받아 $\min$** (f,g 임의라 전개 불가).

### 6.3 이중 제약 + min

- 비선형 ε-δ 에서 항상 등장.
- 국소화 모자 (변수 인자를 상수로) + 정밀도 다이얼 (ε 도달).
- 분자 변수 → 상한, 분모 변수 → 하한.

### 6.4 +1 Padding

- 분모에 들어갈 양 ($M$, $|\beta|$, $|L|$ 등) 이 0 될 가능성 있으면 `+1` 으로 strict 양수화.
- 사슬 끝은 `≤ ε` 으로 닫힘 (등호 가능). 0 케이스 자동 흡수.

### 6.5 부호 추적 (strict vs non-strict)

- 사슬에 `<` 한 번이라도 끼면 전체 `<`.
- ε-N / ε-δ 결론은 항상 strict `< ε`.
- 사전탐색 끝은 부등호 (`<`), δ 또는 k 잡는 순간만 `=` 등호.

### 6.6 가감 트릭 (add-and-subtract)

- $X - Y$ 에 $-Z + Z$ 끼워 넣어 두 조각으로 쪼개기.
- 곱의 극한 ($fg-LM$), 유일성 ($L_1-L_2$), 비율 극한 등에서 반복 등장.

### 6.7 ε/N 분배

- 합 $A + B < \epsilon$ 을 만들 때 각 조각 $\epsilon/2$ 로. 세 조각이면 $\epsilon/3$.
- $\tfrac\epsilon2$ 는 **정밀도**(결론부), δ는 **울타리**(가정부) — 혼동 금지.

### 6.8 max(N₁, N₂) / min(δ₁, δ₂)

- 두 가정을 동시 활성화. ε-N은 더 큰 장벽 max(N₁,N₂), 함수극한은 더 좁은 울타리 min(δ₁,δ₂).

### 6.9 귀류법 + ε/2 분리

- 유일성·부등식 보존. $d = $ (두 후보 간 거리) $> 0$, $\epsilon = \tfrac d2$ → 삼각부등식으로 $d < d$ 모순.
- ⟺ 정리는 두 화살표를 따로 증명, **가정·목표가 맞바뀜**. (⟹ 쪼개 씀 / ⟸ min 합성)

### 6.10 분모 하한 (역수 뒤집기)

- 분모 변수가 0에 닿으면 분수 폭발 → 양의 상수로 **하한**.
- 구체: $|x| > 2$. 추상: $|g| > \tfrac{|M|}2$ (몫의 극한). 분수형 ε-δ의 일반화.

### 6.11 결론 제곱해 δ 역산

- $\sqrt{}$·거듭제곱: 목표 $\sqrt x < \epsilon$ 을 제곱 → $x < \epsilon^2$ → $\delta = \epsilon^2$.

---

## 7. 본인 약점 메모

체크포인트 — 비슷한 문제 풀 때 미끄러지기 쉬운 지점:

**대수·부호 (1~4강부터 누적)**
- [ ] **대수 손맛**: 불필요한 우회. 인수분해 직진 연습.
- [ ] **부등호 슬립**: 사전탐색 끝 `=` 습관 / 부호 뒤집기(×(-1)) 들어가는 좌극한·절댓값 풀기에서 재발. (단 "$A<B<0 \Rightarrow |A|>|B|$" 는 경계조건까지 정확히 일반화함)
- [ ] **min 모자 깜빡**: 비선형 ε-δ 에서 $\min$ 빼먹기.
- [ ] **strict 부호 추적**: 사슬에 한 줄이라도 `<` 면 전체 `<`.
- [ ] **단조 = 유계 혼동** / **인덱스 vs 값 혼동** (ε-N).

**증명 서술 (5~6강 추가)**
- [ ] **정의 인용 시 결론부 누락**: 가정($0<|x-a|<\delta$)만 적고 결론($|f(x)-L|<\epsilon$) 흘림. 정의 = 가정 ⟹ 결론 한 세트.
- [ ] **정밀도(ε/N) vs 울타리(δ) 혼동**: `δ = ε/2` 로 적기. ε/2는 결론부, δ는 하위극한에서 받아 min.
- [ ] **조각함수 조각 명시 안 함**: 좌/우극한에서 어느 조각 쓰는지 안 밝히고 전개. $[x]$ 류에서 값 자체 틀림.
- [ ] **결론값만 답하고 근거 정리 건너뜀**: "좌≠우라 극한없음" — 어느 정리(Thm(1) 대우)에서 나온 보장인지 연결.

**교정된 오개념:**
- "수렴수열은 단조증가/감소" → 거짓. 진동 수렴 가능, 유계만 보장.
- "함수극한의 δ는 정의역 오차" → "오차"보다 "이웃 반경"이 정확.
- "$x \ne a$ 는 불연속 표현" → 거짓. 극한을 $f(a)$ 와 **독립**으로 정의하는 장치 (연속/불연속 판정 가능하게).

---

## 8. 다음 세션 예정

- **7강 연속함수(1)**: 연속의 정의, 우측·좌측 연속, 연속정리(1)(2).
  - 핵심 연결: 극한($x \ne a$ 로 정의)과 함수값 $f(a)$ 의 **일치** = 연속. 5~6강에서 깐 "극한은 $f(a)$ 와 독립"이 회수됨.
- **8강 연속함수(2)**: 연속정리(3)(4), **중간값 정리(IVT)**.
