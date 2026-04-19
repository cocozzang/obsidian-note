---
id: b3e7f241-9c4a-4d58-a1e2-0f6c83d7b429
aliases:
  - 52강 정적분의 계산기법(3)
  - 역함수와 정적분
  - 기함수 우함수 정적분
  - 대칭성과 정적분
tags:
  - 정적분
  - 기함수
  - 우함수
  - 대칭성
  - 역함수와정적분
  - 정적분계산기법
pages: 155-159
subject: 대학기초수학
title: 정적분의 계산기법(3), 역함수와 정적분
topics:
  - 기함수/우함수의 정적분 대칭성
  - f(x)+f(-x) 꼴의 정적분
  - f(x)+f(a-x) 꼴의 정적분
  - 역함수와 정적분 공식
---

# 정적분의 계산기법(3), 역함수와 정적분

## 1. 기함수·우함수의 정적분 (복습 및 심화 적용)

[[51-integral-techniques-2|51강]]에서 다룬 기함수/우함수 성질을 복합 함수에 적용하는 유형이다.

**핵심 공식 정리**

$$\int_{-a}^{a} f(x)\, dx = \begin{cases} 0 & (f \text{가 기함수}) \\ 2\displaystyle\int_{0}^{a} f(x)\, dx & (f \text{가 우함수}) \end{cases}$$

**기함수·우함수 판별**

- 기함수: $f(-x) = -f(x)$ → **기 × 기 = 우**, **우 × 기 = 기**
- 우함수: $f(-x) = f(x)$ → **우 × 우 = 우**

---

### 예제 333

함수 $f(x) = \tan(\sin x)$에 대하여 $\displaystyle\int_{-\frac{\pi}{6}}^{\frac{\pi}{6}} f(x)\, dx$의 값은?

> [!summary]- 풀이
> $f(-x) = \tan(\sin(-x)) = \tan(-\sin x) = -\tan(\sin x) = -f(x)$
>
> $f(x)$는 **기함수**이므로
>
> $$\int_{-\frac{\pi}{6}}^{\frac{\pi}{6}} f(x)\, dx = 0$$

---

### 예제 334

정적분 $\displaystyle\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} |x|\cos x\, dx$의 값은?

① $2\pi$ ② $\pi - 1$ ③ $\dfrac{\pi}{2} + 1$ ④ $\pi - 2$ ⑤ $\dfrac{\pi}{2} - 1$

> [!summary]- 풀이
> $|x|$는 우함수, $\cos x$는 우함수이므로 $|x|\cos x$는 **우함수**이다.
>
> $$\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} |x|\cos x\, dx = 2\int_{0}^{\frac{\pi}{2}} x\cos x\, dx$$
>
> 부분적분: $u = x,\ dv = \cos x\, dx$
>
> $$\int x\cos x\, dx = x\sin x - \int \sin x\, dx = x\sin x + \cos x$$
>
> $$= 2\left[x\sin x + \cos x\right]_{0}^{\frac{\pi}{2}} = 2\left(\frac{\pi}{2} \cdot 1 + 0 - 0 - 1\right) = \pi - 2$$
>
> **정답: ④**

---

### 예제 335

$f(x) = ax^2 + bx + c$이고 $\displaystyle\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} f(x)\sin x\, dx = 4$일 때, $b$의 값을 구하여라.

> [!summary]- 풀이
> $g(x) = f(x)\sin x = ax^2\sin x + bx\sin x + c\sin x$로 분해한다.
>
> - $ax^2\sin x$: 우함수 × 기함수 = **기함수** → 적분 = 0
> - $c\sin x$: 상수 × 기함수 = **기함수** → 적분 = 0
> - $bx\sin x$: 기함수 × 기함수 = **우함수** → 구간을 반으로 줄여 계산
>
> $$\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} g(x)\, dx = 2\int_{0}^{\frac{\pi}{2}} bx\sin x\, dx = 4$$
>
> 부분적분: $u = x,\ dv = \sin x\, dx$
>
> $$\int x\sin x\, dx = x(-\cos x) - \int (-\cos x)\, dx = -x\cos x + \sin x$$
>
> $$2b\left[-x\cos x + \sin x\right]_{0}^{\frac{\pi}{2}} = 2b\left(0 + 1 - 0 - 0\right) = 2b = 4$$
>
> $$b = 2$$

---

## 2. f(x) + f(-x) 꼴의 정적분

### 핵심 아이디어

$f(x) + f(-x) = h(x)$가 주어졌을 때, 대칭 구간 $[-a, a]$의 적분은:

$$\int_{-a}^{a} f(x)\, dx = \int_{-a}^{0} \bigl(f(x) + f(-x)\bigr)\, dx = \int_{0}^{a} \bigl(f(x) + f(-x)\bigr)\, dx$$

즉 절반 구간에서 $h(x)$를 적분하면 전체 적분값과 같다.

---

### 예제 336

연속함수 $f(x)$가 $f(x) + f(-x) = \sin\dfrac{x}{2} + 1$을 만족할 때,
$\displaystyle\int_{-\pi}^{\pi} f(x)\, dx$의 값을 구하여라.

> [!summary]- 풀이
> $f(x)$와 $f(-x)$는 $x = 0$에 대해 대칭이므로
>
> $$\int_{-\pi}^{\pi} f(x)\, dx = \int_{0}^{\pi} \bigl(f(x) + f(-x)\bigr)\, dx = \int_{0}^{\pi} \left(\sin\frac{x}{2} + 1\right)\, dx$$
>
> $$= \left[-2\cos\frac{x}{2} + x\right]_{0}^{\pi} = (0 + \pi) - (-2 + 0) = \pi - 2$$

---

## 3. f(x) + f(a-x) 꼴의 정적분

### 핵심 아이디어

$f(x) + f(a-x) = h(x)$가 주어졌을 때, $f(x)$와 $f(a-x)$는 $x = \dfrac{a}{2}$에 대해 대칭이다.

$$\int_{0}^{a} f(x)\, dx = \int_{0}^{\frac{a}{2}} \bigl(f(x) + f(a-x)\bigr)\, dx$$

---

### 예제 337

연속함수 $f(x)$가 $f(x) + f(1-x) = 1$을 만족할 때,
$\displaystyle\int_{0}^{1} f(x)\sin\pi x\, dx$의 값은?

① $\dfrac{1}{\pi}$ ② $\dfrac{2}{\pi}$ ③ $1$ ④ $\pi$ ⑤ $2\pi$

> [!summary]- 풀이
> $g(x) = f(x)\sin\pi x$로 놓으면
>
> $$\int_{0}^{1} g(x)\, dx = \int_{0}^{\frac{1}{2}} \bigl(g(x) + g(1-x)\bigr)\, dx$$
>
> $g(x) + g(1-x)$를 계산한다.
>
> $\sin(\pi - \pi x) = \sin\pi x$이므로:
>
> $$g(1-x) = f(1-x)\cdot\sin(\pi(1-x)) = f(1-x)\cdot\sin\pi x$$
>
> $$g(x) + g(1-x) = \sin\pi x\cdot\bigl(f(x) + f(1-x)\bigr) = \sin\pi x \cdot 1$$
>
> $$\int_{0}^{\frac{1}{2}} \sin\pi x\, dx = \left[-\frac{1}{\pi}\cos\pi x\right]_{0}^{\frac{1}{2}} = -\frac{1}{\pi}(0 - 1) = \frac{1}{\pi}$$
>
> **정답: ①**

---

### 예제 338

연속함수 $f(x)$가 $f(x) + f(\pi - x) = 2\sin^2 x + 1$을 만족할 때,
$\displaystyle\int_{0}^{\pi} f(x)\, dx$의 값은?

① $\dfrac{\pi}{3}$ ② $\dfrac{\pi}{2}$ ③ $\pi$ ④ $\dfrac{3}{2}\pi$ ⑤ $2\pi$

> [!summary]- 풀이
> $f(x)$와 $f(\pi-x)$는 $x = \dfrac{\pi}{2}$에 대해 대칭이므로
>
> $$\int_{0}^{\pi} f(x)\, dx = \int_{0}^{\frac{\pi}{2}} \bigl(f(x) + f(\pi-x)\bigr)\, dx = \int_{0}^{\frac{\pi}{2}} (2\sin^2 x + 1)\, dx$$
>
> $2\sin^2 x = 1 - \cos 2x$를 이용하면:
>
> $$= \int_{0}^{\frac{\pi}{2}} (2 - \cos 2x)\, dx = \left[2x - \frac{\sin 2x}{2}\right]_{0}^{\frac{\pi}{2}} = \pi - 0 = \pi$$
>
> **정답: ③**

---

### 예제 339

함수 $f(x) = \dfrac{2x}{x^2 + 1}$일 때, $\displaystyle\int_{0}^{\frac{1}{2}} \{f(x) + f(1-x)\}\, dx$의 값은?

① $\dfrac{1}{2}\ln 2$ ② $\ln 2$ ③ $2\ln 2$ ④ $1$ ⑤ $2$

> [!summary]- 풀이
> $f(x) + f(1-x)$를 구간 $[0, \frac{1}{2}]$에서 적분하는 것은 $f(x)$를 $[0, 1]$에서 적분하는 것과 같다.
>
> $$\int_{0}^{\frac{1}{2}} \{f(x) + f(1-x)\}\, dx = \int_{0}^{1} f(x)\, dx = \int_{0}^{1} \frac{2x}{x^2+1}\, dx$$
>
> $u = x^2 + 1$로 치환하면:
>
> $$= \left[\ln(x^2+1)\right]_{0}^{1} = \ln 2 - \ln 1 = \ln 2$$
>
> **정답: ②**

---

### 예제 340

모든 실수 $x$에 대하여 미분가능한 함수 $f(x)$가 $f(1-x) = 1 - f(x)$를 만족한다.
다음 중 항상 성립한다고 할 수 없는 것은?

① $f(0)+f(1)=1$ ② $f'(0)=f'(1)$ ③ $\displaystyle\int_{0}^{1} f(x)\, dx = \dfrac{1}{2}$

④ $f\!\left(\dfrac{1}{2}\right) = \dfrac{1}{2}$ ⑤ $f(0) = 0$

> [!summary]- 풀이
> 주어진 조건: $f(1-x) + f(x) = 1$ ···(★)
>
> **(1)** ★에 $x = 0$ 대입: $f(1) + f(0) = 1$ → **참**
>
> **(2)** ★을 미분: $-f'(1-x) + f'(x) = 0$
> $x = 0$ 대입: $-f'(1) + f'(0) = 0$ → $f'(0) = f'(1)$ → **참**
>
> **(3)**
> $$\int_{0}^{1} f(x)\, dx = \int_{0}^{\frac{1}{2}} \bigl(f(x) + f(1-x)\bigr)\, dx = \int_{0}^{\frac{1}{2}} 1\, dx = \frac{1}{2}$$ → **참**
>
> **(4)** ★에 $x = \dfrac{1}{2}$ 대입: $2f\!\left(\dfrac{1}{2}\right) = 1$ → $f\!\left(\dfrac{1}{2}\right) = \dfrac{1}{2}$ → **참**
>
> **(5)** ★에 $x = 0$ 대입: $f(1) + f(0) = 1$ → $f(0) = 1 - f(1)$
> $f(1)$이 $1$이라는 보장이 없으므로 $f(0) = 0$은 항상 성립하지 **않는다**.
>
> **정답: ⑤**

---

### 예제 341

함수 $f(x)$가 구간 $0 \leq x \leq 1$에서 $f(x) + f(1-x) = \left|x - \dfrac{1}{2}\right|$를 만족시킬 때,
$\displaystyle\int_{0}^{1} f(x)\, dx$의 값은?

① $\dfrac{1}{8}$ ② $\dfrac{1}{4}$ ③ $\dfrac{1}{2}$ ④ $1$ ⑤ $2$

> [!summary]- 풀이
> $$\int_{0}^{1} f(x)\, dx = \int_{0}^{\frac{1}{2}} \bigl(f(x) + f(1-x)\bigr)\, dx = \int_{0}^{\frac{1}{2}} \left|x - \frac{1}{2}\right|\, dx$$
>
> $0 \leq x \leq \dfrac{1}{2}$에서 $x - \dfrac{1}{2} \leq 0$이므로 $\left|x - \dfrac{1}{2}\right| = -x + \dfrac{1}{2}$
>
> $$= \int_{0}^{\frac{1}{2}} \left(-x + \frac{1}{2}\right)\, dx = \left[-\frac{1}{2}x^2 + \frac{1}{2}x\right]_{0}^{\frac{1}{2}} = -\frac{1}{8} + \frac{1}{4} = \frac{1}{8}$$
>
> **정답: ①**

---

## 4. Thm 49: 역함수와 정적분

### 정리

함수 $f(x)$의 역함수를 $g(x)$라 할 때:

$$\int_{a}^{b} f(x)\, dx + \int_{f(a)}^{f(b)} g(x)\, dx = bf(b) - af(a)$$

![Thm49 역함수와 정적분 기하학적 해석](./images/04-integral/thm50.md)

### 기하학적 해석

$y = f(x)$와 $y = g(x)$는 $y = x$에 대해 대칭이다.
두 적분의 합은 꺾인 직사각형 $[a,b]\times[f(a),f(b)]$의 넓이 $bf(b) - af(a)$와 같다.

### 대수적 증명 (부분적분 활용)

$\displaystyle\int_{f(a)}^{f(b)} g(x)\, dx$에서 $g(x) = y$로 놓으면 $f(y) = x$이고:

$$f'(y) = \frac{dx}{dy} \implies dx = f'(y)\, dy$$

적분 한계: $x = f(a) \Rightarrow y = a$, $x = f(b) \Rightarrow y = b$

$$\int_{f(a)}^{f(b)} g(x)\, dx = \int_{a}^{b} y \cdot f'(y)\, dy$$

부분적분 ($u = y$, $dv = f'(y)\, dy$):

$$= \left[y f(y)\right]_{a}^{b} - \int_{a}^{b} f(y)\, dy = \bigl\{b f(b) - a f(a)\bigr\} - \int_{a}^{b} f(x)\, dx$$

따라서:

$$\int_{a}^{b} f(x)\, dx + \int_{f(a)}^{f(b)} g(x)\, dx = bf(b) - af(a) \quad \blacksquare$$

---

### 예제 342

함수 $f(x) = xe^x\ (0 \leq x \leq 1)$의 역함수 $g(x)$에 대하여
$\displaystyle\int_{0}^{e} g(x)\, dx$를 구하여라.

> [!summary]- 풀이
> $f(0) = 0$, $f(1) = e$이므로 $a = 0,\ b = 1$
>
> $$\int_{0}^{e} g(x)\, dx = b f(b) - a f(a) - \int_{0}^{1} f(x)\, dx = 1 \cdot e - 0 - \int_{0}^{1} xe^x\, dx$$
>
> 부분적분: $\displaystyle\int xe^x\, dx = xe^x - e^x$
>
> $$= e - \left[xe^x - e^x\right]_{0}^{1} = e - (e - e - 0 + 1) = e - 1$$

---

### 예제 343

함수 $f(x)$에 대하여 $f(0) = \dfrac{1}{5}$, $f(1) = 1$일 때,
$\displaystyle\int_{0}^{1} f(x)\, dx + \int_{\frac{1}{5}}^{1} f^{-1}(x)\, dx$의 값은?

> [!summary]- 풀이
> Thm 49 공식에서 $a = 0,\ b = 1$:
>
> $$bf(b) - af(a) = 1 \cdot f(1) - 0 \cdot f(0) = 1 \cdot 1 - 0 = 1$$

---

### 예제 344

정적분 $\displaystyle\int_{0}^{1} e^x\, dx + \int_{1}^{e} \ln x\, dx$의 값은?

> [!summary]- 풀이
> $f(x) = e^x$의 역함수는 $g(x) = \ln x$이고 $f(0) = 1$, $f(1) = e$
>
> $$bf(b) - af(a) = 1 \cdot e - 0 \cdot 1 = e$$

---

### 예제 345

함수 $f(x) = e^x + e^{2x}$와 그 역함수 $g(x)$에 대하여
$\displaystyle\int_{0}^{\ln 2} f(x)\, dx + \int_{2}^{6} g(x)\, dx$의 값은?

① $3\ln 2$ ② $6\ln 2$ ③ $6\ln 3$ ④ $8\ln 2$ ⑤ $8\ln 3$

> [!summary]- 풀이
> $f(0) = 1 + 1 = 2$, $f(\ln 2) = 2 + 4 = 6$
>
> $a = 0,\ b = \ln 2$이므로:
>
> $$b f(b) - a f(a) = \ln 2 \cdot 6 - 0 \cdot 2 = 6\ln 2$$
>
> **정답: ②**

---

### 예제 346

함수 $f(x) = \tan x\ \left(-\dfrac{\pi}{2} < x < \dfrac{\pi}{2}\right)$의 역함수를 $g(x)$라 할 때,
$\displaystyle\int_{0}^{1} g(x)\, dx$의 값은?

① $\dfrac{\pi}{4} - \ln\dfrac{\sqrt{2}}{2}$ ② $\dfrac{\pi}{4} - \ln\sqrt{2}$ ③ $\dfrac{\pi}{4} - 1$

④ $1 - \ln\dfrac{\sqrt{2}}{2}$ ⑤ $1 - \ln\sqrt{2}$

> [!summary]- 풀이
> $f(0) = 0$, $f\!\left(\dfrac{\pi}{4}\right) = 1$이므로 $a = 0,\ b = \dfrac{\pi}{4}$
>
> $$\int_{0}^{1} g(x)\, dx = bf(b) - af(a) - \int_{a}^{b} f(x)\, dx = \frac{\pi}{4}\cdot 1 - 0 - \int_{0}^{\frac{\pi}{4}} \tan x\, dx$$
>
> $$\int \tan x\, dx = -\ln|\cos x| + C$$
>
> $$= \frac{\pi}{4} - \left[-\ln\cos x\right]_{0}^{\frac{\pi}{4}} = \frac{\pi}{4} - \left(-\ln\frac{1}{\sqrt{2}} + \ln 1\right) = \frac{\pi}{4} - \ln\sqrt{2}$$
>
> **정답: ②**

---

## 관련 주제

- [[51-integral-techniques-2|51강: 정적분의 계산기법(2)]]
- [[45-integration-by-parts|45강: 부분적분]]
- [[53-derivative-integral-1|53강: 미분과 정적분(1)]]

---

**학습 포인트:**

1. 기함수/우함수의 성질은 **적분 구간이 원점 대칭**일 때 강력하게 활용된다
2. $f(x) + f(-x) = h(x)$ 형태는 **절반 구간의 $h(x)$ 적분**으로 변환한다
3. $f(x) + f(a-x) = h(x)$ 형태는 **대칭축 $x = a/2$** 를 기준으로 절반 구간에서 계산한다
4. 역함수 정적분 공식 $\int_a^b f + \int_{f(a)}^{f(b)} g = bf(b) - af(a)$는 **부분적분**으로 유도된다
