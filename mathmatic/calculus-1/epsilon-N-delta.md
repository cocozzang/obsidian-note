---
id: epsilon-N-delta
aliases:
  - 엡실론논법
  - 엡실론-N
  - 엡실론-델타
  - ε-N
  - ε-δ
tags:
  - calculus-1
  - limits
  - rigorous-proof
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

---

## 3. 핵심 도구 및 패턴 모음

### 3.1 양화사 순서

- 정의의 첫 양화사는 도전 ($\forall \epsilon$), 두 번째는 응답 ($\exists k$ 또는 $\exists \delta$).
- 뒤집으면 의미 자체가 달라짐.

### 3.2 응답 변수의 종속성

- $k = k(\epsilon)$, $\delta = \delta(\epsilon)$
- 응답 변수에 다른 자유변수 ($n$ 또는 $x$) 가 끼면 안 됨.

### 3.3 이중 제약 + min

- 비선형 ε-δ 에서 항상 등장.
- 국소화 모자 (변수 인자를 상수로) + 정밀도 다이얼 (ε 도달).
- 분자 변수 → 상한, 분모 변수 → 하한.

### 3.4 +1 Padding

- 분모에 들어갈 양 ($M$, $|\beta|$ 등) 이 0 될 가능성 있으면 `+1` 으로 strict 양수화.
- 사슬 끝은 `≤ ε` 으로 닫힘 (등호 가능).
- 0 케이스 자동 흡수.

### 3.5 부호 추적 (strict vs non-strict)

- 사슬에 `<` 한 번이라도 끼면 전체 `<`.
- ε-N / ε-δ 결론은 항상 strict `< ε`.
- 사전탐색 끝은 부등호 (`<`), δ 또는 k 잡는 순간만 `=` 등호.

### 3.6 가감 트릭 (add-and-subtract)

- $X - Y$ 에 $-Z + Z$ 끼워 넣어 두 조각으로 쪼개기.
- 곱의 극한, 합성 함수, 비율 극한 등에서 반복 등장.

### 3.7 ε/N 분배

- 합 $A + B < \epsilon$ 을 만들 때 각 조각 $\epsilon/2$ 로.
- 세 조각이면 $\epsilon/3$, 네 조각이면 $\epsilon/4$.

### 3.8 max(N₁, N₂)

- 두 ε-N 가정을 동시에 활성화시키기 위해 더 큰 장벽 채택.
- 함수 극한에서는 min(δ₁, δ₂) — 더 좁은 울타리 채택. (이중 제약의 일반화)

---

## 4. 본인 약점 메모

체크포인트 — 비슷한 문제 풀 때 미끄러지기 쉬운 지점:

- [ ] **대수 손맛**: 불필요한 우회. 예: $(3x+1) - 7$ 을 직접 $3x-6 = 3(x-2)$ 로 가야 하는데 양쪽에 +2 끼우는 식. **인수분해 직진 연습.**
- [ ] **부등호 슬립**: 사전탐색 마지막을 `=` 로 끝내는 습관. (`|x-2| = \epsilon/3` ❌ → `|x-2| < \epsilon/3` ⟹ δ = ε/3 ✓)
- [ ] **min 모자 깜빡**: 비선형 ε-δ 에서 $\delta = \epsilon/5$ 만 적고 $\min$ 빼먹기. ε 큰 영역에서 증명이 무너짐.
- [ ] **단조 = 유계 혼동**: "수렴 ⟹ 단조" 거짓. ($(-1)^n/n$ 진동수렴 반례.) "수렴 ⟹ 유계" 만 참.
- [ ] **인덱스 vs 값 혼동**: 수열의 번호 $n$ 과 수열의 값 $a_n$ 헷갈리기. ε-N 가정은 **항의 번호 ($n \ge k$)** 통제.
- [ ] **strict 부호 추적**: 가정의 strict 가 결론까지 전염되는지 확인. 사슬에 한 줄이라도 `<` 면 전체 `<`.

---

## 5. 다음 세션 예정

- 극한의 유일성 정리: $\lim a_n = L_1 \land \lim a_n = L_2 \implies L_1 = L_2$
- 신규 도구: **귀류법** + ε/2 분리 (두 극한 동시 가정으로 모순 도출)
